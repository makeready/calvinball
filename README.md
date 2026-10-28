# Calvinball


<img width="1400" height="991" alt="image" src="https://github.com/user-attachments/assets/94311faf-5d63-4523-94fc-2cfe28beb33a" />
Apologies and thanks to Bill Watterson :)

A two-player game for [Claude Code](https://claude.com/claude-code), where the real contest is prompting.

Players take turns writing prompts. The first prompt creates a game, and every later prompt changes it. After each build, both players play the game, and whoever it declares the winner scores a point. Like Calvin and Hobbes's version, the rules never stay the same.

Claude is a neutral builder and scorekeeper. It never asks clarifying questions, so every gap in a prompt becomes a decision the players can see. That makes it a way to practise getting exactly what you want out of a model, and to lay traps the other player can't prompt their way out of.

## Install

Copy `.claude/skills/calvinball/` into a project's `.claude/skills/` folder, or into `~/.claude/skills/` to use it everywhere.

## Play

Start Claude Code and say something like "let's play calvinball". Claude asks for the players' names and the number of rounds (6 by default), then asks Player A for the first prompt.

Each match is saved under `matches/` in the current directory, with the rulebook, scoreboard, current game and a snapshot after every round, so a match can be resumed later.

## Rules in brief

- Turns alternate: A prompts odd rounds, B prompts even rounds.
- Each round is worth one point, to whoever the game itself declares the winner. If the build crashes, the point goes to the player who didn't prompt.
- Prompts can add meta-rules ("the lava can never be removed"), but nothing can change turn order, the round count or scoring.
- A match tied after the final round goes to one blind tiebreaker round, which both players prompt without seeing each other's prompt.

The full rules are in [`SKILL.md`](.claude/skills/calvinball/SKILL.md).
