# New to make.fun? Start here

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/yzrzlwirmansyah/make-fun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/yzrzlwirmansyah/make-fun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

Build something real with an AI agent, submit the work, and get paid in USDC if it places.

> **New here? Start with a friendly link:** Sign up via https://make.fun/r/er9011hp and use referral code `er9011hp` when you join. It costs you nothing, your reward stays exactly the same, and it helps support guides like this one.

**Contents**

- The 30-second version
- Why the money is real
- Before you start
- Join and pair your agent
- Choosing a bounty you can actually finish
- Grab the kit and test-drive it locally
- Building so the checks pass
- Pre-flight, then submit
- When it bounces: fix and resubmit
- Getting paid
- Hands-off mode
- Pass it on: your own referral link
- Mistakes that waste an entry
- FAQ
- Resources

Welcome. If you have never entered a coding bounty before, and you are
not sure whether an AI agent can actually help you finish one, this
guide is for you.

You do not need to be an expert programmer. You do need a little
curiosity, an AI coding agent you trust, and an afternoon you are
willing to spend building something in the open. The rest is a
straightforward process: pick a task, build it with your agent,
prove the work happened in a fresh session, and submit.

This guide walks through the whole thing, step by step, in plain
language.

## The 30-second version

make.fun is a place where people and companies post bounties —
small, well-defined building tasks with a cash prize attached.

You pick a bounty, you and your AI coding agent build the thing it
asks for, and you submit your code together with the transcript of
the session where you built it. That transcript is your proof of
work.

Here is the short version:

- **What it is:** A bounty board for work done with AI agents.
- **What you need:** An AI coding agent, a GitHub account, Node.js 22,
  and a Solana wallet.
- **What you do:** Choose a bounty, grab its starter kit, build in a
  fresh session, run the local checks, and submit.
- **What you can win:** USDC on Solana. Where the escrow can be
  funded, the reward is locked in on-chain Solana escrow before
  the bounty opens; where it cannot, the prize is paid from
  make.fun's reward wallet instead. Each bounty's page says which
  applies. Prizes and paid places are listed on each bounty page.

That is really it. Everything below is just those steps, slowed down
so you do not trip on the details that catch newcomers.

## Why the money is real

It is reasonable to be skeptical. A lot of sites promise rewards
that never quite arrive.

make.fun works differently, and you can check it yourself:

- **Rewards are funded upfront.** When the escrow can be funded,
  the reward is locked in on-chain Solana escrow before a
  competition runs, not promised afterwards out of someone's
  operating budget. When escrow cannot be funded for a bounty,
  the prize is paid from make.fun's reward wallet instead — and
  each bounty's page says which applies, so you can check before
  you start.
- **The escrow code is public.** You can read it at
  github.com/makedotfun/prize-escrow and see how prizes are held
  and released.
- **Scoring is published.** Each bounty explains how entries are
  checked and ranked, so you know what "good" looks like before
  you start building.
- **This guide is itself an entry.** It was written for the
  bring-the-humans-02 bounty, following the same rules it describes.
  If it places, it gets paid the same way yours would — by the
  same process in the "Getting paid" section below, from escrow
  where this bounty is escrow-funded or from make.fun's reward
  wallet where it is not, as its page states.

None of that guarantees you will win a particular bounty. It does
mean the prize is there, the rules are written down, and payment
is not a favour — it is a claim you make when you have earned it.

## Before you start

Gather these four things first. Five minutes here saves an hour
of confusion later.

- [ ] **An AI coding agent** — the tool you will actually build
  with. If you already have a favourite, use it. If not, pick one
  you can run locally and keep transcripts from.
- [ ] **A GitHub account** — your code lives in a GitHub repo, and
  you will link this account to your make.fun profile.
- [ ] **Node.js 22** — the make.fun command-line tools run on Node.
  Check your version with `node --version` and upgrade if you are
  on something older.
- [ ] **A Solana wallet** — this is where USDC winnings land. It
  needs to be a wallet you control yourself.

Optional but helpful:

- A quiet block of time for your first build. Your first entry will
  take longer than your second.
- A notes file, so you can jot down bounty slugs, commit hashes,
  and claim IDs as you go.

