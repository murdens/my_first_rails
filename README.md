# README

Cars application - creates a database of cars by make, model, year
(https://protected-cliffs-69261.herokuapp.com/cars)

* Ruby version - 5.2.3

* System dependencies

* Configuration - 

* Database creation - scaffold car make:string model:string year:integer

* Database initialization - rails db:migrate

* How to run the test suite - rails server http://localhost:3000/cars 

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions - Deployed to Heroku: 
Required config of Gemfile, gem 'sqlite3'line to the following

group :development, :test do
 gem 'sqlite3'
end

group :production do
  gem 'pg'
end

bundled the changes to Ruby, Git and Heroku $bundle install --without production

*Root config

Updated config roots.rb with:
Rails.application.routes.draw do
  root 'cars#index'
  resources :cars
end

add updates to Git and push same to Heroku

migrate db to Heroku.

$heroku run rails db:migrate



