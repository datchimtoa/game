# HEXA RUSH — MASTER PRODUCT & SYSTEM DOCUMENT

## 1. Product Overview

Hexa Rush is a fast-paced hexagon color puzzle game built as a Telegram Mini App for a global audience. The game is based on the Hextris gameplay loop: colored blocks fall toward a central hexagon, and the player rotates the hexagon to catch blocks and match three or more of the same color to clear them.

The product follows a **Free-to-play + Ad-funded rewards** model:

- Players play for free.
- Players can optionally watch rewarded ads to receive Coins or unlock benefits.
- A portion of ad revenue funds the reward pool.
- Players may later withdraw rewards in TON under controlled conditions.

The game does not promise fixed returns, does not sell investment packages, and does not create a circular economy where new players fund old players.

### 1.1. Product Principles

1. **Backend is the source of truth.**  
   All official scores, Coins, rewards, leaderboard results, and withdrawal requests are decided by the backend.

2. **Client is only a display layer.**  
   The client sends gameplay events and displays results. It never decides Coin balances, reward eligibility, or withdrawal approval.

3. **Every Coin has an origin.**  
   Every Coin earned, spent, held, or reversed must be recorded in a ledger.

4. **Every reward must be verifiable.**  
   Ad rewards must be verified server-side through the ad provider’s reward mechanism.

5. **Every withdrawal must be traceable.**  
   Every withdrawal request must have a full lifecycle and audit history.

6. **No fixed exchange rate promise.**  
   The game may show a reference conversion value, but it must not promise a fixed Coins-to-TON rate.

### 1.2. Target Audience

Hexa Rush targets global Telegram users who enjoy short, skill-based casual games.

Primary markets:

- Southeast Asia
- South Asia
- Eastern Europe
- Latin America
- Africa
- Global English-speaking Telegram users

The game interface is English-first to support global distribution and simplify iconography and asset production.

### 1.3. Product Name and Tagline

Working title:

```text
Hexa Rush
```

Tagline:

```text
Rotate. Match. Earn.
```

## 2. Core Gameplay

### 2.1. Game Concept

The player controls a central hexagon with six sides. Colored blocks fall from the edges of the screen toward the hexagon. The player rotates the hexagon left or right to guide incoming blocks into the correct position.

When three or more blocks of the same color touch, they are cleared. Cleared blocks cause the blocks above them to slide down, which may create additional matches.

The player loses when blocks overflow beyond the outer boundary of the hexagon.

### 2.2. Core Loop

The core gameplay loop is:

```text
A colored block falls toward one side of the hexagon
→ Player rotates the hexagon
→ Block lands on a side
→ If three same-color blocks touch, they clear
→ Cleared blocks may trigger additional matches
→ Player earns points and may create a combo
→ Game speed increases over time
→ Game ends when a side overflows
→ Player sees score, best score, Coins, and rank
```

The emotional loop is:

```text
Play a short game
→ Get close to beating a personal record
→ Want to play one more round
→ Earn Coins and achievements
→ Return the next day
```

### 2.3. First-Time User Experience

When a player opens the Mini App for the first time, they should immediately see the game screen.

The first screen contains:

- The central hexagon.
- Falling colored blocks.
- Current score.
- Best score.
- Coin balance.
- Play button.

Within the first 5–10 seconds, the player should understand:

```text
Tap left or right to rotate the hexagon.
Match three same-color blocks to clear them.
Do not let blocks overflow.
```

There is no long tutorial, no email registration, and no complex onboarding.

### 2.4. Game Rules

#### Blocks and Colors

- The game uses five block colors in the initial version.
- Each block has one color.
- Blocks fall from one of six directions.
- The player does not directly control blocks; the player rotates the hexagon.

#### Matching

- Three or more same-color blocks touching are cleared.
- Matches can occur vertically along a side or around the hexagon.
- After a clear, blocks above slide down and may create chain matches.

#### Combos

Combos are the main source of excitement and skill expression.

