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

**Generate a model/migration/controller**
```ruby
rails g model/migration/controller Name
rails generate model/migration/controller Name
```

**Delete a model/migration/controller generated**
```ruby
rails d model/migration/controller Name
rails destroy model/migration/controller Name
```
---------------------------------

# HEROKU

**Heroku Reset database**
```ruby
heroku pg:reset DATABASE_URL
```

**Recreate DB initialized**
```ruby
heroku run rake db:migrate  
```

**Seed the DB on Heroku**
```ruby
heroku run rake db:seed
````

**See Config Heroku**
```ruby
heroku config
```

**Config something on Heroku**
```ruby
heroku config:set SENDGRID_USERNAME=myusername
```

**Get config of something on Heroku**
```ruby
heroku config:get SENDGRID_USERNAME
=> myusername
```
