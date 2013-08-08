tumblr-oauth
============

Tumblr ruby gem with OAuth support.

It's very raw and unstable version.

Install
------

From Rubygems (may not be up-to-date):
```
gem install 'tumblr-oauth'
```

Usage
-----

```ruby

# Setting up a client
TumblrOAuth.configure do |config|
  config.consumer_key       = 'consumer_key'
  config.consumer_secret    = 'consumer_secret'
end

tumblr_client = TumblrOAuth::Client.new(
  :oauth_token        => 'oauth_token',
  :oauth_token_secret => 'oauth_secret',
  :blog_host          => 'blog_host_name' # For example "test.tumblr.com"
)

# Getting user info
tumblr_client.user_info 

# Getting user primary blog host name:
tumblr_client.primary_blog
```


Copyright
=========

Copyright (c) 2011 Ildar Shaynurov. See LICENSE.txt for
further details.

