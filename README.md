[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

## Welcome



<hr>


**What is Flask?** Flask is a microframework for Python based on Werkzeug and Jinja2.

Project Structure
--------

  ```sh
  ├── Procfile
  ├── Procfile.dev
  ├── README.md
  ├── app.py
  ├── config.py
  ├── error.log
  ├── forms.py
  ├── models.py
  ├── requirements.txt
  ├── static
  │   ├── css
  │   │   ├── bootstrap-3.0.0.min.css
  │   │   ├── bootstrap-theme-3.0.0.css
  │   │   ├── bootstrap-theme-3.0.0.min.css
  │   │   ├── font-awesome-3.2.1.min.css
  │   │   ├── layout.forms.css
  │   │   ├── layout.main.css
  │   │   ├── main.css
  │   │   ├── main.quickfix.css
  │   │   └── main.responsive.css
  │   ├── font
  │   │   ├── FontAwesome.otf
  │   │   ├── fontawesome-webfont.eot
  │   │   ├── fontawesome-webfont.svg
  │   │   ├── fontawesome-webfont.ttf
  │   │   └── fontawesome-webfont.woff
  │   ├── ico
  │   │   ├── apple-touch-icon-114-precomposed.png
  │   │   ├── apple-touch-icon-144-precomposed.png
  │   │   ├── apple-touch-icon-57-precomposed.png
  │   │   ├── apple-touch-icon-72-precomposed.png
  │   │   └── favicon.png
  │   ├── img
  │   └── js
  │       ├── libs
  │       │   ├── bootstrap-3.0.0.min.js
  │       │   ├── jquery-1.10.2.min.js
  │       │   ├── modernizr-2.6.2.min.js
  │       │   └── respond-1.3.0.min.js
  │       ├── plugins.js
  │       └── script.js
  └── templates
      ├── errors
      │   ├── 404.html
      │   └── 500.html
      ├── forms
      │   ├── forgot.html
      │   ├── login.html
      │   └── register.html
      ├── layouts
      │   ├── form.html
      │   └── main.html
      └── pages
          ├── placeholder.about.html
          └── placeholder.home.html
  ```

### Screenshots

![Pages](https://github.com/realpython/flask-boilerplate/blob/master/screenshots/pages.png)

![Forms](https://github.com/realpython/flask-boilerplate/blob/master/screenshots/forms.png)


### Quick Start

1. Clone the repo
  ```
  $ git clone https://github.com/Prajakta-collab/FlaskWebsite.git
  $ cd flask-boilerplate
  ```

2. Initialize and activate a virtualenv:
  ```
  $ virtualenv --no-site-packages env
  $ source env/bin/activate
  ```

3. Install the dependencies:
  ```
  $ pip install -r requirements.txt
  ```

5. Run the development server:
  ```
  $ python app.py
  ```

6. Navigate to [http://localhost:5000](http://localhost:5000)


Deploying to Heroku
------

1. Signup for [Heroku](https://api.heroku.com/signup)
2. Login to Heroku and download the [Heroku Toolbelt](https://toolbelt.heroku.com/)
3. Once installed, open your command-line and run the following command - `heroku login`. Then follow the prompts:

  ```
  Enter your Heroku credentials.
  Email: michael@mherman.org
  Password (typing will be hidden):
  Could not find an existing public key.
  Would you like to generate one? [Yn]
  Generating new SSH public key.
  Uploading ssh public key /Users/michaelherman/.ssh/id_rsa.pub
  ```

4. Activate your virtualenv
5. Heroku recognizes the dependencies needed through a *requirements.txt* file. Create one using the following command: `pip freeze > requirements.txt`. Now, this will only create the dependencies from the libraries you installed using pip. If you used easy_install, you will need to add them directly to the file.
6. Create a Procfile. Open up a text editor and save the following text in it:

  ```
  web: gunicorn app:app --log-file=-
  ```

   Then save the file in your applications root or main directory as *Procfile* (no extension). The word "web" indicates to Heroku that the application will be attached to the HTTP routing stack once deployed.

7. Create a local Git repository (if necessary):

  ```
  $ git init
  $ git add .
  $ git commit -m "initial files"
  ```

8. Create your app on Heroku:

  ```
  $ heroku create <name_it_if_you_want>
  ```

9. Deploy your code to Heroku:

  ```
  $ git push heroku master
  ```

10. View the app in your browser:

  ```
  $ heroku open
  ```



12. Having problems? Look at the Heroku error log:

  ```
  $ heroku logs
  ```



