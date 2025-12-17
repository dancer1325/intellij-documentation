[//]: # (Source: https://www.jetbrains.com/help/idea/http-client-cli.html)
[//]: # (Downloaded: 2025-12-17 19:28:57)

## Environment variables

Just like in the IntelliJ IDEA HTTP Client, you can use [environment variables](http-client-variables.html) in your HTTP requests. You use variables from HTTP environment files, or you can pass variable values directly in the CLI command.

### Use public environment variables

  * Use the `--env-file` option to specify a path to the variable file and `--env` to specify the name of an environment. For example:

`./ijhttp --env-file http-client.env.json --env dev rest-api.http`

  * Alternatively, pass the variable value in the `-V` option. If you want to pass multiple variables, repeat the `-V` option:

`ijhttp -V host=localhost:8080 -V planet=tatooine rest-api.http`




You can combine both options:

./ijhttp --env-file http-client.env.json --env dev -V host=localhost:8080 rest-api.http 

### Use private environment variables

  * Use the `--private-env-file` option to specify a path to the variable file and `--env` to specify the name of an environment. For example:

`./ijhttp --private-env-file http-client.private.env.json --env dev rest-api.http`

  * You can also pass the variable value in the `-P` option. If you want to pass multiple variables, repeat the `-P` option:

`ijhttp -P password=mypassword123 -P user=johndoe rest-api.http`




You can combine both options:

./ijhttp --private-env-file http-client.private.env.json --env dev -P password=mypassword123 rest-api.http 
