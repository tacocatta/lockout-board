# Square Off

A judging app and projector scoreboard for a team math competition. Teams race to solve problems on a shared board, and the first team to solve a problem claims that square.

**Live:** https://tacocatta.github.io/square-off/

## How the game works

- Teams of about 4 work on a board of problems (16 per round), all shown on the projector.
- When a team thinks it has an answer, it hands in a slip with the problem number and answer.
- The first team with a correct answer **claims** the problem: full points, and the square turns their colour.
- Every other team can still solve it, for fewer points the later they are.
- Each round has a countdown. The team with the most points wins, and ties go to the team that reached that score first.

## Scoring

Each problem is worth points based on difficulty: **Easy 10, Medium 20, Hard 30, Boss 50**.

The app starts with these recommended rules (change them in **Setup → Scoring rules**, or switch them all off for basic lockout):

- **Sliding scale:** every team can score on every problem. The 1st correct team gets 100% of its points, and each later team gets a bit less. With 10 teams that's 100%, 90%, 80% … 10%.
- **Claim cap:** a team can claim at most 3 problems per round. After that, it can still solve problems other teams have claimed.
- **Bounties:** unclaimed problems gain +10 points every 5 minutes.
- **Comeback:** in the last 4 minutes, the bottom 3 teams score ×1.5.
- **No penalty** for wrong answers.

Ties go to the team that reached that score first.

## Running it

1. Open the app on the judges' laptop (**Judge** view).
2. Open it in a second tab, switch to **Projector**, move it to the projector screen and press **Full screen**.
3. In **Setup → Boards**, press **Add Set 1** for three 13-minute rounds, or write your own problems in **Setup**.
4. Pick the round from the **Board** menu and press **Start**.
5. For each slip, pick the team and the problem, compare the slip with the answer shown, and press **Correct** or **Wrong**.

Add, remove or rename teams (up to 16) in **Setup → Teams**. Both tabs must be in the same browser on the same computer. Scores are saved in that browser. Use **Setup → Copy backup** to keep a copy.

## Writing problems

Write math in LaTeX between dollar signs, like `$\frac{1}{x}$` or `$2^{10}$`. To accept more than one answer, separate them with `|`, as in `Sunday|sun`.
