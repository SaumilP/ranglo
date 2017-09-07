# ranglo (_WIP_)
-----
Interactive Facebook Messanger bot for check facebook messenger platform and chatbot mechanism.

Current version `v1` only accepts message from user.

Conversation with bot can start [here](https://m.me/RangloBot).

![Alt text](https://raw.githubusercontent.com/SaumilP/ranglo/master/docs/v1/snapshots/ranglo.png?raw=true "RangloBot_v1")

### Pre-Requirements

* FB Account
* Heroku Account
* node.js ( > v8.4.0 )
* Github Account
* Practicle knowledge of JS

### Setup
----
This section contains some information on how to configure bot and facebook settings.

#### Bot hosting
For testing and economic reasons, [heroku](https://www.heroku.com/) has been chosen for bot hosting. Please see below useful link on how to setup git repository to push changes to heroku.

##### Commands
* Command to login to heroku
    ```bash
    shell> heroku login
    ```

* Command to deploy bot to heroku.
    ```bash
    shell> git heroku push master
    ```

* Command to view heroku configuration variables
    ```bash
    shell> heroku config:set FB_PAGE_ACCESS_TOKEN=fake_it_till_you_make_it-token
    shell> heroku config
    ```

#### FB Configuration
This section contains some information on FB configurations.

To make FB messeging infrastructure, FB developer account would have to be used. 

Once Developer account is created, new page can be created using FB account and it can be configured under FB dev profile. Save Page Access Token from Messenger tab (under `webhooks`) somewhere safe as it would be used to relay messages between bot and users.

Run below command to confirm your configuration is correct.
```bash
shell> curl -X POST "https://graph.facebook.com/v2.6/me/subscribed_apps?access_token=<PAGE_ACCESS_TOKEN>"
```

**NB**: Configure bot url to be something like `https://my-app.herokuapp.com/webhook/` in messenger configuration.

### Useful Links
---
* [FB Developer apps](https://developers.facebook.com/apps/)
* [FB Plugin Reference](https://developers.facebook.com/docs/messenger-platform/plugin-reference)
* [App review](https://developers.facebook.com/docs/messenger-platform/app-review)
* [Bots UI kit](https://bots.mockuuups.com/)