| Combo | Condition |
|---|---|
| Nice | Clear 2 groups within 5 seconds |
| Great | Clear 3 groups within 7 seconds |
| Amazing | Clear 4 groups within 10 seconds |
| Insane | Clear 5 groups in a row |

Combo moments should have clear visual and haptic feedback.

#### Difficulty

- Blocks fall slowly at the beginning.
- Speed increases after approximately 20–30 clears.
- Difficulty should scale primarily by the number of blocks cleared, not only by elapsed time.
- New players should be able to reach 300–800 points in their first few games.

#### Game Over

The game ends when blocks overflow beyond the hexagon boundary.

When the game ends:

- The result screen appears first.
- No ad should appear immediately.
- The player sees score, best score, Coins earned, and rank.
- The player may then choose whether to watch a rewarded ad to continue.

## 3. Player Progression

### 3.1. Score System

Score comes from clearing blocks and creating combos.

| Action | Points |
|---|---:|
| Clear one group of 3 blocks | 10 |
| Clear one group of 4 blocks | 18 |
| Clear one group of 5 blocks | 30 |
| Combo x2 | 1.5x score multiplier |
| Combo x3 | 2x score multiplier |
| Combo x4 | 3x score multiplier |

Score is used for:

- Personal best score.
- Daily leaderboard.
- Weekly leaderboard.
- Achievement progress.

Score is not directly converted into Coins at a fixed rate.

### 3.2. Coins

Coins are the internal reward currency.

Coins are used for:

- Buying boosters.
- Unlocking bonus challenges.
- Participating in events.
- Opening Mystery Rewards.
- Future reward conversions under controlled conditions.

Coins are not money. They are an internal points system with full transaction history.

### 3.3. Coin Sources

| Source | Coins |
|---|---:|
| Complete a game | 5–20 |
| First time reaching 500 points | 300 |
| First time reaching 1,000 points | 800 |
| First time reaching 2,000 points | 2,000 |
| First time creating a x4 combo | 500 |
| Complete a daily quest | 50–300 |
| Watch a rewarded ad | 30–100 |
| Invite a qualified friend | 100–500 |
| Weekly leaderboard reward | 500–10,000 |

### 3.4. Coin Spending

To prevent Coins from becoming only a “waiting-for-withdrawal” balance, players need ways to spend them.

| Action | Coins |
|---|---:|
| Buy Slow Time booster | 250 |
| Buy Clear One Color booster | 400 |
| Buy Shield booster | 300 |
| Unlock Bonus Challenge | 1,000 |
| Open Mystery Reward | 500 |
| Join a special event | 2,000–10,000 |

The goal is for at least 40–60% of earned Coins to be spent inside the game.

## 4. Achievements

Achievements are one-time rewards that create a clear sense of progression.

### 4.1. Best Score Achievements

| Milestone | Reward |
|---|---:|
| Reach 300 points | 300 Coins |
| Reach 500 points | 800 Coins |
| Reach 1,000 points | 2,000 Coins |
| Reach 2,000 points | 5,000 Coins |
| Reach 3,000 points | 10,000 Coins |
| Reach 5,000 points | 20,000 Coins |

### 4.2. Combo Achievements

| Milestone | Reward |
|---|---:|
| Create a x2 combo | 200 Coins |
| Create a x3 combo | 500 Coins |
| Create a x4 combo | 1,500 Coins |
| Create a x5 combo | 4,000 Coins |

### 4.3. Total Score Achievements

| Milestone | Reward |
|---|---:|
| Reach 5,000 total points | 1,000 Coins |
| Reach 25,000 total points | 4,000 Coins |
| Reach 100,000 total points | 12,000 Coins |
| Reach 250,000 total points | 30,000 Coins |

### 4.4. Achievement Rules

- Achievements unlock only from valid game sessions.
- Achievements based on flagged sessions cannot be claimed.
- If an achievement requires manual claiming, the system must revalidate the condition before issuing the reward.
- Each achievement can be claimed only once.

## 5. Daily Engagement

### 5.1. Daily Quests

