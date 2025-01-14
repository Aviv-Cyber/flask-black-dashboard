# [Black Dashboard Flask](https://appseed.us/product/black-dashboard/flask/)

Open-source **Flask Dashboard** generated by `AppSeed` op top of a modern `Bootstrap` design. Designed for those who like bold elements and beautiful websites, **[Black Dashboard](https://appseed.us/product/black-dashboard/flask/)** is ready to help you create stunning websites and webapps. **Black Dashboard** is built with over 50 frontend individual elements, like buttons, inputs, navbars, nav tabs, cards, or alerts, giving you the freedom of choosing and combining.

- 👉 [Black Dashboard Flask](https://appseed.us/product/black-dashboard/flask/) - `product page`
- 👉 [Black Dashboard Flask](https://flask-black-dashboard.appseed-srv1.com/) - `LIVE Demo`
- 👉 [Complete documentation](https://docs.appseed.us/products/flask-dashboards/black-dashboard) - `Learn how to use and update the product`
- ✅ Deployment: [Render](#deploy-on-render)
  - 👉 See [VIDEO Presentation](https://www.youtube.com/watch?v=UjYis-lPLNg)
  
<br />

> 🚀 Built with [App Generator](https://appseed.us/generator/), timestamp: `2022-05-25 09:44`

- ✅ `Up-to-date dependencies`
- ✅ [Black Dashboard](https://www.creative-tim.com/product/black-dashboard?AFFILIATE=128200), Persistent `Dark-Mode`
- ✅ `DB Tools`: SQLAlchemy ORM, `Flask-Migrate` (schema migrations)
- ✅ `Persistence`: SQLite (dev), MySql (prod)
- ✅`Authentication`: Session Based, `OAuth` via Github
- ✅ `Deployment`: Docker, Page Compression (Flask-Minify) 

<br />

![Black Dashboard - Seed project provided by AppSeed.](https://user-images.githubusercontent.com/51070104/189294897-7b847e63-8d6e-48a5-942c-809155825d08.gif)

<br /> 

## ✨ Start the app in Docker

> 👉 **Step 1** - Download the code from the GH repository (using `GIT`) 

```bash
$ git clone https://github.com/app-generator/flask-black-dashboard.git
$ cd flask-black-dashboard
```

<br />

> 👉 **Step 2** - Start the APP in `Docker`

```bash
$ docker-compose up --build 
```

Visit `http://localhost:5085` in your browser. The app should be up & running.

<br />

## ✨ Create/Edit `.env` file

The meaning of each variable can be found below: 

- `DEBUG`: if `True` the app runs in develoment mode
  - For production value `False` should be used
- `ASSETS_ROOT`: used in assets management
  - default value: `/static/assets`
- `OAuth` via Github
  - `GITHUB_ID`=<GITHUB_ID_HERE>
  - `GITHUB_SECRET`=<GITHUB_SECRET_HERE> 

<br />

## ✨ Manual Build

> Download the code 

```bash
$ git clone https://github.com/app-generator/flask-black-dashboard.git
$ cd flask-black-dashboard
```

<br />

### 👉 Set Up for `Unix`, `MacOS` 

> Install modules via `VENV`  

```bash
$ virtualenv env
$ source env/bin/activate
$ pip3 install -r requirements.txt
```

<br />

> Set Up Flask Environment

```bash
$ export FLASK_APP=run.py
$ export FLASK_ENV=development
```

<br />

> Start the app

```bash
$ flask run
// OR
$ flask run --cert=adhoc # For HTTPS server
```

At this point, the app runs at `http://127.0.0.1:5000/`. 

<br />

### 👉 Set Up for `Windows` 

> Install modules via `VENV` (windows) 

```
$ virtualenv env
$ .\env\Scripts\activate
$ pip3 install -r requirements.txt
```

<br />

> Set Up Flask Environment

```bash
$ # CMD 
$ set FLASK_APP=run.py
$ set FLASK_ENV=development
$
$ # Powershell
$ $env:FLASK_APP = ".\run.py"
$ $env:FLASK_ENV = "development"
```

<br />

> Start the app

```bash
$ flask run
// OR
$ flask run --cert=adhoc # For HTTPS server
```

At this point, the app runs at `http://127.0.0.1:5000/`. 

<br />

## Deploy on Render

The product can be easily deployed on Render using [Python Deployer](https://github.com/app-generator/deploy-automation-render) (`open-source` tool).

<br />

> 👉 **Step 1**: Set UP a [Render](https://render.com/) account 

- Create account
- Create an [API_KEY](https://render.com/docs/api)
- Attach a `credit card` to the account
  - **Note**: Each Python service deployed on Render requires a monthly payment

<br />

> 👉 **Step 2**: Download [Python Deployer](https://github.com/app-generator/deploy-automation-render)

```bash
$ git clone https://github.com/app-generator/deploy-automation-render.git   
$ cd deploy-automation-render
$ pip install -r requirements.txt
```

<br />

> 👉 **Step 3**: Set up the `ENV` as suggested in the [deployer](https://github.com/app-generator/deploy-automation-render) help

```bash
$ export RENDER_API_KEY=<RENDER_API_KEY>   # mandatory
$ export RENDER_OWNER_ID=<RENDER_OWNER_ID> # needs to have a CC attached, used for Billing
```

<br />

> 👉 **Step 4**: Deploy the repo

```bash
$ python.exe deployer.py flask https://github.com/app-generator/flask-star-admin "run:app"
```

The new service should be visible on your Render Dashboard and soon be LIVE. 

<br /> 

https://user-images.githubusercontent.com/51070104/200280789-e56eddac-324e-4f09-bf90-190ef9aebe26.mp4

<br />

### 👉 Create Users

By default, the app redirects guest users to authenticate. In order to access the private pages, follow this set up: 

- Start the app via `flask run`
- Access the `registration` page and create a new user:
  - `http://127.0.0.1:5000/register`
- Access the `sign in` page and authenticate
  - `http://127.0.0.1:5000/login`

<br />

## Recompile CSS

To recompile SCSS files, follow this setup:

<br />

> 👉 **Step #1** - Install tools

- [NodeJS](https://nodejs.org/en/) 12.x or higher
- [Gulp](https://gulpjs.com/) - globally 
    - `npm install -g gulp-cli`
- [Yarn](https://yarnpkg.com/) (optional) 

<br />

> 👉  **Step #2** - Change the working directory to `assets` folder

```bash
$ cd apps/static/assets
```

<br />

> 👉  **Step #3** - Install modules (this will create a classic `node_modules` directory)

```bash
$ npm install
// OR
$ yarn
```

<br />

> 👉  **Step #4** - Edit & Recompile SCSS files 

```bash
$ gulp
```

The generated file is saved in `static/assets/css` directory.

<br />

## ✨ Code-base structure

The project is coded using blueprints, app factory pattern, dual configuration profile (development and production) and an intuitive structure presented bellow:

```bash
< PROJECT ROOT >
   |
   |-- apps/
   |    |
   |    |-- home/                           # A simple app that serve HTML files
   |    |    |-- routes.py                  # Define app routes
   |    |
   |    |-- authentication/                 # Handles auth routes (login and register)
   |    |    |-- routes.py                  # Define authentication routes  
   |    |    |-- models.py                  # Defines models  
   |    |    |-- forms.py                   # Define auth forms (login and register) 
   |    |
   |    |-- static/
   |    |    |-- <css, JS, images>          # CSS files, Javascripts files
   |    |
   |    |-- templates/                      # Templates used to render pages
   |    |    |-- includes/                  # HTML chunks and components
   |    |    |    |-- navigation.html       # Top menu component
   |    |    |    |-- sidebar.html          # Sidebar component
   |    |    |    |-- footer.html           # App Footer
   |    |    |    |-- scripts.html          # Scripts common to all pages
   |    |    |
   |    |    |-- layouts/                   # Master pages
   |    |    |    |-- base-fullscreen.html  # Used by Authentication pages
   |    |    |    |-- base.html             # Used by common pages
   |    |    |
   |    |    |-- accounts/                  # Authentication pages
   |    |    |    |-- login.html            # Login page
   |    |    |    |-- register.html         # Register page
   |    |    |
   |    |    |-- home/                      # UI Kit Pages
   |    |         |-- index.html            # Index page
   |    |         |-- 404-page.html         # 404 page
   |    |         |-- *.html                # All other pages
   |    |    
   |  config.py                             # Set up the app
   |    __init__.py                         # Initialize the app
   |
   |-- requirements.txt                     # App Dependencies
   |
   |-- .env                                 # Inject Configuration via Environment
   |-- run.py                               # Start the app - WSGI gateway
   |
   |-- ************************************************************************
```

<br />

## PRO Version

> For more components, pages and priority on support, feel free to take a look at this amazing starter:

Black Dashboard is a premium Bootstrap Design now available for download in Django. Made of hundred of elements, designed blocks, and fully coded pages, Black Dashboard PRO is ready to help you create stunning websites and web apps.

- 👉 [Black Dashboard PRO Flask](https://appseed.us/product/black-dashboard-pro/flask/) - product page
  - ✅ `Enhanced UI` - more pages and components
  - ✅ `Priority` on support

<br >

![Black Dashboard PRO - Full-Stack Starter generated by AppSeed.](https://user-images.githubusercontent.com/51070104/169471630-e96cec9b-ef57-4c06-9b36-62b9bbf255f3.png)

<br />

---
[Black Dashboard Flask](https://appseed.us/product/black-dashboard/flask/) - Open-source starter generated by **[App Generator](https://appseed.us/generator/)**.
