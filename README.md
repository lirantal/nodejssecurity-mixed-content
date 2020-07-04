# Mixed Content

The following exercise shows a practical example of browsers issuing a mixed content warning.

### Requirements

We will be using [Heroku](https://www.heroku.com/) as our hosting platform for an Express Node.js application, as we will need both an HTTPS enabled hosting, as well as an HTTP hosting to switch on and off the HTTP Strict Transport Security header.

## Source code

Obtain the source code from the official GitHub repository at: https://github.com/lirantal/nodejssecurity-mixed-content

Once you cloned the repository, the overall projects file structure that you should be aware of is:

1. An express server in `server.js`
2. A handlebars template in `views/home.handlebars` which serves an example website
3. A `public` directory which has an image that we will use

## Deployment

You'll need an Heroku account to deploy the Express web app there.

1. Sign-up for a free Heroku account, and have the `heroku` CLI installed.
2. `npm install` all the dependencies in the project.
3. Create a Heroku Node.js project
4. Login from the CLI using: `heroku login` 5. Using the `heroku` CLI create a new project, such as: `heroku git:remote -a mixed-content` to instantiate a git remote for the project, assuming `mixed-content` is the name of the heroku project name you used in step (3).
6. Deploy the app using `git push heroku master`

At this point, it should be available as both HTTPS and HTTP endpoints, such as:
* https://mixed-content.herokuapp.com/
* http://mixed-content.herokuapp.com/
