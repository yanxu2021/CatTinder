# CatTinder
First Full Stack Project

# Continue developing
- install font
- insert GIF
- implement moving background
- set up not found page(differently)
- cat has profile pic-db install and upload option
- app icon for browser 
- update the tests and validations

# Cat Tinder! Combining React and Rails
- Full-stack application. 
- React with JavaScript frontend.
- Ruby on Rails backend.

## This Is So Fetch
- Consuming External APIs with Fetch/fetʃ/ v.n.取得
## Cat Tinder Frontend
- Cat Tinder Introduction, Routing, and Wireframes
```
1. Create React App
    $ yarn create react-app cat-tinder-frontend
    $ cd cat-tinder-frontend
2. Branch-main(initial commit to the frontend repo)备忘，一定要记得initial main branch！！！
3. Create Directories: components, pages, assets
4. Create component files: Header.js, Footer.js
5. Create pages files: Home.js, CatIndex.js, CatShow.js, CatNew.js, CatEdit.js, NotFound.js
6. Installs: Reactstrap, React router(备忘，in the right folder！！！)
    $ yarn add react-router-dom
    $ yarn add bootstrap
    $ yarn add reactstrap
    $ yarn start
7. Routes: Create routes in App.js for all components
8. Create mock cats: Create a file in the src directory, add an array of cat objects, import the cat object to App.js
9. Add UI Features: style Header component, style NotFound page, style Footer component
```
- **ADD,COMMIT,PUSH to GitHub**
```
Make sure the working folder 
    $ git init
    $ add .
    $ commit -m "Message"
    $ branch -M main
    $ git remote add origin repo_link
    $ git push origin main
```
- Cat Tinder Testing with Jest and Enzyme
```
    $ yarn add -D enzyme react-test-renderer enzyme-adapter-react-16
    $ yarn test
Control + C to stop the testing suite.
```
- Cat Tinder Read Functionality
- Cat Tinder Create Functionality
- Cat Tinder Update Functionality
## Cat Tinder Backend
- Cat Tinder API Introduction
```
    $ rails new cat_tinder_backend -d postgresql -T
    $ cd cat_tinder_backend
    $ rails db:create
    $ bundle add rspec-rails
    $ rails generate rspec:install
    $ rails server
Make sure rails app is working
```

- **ADD,COMMIT,PUSH to GitHub**
```
Make sure the working folder 
    $ git init
    $ add .
    $ commit -m "Message"
    $ branch -M main
    $ git remote add origin repo_link
    $ git push origin main
```
- Cat Tinder API Seeds
```
    $ rials g resource Cat name:string age:integer enjoys:text
    $ rails db:migrate
    $ rspec spec
```
Make sure rspec is working

 ```ruby
 cats = [...]

 cats.each do |attributes|
    Cat.create attributes
    puts "creating cat #{attributes}"
end
```
`$ rails db:seed`

Trouble shooting
```
    $ rails db:drop
    $ rails db:create
    $ rails db:migrate
    $ rails db:seed
```
- Cat Tinder API CORS(Cross-Origin Resource Sharing)
1. app/controllers/application_controller.rb
As a developer,enable the controller to accept requests from outside applications.
```ruby
    skip_before_action :verify_authenticity_token
```
2. cat_tinder_backend/Gemfile
```ruby
    gem 'rack-cors', :require => 'rack/cors'
```
3. create cors.rb file<-config/initializers/cors.rb
config/initializers/cors.rb
```ruby
Rails.application.config.middleware.insert_before 0, Rack::Cors do
  allow do
    origins '*'  # <- change this to allow requests from any domain while in development.

    resource '*',
      headers: :any,
      methods: [:get, :post, :put, :patch, :delete, :options, :head]
  end
end
```
`$ bundle install`
- Cat Tinder API Endpoints
- Cat Tinder API Validations
## Bringing it Together!
- Cat Tinder Fetch for Read Functionality
- Cat Tinder Fetch for Create Functionality
- Cat Tinder Fetch for Update Functionality
- Cat Tinder Fetch for Delete Functionality

