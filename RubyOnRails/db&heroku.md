# DATA base commands and Heroku

## Data Base basic commands for postgresql

**Create a DB**
```ruby
rails db:create
```

**Create a migration**
```ruby
rails g migration User name:string email:string
```

**Upload the migration**
```ruby
rails db:migrate
```
 
**Check migration status**
```ruby
rails db:migrate:status
```
**Reset the db**
```ruby
rails db:drop
```
<p><b>Warning </b>-> you need do re do a db:create to generate a new empty DB.</p>
---------------------------------

# HEROKU

**Heroku Reset database**
```shell
heroku pg:reset DATABASE_URL
```

**Recreate DB initialized**
```shell
heroku run rake db:migrate  
```

**Seed the DB on Heroku**
```shell
heroku run rake db:seed
````




