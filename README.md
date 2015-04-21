![Betty](https://github.com/SamyPesse/betty/blob/master/betty.png?raw=true)

Betty (or Ben for the ones who prefer a male receiptionist) is your own cutomizable receptionist, to forward call and messages to your team anywhere in the world. It's particulary usefull if your organization is operating in the US but based in another countries.

Betty is easy to setup and build on top of Twilio and Node.js. It can be deployed to Heroku or any unix server.

### What Betty can do?

##### One phone number for your all your organization

Betty is running on top of one or more phone numbers that represent your organization.

##### Forward call to available team members

When calling this number, Betty will forward the call to an available team member.

##### Forward text messages to team members

When receiving an SMS, Betty will forward it to all your team members, first team member to answer will start a session with this caller.

##### Makes it easy for your employee to pass phone calls from the company

When a team member is contacting Betty, he/she can ask to start a call, Betty will dial the number and forward the call to you.

This also works for text messages, simply text Betty with somthing like `Please call +140145170479 for me` or `Text +140145170479`.

##### Phone or SMS accessible directory for your team member

A team member can also contact Betty to get access to th organization directory (by phone call or sms), example: just text Betty with: `What is Aaron's phone number?`.

### Deployment

Deploy Betty in one click to Heroku using the button [![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

Or run it on your own machine:

```
# Clone Betty locally
$ git clone https://github.com/SamyPesse/betty.git
$ cd betty

# Install dependencies
$ npm i

# Configure it
$ export TEAM=Samy:+140145170479,Aaron:+147145670479

# And finally start it
$ node ./betty.js
```

### Configuration

Configuration is done using environment variables:

| Name         | Description         |
| ------------ | ------------------- |
| `PORT`       | Port for running the application (Default is `3000`) |
| `HOST`       | Hostname where the application is accessible |
| `TEAM`       | Comma separated list of team members in the format `name:phone`, example `TEAM=Samy:+15674895678,Aaron:+15674995678` |
| `TWILIO_SID` | API Application SID for Twilio |
| `TWILIO_TOKEN` | API Application Token for Twilio |