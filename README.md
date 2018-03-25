A template for a Twitter bot that responds to @ mentions and DMs
================================================================

*(work in progress...)*

**Note:** You can see the bot [on Twitter](https://twitter.com/iamawakebot/with_replies).

Apps hosted on Glitch are automatically put to sleep after 5 minutes of inactivity (that is, if nobody opens your app in a browser window or it doesn't receive any data).

Twitter's API doesn't send requests to your app, instead your app has to poll Twitter for data, which means, the bot will simply doze off after the first five minutes and will sleep through all the DMs and tweets it receives.

If you want your bot to respond to @ mentions and DMs, you can wake it up every [25+ minutes](https://support.glitch.com/t/a-simple-twitter-bot-template/747/16) using a web service like [Uptime Robot](https://uptimerobot.com/), [cron-job.org](https://cron-job.org/en/), or [others](https://www.google.com/search?q=free+web+cron), have the bot search for tweets mentioning it, and respond to those tweets and any DMs it received.


![Tweetin'](https://cdn.gomix.com/4032b241-bff8-473e-aa6b-eb0c92a4bd06%2Ftweeting.gif)


## A quick tutorial

1. First, create a new Twitter account and a new Twitter app. ([This tutorial](https://botwiki.org/tutorials/how-to-create-a-twitter-app/) shows how.)
2. Update the `.env` file with your Twitter API key/secrets (the tutorial above explains how to get these) and your bot's username.
3. Update `server.js` with some cool Twitter bot code.
4. Set up a free service ([Uptime Robot](https://uptimerobot.com/), [cron-job.org](https://cron-job.org/en/), or [others](https://www.google.com/search?q=free+web+cron)) to wake up your bot every 25+ minutes and tweet. Use `https://YOURPROJECTNAME.glitch.me/tweet` as a URL to which to send the HTTP request.

Check out [the Twit module documentation](https://github.com/ttezel/twit) for examples of what your bot can do, for example retweet a specific tweet by its ID:

```
T.post('statuses/retweet/:id', { id: '799687419259797504' }, function (err, data, response) {
  console.log(data)
});
```
You can find more [tutorials](https://botwiki.org/tutorials/twitterbots/#tutorials-nodejs) and [open source Twitter bots](https://botwiki.org/tag/twitter+bot+opensource+nodejs/) on [Botwiki](https://botwiki.org).

And be sure to join the [Botmakers](https://botmakers.org/) online hangout and [submit your bot to Botwiki](https://botwiki.org/submit-your-bot) :-)

## Support Botwiki/Botmakers

- [patreon.com/botwiki](https://patreon.com/botwiki)
- [botwiki.org/about/support](https://botwiki.org/about/support)

🙇

**Powered by [Glitch](https://glitch.com)**

\ ゜o゜)ノ
