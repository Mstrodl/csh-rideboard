# RideBoard

RideBoard is CSH service that allows the members to carpool, allowing those that do not have a car to participate in events.

[![Build Status](https://travis-ci.org/ag-ayush/rideboard.svg?branch=master)](https://travis-ci.org/ag-ayush/rideboard)
[![License](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/ag-ayush/rideboard/blob/master/LICENSE)
[![Contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](https://github.com/ag-ayush/rideboard/issues)

## Contributing
All contributors are welcome! If you would like to contribute:

### Dependencies
1. You will need `python3` ([Install Guide](https://docs.python-guide.org/starting/installation/#installation-guides)).
2. You will need `pip` ([Install Guide](https://packaging.python.org/tutorials/installing-packages/#ensure-you-can-run-pip-from-the-command-line)).
3. And lastly you will need to install `virtualenv` by running `pip install virtualenv`.

### Setup
1. Fork this repo and clone it locally
2. `cd rides/`
2. Create a python virtual environment, activate it and install requirements.
  - `virtualenv rides-env`
  - `source rides-env/bin/activate`
  - `pip install -r requirements.txt`
5. You will need everything in < ... >. You can create your own if you are hosting your own application or ask me for these if you would like to contribute to CSH. Please put this in `config.sh`
```
export SERVER_NAME=127.0.0.1:8080
export IP=localhost
export PORT=8080
export SQLALCHEMY_DATABASE_URI=postgresql://<LDAP DN>:<LDAP PW>@<MySQL Database>
export OIDC_CLIENT_SECRET=<OIDC Secret>
export GOOGLE_CLIENT_ID=<Google Client ID>
export GOOGLE_CLIENT_SECRET=<Google Client Secret>
```
6. Create and run with docker: `docker build --pull --rm -f "Dockerfile" -t rideboard:ubuntu "."` followed by `docker run -d -p 8080:8080 rideboard:ubuntu`
7. Run the startup.sh script to run locally.
8. Now you can make your changes. Make sure the changes made work and that your code passes pylint (run `pylint rides/`). Once you do that you can make your pullrequest.
