# Salon Appointment Scheduler

A Bash script connected to a PostgreSQL database that lets customers book salon appointments from the terminal.

Built as part of the freeCodeCamp Relational Databases certification.

## What it does

- Shows a numbered list of available services
- Asks for the customer's phone number
- Registers new customers (asks for their name) or recognizes returning ones
- Asks for the appointment time and saves the appointment
- Confirms the booking, e.g. `I have put you down for a cut at 10:30, Fabio.`

## Tech used

- Bash
- PostgreSQL
- Git and GitHub

## Database

The `salon` database has three tables:

| Table | Purpose |
|---|---|
| `customers` | Stores customer name and unique phone number |
| `services` | Stores the services the salon offers |
| `appointments` | Links a customer to a service at a given time |

## How to run

1. Restore the database:
   ```bash
   psql -U postgres < salon.sql
   ```
2. Make the script executable:
   ```bash
   chmod +x salon.sh
   ```
3. Run it:
   ```bash
   ./salon.sh
   ```

## Files

- `salon.sh`: the booking script
- `salon.sql`: database dump (tables and services)
