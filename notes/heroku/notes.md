# Heroku Overview

When we published our personal website project, we used the GitHub Pages platform to host our site. GitHub Pages can host static websites, but it is not currently able to host dynamic web applications which rely on server-side software. To host our web application, we will use a different hosting provider called [Heroku](https://www.heroku.com/).

> Heroku is a cloud platform that lets companies build, deliver, monitor and scale apps — we're the fastest way to go from idea to URL, bypassing all those infrastructure headaches. - [Heroku website](https://www.heroku.com/what)

Heroku provides us with the ability to configure and manage remote servers. We will configure one or more of these servers to host our web application's source code and serve HTTP responses upon request. Each Heroku server has a unique URL address that you can visit to interact with your application. Heroku also provides you the ability to remote login to your server to run commands, check server logs, etc.

We can use Heroku to serve applications written in many of today's popular programming languages, including Node.js, Python, Ruby, and more. This means learning how to manage Heroku servers will be beneficial to you regardless of which programming language you are using in the future. Heroku can host all kinds of apps.

For more information about how Heroku works, see: https://devcenter.heroku.com/articles/how-heroku-works.

## Prerequisites

  + Login to an existing Heroku account, or [register](https://signup.heroku.com/) for a new one. Make sure to confirm your account by clicking a confirmation link the confirmation email sent to you by Heroku.

> Security Alert: consider eventually enabling multi-factor authentication on your Heroku account to keep your account and your servers safe from intrusion. Don't worry about doing this now if you don't feel like it, but take a moment to do so when you have time.

## Installation

In addition to using Heroku's online platform, we will use the [Heroku Toolbelt](https://devcenter.heroku.com/articles/heroku-cli) command-line utility to interface with Heroku's resources and capabilities.

Source Code: https://github.com/heroku/cli.

Installation Guide:  https://devcenter.heroku.com/articles/heroku-cli#download-and-install.

```` sh
which heroku
#> /usr/local/bin/heroku (Mac example)
````

## Authentication

After installing Heroku Toolbelt, authenticate using your Heroku account credentials:

```` sh
heroku login
````

Authentication Guide: https://devcenter.heroku.com/articles/heroku-cli#getting-started.

## Usage

Heroku CLI Guides and Documentation: https://devcenter.heroku.com/categories/command-line.

Heroku Node.js Application Tutorial: https://devcenter.heroku.com/articles/getting-started-with-nodejs.

List applications:

```` sh
heroku apps
````

Create a Heroku application server (ideally from within the root directory of an existing project):

```` sh
heroku create # or optionally specify a name, like: heroku create my-app-name
````

Deploy the application's source code to the application server:

```` sh
git push origin master # best practice: commit and push your code to a remote repository before deploying
git push heroku master
````

Visit the application in a browser and note its URL for future reference:

```` sh
heroku open
````

Check your logs:

```` sh
heroku logs
````