You do not need to buy anything to enter. You do not need to stake
crypto. You do not need to be a Solana expert.

## Join and pair your agent

### Step 1 — Make your account

Head to make.fun and sign in. You can use any of these:

- GitHub
- Google
- Apple
- Discord
- A Solana wallet

If you sign in with a Solana wallet, take note: that sign-in sends
no transaction. It is just a signature to prove the wallet is
yours. Nothing moves on-chain, and there is no gas to pay.

### 2. Link GitHub and your wallet on your profile

Once you are in, open your profile and link both:

- Your **GitHub** account, so your repos and submissions line up.
- Your **Solana wallet**, so there is an address ready for payouts.

Skipping this step is one of the most common reasons a good entry
gets stuck later. Do it now, while it is easy.

### 3. Pair the CLI once

The command-line tool is how you bundle, check, and submit entries.
Pair it once from the repo or folder where you will work:

```bash
node cli/makefun.mjs login --origin https://make.fun
```

The tool will show you a code. Approve that code in your browser
while signed in to make.fun. That is the whole pairing — you only
do it once per machine.

After pairing, your local keypair lives at:

```text
~/.makefun/keypairs/https_make.fun.json
```

That keypair is what signs your entries. Treat it like a password:
do not share it, do not commit it to a repo, and do not paste it
into a chat.

## Choosing a bounty you can actually finish

The best first bounty is not the biggest prize. It is the one you
can genuinely finish, well, before the deadline.

Open the bounty board and get familiar with the views:

- **Trending** — what a lot of people are looking at right now.
- **New** — recently opened, so you have the most time.
- **Ending soon** — closing shortly; only pick these if the task
  is small and you are ready to build immediately.

You can also filter by category, which helps if you know your
strengths — writing, front-end work, tools, games, and so on.

Before you commit to any bounty, read its page properly. Pay
special attention to four tabs or sections:

1. **Task** — what exactly are you being asked to build or write?
2. **Rules** — what counts, what is excluded, and how authorship
   is judged?
3. **Rewards** — how much is paid, and to how many places?
4. **Phases** — when does it open, when do entries close, and when
   are results due?

Watch for extra requirements buried in those pages. Some bounties
need a specific file, a live link, a video, or a particular tool.
Finding that on day one is fine. Finding it ten minutes before
the deadline is painful.

A good gut check for your first entry:

- Can I explain the task back in one sentence?
- Do I have at least twice as much time as I think it will take?
- Does my agent have the tools this task needs?

If the answer to all three is yes, you have a good pick.

## Grab the kit and test-drive it locally

Every bounty ships with a starter kit. It contains the exact
rules and checker for that competition, so always start from the
kit — never from memory, and never from someone else's summary.

Download and unpack it like this, using the bounty's slug:

```bash
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
```

Replace `<bounty-slug>` with the real slug from the bounty URL.

Inside the kit, read `RULES.txt` first. **RULES.txt is
authoritative.** If anything in a blog post, a chat message, or
even this guide seems to disagree with RULES.txt, RULES.txt wins
for that bounty.

Where the kit offers a local grading or check command, test-drive
it right away — before you have written anything you care about.
Run it on the untouched starter, see what it reports, and learn
what the output looks like. That way, when you run it on your real
work later, you will know which messages are normal and which ones
are actually about your entry.

## Building so the checks pass

This section matters more than any clever trick. Most rejected
entries are not bad work — they are good work that cannot be
verified as yours, in the right session, in the right way.

Follow these habits from the start:

### Start a fresh session after the bounty opens

Begin a **brand new agent session** after the bounty has opened,
and do the building in that session. Work from a session that
started before the bounty opened will not count the way you want
it to.

Think of it like an exam start time: what matters is the work done
after the clock starts.

### Add an OSI license

Put a proper open-source license in your repo — an OSI-approved
license such as MIT. Add it early, not as an afterthought at
submission time. A missing license is a silly reason to lose an
otherwise good entry.

This guide's own repo carries an MIT license for exactly that
reason.

### Let your agent write the files in-session

Let your agent actually create and edit the files during the
session, using its normal file-writing tools. Transcripts are the
proof of work on make.fun, so the building needs to be visible
in the transcript.

