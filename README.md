## CloudFoundry PHP Example Application:  PHPMyAdmin

This is an example application which can be run on CloudFoundry using the [PHP Build Pack].

This is an out-of-the-box implementation of PHPMyAdmin 4.2.2.  It's an example how common PHP applications can easily be run on CloudFoundry.

### Usage

1. Clone the app (i.e. this repo).

  ```bash
  git clone https://github.com/gfoligna/cf-ex-phpmyadmin
  cd cf-ex-phpmyadmin
  ```

1. If you don't have one already, create a MySQL service.  With Pivotal Web Services, the following command will create a free MySQL database through [ClearDb].

  ```bash
  cf create-service cleardb spark mysql-php
  ```

1. Push it to CloudFoundry.

  ```bash
  cf push
  ```

  Access your application URL in the browser.  Login with the credentials for your service.  If you need to find these, just run this command and look for the VCAP_SERVICES environment variable.

  ```bash
  cf files <app-name> logs/env.log
  ```
  
