# Example 3: Car loan, fixed or variable interest rate?

**Who asked:** someone choosing between two car loan offers from their bank.

**The question:**

> The bank offered me a car loan of 300,000 EGP over 5 years. Option A: fixed rate 22%.
> Option B: variable rate, starts at 19% and follows the central bank rate. The bank employee
> explained it but I didn't understand anything. What's the difference?

Both answers below come from Claude, given the same question on 2026-10-19: once without the
skill and once with it. They're copied unedited. The monthly payments in both were checked and
are correct, assuming interest is charged only on what's still owed. Neither answer is
financial advice.

---

## Before: Claude without the skill

> ## The short version
> 
> - **Option A (fixed 22%)**: your monthly payment is set on day one and never changes for 5 years. You pay more at the start, but you know exactly what you'll pay.
> - **Option B (variable, starts at 19%)**: you pay less at the start, but your rate rises or falls whenever the Central Bank of Egypt changes its rate. If the Central Bank raises rates, your payment goes up. If it cuts them, your payment goes down.
> 
> So you're choosing between **paying a bit more for certainty** (A) and **paying less now but taking the risk** (B).
> 
> ## A simple way to picture it
> 
> Think of renting a flat.
> 
> - **Fixed** is a 5-year lease at a set rent. If rents in the area jump, you're protected. If they drop, you're still stuck paying the old rent.
> - **Variable** is rent that the landlord reviews every few months to match the market. It's cheaper today, but you don't know what it will be next year.
> 
> ## What it means in money (300,000 EGP over 60 months)
> 
> | | Monthly payment | Total paid back | Total interest |
> |---|---|---|---|
> | **A: Fixed 22%** | ~8,290 EGP | ~497,000 EGP | ~197,000 EGP |
> | **B: Variable, if it stays at 19% the whole time** | ~7,780 EGP | ~467,000 EGP | ~167,000 EGP |
> 
> At the start, B saves you about **500 EGP a month**. If the rate never moved, that would add up to about **30,000 EGP** over the 5 years.
> 
> The catch is that the rate on B probably **won't** stay at 19%. Here's what B would cost if the rate ended up at different levels for the whole loan:
> 
> | Variable rate ends up at | Monthly payment | Total interest | Compared with fixed (A) |
> |---|---|---|---|
> | 16% (Central Bank cuts 3 points) | ~7,300 EGP | ~138,000 EGP | you save ~59,000 |
> | 19% (no change) | ~7,780 EGP | ~167,000 EGP | you save ~30,000 |
> | 22% (rises 3 points) | ~8,290 EGP | ~197,000 EGP | about the same |
> | 25% (rises 6 points) | ~8,810 EGP | ~228,000 EGP | you pay ~31,000 more |
> | 28% (rises 9 points) | ~9,340 EGP | ~260,000 EGP | you pay ~63,000 more |
> 
> *(These figures are rounded and assume the rate sits at that level for the whole loan. In real life it moves around. Changes in the first year or two matter most, because that's when you still owe the most.)*
> 
> **The rule of thumb:** B works out cheaper as long as the rate averages below about 22%, which means the Central Bank can't raise rates by more than about 3 points and keep them there.
> 
> ## Is a 3-point rise realistic?
> 
> In Egypt, yes. Between 2022 and 2024 the Central Bank raised its rate from about 8% to about 27%, so anyone on a variable loan then saw their payments climb a lot. Rates have been coming down since 2025, but over 5 years they can move a long way in either direction. Nobody can tell you which way they'll go, including the bank employee.
> 
> ## How to decide
> 
> **Choose A (fixed) if:**
> - your budget is tight and a jump of 1,000 to 1,500 EGP a month would hurt
> - you want to sleep well and know your exact payment for 5 years
> 
> **Choose B (variable) if:**
> - you could comfortably handle a higher payment if rates rise
> - you think rates are more likely to fall or stay flat
> - you might pay the loan off early (then you're exposed to rate changes for a shorter time)
> 
> If you're unsure, fixed is the safer default for a car loan on a household budget. The extra ~500 EGP a month is basically what you pay for insurance against rate rises.
> 
> ## Ask the bank these before you sign
> 
> 1. **Is the 22% on a "declining balance" (متناقص) or is it "flat" (ثابت)?** This is the most important question. In Arabic, "ثابت" can mean "fixed" or "flat", and the two are very different. My numbers above assume a declining balance. If 22% is a *flat* rate, you'd pay 66,000 EGP interest every year, about **10,500 EGP a month and 330,000 EGP in interest**, which is far more expensive.
> 2. **For B: what exactly is the formula?** Usually it's "Central Bank rate + X%". Ask what X is and confirm that it stays fixed.
> 3. **How often does the variable rate change?** Every quarter? Right away when the Central Bank moves?
> 4. **When the rate changes, does my monthly payment change, or does the number of months change?**
> 5. **Is there a maximum (a cap)** on how high the variable rate can go?
> 6. **Are there fees for paying early**, and can I switch from variable to fixed later?
> 7. **Can I have both repayment schedules in writing**, showing the monthly amount and the total cost?
> 
> With the answers to questions 1 and 2, you'll know which option is really cheaper and how much risk B carries.

---

## After: Claude with the skill

> ### The picture: two ways to pay for a long taxi ride
> 
> Think of your loan as a 5-year taxi ride. The interest rate is the price per kilometre.
> 
> - **Option A (fixed 22%)** is like an app ride where the price is agreed before you get in. Traffic, fuel prices, anything can change. Your price doesn't.
> - **Option B (variable, starts at 19%)** is a taxi with a meter. The meter starts cheaper. But the central bank controls how fast it runs. When the central bank raises its rate, your meter speeds up. When it cuts its rate, your meter slows down.
> 
> ### What actually matters
> 
> B starts **3 points cheaper** (19% instead of 22%).
> The only question is this: will the central bank push your rate up by more than those 3 points during the 5 years? Nobody knows for sure. Not you, and not the bank.
> 
> ### Option A: the agreed price
> 
> You pay about **8,290 EGP a month**, the same for all 60 months.
> In total you pay about 497,000. So about 197,000 of that is interest.
> 
> Why is it higher than B? With A, the bank carries the risk that rates go up. The extra 3 points is what it charges you for carrying that risk.
> 
> ### Option B: the meter
> 
> You start at about **7,780 EGP a month**. That's about **500 less** than A.
> After that, it follows the central bank. A few examples:
> 
> | What the central bank does | Your monthly payment | Total over 5 years | Compared to A |
> |---|---|---|---|
> | Nothing, you stay at 19% | 7,780 | ~467,000 | ~30,000 less |
> | Cuts 6 points after year 1 (you go to 13%) | 7,780, then ~6,980 | ~428,500 | ~68,500 less |
> | Raises 6 points after year 1 (you go to 25%) | 7,780, then ~8,630 | ~507,500 | ~10,500 more |
> | Raises 10 points after year 1 (you go to 29%) | 7,780, then ~9,220 | ~536,000 | ~39,000 more |
> 
> Roughly: B costs you more only if the rate climbs more than 3 points and stays up for a long time. A rise in the first years hurts most, because that's when you still owe the most.
> 
> And rates in Egypt do move a lot. From 2022 to 2024 the central bank raised its rate by about 19 points, then it started cutting in 2025.
> 
> ### Why it matters to you
> 
> The real question isn't only "which is cheaper". It's "can my budget handle a surprise?"
> 
> - If 8,290 a month is already the most you can pay, a meter that could jump to 9,000 or more is dangerous. A gives you a payment that never changes.
> - If you have room in your budget for a jump of 1,000 to 1,500 a month, B starts cheaper and could save you tens of thousands. But it could also cost you more.
> 
> ### The catch
> 
> - **A:** you pay about 500 more every month from day one. If rates fall, you don't get any of the benefit. Paying the loan off early to escape usually costs a fee.
> - **B:** you can't know your payment for the next 5 years. There's no limit on how high it goes, unless the bank puts a maximum in writing.
> 
> ### Ask the bank these 3 things before you sign
> 
> 1. The exact monthly payment for each option, in writing. My numbers assume interest is charged only on what you still owe, which is the usual way. If they say the 22% is "flat", the payment is much higher: about 10,500 a month.
> 2. For B: how often can the rate change, and is there a maximum it can reach?
> 3. For B: when the rate goes up, does your monthly payment go up, or does the loan get longer?
> 
> ### In one line
> 
> A means paying about 500 more a month for a payment that never changes. B means starting cheaper and betting that rates won't rise more than about 3 points. Which one is right depends on how big a surprise your budget can take.

---

## What changed

| Before (about 850 words) | After (about 690 words) |
|---|---|
| A renting picture at the start, then mostly tables and rules | One picture kept to the end: an app ride with an agreed price vs. a taxi meter that the central bank speeds up or slows down |
| A table of rates that stay the same for the whole loan | A table of things that could really happen ("the central bank raises 6 points after year 1"), with the monthly payment before and after |
| "How to decide" lists and 7 questions for the bank | Turns it into one personal question: **can your budget handle a surprise?** Then 3 questions for the bank |
| Ends with what the answers to the questions will tell you | Ends with one line: A = about 500 more a month for a payment that never changes; B = start cheaper and bet rates won't rise more than about 3 points |

The "before" answer goes deeper. For example, it explains that the Arabic word "ثابت" can mean
"fixed" or "flat", and that a *flat* rate costs far more. The "after" answer is the one you
could explain to your family at dinner.
