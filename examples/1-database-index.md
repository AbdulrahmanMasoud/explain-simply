# Example 1: Why does the database need an index?

**Who asked:** a developer building a sales report for an online shop. The report finds
customers who match rules like "spent 5,000 and has 3 orders".

**The question:**

> Why do we need to add an index on the orders table?

This example is based on the real conversation the skill came from. The shop, table names and
numbers are changed to demo data. The "before" answer is correct, but it didn't help. The person
replied: *"I still don't understand it, make it easy to understand."*

---

## Before: correct, but too technical

> The report query needs six values from every completed order: `status`, `customer_id`,
> `created_at`, `grand_total`, `refunded` and `store_id`. That's about 2 million orders. No
> index on the `orders` table holds all six.
>
> **What happens without it**
>
> The existing indexes each hold only one or two of those values:
>
> | Index | Columns |
> |---|---|
> | `idx_orders_customer_id` | customer_id |
> | `idx_orders_status` | status |
> | `idx_orders_store_status_created` | store_id, status, created_at |
>
> MySQL uses `idx_orders_customer_id` to find the orders. Then, for each order, it jumps to that
> order's full row in the table to read the other five values. The table is about 2 GB, and the
> server only keeps part of it in memory. So it reads from disk again and again, in no
> particular order. That's why the same query took 8 seconds once and 90 seconds the next time.
>
> **What the index does**
>
> The index is a small copy of just those six columns, sorted by status and then customer.
> MySQL reads only this small copy, from start to end, and never opens the big table. `EXPLAIN`
> shows this as "Using index". Result: under 1 second, every time.
>
> **Cost**
>
> About 80 MB more disk space. Each order save updates one more index entry. It takes about 15
> seconds to build.

---

## After: with the explain-simply style

> **The orders table is like a big room full of folders**
>
> Each order is one **big folder** with many pages: customer, address, payment, delivery,
> totals, status, and much more. There are about **2 million** completed-order folders.
>
> To answer "who spent 5,000 and has 3 orders?", we only need **6 small facts** from each folder:
>
> ```
> customer · status · date · total · refunded · store
> ```
>
> **Without the index**
>
> The database has to **walk to every folder, open it, and read those 6 facts**. That's 2
> million folders, every time.
>
> - That's why it took between **8 and 90 seconds**.
> - While it's doing that, the database is busy, so the **website gets slower** for customers.
>
> **With the index**
>
> An index is a **small notebook** that already has those 6 facts for every order, written in
> order:
>
> ```
> status    customer  date        total  refunded  store
> complete  101       2026-09-01  450    0         Downtown
> complete  101       2026-09-20  300    0         Downtown
> complete  102       2026-08-11  1200   0         Airport
> ```
>
> Now the database **reads only the notebook** and never opens the folders.
>
> - The notebook is about **80 MB**, around 25 times smaller than the folders.
> - It takes **less than 1 second**, every time.
> - The database **updates the notebook by itself** whenever an order is saved.
>
> **Why we need it**
>
> The query runs every time someone opens the **sales report**. Without the index it's slow and
> slows the shop down. With it, it's fast.
>
> It costs about 80 MB of disk space and a tiny bit of extra work each time an order is saved.

The person's reply: *"good way for explaining"*.

---

## What changed

| Before | After |
|---|---|
| Starts with column names and index names | Starts with a picture: a room of folders |
| Explains how the database engine works inside | Explains what the database has to *do*: walk to every folder |
| Terms like "index", "EXPLAIN", "disk reads" | One new word, "index", explained as a small notebook |
| The numbers are there, but buried in technical sentences | The same numbers, in bold, next to what they mean |
| You need to know databases to follow it | Anyone can follow it and repeat it to a colleague |
