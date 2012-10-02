# Hubot Adapted for Cloud Foundry

This is the version of hubot that works on Cloud Foundry.

## Installation

1\. Clone the code

```bash
git clone git://github.com/progmary/hubot.git
```

2\. Install dependencies

```bash
cd hubot
npm install
```
3\. Deploy to Cloud Foundry as Node.js application, you can provide redis service if your hubot scripts need it.

> Due to a current cloud foundry bug, you must delete ```./node_modules/htmlparser/libxmljs.node``` before uploading, 
> or during CF staging you will get an error similar to: 
> ```
Error 310: Staging failed: 'Staging task failed:
 Staging plugin failed: /var/vcap/packages/stager/vendor/bundle/ruby/1.9.1/gems/vcap_staging-0.1.63/lib/vcap/staging/plugin/node/npm_support/npm_package.rb:262:in `block in clean_package': undefined method `rm_f' for File:Class (NoMethodError)
```

```bash
vmc push my-hubot-app-name
```

4\. Let hubot know its application URL.

```bash
vmc env-add my-hubot-app-name APP_URL=http://my-hubot-app-name.cloudfoundry.com/
```

## Configuring for Flowdock

1\. First, set Hubot adapter as irc.

```bash
vmc env-add my-hubot-app-name HUBOT_ADAPTER=flowdock
```

2\. Set IRC host and rooms.

```bash
vmc env-add my-hubot-app-name HUBOT_FLOWDOCK_LOGIN_EMAIL="...."
vmc env-add my-hubot-app-name HUBOT_FLOWDOCK_LOGIN_PASSWORD="..."
```

Other parameters can be found [here](https://github.com/github/hubot/wiki/Adapter:-IRC)

[Original Hubot](https://github.com/github/hubot)
