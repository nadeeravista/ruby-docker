### Step 1 - Run the following command to run
`docker-compose run --no-deps web rails new . --force --database=postgresql`

### Step 2 - Build docker
```
default: &default
  adapter: postgresql
  encoding: unicode
  host: db
  username: postgres
  password: password
  pool: 5

development:
  <<: *default
  database: myapp_development


test:
  <<: *default
  database: myapp_test
```

### Step 3 - Run docker detached
Stop docker contaiiners and run the following again if not working
```
docker-compose build
docker-compose up -d
docker-compose run web rake db:create
```
Your app spunded up in port 3000

### Step 4 - Start coding rails
[link text itself]: //HOWTO-RAILS.md
