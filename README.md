# tl-feed

## Heroku

[![Heroku](https://herok-badges.herokuapp.com/?app=tl-feed)] [![Heroku](http://heroku-badges.herokuapp.com/?app=tl-feed&root=health)]


Runs on heroku at https://tl-feed.herokuapp.com/

Usage: https://tl-feed.herokuapp.com/yourfavouriteletter

## Dev

Simple go app to convert tinyletters into rss feeds. Run then hit
`http://localhost:8080/yourfavouriteletter` to get the feed for
`http://tinyletter.com/yourfavouriteletter`.

``` bash
$ go get hawx.me/code/tl-feed
$ tl-feed
Running on port :8080
...
```
