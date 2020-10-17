
# Dota Bot for Telegram

A bot to be like mango byte but for telegram

Get DOTA statistics about matches, players, etc


## Local Development
 - No api key needed, however rate limits apply
   - Api documentation can be found [here](https://docs.opendota.com/#)


## Installation & Environment Configuration 
 - Create a virtual environment using `python -m venv venv`
 - Activate virtual environment with `source venv/bin/activate` or windows equivalent
 - `pip install -r requirements.txt` to install dependencies
 - `cp .env.example .env` and change values as needed
 - `pre-commit install` adds the testing and lint hooks to pre-push (to make sure you do the right thing)

## Environment Variables
 - `OPEN_DOTA_API_BASE_URL` :: Base url for OpenDota API
 - `LOG_LEVEL` :: Log level to use, defaults to `debug`. Options are info, warning, critical, error, and debug
 - `TELEGRAM_BOT_TOKEN` :: Bot token obtained from @BotFather on telegram. Used for personal development with live testing
 - `POSTGRES_USER` :: User name for the dockerized postgres instance
 - `POSTGRES_PASSWORD` :: Password for the dockerized postgres instance
 - `POSTGRES_DB` :: Name of the dockerized postgres database


## Running the Database

Database is a dockerized PostgreSQL constainer. Requires docker desktop
 - Run `./scripts/docker_up.sh` from root of project directory

## Testing
Test cases uses default Python testing module `unittest` but uses `pytest` as the test runner
 - Write your unit tests
 - From the command line `pytest`
