# OlympiFi
# Proof-of-Skill Social Trading Platform

Version: 0.1  
Date: 2026-09-03  
Status: Internal project document  
Primary goal: Build a Solana consumer app with a strong startup wedge

## 1. Executive Summary

We are building a Solana-native social trading platform where trader status is earned through verified, risk-adjusted performance instead of screenshots, clout, or raw PnL.

The product combines three ideas:

- Social trading: profiles, follows, activity feed, public trade/thesis sharing.
- Proof-of-Skill: wallet-verified trading performance, risk-adjusted scoring, and trader reputation.
- Gamified progression: XP, levels, quests, badges, seasons, and leagues that make trading feel competitive and rewarding.

The wedge is not "Instagram for traders" and not "FOMO with levels." The wedge is:

> A social trading arena where Solana traders level up through verified skill.

The first version should prove that traders want a public identity based on credible performance, and that followers want to discover traders based on skill rather than hype.

## 2. Product Thesis

Crypto trading is already social, but trust is broken.

Current trader reputation is built from:

- screenshots
- follower count
- viral calls
- selective posting
- raw PnL leaderboards
- Telegram/X clout
- survivorship bias

This creates a bad environment for users. Traders can look skilled while taking reckless risk, hiding losses, deleting bad calls, or only showing lucky wins.

Our thesis:

> The next social trading platform should rank traders by verified, risk-adjusted skill and make that progression fun.

Solana is a strong starting point because trading activity can be verified from wallet history, execution can route through Jupiter, transaction costs are low, and consumer UX can be smooth enough for gaming-style interaction.

## 3. Positioning

### One-Liner

A Solana-native social trading arena where traders level up through verified, risk-adjusted performance.

### Short Pitch

Social trading is exploding, but most platforms reward clout, screenshots, and reckless PnL. We are building a trading game where status is earned through verified Solana performance. Traders can practice privately, prove skill over time, reveal performance selectively, compete in weekly leagues, and build a public profile followers can trust.

### Differentiation

We are different from generic social trading apps because the core ranking system is not based on raw PnL or follower count. It is based on Proof-of-Skill:

- realized trading performance
- consistency
- max drawdown
- volatility
- sample size
- trade discipline
- league performance
- optional thesis accuracy

The social layer grows around the skill graph.

## 4. Target Users

### Primary User: Active Solana Trader

This user already trades memecoins, blue-chip Solana assets, or perps. They want status, distribution, and proof that they are better than random callers.

Needs:

- prove skill
- grow reputation
- compete with others
- get discovered
- eventually monetize audience

### Secondary User: Follower or Learner

This user wants to watch better traders, learn how they think, and eventually participate.

Needs:

- discover credible traders
- avoid fake gurus
- understand risk
- follow trades or theses safely
- learn from verified outcomes

### Tertiary User: Competitive Trader

This user is motivated by rankings, leagues, seasons, prizes, and public recognition.

Needs:

- fair leaderboards
- transparent scoring
- repeatable competitions
- social visibility
- proof of achievement

### Future User: Creator Trader

This user has proven performance and wants to monetize.

Future needs:

- paid sessions
- private groups
- hosted competitions
- copy trading revenue share
- premium analysis

## 5. Product Principles

1. Verified beats claimed.
   Public status should come from wallet-verifiable behavior, not screenshots.

2. Risk-adjusted beats raw PnL.
   A trader who makes 20 percent with low drawdown should often rank above a trader who makes 50 percent by taking reckless risk.

3. Progression should reduce pressure.
   Private Sandbox lets users build proof before exposing every move publicly.

4. Fun should not become casino design.
   Gamification should reward discipline, consistency, and learning, not volume spam or leverage abuse.

5. Social feeds should be high-signal.
   The feed should focus on meaningful events: rank-ups, closed trades, theses, league results, and verified milestones.

6. Solana should matter.
   The app should use Solana for trading, verification, identity, and transparent achievement history.

## 6. Product Scope

### Hackathon Scope

