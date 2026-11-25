# Lockout Board

A live judging app and projector scoreboard for **lockout-style math competitions**. Teams race to solve problems on a shared board. The first team to solve a problem claims it, the next few teams can still score on it, and problems unlock in timed waves.

It's a single `index.html` with no install, no build step and no server.

**Live:** https://tacocatta.github.io/lockout-board/

## Running a competition

1. Open the app on the judges' laptop. You start in the **Judge** view.
2. Open it again in a second tab, switch to **Projector**, drag the tab onto the projector screen and press **Full screen** (bottom-right corner).
3. Press **Start** to begin the countdown.
4. For each answer slip a team hands in, the judge picks the team and the problem, checks the slip against the answer on screen, and presses **Correct** or **Wrong**.

The two tabs stay in sync live as long as they're open in the same browser on the same computer.

## Scoring rules

All rules can be changed or turned off in **Setup → Scoring rules**. Changing a rule recalculates every score, including slips already recorded.

| Rule | Default | How it works |
| --- | --- | --- |
| **Base points** | Easy 10, Medium 20, Hard 30, Boss 50 | Set per problem. |
| **Solve order** | 100%, 100%, 50%, 25% | The 1st and 2nd teams to solve a problem get full points, the 3rd gets half, the 4th a quarter. Then the problem closes. The first team to solve it *claims* it, and its card turns that team's colour. |
| **Claim cap** | 3 per wave | A team can claim at most 3 problems in each wave. After that, it can still solve problems other teams have already claimed. |
| **Bounties** | +5 every 5 min | Unclaimed problems grow in value over time, counted from when their wave opens. The value is locked in when someone claims the problem, and later solvers get their percentage of that locked value. |
| **Topic sweep** | +20 | Claim every problem in a topic (any topic with 2 or more problems) for a bonus. |
| **Comeback** | Bottom 3 teams ×1.5 | Once the last wave opens, the three lowest-ranked teams score 1.5× on every solve. |
| **Wrong answers** | No penalty | The penalty can be switched on in Setup. Wrong answers are still logged. |
| **Ties** | Always on | The team that reached that score first ranks higher. |

The active rules are listed on the projector under the leaderboard.

## Views

- **Judge:** record slips. Once you pick a team and a problem, it shows the problem, the answer, and exactly how many points that team would get, including bounty, comeback and sweep. Problems a team can't take are greyed out (locked wave, already solved, closed, or at the claim cap). You can also type the slip's answer for the app to check: `1/2`, `0.5` and `2/4` all count as the same answer. Also has undo, opening a wave early, and adding bonus or penalty points (for example for a lightning final).
- **Projector:** one screen showing every open question with LaTeX math and text sized to fit, claimed cards in team colours, bounty tags, the live leaderboard with comeback and sweep markers, the countdown, and pop-up banners for claims, sweeps, bounties and new waves. Click a question to show it full screen.
- **Log:** every slip with the points it earned, a Remove button for each, standings (points, claims, solves, sweeps), and **Copy results**.
- **Setup:** problems and answer key, scoring rules, waves, team names and colours, start fresh, and backup and restore.

## Writing problems

- Write math in LaTeX between dollar signs, like `$\frac{1}{x}$` or `$2^{2026}$`, or use `$$ … $$` for a centred line. The math is drawn by MathJax, which loads from the internet. Without internet the raw text still shows.
- Accept more than one answer by separating them with `|`, for example `Sunday|sun`.
- Problems that share a topic name form a sweep group.
- Add, delete and reorder problems freely, and add as many waves as you like. Board numbers follow the order in Setup.
- The app comes with 16 sample problems (answers checked) for testing. Replace them before the real event.

## Data

Everything is saved in the browser on that computer (`localStorage`), so refreshing loses nothing, and nothing is sent anywhere. Use **Setup → Copy backup** to save a copy or move a game to another computer.