Each day, players have three simple quests:

| Quest | Condition | Coins |
|---|---|---:|
| Play 3 games | Complete 3 valid games | 50 |
| Score 800 in one game | Reach 800 points in one valid game | 100 |
| Make a x3 combo | Create a x3 combo | 120 |

Quests reset daily. Players can claim rewards immediately after completion.

### 5.2. Login Streak

Players receive small rewards for opening the game on consecutive days.

| Consecutive Day | Coins |
|---:|---:|
| Day 1 | 20 |
| Day 2 | 30 |
| Day 3 | 50 |
| Day 5 | 100 |
| Day 7 | 200 |

If a player misses a day, the streak resets.

The goal is habit formation, not easy Coin farming.

## 6. Leaderboards

### 6.1. Daily Leaderboard

- Resets every day.
- Based on the player’s best score that day.
- Displays top 50.
- Top 10 receive Coins.

### 6.2. Weekly Leaderboard

- Resets every week.
- Based on total valid points accumulated during the week.
- Displays top 100.
- Top 20 receive larger Coin rewards.

### 6.3. Player Rank Visibility

Players should always see their own rank, even outside the top positions:

```text
Your rank: #184
Score: 1,240
Top 100 requires: 1,580
```

This creates motivation to keep playing.

### 6.4. Leaderboard Rules

- Only valid sessions count.
- One user appears only once per leaderboard.
- Flagged sessions do not count.
- If fraud is confirmed after rewards are paid, the system must support reward reversal.

## 7. Referral System

### 7.1. Purpose

The referral system grows the player base without paying for fake clicks or bots.

### 7.2. Referral Flow

```text
Player A shares a referral link
→ Player B opens the game through the link
→ Player B plays at least 3 valid games
→ Referral becomes qualified
→ Both players receive rewards
```

### 7.3. Valid Referral Conditions

A referral is valid only when:

- The invited player opens the game through the referral link.
- The invited player completes at least 3 valid games.
- The invited player is not the same person as the referrer.
- One Telegram account can be counted as a referral only once.
- There are no signs of multi-account abuse.

### 7.4. Referral Rewards

| Event | Referrer Reward | Invited Player Reward |
|---|---:|---:|
| Friend opens the game | 0 Coins | 100 Coins |
| Friend plays 3 games | 200 Coins | 100 Coins |
| Friend reaches 1,000 points | 300 Coins | 0 Coins |

## 8. Ads and Monetization

### 8.1. Ad Providers

| Provider | Role |
|---|---|
| AdsGram | Primary rewarded ad provider |
| TADS | Banner, fullscreen, and supplemental rewarded ads |

AdsGram requires a Reward URL for server-side reward verification. TADS provides publisher tools and ad widgets for Telegram Mini Apps.

### 8.2. Ad Placements

| Placement | Preferred Provider | Condition |
|---|---|---|
| Continue After Game Over | AdsGram | Score reaches threshold; revive not yet used |
| Double Coins | AdsGram | Game reaches score threshold; daily limit available |
| Bonus Challenge | AdsGram | Daily quests completed |
| Mystery Reward | AdsGram or TADS | Combo or score milestone reached |
| Home Banner | TADS | Shown only on Home screen |
| Result Banner | TADS | Shown after result screen |
| Fullscreen | TADS | After 3–5 games, with cooldown |

### 8.3. Rewarded Ad Principle

Players must choose to watch ads. Ads must provide clear value.

The system should avoid:

- Showing ads during active gameplay.
- Forcing ads to continue.
- Showing too many ads per session.
- Promising rewards that the economy cannot sustain.

### 8.4. Rewarded Ad Flow

```text
Player chooses to watch an ad
→ System creates a pending reward request
→ Player watches the ad
→ Ad provider confirms completion
→ Ad provider calls the game’s Reward URL
→ Backend verifies the request
→ Backend marks reward as verified
→ Coins are added through the Coins Ledger
→ Player sees the updated balance
```

### 8.5. Reward Rules