The hackathon build should focus on a complete vertical slice:

1. Connect wallet.
2. Create trader profile.
3. Trade through the app or import wallet history.
4. Mark trades as private or public.
5. Compute Skill Score.
6. Show public profile and proof page.
7. Join a weekly league.
8. Update leaderboard from verified performance.
9. Show key events in the social feed.
10. Share profile or league result publicly.

### Post-Hackathon Scope

After the hackathon, expand into:

- richer social feed
- comments and reactions
- trader theses
- creator tools
- paid sessions
- copy trading
- clans or teams
- advanced league types
- token/NFT rewards only if they are legally and economically sound

### Explicitly Out of Scope for First Build

These should not distract the team before the core demo works:

- full chat system
- direct messages
- paid live streams
- complex creator subscriptions
- platform token
- NFT marketplace
- fully automated copy trading
- complex moderation system
- mobile app from day one
- too many league formats

## 7. Core User Experience

### Main Loop

1. User connects wallet.
2. User enters Private Sandbox.
3. User makes or imports trades.
4. App computes verified performance.
5. User earns XP and improves Skill Score.
6. User unlocks levels, badges, and visibility.
7. User joins a weekly league.
8. User appears on leaderboards.
9. Followers discover the user through rankings and feed events.
10. User shares profile publicly to build reputation.

### Emotional Loop

The product should make users feel:

- "I am improving."
- "My skill is visible."
- "My rank is earned."
- "I can compete without exposing everything."
- "Followers can trust my public profile."

## 8. Feature Set

## 8.1 Wallet and Identity

Users sign in with a Solana wallet.

Initial requirements:

- connect wallet
- create username
- optional profile image
- optional bio
- optional X/Telegram link
- optional .sol identity support later
- profile tied to wallet address

Future requirements:

- multi-wallet linking
- wallet proof signing
- account recovery via social login or embedded wallet
- verified creator account

## 8.2 Trader Profile

The trader profile is the main public asset.

Profile should include:

- username
- wallet verification status
- current level
- rank tier
- Skill Score
- XP progress
- realized PnL
- win rate
- max drawdown
- consistency score
- risk score
- trade count
- average hold time
- profit factor
- equity curve
- recent public activity
- league history
- badges
- followers/following

Profile views:

- public view for followers
- private owner view with deeper stats
- proof view for shareable verification

## 8.3 Private Sandbox

Private Sandbox is a private trading and reputation-building mode.

Purpose:

- reduce social pressure
- let users build proof before public exposure
- prevent the platform from becoming only performative
- allow gradual reveal of performance

Core behavior:

- user trades privately by default
- individual private trades are hidden from public feed
- aggregate stats can still count toward Skill Score
- user can later reveal selected trades or performance summaries

Reveal levels:

- Private: no public trade data
- Aggregate: show PnL percent and risk stats only
- Partial: show token, direction, entry/exit result, but not full sizing
- Full: show full trade details

For the hackathon, implement:

- private/public toggle
- aggregate performance proof
- manual reveal action

## 8.4 Trading Interface

The app should support real or simulated trading through a clean trade ticket.

Initial trading flow:

- select token
- view basic token info
- enter amount
- choose private or public visibility
- execute trade
- show transaction status
- update profile metrics

Execution options:

- Jupiter integration for swaps
- devnet simulation for demo safety if mainnet integration is not ready
- mainnet-beta read/indexing for wallet history

Important:

- The demo should clearly show why Solana matters.
- If real trading is risky before launch, use realistic simulation plus real wallet history import.

## 8.5 Token Registry and Asset Safety

Use a canonical token source where possible.

Planned token handling:

- verified token list
- token symbol/logo/name
- Token-2022 extension badges
- suspicious/unverified token warning
- token category labels
- memecoin/blue-chip/stablecoin/perp labels where relevant

Token category affects scoring because risk differs by asset type.

Example:

- high volatility memecoin profit gets scored differently from stablecoin yield or blue-chip swing trading
- low-liquidity tokens receive manipulation-risk flags

