# i4Policy Digital Policy Consultation

This is the opensource code repository of the digital policy consultation tool that will serve as the backbone for policy consultations across several countries in Africa and beyond. There are two key components to the app: a) web-app b) messenger bot. 

## User Stories

### Web App: 
We are going to modify a fork of Consul (information and documentation can be found below), a civic engagement tool developed by the city council of Madrid from 2015 onward. The core user story is as follows: 

* a) As a User, I want to see how the consultation works so that I know what I’m supposed to do.

* b) As a User, I want to interact with each sentence and section of the policy document so that I can provide my feedback without any minimum required input. 

*c) As a User, I want to see my tangible contribution so that I can feel proud of my contribution, share it, and encourage others to get involved. 

*d) As a User, I want to be able to remain anonymous to the admin with my contribution. 

*e) As a User, I want to be notified when the final version of the policy is released. 

*f) As an Admin, I want to be able to see all of the inputs from the consultation.

*g) As an Admin, I want to be able to respond and interact with specific pieces of feedback and deliberation so that I can get more clarity or provide further clarity. 

*h) As an Admin, I want to be able to publish the revised, final version of the policy to the platform for users to see.

### Messenger Bot: 

This is in efforts to make the consultation as representative as possible, and cater to a larger part of the population by (a) hitting them on the mediums they are frequenting already and (b) catering to the part of the population that only has access to Free Basics. 

So if somebody doesn’t have access to go onto the web app and access the document that way they should be able to participate like so:

*a) As a User, I want to read the policy in a digestible, non-overwhelming format so that I can get a grip on each section. 

*b) As a User, I want to be able to provide my feedback on every section through the bot. 

*c) As a User, I want to be able to provide overall feedback on the policy document. 

*d) As an Admin, I want to be able to see all of the input from the bot interactions on my admin dashboard. 

We will use one of the Ruby wrappers or Rails libraries for messenger implementation to keep the stack consistent across the board. Will also be handy for the integration, because we want citizen input from the bot and citizen input from the app to essentially feed into the same db. 

We are using the following Ruby client to build the bot into the application: 

https://github.com/jgorset/facebook-messenger

# Using CONSUL

Citizen Participation and Open Government Application

[![Build Status](https://travis-ci.org/consul/consul.svg?branch=master)](https://travis-ci.org/consul/consul)
[![Code Climate](https://codeclimate.com/github/consul/consul/badges/gpa.svg)](https://codeclimate.com/github/consul/consul)
[![Coverage Status](https://coveralls.io/repos/github/consul/consul/badge.svg)](https://coveralls.io/github/consul/consul?branch=master)
[![Crowdin](https://d322cqt584bo4o.cloudfront.net/consul/localized.svg)](https://crowdin.com/project/consul)
[![License: AGPL v3](https://img.shields.io/badge/License-AGPL%20v3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)

[![Accessibility conformance](https://img.shields.io/badge/accessibility-WAI:AA-green.svg)](https://www.w3.org/WAI/eval/Overview)
[![A11y issues checked with Rocket Validator](https://rocketvalidator.com/badges/checked_with_rocket_validator.svg?url=https://rocketvalidator.com)](https://rocketvalidator.com/opensource)

[![Join the chat at https://gitter.im/consul/consul](https://badges.gitter.im/consul/consul.svg)](https://gitter.im/consul/consul?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](https://github.com/consul/consul/issues?q=is%3Aissue+is%3Aopen+label%3APRs-welcome)

This is the opensource code repository of the eParticipation website CONSUL, originally developed for the Madrid City government eParticipation website

## Current state

Development started on [2015 July 15th](https://github.com/consul/consul/commit/8db36308379accd44b5de4f680a54c41a0cc6fc6). Code was deployed to production on 2015 september 7th to [decide.madrid.es](https://decide.madrid.es). Since then new features are added often. You can take a look at the current features at the [project's website](http://consulproject.org/) and future features at the [Roadmap](https://github.com/consul/consul/projects/6) and [open issues list](https://github.com/consul/consul/issues).

## Configuration for development and test environments

**NOTE**: For more detailed instructions check the [docs](https://consul_docs.gitbooks.io/docs/)

Prerequisites: install git, Ruby 2.3.2, `bundler` gem, Node.js and PostgreSQL (>=9.4).

```bash
git clone https://github.com/consul/consul.git
cd consul
bundle install
cp config/database.yml.example config/database.yml
cp config/secrets.yml.example config/secrets.yml
bin/rake db:create
bin/rake db:migrate
bin/rake db:dev_seed
RAILS_ENV=test rake db:setup
```

Run the app locally:

```bash
bin/rails s
```

Prerequisites for testing: install ChromeDriver >= 2.33

Run the tests with:

```bash
bin/rspec
```

You can use the default admin user from the seeds file:

 **user:** admin@consul.dev
 **pass:** 12345678

But for some actions like voting, you will need a verified user, the seeds file also includes one:

 **user:** verified@consul.dev
 **pass:** 12345678

## Configuration for production environments

See [installer](https://github.com/consul/installer)

## Documentation

Check the ongoing documentation at [https://consul_docs.gitbooks.io/docs/content/](https://consul_docs.gitbooks.io/docs/content/) to learn more about how to start your own CONSUL fork, install it, customize it and learn to use it from an administrator/maintainer perspective. You can contribute to it at [https://github.com/consul/docs](https://github.com/consul/docs)

## License

Code published under AFFERO GPL v3 (see [LICENSE-AGPLv3.txt](LICENSE-AGPLv3.txt))

## Contributions

See [CONTRIBUTING.md](CONTRIBUTING.md)