- Client callbacks alone are not enough to add Coins.
- Each reward must have a unique external ID from the provider.
- One reward can be credited only once.
- The system must limit rewards per user per day.
- The system must limit total rewards per day across all users.
- If an ad fails or the player closes it early, no Coins are added.
- If the provider calls the Reward URL late, the system must still process it exactly once.

## 9. Economy

### 9.1. Economy Goal

The economy must ensure:

```text
Total Coins issued <= Ad revenue + operational budget
```

The most important metric is:

```text
Payout ratio = Total reward value paid or committed / Total ad revenue
```

Target:

```text
Payout ratio <= 60–70%
```

The remaining revenue is reserved for infrastructure, fraud losses, marketing, and operational reserves.

### 9.2. Economy Levers

| Lever | Effect |
|---|---|
| Reduce Coins per game | Reduce Coin issuance |
| Increase achievement conditions | Reduce Coin issuance |
| Reduce daily ad reward limit | Reduce cost |
| Increase booster prices | Increase Coin spending |
| Increase referral conditions | Reduce fraud |
| Reduce leaderboard prize pool | Reduce cost |

### 9.3. Economy Balancing Process

1. Measure real eCPM by geography.
2. Calculate average revenue per active user.
3. Calculate average Coins issued per user.
4. Calculate payout ratio.
5. If payout ratio exceeds 70%, reduce rewards or increase conditions.
6. If payout ratio is below 40%, consider increasing rewards to improve retention.

### 9.4. Events and Prize Pools

Events must have a fixed budget.

Example:

```text
Weekly Tournament
- Prize pool: 100,000 Coins
- Top 20 players receive rewards
- Budget is fixed from the ad revenue fund
```

Rules:

- No profit promises.
- No paid entry with real money.
- Entry uses Coins or gameplay conditions only.
- Anti-fraud checks are required before rewards are paid.

## 10. System Architecture Overview

### 10.1. Core Systems

| System | Responsibility |
|---|---|
| Player System | Telegram identity, profile, Coins, history |
| Gameplay System | Game sessions, events, scores, best scores |
| Reward System | Achievements, quests, streaks, leaderboard, referral |
| Ads System | AdsGram, TADS, reward verification, limits |
| Wallet System | Coin balance, withdrawal requests, transaction history |
| Operations System | Admin panel, reporting, fraud, configuration |

### 10.2. System Principle

```text
Every Coin, official score, reward, and withdrawal request
must be recorded and decided by the backend.
```

The client is only an interface. It never decides:

- Coin balance.
- Reward eligibility.
- Withdrawal eligibility.
- Leaderboard results.

## 11. Data Model and Flows

### 11.1. Core Data Entities

| Entity | Responsibility |
|---|---|
| Users | Player identity and profile |
| Game Sessions | One gameplay round |
| Game Events | Gameplay evidence |
| Coins Ledger | Every Coin change |
| Achievements | Achievement status |
| Daily Quests | Quest progress |
| Streaks | Login streak |
| Leaderboards | Ranking results |
| Referrals | Invitation relationships |
| Ad Rewards | Ad reward verification |
| Wallets | Coin balance |
| Withdrawals | Withdrawal requests |
| Fraud Flags | Abuse detection |
| Admin Audit Logs | Admin action history |
| System Config | Game configuration |

### 11.2. User Data

Each player has:

- Telegram ID.
- Username and display name.
- Language.
- Account status.
- Coin balance.
- Best score.
- Total score.
- Games played.
- Streak.
- Referral code.
- Referrer.
- Risk level.
- Admin notes.

### 11.3. Game Session Data

Each game session stores:

- Session ID.
- Player ID.
- Start and end time.
- Duration.
- Status.
- Client-reported score.
- Server-calculated score.
- Max combo.
- Blocks cleared.
- Coins awarded.
- Fraud risk score.
- Flag reasons.

### 11.4. Game Event Data

The client records events such as:

- Game start.
- Block spawn.
- Rotation.
- Block placement.
- Match clear.
- Combo.
- Game over.
- Revive used.

