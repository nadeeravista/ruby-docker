Careate a active record/database table called Bank with one string column called name. 
Migrate database. 
Connecting to rails console
Add some data. 
```
docker-compose run web rails g scaffold Band name:string
docker-compose run web rails db:migrate
docker-compose run web rails c
irb(main):005:0> Band.create(name: "The Beatles")
````
