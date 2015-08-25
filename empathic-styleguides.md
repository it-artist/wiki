### Empathic styleguides
These styleguides are meant to be empathic to the next person who maintains the project

## Application

# Code

- double quotes always!

# Controllers
- code that connects to other parts of app and is longer than (something like) 3 lines should go to a class or module under app/services/:service_name.rb or app/models/:model_name/:service_name.rb
- code that performs some AR queries or searches OR generates more variables with similar context living with one template (eg. @users_without_posts, @authors, @posts living in posts.html.erb) and is longer than 3 lines should go to a class or module in app/models/:model_name/:context_name.rb
- dont use respond_to block if there is only one format to be requested. better use render json: ... directly

# Models
- 

# Testing
- if its a biz logic with many scenarios or you need to cover a bug or you need to decide about design => unit test
- if its a controller test (a simple user action) or you need to cover a feature (more user actions in an expected order) => integration test
- if its an API test => controller unit test

## Development process

- branch naming (if your name is Anthony Bardot): AB-task-name
- commit messages: angular commit message format
- PR process:
  - no commiting to master!
  - mention @papricek in comment if added some commits after publishing PR
  - image if visual task
  - video if flow

# Javascript
- use data-behavior value for init a js that controls a block
- if js class is called CommentForm, than all additional information should be stored within data-comment-form attributes
