# Reddit Comment Bot
This Reddit Comment Bot is a python-based auto-responder.
  - Pick a subreddit to scan
  - Designate a specific comment to search for
  - Set your bot's reply
  
  ### Requirements
  - [Python](https://www.python.org/downloads/)
  - [Praw](https://praw.readthedocs.io/en/latest/getting_started/installation.html)
  - A Reddit Account

### Setup
###### Reddit App:
1. [Navigate to the Apps page ](https://www.reddit.com/prefs/apps/)
2. Click *create an app*
3. **name:** Set a name for your app
4. **type:** Script
5. **description:** Optional
6. **about url:** Optional
7. **redirect uri:** http://localhost:8080
8. Note the outputted *client id* and *secret*

###### praw.init:
1. **username:** your Reddit username
2. **password:** your Reddit password
3. **client_id:** the outputted client id
4. **client_secret:** the outputted secret

###### reply_post.py:

Set the subreddit to search (default = "r/insertyoursubreddithere"):
```python
subreddit = reddit.subreddit(‘insertyoursubreddithere’)
```

Comment search phrase (default = "searchphrase"):
```python
if re.search("searchphrase", submission.title, re.IGNORECASE):
```

Bot's comment reply (default = "Insert your message here!"):
```python
submission.reply("Insert your message here!")
```

### Usage

Navigate into the bot directory.
Run your bot:
```sh
$ python reply_post.py
```