The backend uses these events to recalculate the score and detect abnormal behavior.

### 11.5. Coins Ledger

Every Coin change must create a ledger entry containing:

- Player.
- Change type: earn, spend, hold, release, reverse.
- Amount.
- Balance before.
- Balance after.
- Source.
- Reference ID.
- Reason.
- Timestamp.

### 11.6. Core Data Flows

#### Gameplay Flow

```text
Player opens app
→ Backend verifies Telegram identity
→ Creates or updates user
→ Player taps Play
→ Backend creates session
→ Client plays and records events
→ Client sends finish request
→ Backend recalculates score
→ Updates best score and total score
→ Adds Coins through ledger if applicable
→ Returns official result
```

#### Ad Reward Flow

```text
Player chooses to watch ad
→ Backend creates pending reward request
→ Player watches ad
→ Provider confirms completion
→ Provider calls Reward URL
→ Backend verifies external ID
→ If valid, marks reward verified
→ Adds Coins through ledger
→ Updates wallet balance
```

#### Withdrawal Flow

```text
Player opens Wallet
→ Checks minimum Coin requirement
→ Selects TON address
→ Backend checks fraud and limits
→ Creates withdrawal request
→ Holds Coins
→ Adds request to queue
→ Admin approves in batch
→ Treasury sends TON
→ Records transaction hash
→ Marks withdrawal completed
→ Ledger records Coin deduction
```

## 12. Wallet and Withdrawals

### 12.1. Internal Wallet

The wallet is the player’s internal Coin balance, not a separate crypto wallet.

It contains:

- Available Coins.
- Held Coins.
- Total Coins earned.
- Total Coins spent.
- Linked TON address.
- Wallet status.
- Transaction history.

### 12.2. Withdrawal Method

In the initial phase, the game supports only:

```text
TON wallet
```

The player links a TON address. When approved, the operations team sends TON from the game treasury.

TON Connect enables secure communication between wallets and applications, allowing users to authorize transactions while retaining control of their private keys.

### 12.3. Withdrawal Conditions

A withdrawal request is allowed only when:

- The player has enough available Coins.
- The account is active.
- The account has no high-severity fraud flag.
- The TON address is valid.
- The daily withdrawal limit is available.

### 12.4. Withdrawal Lifecycle

| Status | Meaning |
|---|---|
| Pending | Request created, waiting for review |
| Under Review | Being reviewed by operations or anti-fraud |
| Approved | Approved, waiting for TON transfer |
| Processing | TON transfer in progress |
| Completed | TON transfer successful |
| Rejected | Request rejected; Coins returned |
| Failed | Transfer failed; requires handling |

### 12.5. Initial Withdrawal Limits

| Limit | Value |
|---|---|
| Minimum withdrawal | 25,000 Coins |
| Requests per day | 1 |
| System-wide daily payout cap | Enabled |
| Approval method | Batch approval |
| Automatic instant withdrawal | Disabled |

### 12.6. Withdrawal Rules

- Do not promise a fixed Coins-to-TON exchange rate.
- If a reference rate is shown, clearly label it as subject to change.
- Every withdrawal request must be a separate database record.
- If a withdrawal is rejected, Coins must return to the available balance.
- The ledger must record the reason for rejection.
- Never store treasury seed phrases or private keys in the database or client.

## 13. Fraud and Anti-Abuse

### 13.1. Goal

Prevent bots, auto-play, multi-account abuse, and reward exploitation without blocking legitimate players unnecessarily.

### 13.2. Fraud Signals

| Category | Signals |
|---|---|
| Gameplay | Abnormal game duration, abnormal event density, impossible score |
| Account | Multiple accounts from same IP or device |
| Ads | Duplicate reward IDs, rewards too fast, coordinated reward claims |
| Referral | Self-referral, multi-account networks |
| Withdrawal | New account withdrawing immediately, repeated requests from same IP/device |

### 13.3. Fraud Actions

