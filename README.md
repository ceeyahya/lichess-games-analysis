[![Mastodon](https://img.shields.io/badge/Mastodon-5c4bdf?style=for-the-badge&logo=Mastodon&logoColor=ffffff&link=https://fosstodon.org/@hya)](https://fosstodon.org/@hya)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=LinkedIn&logoColor=ffffff&link=https://www.linkedin.com/in/yahya-chahine/)](https://www.linkedin.com/in/yahya-chahine/)
[![Portfolio](https://img.shields.io/badge/Portfolio-6366f1?style=for-the-badge&logo=Internet-Explorer&logoColor=ffffff&link=https://www.chahineyahya.dev)](https://www.chahineyahya.dev)

# Lichess Games: Data Analysis

## Project Purpose

Chess has gained more popularity with the release of the Netflix's the Queen's Gambit, and the COVID-19 lockdowns.
Due to it's strict rules and limited (in computer metrics) numbers of possible moves, chess has been an ideal study subject
for Artificial Intelligence and Machine Learning research.

> **NOTE**
> This README only aims to provide a short introduction to the project, a more detailed write up is available on my portoflio
> [https://chahineyahya.dev/projects/norman-says](https://chahineyahya.dev/projects/norman-says).

## Analysis

The dataset consists of ~20000 chess games harvested from Lichess.org, each row contains the following columns:

- game_id: a unique identifier for each game.
- rated: a boolean that determines whether the game is friendly (will not impact your ELO) or rated.
- created_at: the timestamp at which the game started.
- last_move_at: when was the last move of the game played.
- turns: the total number of turns the game took.
- victory_status: the outcome of the game (mate, draw, resign, outoftime).
- winner: who from black or white won the game.
- increment_code: the increment code explained earlier i.e. the duration of the game and the small amount of time added
  to the time after the opponent's turn.
- white_id: white player's Lichess username.
- white_rating: white player's ELO (explained in the next section).
- black_id: black player's Lichess username.
- black_rating: white player's ELO.
- all_moves: all moves of the game in chess notation mentioned earlier.
- opening_name: games in chess are divided into 3 parts openings, mid-game and endings this column states the opening's name.
- opening_eco: each standard opening is attributed a code that can be accessed [here](https://www.365chess.com/eco.php).
- opening_ply: the number of moves in the opening phase.

The code in the Jupyter Notebook analyses the dataset, and provides in-depth insights about the dataset i.e. ELO Distribution, Number of checks,
Castling statistics and more. Finally it investigates the possibility of using the dataset for Machine Learning predictions.

## Setup

The project is setup using pipenv and pyenv, a local setup is therefore fairly simple.

- Start by cloning the repo.

```console
git clone git@github.com:ceeyahya/lichess-games-analysis.git
```

- Create a virtual environment with the your favourite utility.

- Install the dependencies.

```console
pipenv install
```

- Start running the code.

## Dataset

The dataset used for this analysis was downloaded from [Kaggle.com](https://kaggle.com) and is accessible by clicking
on this [link](https://www.kaggle.com/datasets/datasnaek/chess).
