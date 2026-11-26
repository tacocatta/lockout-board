# Square Off

A judging app and projector scoreboard for a team math competition. Teams race to solve problems on a shared board, and the first team to solve a problem claims that square.

**Live:** https://tacocatta.github.io/lockout-board/

## How the game works

- Teams of about 4 work on a board of problems (16 per round), all shown on the projector.
- When a team thinks it has an answer, it hands in a slip with the problem number and answer.
- The first team with a correct answer **claims** the problem: full points, and the square turns their colour.
- The next correct team gets half points, and then the problem is closed.
- Each round has a countdown. The team with the most points wins, and ties go to the team that reached that score first.

## Scoring

Each problem is worth points based on difficulty: **Easy 10, Medium 20, Hard 30, Boss 50**.

Optional extra rules, under **Setup → Scoring rules** (all off by default):

- **Solve order:** change how many teams can score on a problem and what share they get, e.g. 100%, 100%, 50%, 25%.
- **Bounties:** unclaimed problems gain points every few minutes.
- **Comeback:** in the last few minutes, the bottom teams score extra.
- **Wrong-answer penalty:** lose points for each wrong slip.

## Running it

1. Open the app on the judges' laptop (**Judge** view).
2. Open it in a second tab, switch to **Projector**, move it to the projector screen and press **Full screen**.
3. In **Setup → Boards**, press **Add Set 1** for three ready-made 15-minute rounds, or write your own problems in **Setup**.
4. Pick the round from the **Board** menu and press **Start**.
5. For each slip, pick the team and the problem, compare the slip with the answer shown, and press **Correct** or **Wrong**.

Both tabs must be in the same browser on the same computer. Scores are saved in that browser. Use **Setup → Copy backup** to keep a copy.

## Writing problems

Write math in LaTeX between dollar signs, like `$\frac{1}{x}$` or `$2^{10}$`. To accept more than one answer, separate them with `|`, as in `Sunday|sun`.
