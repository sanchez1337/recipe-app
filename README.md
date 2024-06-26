# Personal recipes app
Following udemy course "Build a Backend REST API with Python Django - Advanced"
Will be trying to firstly take the course and create an API, 
then try to create a frontend with Vue.Js and hopefully using TDD with Cypress.
Eventually what I would like of this to become would be some kind of 
personal recipes repository, where eventually you could insert a link to 
some other recipe website - this app would be able to scrape it 
and present it in uniformed form without any clutter.
Additional functionality which will try to implement as I go:
- saving ingredients used by user - possibly with pictures and price
- adding notes to the recipe

My programming knowledge is still very limited, so you are looking at
the code at your own risk, but if you happen to see it and perhaps
have any suggestions on how to improve it,
please let me know - I will very much appreciate it!
<br><br>
#TODO: Installation - will contain final deployment steps, this one has to go to 
section called Development(?)


# Installation

Copy ```.env.sample``` to ```.env``` and update the values with your secure passwords.

THen all you have to do is run:
```bash
docker compose build
```
It will grab ```python:3.11.9-alpine3.19``` image from docker hub, install 
all python packages
from ```requirements.txt*``` and additionally set up Postgres container.

After that it will use ```docker-compose.yml``` build an image 
from ```Dockerfile``` with
```DEV=true``` as an argument - for now adding flake8 to the development build.



# Usage
In main folder of the project run for start of the stack:
```bash
docker compose up -d
```
In order to see log stream enter:
```bash
docker compose logs -f
```
Go to ```localhost:8000/admin``` to open Django admin panel.\
Go to ```localhost:8000/api/docs``` to open Swagger automatic API documentation.

## Demo 
Wanted to try out some deployment strategies so for the time being
project is up and running on AWS EC2 Instance under domain
[https://recipe.sancholabs.com](https://recipe.sancholabs.com)

## Note
 Please note, I also have no idea yet how to write a proper README file,
 so it's kind of messy, sorry about that

 I am also not really experienced with proper way of working with Git 
 so my commits might look kind of messy, will try to read up on that and 
 improve as I go.
 Currently working on main branch - 
 I am aware this isn't really realistic scenario but want to start using 
 develop or feature branches when I will be sure I know what I am doing.
 \
I've made that repo public in hope this will force me write code more often.

04-04-2024: Upgraded to django 4\
04-04-2024: Upgraded to django 5