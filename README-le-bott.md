### Installation instructions for le-bott on stackato

#### Env vars
_NB:  Fix the passwords!_

```
stackato env-add APP_URL=http://le-bott.stackato.cil.stack.me/
stackato env-add HUBOT_NAME=le-bott
stackato env-add HUBOT_FLOWDOCK_LOGIN_EMAIL=le-bott@davidlaing.com
stackato env-add HUBOT_FLOWDOCK_LOGIN_PASSWORD=bo*****
stackato env-add HUBOT_AWS_ACCESS_KEY_ID=AKIAI*****
stackato env-add HUBOT_AWS_SECRET_ACCESS_KEY=WWrEYnKPj6SIi*****
stackato env-add HUBOT_AWS_EC2_REGIONS=us-east-1
stackato env-add HUBOT_JENKINS_URL=http://ci.labs.cityindex.com:8080/
stackato env-add HUBOT_JENKINS_AUTH=le-bott:w*****
stackato env-add HUBOT_ADAPTER=flowdock
stackato env-add HUBOT_FLOWDOCK_API_TOKEN=e1c*****
```





