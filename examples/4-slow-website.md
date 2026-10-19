# Example 4: "Compress the images and add a CDN"?

**Who asked:** a marketing manager whose developer gave a technical reason for a slow website.

**The question:**

> I'm the marketing manager. Our developer says the website is slow because "the images aren't
> compressed and we don't have a CDN". Our homepage takes about 9 seconds to load on mobile and
> the images on it add up to about 14 MB. What does he mean, and is it worth doing?

Both answers below come from Claude, given the same question on 2026-10-19: once without the
skill and once with it. They're copied unedited.

---

## Before: Claude without the skill

> # What your developer means, and whether it's worth doing
> 
> **Short answer: yes, it's worth doing.** Fixing the images is probably the cheapest and biggest speed gain you can get. 14 MB of images on one page is very heavy. A well-built homepage usually has about 1–2 MB of images in total.
> 
> ---
> 
> ## The two problems, in plain terms
> 
> ### 1. "The images aren't compressed"
> 
> Each image is like a parcel. Right now every photo is shipped in a box far bigger than it needs to be.
> 
> - Images are often uploaded straight from a camera or a design tool, for example 4000 pixels wide and 2–3 MB each.
> - A phone screen only needs about 1000–1200 pixels of width, even on a sharp screen. So the phone downloads a huge file and then shrinks it to fit.
> - **Compressing** means saving each image at the size it's actually shown, in a modern format (WebP or AVIF), with sensible quality settings. A 2.5 MB banner usually ends up at around 150–250 KB, and to the eye it looks the same.
> 
> ### 2. "We don't have a CDN"
> 
> A **CDN (Content Delivery Network)** is a network of servers in many locations that keep copies of your images.
> 
> - **Without a CDN:** every visitor fetches every image from our one server, wherever it is. The further away they are, the longer each request takes.
> - **With a CDN:** each visitor gets the images from a server near them. It's like keeping stock in local warehouses instead of shipping every order from one central warehouse.
> - **Bonus:** it takes load off our main server, so the site stays fast during campaigns and traffic peaks.
> 
> ---
> 
> ## What this means for your 9 seconds
> 
> Rough math: on a typical mobile 4G connection, downloading 14 MB takes about **6–10 seconds on its own**. So the images are likely most of your 9 seconds.
> 
> | | Today | After compression | After compression + CDN |
> |---|---|---|---|
> | Image weight | ~14 MB | ~1.5–2 MB | ~1.5–2 MB |
> | Mobile load time (estimate) | ~9 s | ~3–4 s | ~2–3 s |
> 
> These are estimates. Other things also slow pages down (tracking tags, scripts, the server itself), so ask your developer to measure before and after.
> 
> ---
> 
> ## Why it matters for marketing
> 
> - **People leave.** Google's research found that more than half of mobile visitors abandon a page that takes longer than 3 seconds to load. At 9 seconds, many people who click your ads leave before they ever see the page. You still pay for those clicks.
> - **Search rankings.** Google uses page speed (its "Core Web Vitals") as a ranking signal.
> - **Ad costs.** Google Ads looks at landing page experience when setting your Quality Score, and that affects what you pay per click.
> - **Customers' data.** 14 MB per visit eats into people's mobile data plans, and some will notice.
> 
> ---
> 
> ## What it costs
> 
> - **Compression:** usually a few days of developer work at most. Most of that is a one-off setup so new images are resized and converted automatically when uploaded, plus fixing the images already on the site. Little or no ongoing cost.
> - **CDN:** services like Cloudflare have a free plan, and paid plans start at around $20–25 a month. Others, like Amazon CloudFront, charge by usage, which is usually modest for a site like ours. Setup is typically a day or two, mostly testing. One side effect: when you replace an image, the change can take a few minutes to show up unless the developer clears the CDN's copy.
> 
> ---
> 
> ## What I'd do
> 
> 1. **Compress the images first.** It's the biggest gain for the least money.
> 2. **Add the CDN next.** Smaller extra gain, low monthly cost.
> 3. **Agree image rules with your team.** For example: homepage banners at most ~2000 px wide and under ~300 KB, other images under ~150 KB, exported as WebP (or JPG at about 80% quality). A lot of those 14 MB probably come from uploads, so without rules the problem comes back.
> 4. **Measure it.** Run the homepage through Google PageSpeed Insights (pagespeed.web.dev) before and after, so you can see the improvement and report on it.
> 
> ### Questions to ask your developer
> 
> - Which images on the homepage are the biggest? (He can list them in a few minutes.)
> - Can new uploads be resized and compressed automatically?
> - Do images further down the page only load when someone scrolls to them ("lazy loading")? That makes the first screen appear much faster.
> - How many days will this take, and what will the CDN cost per month?