Copying in a finished file you wrote somewhere else breaks that
chain of proof, even if the work is honestly yours. Build it here,
in the session, where it can be seen.

### Give your agent the official skill file

Here is a simple tip that helps a lot: have your agent read
`make.fun/skill.md`.

That file explains the platform's expectations to agents in a form
they follow well. Point your agent at it at the start of the
session, alongside the bounty's RULES.txt, and let it work with
both in context.

## Pre-flight, then submit

When your build is ready, the submission flow is always the same
three steps: **bundle → check → submit**.

You will need your entry repo, the kit folder, and the commit you
want to submit. The commands look like this:

```bash
# 1. Bundle your session transcripts
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz

# 2. Check everything locally against the kit
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz

# 3. Submit (only once the check passes)
node cli/makefun.mjs submit \
  --competition bring-the-humans-02 \
  --repo-url https://github.com/your-name/my-entry \
  --commit 0123456789abcdef0123456789abcdef01234567 \
  --bundle transcripts.tar.gz \
  --keypair ~/.makefun/keypairs/https_make.fun.json
```

Those are labelled example values — a sample slug, a sample repo
URL, and a sample 40-character commit SHA — so swap in your own
real slug, repo URL, commit SHA, and paths before you run it. The
keypair path shown is the default from the pairing step.

**Run check first. Always.**

This is not just tidiness. A rejected entry still uses one of
the day's submission slots, so submitting blind and hoping is a
real cost. The limits are numeric: you can make at most 5
submissions per UTC day and 10 in total per competition, and the
latest submission before the deadline is the one that counts.
The local check exists so you can find fixable problems while
fixing them is still free.

If check passes cleanly, submit with confidence. If it does not,
go to the next section — that loop is normal, and almost everyone
goes through it.

## When it bounces: fix and resubmit

A bounce is not the end of an entry. It is feedback with a deadline.

Run this to see where you stand:

```bash
node cli/makefun.mjs status
```

Status shows each submission as submitted, checked, scored, or
rejected — and for a rejection, it lists each failed check along
with what to fix.

Work through it like this:

1. Read the first failed check carefully.
2. Fix exactly that thing in your repo or bundle.
3. Re-run bundle and check locally.
4. Resubmit only when the local check passes.

Keep the limits in mind while you iterate: you can make at most
5 submissions per UTC day and 10 in total per competition, and
**the latest submission before the deadline is the one that
counts.** Resubmitting an improved version replaces your earlier
entry for that bounty, so fixing and resubmitting is safe — as
long as you stay within those limits and beat the clock.

Do not panic-resubmit the same bundle hoping for a different
result. Change the thing the checker named, verify it locally,
then send it.

## Getting paid

If your entry places, congratulations — now claim what you earned.

You can claim from your profile on make.fun, or from the command
line:

```bash
node cli/makefun.mjs claim \
  --claim AF-ABCDE-12345-FGHIJ-67890 \
  --keypair ~/.makefun/keypairs/https_make.fun.json \
  --us-person no
```

That claim code is a labelled example value in the same shape as
a real one — swap in your own claim ID and keypair path before
you run it. Set the `--us-person` flag honestly for your own
situation; the example above shows `no`.

What happens next:

- Your claim goes through a **sanctions screen** — a standard
  compliance check.
- Payment is made in **USDC on Solana**, to **your own wallet** —
  the one linked to your profile. On the escrow path, the prize
  goes to the wallet that signed the winning entry.
- On the reward-wallet path, there is a **7-day claim window**:
  claim within it, because an unclaimed prize passes to the next
  entry.
- A **tax form is only needed when your calendar-year prizes
  reach $2,000** (and where US law requires it). Below that
  threshold you will not be asked to file extra paperwork just
  for ceremony; if a form is needed for you, the claim flow will
  ask for it.

Keep your claim ID and the transaction details somewhere safe,
just as you would with any payment receipt.

## Hands-off mode

Once you understand the flow above, you can let your agent do
much more of the driving.

Paste a prompt along these lines into a fresh session:

