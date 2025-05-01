# FIFA World Cup Database

A PostgreSQL database containing historical World Cup match data from 2014 and 2018 tournaments, designed for sports analytics and educational purposes.

## Database Structure

### Tables

1. **teams**
   - `team_id`: Primary key (serial)
   - `name`: Team name (varchar)

2. **games**
   - `game_id`: Primary key (serial)
   - `year`: Tournament year (integer)
   - `round`: Match stage (varchar)
   - `winner_id`: Foreign key to teams (integer)
   - `opponent_id`: Foreign key to teams (integer)
   - `winner_goals`: Goals scored by winner (integer)
   - `opponent_goals`: Goals scored by opponent (integer)

### Relationships
- `games.winner_id` → `teams.team_id`
- `games.opponent_id` → `teams.team_id`

## Installation

1. Ensure PostgreSQL is installed (version 12 or higher recommended)
2. Create a new database user if needed:
   ```sql
   CREATE USER freecodecamp WITH PASSWORD 'yourpassword';
