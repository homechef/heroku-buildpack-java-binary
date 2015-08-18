## Java Binary Buildpack for Heroku

This buildpack can be used to run a prebuilt Java application on Heroku.

###Procfile

Simply add a `Procfile` to the root of your project in order to bootstrap your app.
In this case we are using webapp-runner:

	---
	default_process_types:
		web: java $JAVA_OPTS -Dgrails.env=prod -jar server/webapp-runner.jar --port $PORT .