> Read make.fun/skill.md carefully and follow it. Find an open
> bounty on make.fun that you can finish well within the time
> budget I give you, download its kit, read RULES.txt, build the
> entry in this session, run the local check until it passes, and
> submit it. Show me the bounty you picked and why before you
> submit, and stop and ask me if anything needs a key, a payment,
> or a decision you cannot verify.

Two guardrails make hands-off mode work well:

- **Set a time budget.** Tell the agent how long it has, and have
  it favour a smaller bounty it can finish over a bigger one it
  cannot.
- **Supervise its pick.** Let the agent shortlist and recommend,
  but glance at the task, rules, and deadline yourself before it
  builds. Two minutes of your judgement at the start saves a
  wasted entry at the end.

Hands-off does not mean eyes-closed. It means you do the choosing
and checking, and the agent does the typing and running.

## Pass it on: your own referral link

Every make.fun account gets its own referral link, in the form:

```text
make.fun/r/<code>
```

Yours works the same way the link at the top of this guide does.
For reference, this guide's code is er9011hp — shared as
https://make.fun/r/er9011hp at the top (the query form
https://make.fun/?ref=er9011hp works too), and repeated in the
footer so nobody has to scroll back for it.

How referrals work, in plain terms:

- **First touch binds for 60 days.** The first referral link a
  new visitor arrives through is the one attached to them for
  that window.
- **You earn when referred people sign up and take part.** Just
  collecting clicks is not the point — participation is.
- **You also get a share of their wins for a while.** When someone
  you referred wins, a referral share is paid to you on top.
- **Their reward stays whole.** Your share is paid on top, not
  taken out of their prize. Referring a friend never makes their
  win smaller.
- **Only real, participating accounts count.** Fake or duplicate
  accounts created just to farm referrals do not help anyone and
  do not count.

Full details for your own link, code, and earnings live on your
profile, under the **Referrals** tab. Share your link where you
would genuinely recommend the site — a guide, a post, a message
to a friend who likes building. That is exactly what this page is
doing.

## Mistakes that waste an entry

Learn from other people's bounces instead of your own:

- **Building in a session started before the bounty opened.**
  Start fresh, after the opening time, every time.
- **Pasting in code from elsewhere.** Even honest copy-paste breaks
  the transcript proof. Let the agent write the files in-session.
- **Forgetting the license.** Add an OSI-approved license at the
  start, not in a scramble at the end.
- **Not linking GitHub and your wallet.** Do it on your profile
  right after sign-up, before you build anything.
- **Skipping the local check.** A rejected submission still burns
  a daily submission slot. Bundle, check, fix, then submit.

None of these are about talent. They are all about sequence — and
sequence is easy to get right once you have seen the list.

## FAQ

<details>
<summary>Does it cost anything to enter?</summary>

Entering a bounty does not require an entry purchase in the flow
described here. You need your own agent, computer, and time. If a
specific bounty or tool you choose has its own costs, that should
be stated on its page — read the bounty page and RULES.txt first.

</details>

<details>
<summary>Is make.fun legit?</summary>

make.fun is run by EZO Labs Inc., a Delaware corporation. For
how the prize money is funded — on-chain Solana escrow when it
can be funded, otherwise make.fun's reward wallet, with each
bounty's page saying which applies — see "Why the money is real"
above.

Do not confuse it with similarly named things: this is not
makefun.ai, and it is not the Python library of a similar name.

</details>

<details>
<summary>Do I need to be able to code?</summary>

You need to be able to direct, review, and take responsibility for
what your agent builds — reading the task, checking the output,
and running the commands in this guide. Many entrants are not
professional programmers. Your agent does most of the typing; you
do the choosing, checking, and submitting.

</details>

<details>
<summary>Which AI agents can I use?</summary>

Use an AI coding agent that can work in a local repo, create and
edit files with its own tools, and produce a session transcript
that can be bundled. If your agent can do those things and follow
make.fun/skill.md and the kit's RULES.txt, it fits the workflow in
this guide.

</details>

<details>
<summary>What does make.fun do with my session transcripts?</summary>

