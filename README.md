# SpotMusic - Integrations

## About

This repo contains the application that exports and shares data in social networks, such as: Instagram, Facebook, Twitter, WhatsApp. 
It is responsible to be the _anti-corruption layer_ between SpotMusic and the external world. 
It produces events every time that a external account is connected with us, and when someone shares a post in any social network.

## Project Structure

- internal
  - **apis**: Is where the external APIs lives to connect with the social-networks
  - **domain**: Where we keep our domain modules like the entities, values, consts, interfaces, etc. Everything strict related to SpotMusic only.
  - **infra**: The infrastructure modules to use third-party tooling as Kafka, MySQL, Redis, so on.
  - **producers**: It produces events to _kafka_ based on event triggers. 
  - **services**: Where we keep the business logic to do some action. 

## Running It

This project uses **docker** and **docker-compose**, so to execute it, you must have them previously installed. 

```bash
docker build -t spotmusic/integrations . 
```

```bash
docker run spotmusic/integrations
```