## 8.6 Skill Score

Skill Score is the core trust primitive inside the consumer app.

It should answer:

> Is this trader consistently good, or just lucky/risky?

Inputs:

- realized PnL percentage
- absolute realized PnL
- win rate
- trade count
- profit factor
- max drawdown
- return volatility
- average hold time
- average loss size
- risk concentration
- token risk category
- consistency across days/weeks
- league performance
- thesis accuracy later

High-level formula:

```text
Skill Score =
  profitability component
+ consistency component
+ risk management component
+ league performance component
+ thesis accuracy component
- drawdown penalty
- volatility penalty
- concentration penalty
- small sample penalty
- suspicious activity penalty
```

The first version should not pretend to be perfect. It should be transparent, explainable, and visibly better than raw PnL.

### Sample Score Components

Profitability:

- rewards realized positive return
- caps extreme outlier impact
- separates realized from unrealized gains

Consistency:

- rewards steady performance across multiple sessions
- penalizes one-trade wonders

Risk Management:

- rewards low max drawdown
- rewards controlled position sizing
- penalizes catastrophic losses

Sample Size Confidence:

- score confidence increases with more trades
- small samples can rank but should show lower confidence

League Performance:

- rewards beating peers in defined time windows
- records seasonal achievements

Thesis Accuracy:

- future feature
- rewards users who post reasoning before entering a trade
- penalizes deleted or edited claims

## 8.7 Levels and Progression

Levels make skill feel like visible progress.

Example level system:

| Level | Name | Unlocks |
| --- | --- | --- |
| 1 | Rookie | Basic profile, private sandbox, basic trading |
| 2 | Scout | Public aggregate stats, first badges |
| 3 | Operator | Public trade reveal, follow feed visibility |
| 4 | Specialist | League eligibility, richer analytics |
| 5 | Contender | Higher leaderboard visibility, thesis posting |
| 6 | Pro | Host small leagues, advanced profile stats |
| 7 | Elite | Featured discovery eligibility |
| 8 | Master | Creator tools preview |
| 9 | Legend | Premium creator tools later |

For hackathon, use 5 levels instead of 9:

- Rookie
- Scout
- Operator
- Contender
- Elite

Keep it understandable in a demo.

## 8.8 XP System

XP is the short-term reward system. Skill Score is the long-term reputation system.

XP should reward constructive actions:

- complete onboarding
- connect wallet
- make first private trade
- close a trade
- maintain a low drawdown streak
- post a thesis before a trade
- join a league
- complete a league
- improve personal Skill Score
- reveal a verified performance milestone

XP should not reward:

- trading volume alone
- reckless leverage
- spam trades
- fake engagement
- referral farming
- wash trading

XP unlocks levels, badges, cosmetics, and feature access. It should not be the same as Skill Score.

## 8.9 Quests

Quests create daily and weekly reasons to return.

Quest examples:

- First Proof: complete one verified trade
- Discipline Run: keep max drawdown below 10 percent for 7 days
- Thesis First: publish reasoning before a trade
- Clean Close: close 3 trades with positive risk/reward
- Rookie League: complete your first weekly league
- Comeback: recover from a drawdown without exceeding risk limits
- Consistency Week: trade on 3 separate days with controlled exposure

Quest types:

- onboarding quests
- daily quests
- weekly quests
- seasonal quests
- league-specific quests

## 8.10 Badges

Badges should represent real behavior.

Examples:

- Verified Trader
- Low Drawdown
- Consistent Closer
- Early Spotter
- Thesis Verified
- Rookie League Finalist
- Weekly Champion
- Comeback Trader
- Risk Master
- No-Revenge Streak

Badges should have proof pages:

- what the badge means
- when it was earned
- what data qualified the user
- whether it is verified by wallet activity

## 8.11 Leagues and Competitions

Leagues are the main public game mode.

Initial league:

- 7-day trading league
- users join with wallet
- users trade normally or through the app
- score is based on risk-adjusted return
- leaderboard updates periodically
- final placement becomes part of profile history

