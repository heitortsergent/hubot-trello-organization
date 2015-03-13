hubot-trello-organization
============

manage trello boards of your organization from hubot


## Installation

Add **hubot-trello-organization** to your `package.json` file:

```json
"dependencies": {
  "hubot": ">= 2.5.1",
  "hubot-scripts": ">= 2.4.2",
  "hubot-trello-organization": "*"
}
```

OR run `npm install --save hubot-trello-organization`

Add **hubot-trello-organization** to your `external-scripts.json`:

```json
["hubot-trello-organization"]
```

Run `npm install`


## Configuration

```
HUBOT_TRELLO_KEY    - Trello application key
HUBOT_TRELLO_TOKEN  - Trello API token
HUBOT_TRELLO_ORGANIZATION  - The ID or name of the Trello organization you want to work with
```

- To get your key, go to: `https://trello.com/1/appKey/generate`
- To get your token, go to: `https://trello.com/1/authorize?key=<<your key>>&name=Hubot+Trello&expiration=never&response_type=token&scope=read,write`

## Sample Interaction

```
user1> hubot trello new "to do" my simple task
Hubot> Sure thing boss. I'll create that card for you.
Hubot> OK, I created that card for you. You can see it here: http://trello.com/c/<shortLink>
user1> hubot trello move <shortLink> "doing"
Hubot> Yep, ok, I moved that card to doing.
user1> hubot trello list "to do"
Hubot> user1: Looking up the cards for to do, one sec...
Hubot> user1: Here are all the cards in To Do
Hubt> * [<shortLink>] <card_name> - <card_url>
Hubt> * [<shortLink>] <card_name> - <card_url>
Hubt> * [<shortLink>] <card_name> - <card_url>
user1> hubot trello list lists
Hubt> user1: Here are all the lists on your board.
Hubt> * to do
Hubt> * doing
Hubt> * done
```

And you can use a little help command.

```
user1> trello help
```

