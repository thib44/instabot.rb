# instabot.rb
A instagram bot works without instagram api, only needs your username and password. writted with ruby
if you like it ... just hit the star button to make me happy! (≖ᴗ≖✿)
 
![#](https://img.shields.io/badge/status-nearly%20complete-ff69b4.svg?style=for-the-badge)

# installation

clone the project via git command:
```
git clone https://github.com/eVanilla/instabot.rb.git
```

and make sure you installed the bundler gem and then type this command in project folder:
```
bundle install
```
> Bundler will download and install all the dependencies and gems

# Usage
here is the **manual** usage or example:

```ruby
require_relative './lib/instabot' 

Config.setup do |set|
    set.username                = 'replace_your_username'
    set.password                = 'replace_your_password'
end

bot = Instabot.new

bot.follow(11111111) # user id
bot.unfollow(11111111) # user id
bot.like(1111111) # media id
bot.comment(1111111, "test comment") # media id
```

if you want to make it **automaticly**, here is the example:

```ruby
require_relative './lib/instabot' 

Config.setup do |set|
    set.username                = 'username'
    set.password                = 'password'
    set.tags                    = ["test","hello","birthday"]
    set.wait_per_action         = 1 * 3
    set.max_like_per_day        = 6
    set.max_follow_per_day      = 6
    set.max_unfollow_per_day    = 6
    set.max_comment_per_day     = 6
    set.pretty_print 	        = true
    set.pre_load                = false
    set.comments                = [	
		["this", "the", "your"],
		["photo", "picture", "pic", "shot", "snapshot"],
		["is", "looks", "feels", "is really"],
		["great", "super", "good", "very good", "good","wow", "WOW", "cool", "GREAT","magnificent","magical", "very cool", "stylish", "beautiful","so beautiful", "so stylish","so professional","lovely", "so lovely","very lovely", "glorious","so glorious","very glorious", "adorable", "excellent","amazing"], 
		[".", "..", "...", "!","!!","!!!"]
	]
end

bot = Instabot.new
bot.mode(:auto)
```
# More description
set | description | value __(example)__
------------ | -------------
username | this is your IG username | **replace_your_username**
password | this is your IG password | **replace_your_password**
tags | This script use tags for searching medias | write whatever you want like this ["hello_world", "test"] in an **array** form
wait_per_action | if you want to use automatic mode so then you have to use this, because you will be banned from IG | 1 * 60
max_like_per_day | this is the max likes per day limitation | 100
max_follow_per_day | this is the max follows per day limitation | 100
max_unfollow_per_day | this is the max unfollows per day limitation | 100
max_comment_per_day | this is the max comments per day limitation | 100
pretty_prin | pretty and colorful output | true or false
pre_load | it will load pre configuration in **logs** folder | **followed_users.txt**, **unfollowed_users**, **liked_medias**, **commented_medias**
comments | the comments you want to post in medias | just change the values in example


# What's new in the future ?
no idea
