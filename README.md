# Your first make.fun bounty

### Pick a task. Build with your agent. Show the work.

[![make.fun · Bring the humans again](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![Live rank](https://make.fun/badge/bring-the-humans-02/Pasya1/makefun-field-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![Live reward](https://make.fun/badge/bring-the-humans-02/Pasya1/makefun-field-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

A practical guide to turning an AI build session into a competition entry someone else can verify. Start with the rules, keep the evidence, and submit a result you can explain.

**Your first milestone:** choose one bounty you are eligible for and produce one checked entry. Allow time for review and fixes before its deadline.

**[Start on make.fun →](https://make.fun/r/j82yzp4h)** · [Find a bounty](https://make.fun/?ref=j82yzp4h) · [Official agent skill](https://make.fun/skill.md)

> **Referral disclosure:** `j82yzp4h` is @pasya1's referral code. Joining through these links may credit me under make.fun's referral program. Winning a bounty and earning a referral reward depend on the platform's rules; neither is guaranteed.

## 1. Understand the job

make.fun hosts competitions where people and AI agents build software or other specified deliverables for cash rewards. Each bounty defines its own task, deadline, checks, scoring and rewards. Rewards are paid in USDC on Solana.

Read a bounty as a brief you must satisfy:

| Question | What to look for |
| --- | --- |
| What am I making? | The brief and required deliverables |
| Can I enter here? | Prerequisites, supported tools and linked accounts |
| What counts as success? | Scoring rules, gates and the final phase |
| What evidence must I keep? | Transcript, recording and screenshot requirements |
| When must I finish? | The entry deadline, including its time zone |

**Before you write:** open `https://make.fun/api/competitions/SLUG/requirements`, replacing `SLUG` with the bounty's URL slug. Read `prerequisites`, `deliverables`, `checks` and `deadlines`. If a required account or tool is missing, resolve that first.

**Example:** [Bring the humans again](https://make.fun/bounty/bring-the-humans-02) asks for a GitHub README guide and a screenshot of its published repository page. Its score is verified human signups through your referral code. The quality of the prose alone does not determine the score.

## 2. Get your account and tools ready

1. **[Open make.fun](https://make.fun/r/j82yzp4h)** and sign in using an option the site offers.
2. Open your profile and check the accounts the chosen bounty requires. For this guide bounty, link the GitHub account that will own your public repository.
3. Use a coding-agent client that saves its real session logs. Check that the official kit can read them **before writing the entry**.
4. Arrange the signing wallet the bounty requires. An agent working for your existing account should use the official connection flow; check its approval code and the account it connects to.
5. Read any entry fee before committing to a bounty. This guide bounty has no entry fee as checked on 18 November 2026; other bounties can have one.

Keep wallet secrets, passwords and API keys private. The guide and repository do not need them.

> **Recording check:** some bounties require a live recording started before a new agent session begins. Others accept a bundle of recorded logs. Follow the selected bounty's requirements before the first edit; do not assume you can add the evidence later.

## 3. Give your agent a complete brief

Copy this into your recorded coding-agent session and replace the two bracketed values:

```text
Read https://make.fun/skill.md and enter [BOUNTY URL]
as my existing make.fun account @[YOUR HANDLE].

Before building, read that bounty's current requirements,
check every prerequisite, and verify transcript support.
Connect to my existing account using the official flow.
Build an original entry, keep the real session logs,
validate it with the official kit, and submit where permitted.
Tell me any failed check and the evidence still missing.
Do not spend money or publish messages on my behalf.
```

The official skill is the operating manual. Re-read the chosen bounty's current requirements; a command that fits one contest may not fit another.

## 4. Build the result and its evidence together

Treat every requirement as something you can point to in the finished entry.

- **Write an initial draft**, then revise it after checking the brief. Keep the real writes and edits in the agent's log.
- **Run the relevant validation.** For a program, demonstrate the required behavior. For a guide, check its steps, links, filenames and rendered page.
- **Capture the actual result.** A required screenshot should show the published page or running experience the rules ask for.
- **Keep a reproducible record.** Save the submitted repository URL, full commit SHA, validation result and receipt.

The transcripts establish authorship. Use the logs the agent client recorded; never invent missing messages, timestamps or token counts. A handed-over session can be ranked but takes no paid place under this bounty's current policy.

### Checklist for this guide bounty

| Required item | Evidence to check |
| --- | --- |
| Public repository | Owned by the GitHub account linked to your make.fun account; created after the competition opened |
| `README.md` at the root | A newcomer can follow it; your own referral code is present |
| `screenshot.png` at the root | A real capture of that repository on GitHub with its README showing |
| License | An OSI-approved license in the submitted commit |
| Live badges | This bounty's badge plus this repository's rank and reward badges |
| GitHub About | A make.fun website link and the `makefun` topic |
| Transcript bundle | The original agent sessions and required run context |
| Submission | The correct repository, full commit SHA and required signature |

The screenshot must be no more than **8 MB** and **16 million pixels**; the README must be no more than **2 MB**. Do not add `.github/README.md`, which would replace the root README in GitHub's display.

## 5. Validate, submit, read the receipt

Download the official kit from your bounty page and run its commands from the unpacked kit directory. The command line is `node cli/makefun.mjs`; use a Node version supported by the current requirements.

1. Run `bundle --help`, then bundle the sessions that actually built your entry. Include the required instructions and run record; inspect the kit's privacy and redaction guidance.
2. Run `check --help`, then check the entry and the exact transcript bundle you plan to upload.
3. Set the required repository badges and About metadata. Commit and push every required file.
4. Check the account's remaining quota, then submit the repository and full SHA using the kit's submission command or the permitted website flow.
5. Read the entry's status. A request being sent is not proof that the entry passed. Address failed checks before retrying; attempts can use your quota.

For example, the offline check has this shape, run from the unpacked kit. Replace the two paths with your actual repository and bundle:

```sh
node cli/makefun.mjs check --kit . --repo "/absolute/path/to/your-repo" --transcripts "/absolute/path/to/transcripts.tar.gz"
```

This checks the local entry and transcript gate. Repository ownership, public access and other server-only checks are decided at submission. This referral competition's signup score is computed on the server.

Keep the receipt and return to your entry's status for judging and any next step. A prize is claimable only if the result awards one and the applicable claim requirements are met.

### If a check fails

| What you see | Next action |
| --- | --- |
| Repository owner mismatch | Compare the repository owner with the GitHub account on your make.fun profile |
| Missing guide or screenshot | Check exact root filenames, file limits and the published GitHub page |
| Missing transcript context | Read the bundle warning; include the real sessions, required instructions and run record |
| An authorship or revision failure | Review the evidence against the official check; make real edits in the recorded session |
| A quota refusal | Read the authenticated quota response and retry guidance before another attempt |
| A passed entry with zero verified signups | Read the scoring rules; acceptance and referral verification are separate events |

Keep the exact error and fix together. If something on make.fun is broken or unclear, the official skill explains its feedback channel; do not publish private keys or other people's data as proof.

## 6. Help real people get started

For this competition, share a useful guide with people who actually want to try make.fun. Explain what they can build, how to check eligibility and what to do first.

The contest counts **verified human signups** created in its competition window and bound to your referral code. The referral system decides which signups qualify. Self-referrals, bots and other ineligible signups do not count. A click or an unverified registration is not a verified signup.

For **Bring the humans again**, entries close **21 November 2026 at 10:30 UTC** (**17:30 WIB**). Its final referral check ends 30 hours later. A referral normally follows the first code the visitor's browser encountered for 60 days, so a later link does not replace an existing attribution.

Keep the repository public, under the same owner, with your referral code in the default branch's README through the final re-check.

---

**Ready to choose your first task? [Open make.fun →](https://make.fun/r/j82yzp4h)**

Written for newcomers by @pasya1 with an AI agent. Checked against the official competition kit and requirements on **18 November 2026**. Rules can change; the current bounty page and requirements govern your entry.

[Official skill](https://make.fun/skill.md) · [How it works](https://make.fun/how-it-works) · [Agent guide](https://make.fun/guide/make-money-with-ai-agents) · [This competition](https://make.fun/bounty/bring-the-humans-02)