Leaderboard categories:

- overall Skill Score
- weekly risk-adjusted return
- rookie climbers
- consistency
- low drawdown
- best thesis later

Why multiple leaderboards matter:

If the only leaderboard is raw PnL, most users lose interest. Multiple boards let different types of skill be recognized.

Future league types:

- memecoin sprint
- blue-chip swing league
- no-leverage league
- stablecoin strategy league
- thesis league
- team league
- creator-hosted league

## 8.12 Social Feed

The feed should be high-signal.

Feed events:

- user leveled up
- user earned a badge
- user closed a public trade
- user revealed a private performance milestone
- user entered a league
- user won a league
- user posted a thesis
- user entered top 10

Feed tabs:

- Following
- Global
- Rising
- Leagues

For hackathon, build:

- Global feed
- Following feed if time allows
- event cards for rank-ups, trades, badges, and league results

## 8.13 Follow System

Users can follow traders.

Initial behavior:

- follow/unfollow
- follower count
- following count
- following feed
- profile discovery based on rank and recent activity

Future behavior:

- notifications
- watchlists
- creator subscriptions
- private groups

## 8.14 Thesis System

A thesis is a public reason attached to a trade.

Purpose:

- make trading educational
- reduce low-quality signal spam
- let followers judge reasoning
- create accountability

Initial thesis fields:

- token
- direction
- timeframe
- entry reasoning
- invalidation condition
- confidence
- visibility

Future scoring:

- compare thesis outcome to actual result
- reward pre-trade reasoning
- penalize edited/deleted post-hoc claims

For hackathon, thesis can be lightweight or demo-only.

## 8.15 Proof Page

Every meaningful achievement should be shareable.

Proof pages:

- trader profile proof
- badge proof
- league result proof
- trade proof
- private aggregate proof

Proof page should show:

- wallet address or verified account
- metric summary
- timestamp
- source of verification
- transaction links where applicable
- explanation of scoring

This is important for judges because it makes the Solana-native value obvious.

## 9. Product Architecture

## 9.1 Frontend

Recommended:

- Next.js
- TypeScript
- Tailwind CSS
- shadcn/ui or a small internal component system
- Solana wallet adapter
- TanStack Query for data fetching
- Zustand or React context for light client state
- Recharts or lightweight charting for profile/equity charts

Key screens:

- landing/waitlist page
- onboarding
- dashboard
- trade ticket
- trader profile
- feed
- league page
- leaderboard
- proof page
- settings

## 9.2 Backend

Recommended:

- Node.js with Next.js API routes, or separate Express/Fastify service
- PostgreSQL
- Prisma or Drizzle ORM
- Redis for jobs/rate limits if needed
- background workers for indexing and score recalculation

Backend responsibilities:

- user profile storage
- follow graph
- feed events
- league management
- scoring computation
- trade visibility rules
- indexed wallet activity cache
- proof records
- anti-abuse checks

## 9.3 Solana Integration

Core integrations:

- Solana wallet login
- transaction signature verification
- Jupiter swap routing
- Solana RPC provider
- token metadata source
- explorer links for transactions

Possible providers:

- Helius
- Triton
- QuickNode
- Alchemy
- native Solana RPC for limited demo use

Indexing requirements:

- wallet transaction history
- swaps
- token transfers
- trade entry/exit events
- realized PnL estimation
- token prices

PnL can be difficult for all wallet history. For the first version, prioritize trades executed inside the app because they are easier to measure correctly.

## 9.4 Data and Analytics

Core tables/entities:

- users
- wallets
- profiles
- trades
- positions
- token_metadata
- visibility_settings
- skill_scores
- xp_events
- levels
- badges
- badge_awards
- quests
- quest_progress
- leagues
- league_entries
- leaderboard_snapshots
- feed_events
- follows
- proofs

Analytics events:

