---
name: explain-simply
description: Explain any complicated idea in plain, jargon-free language (like ELI5, but for adults), for anyone, not only experts. Works for technology, money, contracts, health, science, work processes or a decision someone has to make. Built around one everyday comparison (a room of folders, a shared box of money, a taxi meter), short sentences, "without it / with it", the real numbers from the person's own situation, a tiny example, why it matters to them and what the catch is. Use this whenever someone says they don't understand, asks to make something easier, simpler or clearer, asks "what does X mean", "why do we need X", "explain this", "ELI5", "explain it like I'm not technical", or when an earlier answer full of jargon didn't land, even if they never say "simple".
metadata:
  version: "1.0"
---

# Explain simply

The person might be anyone: a developer, a manager, a shop owner, a student, a parent. They are
smart, but the answer they got was written for an expert, or it's full of words they don't use.
They need to *see* the idea so they can decide or move on. Aim for this: after reading, they
could explain it to a friend in their own words.

## The shape that works

Use these parts in this order, each under a short plain heading. Skip a part only when it
really doesn't apply.

1. **The picture.** Pick one everyday thing the idea behaves like, and map each real part onto
   it out loud: "The orders table is like a big room full of folders. Each order is one
   folder." Keep the same picture to the end; switching pictures halfway makes people lose the
   thread.
2. **What actually matters.** The small core of the problem in one or two lines: "We only need
   6 small facts from each folder."
3. **Without it.** What happens now, or what happens if they don't do it, told inside the
   picture, with the real number: "The database walks to every folder and opens it. 2
   million folders, every time. That's why it took 8 to 90 seconds."
4. **With it.** What changes, with the real number. Add a tiny example (3 to 5 rows of realistic
   data, or one short calculation) when seeing it helps.
5. **Why it matters to you.** Tie it to their real situation: their customers, their money,
   their time, their safety. Not general benefits.
6. **The catch.** Short and honest: what it costs, what it risks, what extra work it needs.
   Without the catch it reads like a sales pitch, and they can't make a fair decision.
7. **The answer in one line**, when there's a decision: "So we add it."

## Writing rules, and why

- **Short sentences, one idea each.** Chains of "which / because / so that" lose readers,
  especially people reading in their second language.
- **Everyday words.** Use a special word only if they'll keep meeting it (like "index" or
  "interest rate"), and define it once through the picture: "An index is a small notebook that
  already has those 6 facts."
- **Real numbers from their situation:** their bill, their loan, their measured times, their
  data. Numbers make it concrete and believable. Never invent numbers and present them as
  theirs. If you don't have any, use a clearly labelled example with round numbers ("say you
  borrow 100,000").
- **Bold the 2 to 4 numbers or words** that carry the point, so a quick reader still gets it.
- **About one screen.** Leave out details they don't need to understand or decide. If they
  might want them, offer them in one line at the end.
- **Simple must stay true.** Every simplified sentence must still be correct. If the picture is
  wrong in a way that matters, say where in one line.
- **Health, law and money:** explain the idea clearly, but don't make the personal decision for
  them or give a diagnosis. Say who can (a doctor, a lawyer, the bank) when it matters.

## Choosing the picture

Use physical, daily things, for example:

| Idea | Picture |
|---|---|
| Database table, storage, index | A room of folders; a small sorted notebook |
| Cache | Items on the shop shelf vs. in the back storeroom |
| Queue, background job | Customers waiting at a counter; a delivery driver with a list |
| Login code, two-factor login | A house key plus a guard who phones you before opening the door |
| Password manager | A safe with one strong key that holds all your other keys |
| The cloud | Renting a storage room instead of building one at home |
| Fixed vs. variable interest rate | A fixed price agreed today vs. a taxi meter that can speed up or slow down |
| Compound interest | A snowball rolling downhill: it grows, and the bigger it gets the faster it grows |
| Inflation | The same 100 pounds fills a smaller shopping basket every year |
| Insurance | Many people put a little in one shared box; whoever has an accident takes from it |

Check the mapping before using it: every important part of the real thing has a matching part,
and the picture doesn't suggest something false.

## When they still don't understand

Don't repeat the same explanation with more detail or more special words; that's what didn't
work. Change the angle: a different, more physical picture, fewer parts, a smaller example.
Only ask which part was unclear if you really can't tell.

## Language

Answer in the person's language and at their level. If they write in Arabic or ask for Arabic,
explain in simple Egyptian Arabic, and keep code, product names and technical terms in English.

## Example

Someone asked "why do we need to add an index on the orders table?". A first technical answer
didn't land, and they said "I still don't understand it, make it easy". (Demo data.)

What didn't work (too technical):

> No current index holds all six columns. MySQL uses idx_orders_customer_id and then jumps to
> each order's row to read the other five values, so it reads from disk again and again, in no
> particular order. EXPLAIN shows "Using index" once the covering index exists…

What worked:

> **The orders table is like a big room full of folders**
> Each order is one big folder with many pages: customer, address, payment, totals, status…
> There are about **2 million** folders.
> To answer "who spent 5,000 and has 3 orders?", we only need **6 small facts** from each folder.
>
> **Without the index**
> The database walks to every folder, opens it, and reads those 6 facts. Every time.
> That's why it took between **8 and 90 seconds**, and the shop gets slower while it runs.
>
> **With the index**
> An index is a **small notebook** that already has those 6 facts for every order, in order:
> ```
> status    customer  date        total
> complete  101       2026-09-01  450
> complete  101       2026-09-20  300
> complete  102       2026-08-11  1200
> ```
> The database reads only the notebook: **less than 1 second**, every time. It updates the
> notebook by itself whenever an order is saved.
>
> **Why we need it**
> The query runs every time someone opens the sales report.
>
> **The catch**
> About **80 MB** of disk, and a tiny bit of extra work each time an order is saved.
