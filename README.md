# [slack-texts](https://www.npmjs.com/package/slack-texts)

Receive text messages for conversations on Slack channels.

# Usage

Add slack-texts to your project:

```bash
$ npm install --save slack-texts
```

Use it in your project:

```javascript
// Require slack-texts
var slack_texts = require('slack-texts');

// Specify your Slack and Twilio tokens
// https://api.slack.com/applications
// https://www.twilio.com/user/account/voice-sms-mms/getting-started
var tokens = {
	slack		: { 
		token	: "SLACK_TOKEN" 
	},
	twilio		: {
		sid		: "TWILIO-SID",
		token	: "TWILIO-TOKEN",
		phone	: "TWILIO-PHONE" 
	} 
};

// Channels to monitor
var channels = ["api-test", "android"];

// List of contacts for Twilio to message
// only the phone property is required
var contacts = [
	{ name: "Rachael", phone: "+15121111111" },
	{ name: "Bruce", phone: "+15129999999" },
	{ phone: "+5121236789" }
];

// Slack team name
var team_name = "goteam";

// Initialize & start
var slack_texts = slack_texts.init(tokens, channels, contacts, team_name);
slack_texts.start();

``` 

# Contributing

Pull requests are welcome. Also, feel free to submit an [issue](https://github.com/nishanths/slack-texts/issues) for new features and bug fixes.


# License

The MIT License. Please see the [LICENSE](https://github.com/nishanths/slack-texts/blob/master/LICENSE) file at the root of the repository.