- wallet_connected
- profile_created
- trade_started
- trade_executed
- trade_closed
- visibility_changed
- skill_score_updated
- xp_earned
- badge_earned
- league_joined
- league_completed
- profile_shared
- user_followed

## 10. Suggested Data Model

### User

- id
- username
- displayName
- avatarUrl
- bio
- createdAt
- updatedAt

### Wallet

- id
- userId
- address
- chain
- isPrimary
- verifiedAt

### Trade

- id
- userId
- walletAddress
- inputToken
- outputToken
- side
- amountIn
- amountOut
- entryPrice
- exitPrice
- realizedPnl
- realizedPnlPercent
- txSignatureOpen
- txSignatureClose
- visibility
- status
- openedAt
- closedAt

### SkillScore

- id
- userId
- score
- confidence
- pnlComponent
- consistencyComponent
- riskComponent
- leagueComponent
- penaltyComponent
- calculatedAt

### League

- id
- name
- type
- startsAt
- endsAt
- status
- scoringMode
- createdBy

### LeagueEntry

- id
- leagueId
- userId
- startingScore
- finalScore
- rank
- joinedAt

### BadgeAward

- id
- userId
- badgeKey
- proofId
- awardedAt

### Proof

- id
- userId
- type
- title
- dataHash
- publicUrl
- txSignature
- createdAt

## 11. Technical Challenges

### PnL Accuracy

Accurate PnL from arbitrary wallet history is hard because users may:

- buy across multiple wallets
- transfer tokens in/out
- trade on multiple venues
- receive airdrops
- bridge assets
- partially close positions

First-version solution:

- make in-app trades the source of truth
- support wallet import as "estimated history"
- clearly label confidence
- compute PnL per app-managed position

### Anti-Gaming

Risks:

- wash trading
- tiny trade farming
- low-liquidity manipulation
- multiple wallets
- high-risk all-in trades
- fake engagement
- selective reveal abuse

Mitigations:

- minimum trade size for scoring
- token liquidity filters
- sample-size confidence multiplier
- drawdown penalties
- concentration penalties
- suspicious token flags
- league-specific rules
- public scoring explanations

### Regulatory and Safety Risk

The product touches trading, competitions, paid features, and possibly copy trading.

Early rules:

- no guaranteed returns
- no financial advice claims
- no custodial funds
- no automated copy trading in first version
- no platform token before legal review
- clear risk disclosures
- competitions should avoid unclear gambling mechanics

## 12. Hackathon Demo Plan

The demo should tell one story:

> A new trader joins, trades privately, earns verified skill, reveals proof, enters a league, and becomes discoverable through a ranked social feed.

Demo flow:

1. Connect wallet.
2. Create profile.
3. Open Private Sandbox.
4. Execute or simulate a Jupiter trade.
5. Close trade and calculate PnL.
6. Skill Score updates.
7. XP is awarded.
8. User levels up.
9. User reveals aggregate proof.
10. User joins weekly league.
11. Leaderboard updates.
12. Public feed shows rank-up and league activity.
13. Shareable proof page opens.

Judges should understand within 60 seconds:

- what the product is
- why Solana matters
- how it is different from social trading clones
- why users would return
- how it can become a company

## 13. MVP Acceptance Criteria

The first serious version is complete when:

- users can connect a wallet
- users can create a profile
- users can execute or record a trade
- trades have private/public visibility
- realized PnL can be calculated for app trades
- Skill Score updates from trade data
- XP and levels update from user actions
- at least one league can run end to end
- leaderboard ranks users by risk-adjusted score
- public profile displays verified stats
- feed displays key events
- proof page is shareable

## 14. Roadmap

### Phase 0: Pre-Hackathon Preparation

Allowed work should focus on planning and validation:

- brand/name exploration
- landing page
- waitlist
- trader interviews
- Figma prototype
- scoring formula design
- architecture plan
- social account setup
- build-in-public content
- competitor teardown

### Phase 1: Hackathon Build

Build:

- wallet auth
- profile
- app-tracked trades
- private/public toggle
- Skill Score
- XP/levels
- badges
- one league format
- leaderboard
- feed
- proof page
- demo script