---

## After: Claude with the skill

> ## Your homepage is a parcel you ship to every visitor
> 
> Every time someone opens your homepage, their phone has to download it. Think of it as a parcel.
> The images are the heavy things inside it.
> Right now that parcel weighs **14 MB**. It also ships from one warehouse, the one place where your website lives.
> 
> Your developer's two points fit this picture:
> 
> - **"The images aren't compressed."** Each image in the parcel is a wall-sized poster, but the phone only shows it at postcard size. Compressing means sending postcard-sized prints, packed tightly. On the phone screen they look the same.
> - **"We don't have a CDN."** A CDN (content delivery network) is a set of local branch warehouses. It keeps copies of your images in many cities. Each phone gets them from the nearest branch, not from the one far-away warehouse.
> 
> ## What actually matters
> 
> A phone on mobile data downloads slowly. The heavier the parcel, the longer the wait.
> Weight is the big problem. Distance is the smaller one.
> 
> ## Without it
> 
> An example with round numbers: a normal 4G phone downloads roughly 1.5 MB per second.
> 14 MB ÷ 1.5 MB per second = about **9 seconds**.
> That is very close to the 9 seconds you measured. So the images are very likely most of your problem. (Other things, like the site's code, add a little time too.)
> 
> ## With it
> 
> Images like yours usually shrink by 70 to 90% after compressing, with no difference you can see. Say 14 MB becomes about 2 MB:
> 
> ```
>                  Parcel weight   Download time (example 4G phone)
> Today            14 MB           about 9 seconds
> Compressed       about 2 MB      about 1 to 2 seconds
> ```
> 
> The CDN then makes the trip shorter on top of that. It helps most for visitors who are far from where your website lives.
> 
> ## Why it matters to you
> 
> - People who click your ads and social posts land on this page, mostly on their phones. Google's own research found that **more than half** of mobile visitors leave if a page takes over **3 seconds**. At 9 seconds, you are paying for clicks from people who leave before they see your offer.
> - Google also looks at page speed when it ranks websites. A slow homepage can cost you free search traffic.
> - 14 MB also uses up your visitors' mobile data, every visit.
> 
> ## The catch
> 
> - **Compressing** is usually a small job. Ask your developer how many days. Someone should check that the main banners still look sharp afterwards.
> - **It has to stay done.** Every new banner your team uploads must be light too, or the page gets heavy again. Ask the developer to make it automatic, or give your team a simple limit (for example, under 300 KB per banner).
> - **A CDN** usually costs a monthly fee (some have free plans) and needs some setup. One thing to know: when you swap a banner, the old one can still show for a while, until the copies in the branches are cleared. Plan for that on launch days.
> 
> ## The answer
> 
> Yes, it's worth doing. Compress the images first: it's cheap and likely gives the biggest gain. Add the CDN next. Ask your developer to measure the load time before and after, so you see the real result.
> 
> If it helps, I can write a short list of questions to ask your developer (cost, time, and how new uploads will stay light).

---

## What changed

| Before (about 780 words) | After (about 580 words) |
|---|---|
| Two different pictures (a parcel for images, warehouses for the CDN) and web terms like WebP, AVIF, Core Web Vitals and Quality Score | One picture all the way: the homepage is a parcel full of wall-sized posters, shipped from one far-away warehouse |
| Says 14 MB takes "about 6–10 seconds" | Does the math with **their** numbers: 14 MB ÷ 1.5 MB per second ≈ **9 seconds**, the same as they measured. That shows the images are the main problem |
| A long "what to do" plan and a list of questions for the developer | A short **catch** section: it has to stay done for every new banner, and an old banner can still show for a while after a change. It offers the question list in one line at the end |

The "before" answer has more depth, which is useful if you want details. The "after" answer
is easier to read and repeat in a meeting.
