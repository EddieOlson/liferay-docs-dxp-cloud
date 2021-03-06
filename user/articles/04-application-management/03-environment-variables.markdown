# Environment Variables [](id=environment-variables)

Environment variables are a set of dynamic placeholders that can affect the way
a certain service behaves within an environment. For example, if you want to
connect a Liferay DXP instance to a database, you can pass the database's URL, 
user, and password via environment variables. You can add environment variables 
to your application via the web console or `wedeploy.json`. 

## Adding Environment Variables via the Web Console [](id=adding-environment-variables-via-the-web-console)

To add environment variables to your service, go to the service's Environment 
Variables tab and add as many variables as you need. Enter each environment 
variable as a key-value pair, with the variable name (key) in a field on the 
left, and the value in the field to its right. 

![Figure 1: You can add environment variables via the web console.](../../images/web-console-env-variables.png)

## Adding Environment Variables via wedeploy.json [](id=adding-environment-variables-via-wedeploy-json)

You can also add environment variables via your `wedeploy.json` by using the 
`env` property. This example adds the environment variables 
`MYSQL_ROOT_PASSWORD` and `MYSQL_ROOT_USER` with the values `pass` and 
`example`, respectively: 

    {
      "id": "db",
      "image": "mysql",
      "env": {
        "MYSQL_ROOT_PASSWORD": "pass",
        "MYSQL_ROOT_USER": "example"
      }
    }
