# GatorAnswer

Teacher/Student interaction software.

## Building

### FIRST RUN

First install docker-compose. Then use:

```bash
docker-compose up --build
```

You can tell this command is done when you see `db_1  |`


Then create the database in another terminal using:

```bash
docker-compose run web rails db:create
```

Then migrate all the tables to the db:

```bash
docker-compose run web rails db:migrate
```

The program should then be up on localhost:3000

### Changes to Gemfile

If you make any changes to the Gemfile you will need to run:

```bash
docker-compose down
docker-compose up --build
```

If you would like to migrate the database you can use

```bash
docker-compose run web rails db:migrate
```
