### Step 1 - Run the following command to run
`docker-compose run --no-deps web rails new . --force --database=postgresql`

### Step 2 - Build docker
`docker-compose build`

### Step 3 - Run docker detached
`docker-compose up -d`
Your app spunded up in port 3000