| Severity | Action |
|---|---|
| Low | Record flag; allow continued play |
| Medium | Exclude from leaderboard; temporarily block rewards |
| High | Block rewards and withdrawals; require review |
| Confirmed fraud | Ban account; reverse rewards; reject withdrawal |

### 13.4. Fraud Rules

- Every flag must have a reason and evidence.
- Do not automatically ban based on one signal.
- Admins must be able to view flag history.
- Admins must be able to remove flags when appropriate.

## 14. Admin Panel

### 14.1. Admin Modules

| Module | Functions |
|---|---|
| Dashboard | DAU, retention, revenue, payout ratio |
| Users | Search players, view profiles, Coins, history |
| Game Sessions | View sessions, events, flags |
| Rewards | View ad, achievement, quest, referral rewards |
| Leaderboards | View periods, results, reward payouts |
| Withdrawals | Approve, reject, track requests |
| Ads | View impressions, fill rate, eCPM, revenue |
| Fraud | View flags, reasons, decisions |
| Content | Configure achievements, quests, events |
| Treasury | View TON balance, payout history |

### 14.2. Admin Roles

| Role | Permissions |
|---|---|
| Viewer | View data only |
| Operator | Approve rewards, handle support cases |
| Finance | Approve withdrawals, manage treasury |
| Super Admin | Manage admins, system configuration |

### 14.3. Audit Log

Every important admin action must be logged:

- Who performed the action.
- When it was performed.
- What changed.
- Why it changed.

Rules:

- Do not delete audit logs.
- Withdrawal approvals must be logged.
- Coin adjustments must be logged.
- Reward configuration changes must be logged.

## 15. Reporting and KPIs

### 15.1. Player Metrics

| Metric | Meaning |
|---|---|
| DAU | Daily active users |
| D1 Retention | Players returning next day |
| D7 Retention | Players returning after 7 days |
| Average Sessions | Games played per user |
| Session Length | Average time spent |

### 15.2. Ad Metrics

| Metric | Meaning |
|---|---|
| Impressions | Number of ad views |
| Fill Rate | Percentage of ad requests filled |
| eCPM | Effective revenue per 1,000 impressions |
| Ad Revenue | Total ad earnings |
| Rewarded Participation | Percentage of eligible players choosing rewarded ads |

### 15.3. Economy Metrics

| Metric | Meaning |
|---|---|
| Coins Issued | Total Coins created |
| Coins Spent | Total Coins used |
| Coins Held | Coins reserved for withdrawals |
| Payout Ratio | Rewards divided by ad revenue |
| ARPDAU | Average revenue per daily active user |

### 15.4. Risk Metrics

| Metric | Meaning |
|---|---|
| Fraud Flags | Number of suspicious activities |
| Blocked Sessions | Sessions excluded from rewards |
| Duplicate Rewards | Rewards credited more than once |
| Pending Withdrawals | Withdrawals waiting for approval |

## 16. Launch Priorities

### 16.1. Phase 1: Foundation

- Telegram player system.
- Game session and event system.
- Server-side scoring.
- Coins Ledger.
- Best score tracking.

### 16.2. Phase 2: Retention

- Achievements.
- Daily Quests.
- Login streak.
- Leaderboards.
- Referral system.

### 16.3. Phase 3: Revenue

- AdsGram rewarded ads.
- Reward URL verification.
- Daily reward limits.
- TADS banner and fullscreen ads.
- Ad performance reporting.

### 16.4. Phase 4: Real Rewards

- Wallet.
- TON withdrawal requests.
- Withdrawal queue.
- Treasury and payout history.
- Admin approval.
- Advanced anti-fraud.

## 17. Final Principles

The system must guarantee three things:

```text
No one can add Coins themselves.
No one can receive the same reward twice.
No one can withdraw money unless the system has verified behavior and rewards.
```

If a feature cannot satisfy all three conditions, it should not be opened to players.

Telegram Mini Apps are web applications displayed inside Telegram, and TON Connect is the standard connection protocol for TON wallets in the Telegram ecosystem.
