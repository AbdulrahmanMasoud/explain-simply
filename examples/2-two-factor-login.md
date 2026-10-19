# Example 2: Why turn on two-factor login?

**Who asked:** someone whose IT person keeps asking them to turn on two-factor authentication
for their work email.

**The question:**

> My IT guy keeps telling me to turn on two-factor authentication for my work email. I already
> have a long password with numbers and symbols. Honestly I don't get why I need this extra step
> every time. Can you explain?

Both answers below come from Claude, given the same question on 2026-10-19: once without the
skill and once with it. They're copied unedited.

---

## Before: Claude without the skill

> Your IT guy is right. Your long password is a good start, but it only protects you from one kind of attack.
> 
> ## What a strong password protects against
> 
> A long password with numbers and symbols makes it very hard for someone to **guess** it. Nobody can type random combinations until they hit yours.
> 
> These days, though, most accounts aren't broken into by guessing. The attacker just **gets hold of the password itself**. A few common ways:
> 
> - **Fake login pages (phishing).** You get an email that looks like it's from Microsoft or Google: "Your mailbox is full, sign in here." The page looks real and you type your password. Now they have it, and it doesn't matter how long it is.
> - **Leaks from other websites.** If you've ever used the same password, or something close to it, on another site and that site gets hacked, your password ends up on lists that criminals buy and try everywhere.
> - **Malware.** A bad attachment or download can record what you type, including your password.
> 
> In all three cases the strength of the password doesn't help, because the attacker isn't guessing. They have the real thing.
> 
> ## What two-factor adds
> 
> Think of your front door. The password is your key. If someone copies your key, they walk right in.
> 
> Two-factor is like also having an alarm that only goes quiet when **your phone** says "yes, that's me." Someone with a copy of your key still can't get in, because they don't have your phone in their hand.
> 
> So even if your password gets stolen in one of the ways above, the thief sees a prompt asking for a code or approval from your phone, and they're stuck.
> 
> ## Why your work email matters so much
> 
> Your work email is the master key to a lot of other things:
> 
> - "Forgot password" links for other work systems go there.
> - Scammers who get into a work mailbox often send fake invoices or "please change our bank details" emails to clients or colleagues *from your real address*. People trust those, and companies lose real money this way.
> - It holds customer details, contracts, and internal conversations.
> 
> That's why IT focuses on it.
> 
> ## About the "extra step every time"
> 
> It's usually much less hassle than people expect:
> 
> - **Most systems remember your device.** On your usual laptop or phone you often only get asked every few weeks, or when you sign in from somewhere new.
> - **It's often just a tap.** Many setups send a notification to your phone and you press "Approve." No code to type.
> - **Passkeys or fingerprint/face sign-in** are an option at many companies and can be even quicker than typing a password.
> 
> One useful habit: if your phone ever asks you to approve a sign-in **that you didn't just start**, press "Deny" and tell IT. That means someone has your password, and two-factor just stopped them.
> 
> ## In short
> 
> - Strong password = hard to **guess**.
> - Two-factor = useless even if **stolen**.
> 
> You need both, because these days stealing is far more common than guessing. A few seconds now and then is a small price for stopping the most common way work email gets broken into.

---

## After: Claude with the skill

> ### Your password is a house key
> 
> Think of your work email as a house. Your password is the key to the front door.
> 
> A long password with numbers and symbols is a very good key. Nobody can guess its shape.
> 
> Two-factor login adds a **guard at the door**. Even when someone uses the right key, the guard phones you first and asks: "Is this you?" In real life, that phone call is a code or an **Approve** button on your phone.
> 
> ### What actually matters
> 
> Most break-ins don't guess the key. They **steal a copy** of it.
> 
> A strong key stops people from guessing it. It does nothing once someone has a copy.
> 
> ### Without it
> 
> Copies of keys get out in ordinary ways:
> 
> - A fake email says "Your mailbox is full, log in here." You type your password into the thief's page.
> - Another website you use gets hacked, and you used the same or a similar password there.
> - Someone sees it on a sticky note or in a shared document.
> 
> In all three cases, the length of your password doesn't matter. The thief has the exact key, so the door opens. No alarm goes off, and you might not notice for weeks.
> 
> ### With it
> 
> The thief has your key, but not your phone. The guard calls you. You didn't ask to come in, so the door stays shut.
> 
> ```
> When                 Who            Password   Your phone       Result
> Mon 09:00, office    You            correct    you tap Yes      In
> Tue 03:00, abroad    A stranger     correct    nobody taps Yes  Blocked
> ```
> 
> Microsoft has said this one step blocks **more than 99%** of automated attacks on accounts.
> 
> Also, it usually isn't every time. Most systems can **remember your own laptop and phone**. Then the guard only calls when you log in from a new device, or every few weeks. Ask your IT guy how yours is set up.
> 
> ### Why it matters to you
> 
> Your work email is the key ring for everything else. Password resets for your other work tools go there. Customers and colleagues trust what comes from it.
> 
> Someone inside it can read private mail, take over your other accounts, or send a fake invoice "from you" that people actually pay. That's why your IT guy keeps asking. One stolen password can hurt the whole company, not just you.
> 
> ### The catch
> 
> - A few seconds at login, mostly on new devices.
> - If you lose or change your phone, you need another way in. Save the backup codes when you set it up, and know who in IT can reset it.
> - Never tap Approve on a request you didn't start. If one pops up out of nowhere, someone has your password. Say no, then change your password and tell IT.
> - It isn't perfect. A very convincing fake page can sometimes trick people into giving the code too. It just makes a break-in much, much harder.
> 
> ### In one line
> 
> Your strong password stops people from guessing the key. Two-factor stops the people who already have a copy. So turn it on.

---

## What changed

Both answers are good, and about the same length. The differences:

| Before | After |
|---|---|
| The door-and-key picture shows up halfway through, then turns into an alarm | Starts with one picture, a house key plus a guard who phones you, and keeps it to the end |
| Lists how passwords get stolen | Same list, then a tiny table: you on Monday get in, a stranger at 3 a.m. with the right password is blocked |
| No downsides, apart from "it's less hassle than you think" | A clear **catch** section: what happens if you lose your phone (save the backup codes), never approve a request you didn't start, and it isn't perfect |
| Ends with a summary | Ends with one line: "So turn it on." |