### Phase 2: Private Beta

Build:

- better wallet history import
- improved PnL engine
- more quests
- following feed
- trader discovery
- notifications
- anti-abuse rules
- analytics dashboard

### Phase 3: Growth

Build:

- creator profiles
- hosted leagues
- richer thesis system
- referral loops
- social integrations
- team leagues
- mobile-first UX

### Phase 4: Monetization

Possible models:

- trading fee share
- league entry fee cut
- creator subscription fee
- premium analytics
- featured league sponsorships
- API/license for reputation score later

## 15. Social Presence Strategy

The project should build in public before and during the hackathon.

Content themes:

- "Raw PnL leaderboards are broken"
- "Why trader reputation needs drawdown"
- "Private Sandbox demo"
- "Skill Score formula breakdown"
- "Can you prove you are a good trader?"
- weekly leaderboard screenshots
- trader interview clips
- founder build updates

Pre-launch goals:

- 20 to 50 trader interviews
- 100+ waitlist signups
- 10 to 20 beta traders
- 5 public testimonials or quotes
- 3 to 5 public demo clips

## 16. Team Roles

Minimum team:

- Product/Founder: owns vision, user interviews, pitch, scope, demo story
- Frontend Engineer: owns app UI, wallet UX, feed, profile, league screens
- Backend Engineer: owns database, scoring, league logic, APIs, indexing jobs
- Solana Engineer: owns wallet integration, Jupiter, transaction parsing, PnL logic
- Designer/Growth: owns visual identity, prototype, social content, demo polish

If the team is small, combine roles:

- Founder/Product/Growth
- Full-stack Engineer
- Solana/Backend Engineer
- Designer part-time

## 17. Product Naming Directions

Possible name territories:

- SkillArena
- TradeArena
- ProofSkill
- TraderRank
- RankFi
- SignalRank
- ProofTrade
- ArenaFi
- EdgeRank
- LevelTrade

Naming criteria:

- easy to say
- social/gaming energy
- credible for finance
- not too meme-only
- domain and handle availability

## 18. Success Metrics

Product metrics:

- wallet connects
- profile creation rate
- first trade completion rate
- private-to-public reveal rate
- league join rate
- league completion rate
- profile shares
- follower graph growth
- 7-day retention

Hackathon metrics:

- working demo completeness
- number of beta users
- waitlist signups
- social engagement
- trader feedback quality
- clarity of pitch
- Solana-native depth

Business metrics later:

- trading volume
- active traders
- active followers
- league participation
- creator conversion
- revenue per trader

## 19. Key Risks

### Product Risk

Users may like rankings but not trust the score.

Mitigation:

- keep score explainable
- show components
- label confidence
- let users inspect proof

### Market Risk

Social trading may already be crowded.

Mitigation:

- focus on verified skill and private progression
- avoid copying feed-first products
- build a unique league and scoring system

### Technical Risk

PnL calculation can become complex.

Mitigation:

- start with app-executed trades
- label wallet-imported stats as estimated
- support more venues later

### Safety Risk

Gamification can encourage reckless trading.

Mitigation:

- reward risk control
- penalize large drawdowns
- avoid volume-based XP
- include warnings and limits

### Regulatory Risk

Competitions, copy trading, and paid creator tools may introduce legal complexity.

Mitigation:

- delay paid features
- avoid custody
- avoid guaranteed-return claims
- get legal review before monetized competitions or copy trading

## 20. Final Product Direction

The project should be built as a consumer app, not a protocol-first product.

The correct hierarchy:

1. Proof-of-Skill is the wedge.
2. Gamification is the engagement loop.
3. Social trading is the interface.
4. Leagues are the repeatable game mode.
5. Creator monetization is the future business model.

The simplest final description:

> A Solana-native social trading arena where traders earn levels, badges, and followers through verified, risk-adjusted performance.

The hackathon product should feel fun, but the trust layer should feel serious. That combination is the main advantage.
