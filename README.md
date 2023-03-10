[![Build Status][travis-image]][travis-url]

![](https://github.com/nickitaliano/mcl-mh-brand-sentiment-analysis-app/blob/master/banner.gif)

<br/>

# MooTweet: Mh-Mcl-Brand-Sentiment-App 🐮

MooTweet is a data product that was built for the Music Hackathon/Music Community Lab, a not-for-profit music organization. The real-time dashboard provides decision support—using Python, NLP methods and Flask framework—to quantify individual and brand engagement on Twitter. 

Originally a modest Search API project, the streaming analytics app now performs sentiment analyses and measures engagement metrics that satisfy the original client goal: use the Twitter Search API to identify the organization’s most brand worthy account. 


<br/>

# How to use Heroku CLI
## Download and Installation(Unix/Linux)

> If you haven't already, log in to your Heroku account and follow the prompts to create a new SSH public key.
```'bash 
$ heroku login
```

> Create a new Git repository and initialize a git repository in a new or existing directory
```bash
$ cd mootweet/
$ git init
$ heroku git:remote -a mootweet
```


<br/>

## Want to deploy your application?

> Commit your code to the repository and deploy it to Heroku using Git.
```bash
$ git add .
$ git commit -am "make it better"
$ git push heroku master
```


<br/>

### Existing Git repository

> For existing repositories, simply add the heroku remote!
```bash
$ heroku git:remote -a mootweet
```

> Get the code
```bash
$ git clone https://github.com/nickitaliano/mcl-mh-brand-sentiment-analysis-app.git
$ cd mcl-mh-brand-sentiment-analysis-app/
```


<br/>

<br/>

### Development Setup
> Virtualenv modules installation (Unix based systems)
```bash
$ virtualenv --no-site-packages env
$ source env/bin/activate
```
<br/>

<br/>

> Install modules - SQLite Database
```bash
$ pip3 install -r requirements.txt
```

> OR with PostgreSQL connector
```bash
$ pip install -r requirements-pgsql.txt
```

<br/>

<br/>

> Set the FLASK_APP environment variable(development only)
```bash
$ (Unix/Mac) export FLASK_APP=run.py
```

> Set up the DEBUG environment
```bash
$ (Unix/Mac) export FLASK_ENV=development
```


<br/>

> Start the application (development mode)
```bash
$ --host=0.0.0.0 - expose the app on all network interfaces (default 127.0.0.1)
$ --port=5000    - specify the app port (default 5000)  
$ flask run --host=0.0.0.0 --port=5000
```
> Access the dashboard in browser: `http://127.0.0.1:5000/`


<br/>

# Creating the app in Heroku

The 2 module app-- sharing a single Postgres database-- is provided with a basic configuration to be executed in [Gunicorn](https://gunicorn.org/).


## Heroku

The application can be easily executed in [Heroku](https:/heroku.com) remote git branch/master. The steps:

> Get the code
```bash
$ git clone https://github.com/nickitaliano/mcl-mh-brand-sentiment-analysis-app
$ cd mcl-mh-brand-sentiment-analysis-app
```

> Visit `http://localhost:5005` in your browser. The app should be up & running.


<br/>


## Deployment 

Gunicorn 'Green Unicorn' is a Python WSGI HTTP Server for UNIX.

> Install using pip

```bash
$ pip install gunicorn
```

> Start the app using gunicorn binary

```bash
$ gunicorn --bind 0.0.0.0:8001 run:app
# Serving on http://localhost:8001
```

> Visit `http://localhost:8001` in your browser. The app should be up & running.


<br/>


<br/>

## Credits & Links
### What is Flask?
---
[Flask](https://www.palletsprojects.com/p/flask/) is a lightweight WSGI web application framework with the ability to scale up to complex applications. The framework began as a simple wrapper around Werkzeug and Jinja and has become one of the most popular Python web application frameworks.


### What is a dashboard?
---
A dashboard app is a set of easy-to-read pages that offer information to the user in real-time regarding their business. The app itself usually consists of graphical representations of the current status and trends within an organization.
```
"Having a well-designed dashboard will allow you to act and make informed decisions based on the data that your business provides." 
```
> - *definition provided by [Creative-Tim - Free Dashboard Templates](https://www.creative-tim.com/blog/web-design/free-dashboard-templates/?ref=appseed)*.


### Ackknowledgements
---
**[Chulong-Li](https://github.com/Chulong-Li/Real-time-Sentiment-Tracking-on-Twitter-for-Brand-Improvement-and-Trend-Recognition)**, a Ohio State Data Scientist, created a fantastic real-time interactive dashboard app. The app analyzes Twitter data, running automated sentiment analyses for branding decision support.

He developed the product using Python development frameworks(Deployed on Heroku). In addition, he drafted a complimentary project article **[featured on Medium](https://medium.com/@ChulongLi)** to get us started.🙌


### Meta
---
Nick Italiano – [@nickitalian0](https://twitter.com/nickitalian0) – nickitaliano.io@gmail.com

Distributed under the MIT license. See ``LICENSE`` for more information.

[https://github.com/yourname/github-link](https://github.com/nickitaliano/)


### Contributing
---
I'm grateful for all the help on this open-source. Please make a PR with the source so I can confirm corrections. Also, feel free to open an issue if you have any suggestions. Thanks!

1. Fork it (<https://github.com/yourname/yourproject/fork>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request


<!-- Markdown link & img dfn's -->
[![Build Status][travis-image]][travis-url]
<!-- 
[![NPM Version][npm-image]][npm-url]
[![Downloads Stats][npm-downloads]][npm-url]


## Usage example

A few motivating and useful examples of how your product can be used. Spice this up with code blocks and potentially more screenshots.

_For more examples and usage, please refer to the [Wiki][wiki]._

## Development setup

Describe how to install all development dependencies and how to run an automated test-suite of some kind. Potentially do this for multiple platforms.

```sh
make install
npm test
```


## Release History

* 0.2.1
    * CHANGE: Update docs (module code remains unchanged)
* 0.2.0
    * CHANGE: Remove `setDefaultXYZ()`
    * ADD: Add `init()`
* 0.1.1
    * FIX: Crash when calling `baz()` (Thanks @GenerousContributorName!)
* 0.1.0
    * The first proper release
    * CHANGE: Rename `foo()` to `bar()`
* 0.0.1
    * Work in progress


[npm-image]: https://img.shields.io/npm/v/datadog-metrics.svg?style=flat-square
[npm-url]: https://npmjs.org/package/datadog-metrics
[npm-downloads]: https://img.shields.io/npm/dm/datadog-metrics.svg?style=flat-square
[travis-image]: https://img.shields.io/travis/dbader/node-datadog-metrics/master.svg?style=flat-square
[travis-url]: https://travis-ci.org/dbader/node-datadog-metrics
[wiki]: https://github.com/yourname/yourproject/wiki
-->
