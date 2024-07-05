# freeCodeCamp_worldCup_SQL

## Overview

This project involves creating, populating, and querying a PostgreSQL database to store and analyze data from the final three rounds of the World Cup tournaments since 2014. The data includes details about the games, the teams involved, and the scores. The project is divided into three main parts: database creation, data insertion, and data querying.

## Database Schema

### Teams Table
- `team_id`: SERIAL PRIMARY KEY
- `name`: VARCHAR UNIQUE NOT NULL

### Games Table
- `game_id`: SERIAL PRIMARY KEY
- `year`: INT NOT NULL
- `round`: VARCHAR NOT NULL
- `winner_id`: INT REFERENCES teams(team_id) NOT NULL
- `opponent_id`: INT REFERENCES teams(team_id) NOT NULL
- `winner_goals`: INT NOT NULL
- `opponent_goals`: INT NOT NULL

## Files in the Repository

- `games.csv`: The source data file containing World Cup game details.
- `insert_data.sh`: A bash script to populate the database with data from `games.csv`.
- `queries.sh`: A bash script containing SQL queries to extract insights from the database.
- `README.md`: This file.

## Setup Instructions

1. **Clone the Repository**
   ```sh
   git clone https://github.com/yourusername/worldcup-database.git
   cd worldcup-database
