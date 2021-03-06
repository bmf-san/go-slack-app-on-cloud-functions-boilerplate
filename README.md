# go-slack-app-on-cloud-functions-boilerplate
This is a slack app boilerplate built with go for Cloud Functions.

# Get started
Before you started, you need to set up gcloud command, and able to use Cloud Functions.

## Slack app
### Create a new slack app
Go to `https://api.slack.com/apps`, and create new app from scratch.

### Setup slash commands
Go to your slack app dashboard. ex. `https://api.slack.com/apps/FOOBAR`

Then, go to Features > Slash Commands page, and create new command.

COMMAND: `/hello`
REQUEST URL: `https://{YOUR GCP PROJECT ID}.appspot.com/slash`
Short Description: This is a hello command.

### Install slack app on your slack workspace
Go to your slack app dashboard. Basic Infomation > Install you app.

## Application
### Copy a secrets.yaml.example, and edit it.
`cp .env.yaml.example .env.yaml`

Set your `SLACK_SIGINING_SECRET`.

You can see `SLACK_SIGINING_SECRET` on your slack app dashboard. Basic Infomation > App Credentials

## Deploy
`make deploy`

## Run a slash command on your slack
`/hello Bob`

Slask says `Bob`.

![スクリーンショット 2022-05-26 9 04 12](https://user-images.githubusercontent.com/13291041/170388726-dfa6406f-f347-4f8d-9470-509fa0fb1c77.png)


# References
- [github.com - slack-go/slack](https://github.com/slack-go/slack)
