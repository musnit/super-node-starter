## Super Node Starter

[![Circle CI](https://circleci.com/gh/Stephn-R/super-node-starter.svg?style=svg&circle-token=15cb369d08b433d47648e998cf8eac8e369ca858)](https://circleci.com/gh/Stephn-R/super-node-starter) [![Code Climate](https://codeclimate.com/repos/567779db7df1497f6c004c1d/badges/e873373aad89c2eca43e/gpa.svg)](https://codeclimate.com/repos/567779db7df1497f6c004c1d/feed) [![dependencies](https://david-dm.org/stephn-r/super-node-starter.svg)](https://david-dm.org/stephn-r/super-node-starter) [![devDependencies](https://david-dm.org/stephn-r/super-node-starter/dev-status.svg)](https://david-dm.org/stephn-r/super-node-starter#info=devDependencies)

### Server Frameworks

- Typescript
- Sequelize

### Details

A complete NodeJS server starter template. This template is designed to give any NodeJS project an extreme running start that includes some of the most common features vital to the Client/Server relationship model while providing various other tools, and resources for quickly building out any part of the server development stack.

Please refer to the [CONTRIBUTING.md](https://github.com/stephn-r/super-node-starter/blob/master/CONTRIBUTING.md) doc for any questions, concerns, or suggestions

#### Running For Development

1. Install modules

```sh
npm install
npm install -g sequelize-cli
npm install -g typescript
npm install -g typings
npm install -g gulp-cli
```

2. Install typescript dependencies

```sh
typings install
```

3. Provide a `.env` file (copy the template) and provider you own values

```sh
cp .env.example .env
```

Create a local SQL database in MySQL/Postgres/etc and fill out the env values to connect there.

4. Run the database migrations
```sh
sequelize db:migrate
```

5. Build the app, compiling typescript files

```sh
tsc
```

Note: You may want to install an editor plugin to automatically do this for you on file save, like atom-typescript

6. Run the app!

```sh
npm start
```

7. Linting your code while developing

Linting is dealt with by eslint, jshint and tslint. There are config files for those in the repo. You should install editor plugins to do this easily and automatically for you as you code and save files, eg, for atom:

```sh
apm install eslint
apm install linter
apm install linter-jshint
apm install linter-eslint
apm install linter-tslint
```

#### Deploying your code to heroku ####
to do...

#### Local Docker Deployment (Still WIP!)

1. Build the Docker Image

```sh
docker build -t super-node-starter .
```

2. Provide a `.env` file (copy the template) and provider you own values

```sh
cp .env.example .env
```

3. Run the app

```sh
docker run -d -P --name web super-node-starter
```

Below is a list of all the supported features. Refer to the [Wiki](https://github.com/stephn-r/super-node-starter/wiki) for more information on how to use them along with configuration options:

#### Middleware Tools
1. Application Logging using Winston
2. CORS Security Headers
3. PassportJS for Session Management
4. Reading Cookies in the Request
5. HTTP Method Overriding for customer headers
6. Body Parsing to provide all content as JSON in `req` object

#### Server Side Tools
1. Response Handler with HTTP Status Codes
2. Basic Folder Structure
3. Sequelize for SQL query building + connecting to relational DBs

#### Code Quality Tools
1. CodeClimate yaml file
2. CircleCI yaml file
3. ESLint Config File to manage code consistency
4. Editor Config File to enforce code indentation
5. Git dotfiles to better manage git history

#### Additional
1. Basic CRON Job template
2. Gulp for task management + additional tasks for:
	a. Detecting vulnerable modules in `package.json`
	b. Compiling Web Assets using Webpack