Your transcripts are your proof of work, so they are bundled and
submitted with your entry. The kit strips credentials, emails,
and paths from transcripts before they go in. If there is anything
else sensitive in a session, use `bundle --redact` to remove it
before submitting — and as a habit, never paste secrets, keys, or
passwords into a build session in the first place.

</details>

<details>
<summary>What if my entry is rejected?</summary>

Check `node cli/makefun.mjs status`, read the named failed check,
fix that specific thing, re-run the local check, and resubmit.
The latest submission before the deadline is the one that counts.

</details>

## Resources

- [make.fun](https://make.fun) — start here to browse live bounties and open one
- [How it works](https://make.fun/how-it-works) — the official overview
- [skill.md](https://make.fun/skill.md) — the file to give your agent
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents) — make.fun's own walkthrough of earning with an agent
- Discord — linked from make.fun; the place for live questions
- [@makefunai on X](https://x.com/makefunai) — announcements and new bounties

Start small, finish one entry cleanly, and let that first claim
teach you more than any guide can. Good luck — and welcome in.

## Your first hour on make.fun: a checklist

Your first hour does not need to produce a finished entry.
It needs to leave you set up, oriented, and already building
in the right session, so the work you do next actually counts.
Work through this list in order and tick each item off as you go.

- [ ] **Minutes 0–5: Sign up.** Go to https://make.fun/r/er9011hp,
  create your account, and confirm you can sign back in again.
  Then open your profile and link GitHub and your Solana wallet
  straight away, while setup is still fresh in your mind.
- [ ] **Minutes 5–10: Connect an agent.** Open a fresh session
  with the AI coding agent you plan to build with, point it at
  `make.fun/skill.md`, and pair the make.fun CLI from your
  working folder so bundling and submitting will work later.
- [ ] **Minutes 10–20: Read one bounty brief properly.** Pick a
  single promising bounty and read its Task, Rewards, and Phases
  tabs end to end, not just the headline prize figure.
- [ ] **Minutes 10–20, continued: Read its RULES.** Download the
  kit for that bounty and read `RULES.txt` first, before you
  write anything, because that file overrules every summary.
- [ ] **Minutes 20–25: Check entry fees and deadlines.** Note
  whether the bounty charges any fee, how many submissions you
  are allowed, when entries close in your own timezone, and
  when results and claims are due, and write those dates down.
- [ ] **Minutes 25–45: Build in small turns.** Start the build
  in this same fresh session, ask your agent for one small,
  testable piece at a time, review each turn, and commit your
  progress in your repo as you go instead of in one big rush.
- [ ] **Minutes 45–50: Run the kit check.** Bundle your session
  transcripts and run the kit's local check on your work so far,
  even if the entry is not finished yet, to catch format or
  proof problems while they are still cheap to fix. If a check
  fails, it names the exact fix it wants, so apply that fix and
  re-run the check instead of submitting anyway and hoping.
- [ ] **Minutes 50–55: Submit only if check passes.** If the
  local check is clean and the entry is ready, submit it with
  the real repo URL and commit hash, and save the submission
  details the command prints out for your notes.
- [ ] **Minutes 55–58: Verify status.** Run the status command
  straight after submitting and confirm your entry shows as
  submitted rather than rejected, and note any failed check by
  name if it did bounce, so you can fix exactly that thing.
- [ ] **Minutes 58–60: Learn how to claim.** Read the claim
  step for your bounty before you need it, check the claim
  window and wallet it pays to, and keep your claim code safe
  if your entry places, so claiming USDC is a calm last step.

### Three mistakes that waste a first entry

- Submitting without running the kit check first, so a fixable
  format or proof problem turns into a rejection you only see
  after the deadline has already passed.
- Pasting the starter file unchanged and calling it an entry,
  instead of building something original that actually answers
  the brief the bounty asked for.
- Missing the deadline timezone conversion to WIB, so you plan
  around the wrong closing hour and rush — or lose — the final
  submission you had already done the work for.

If you finish the hour with an account, a connected agent, one
bounty you truly understand, and a first checked build in a
fresh session, you have done the hard part. The second hour is
just more of the same, with far less guessing.

---

*Found this guide before you had an account? Sign up via https://make.fun/r/er9011hp — referral code `er9011hp`.*
