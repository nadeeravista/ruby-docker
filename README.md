### Step 1 - Run the following command to run
`docker-compose run --no-deps web rails new . --force --database=postgresql`

### Step 2 - Build docker
`docker-compose build`

### Step 3 - Run docker detached
`docker-compose up -d`
Your app spunded up in port 3000

### Step 4 - Replace the contents of config/database.yml with the following:
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

### Step 5 - Stop docker and run the following again if not working
`docker-compose up -d`
