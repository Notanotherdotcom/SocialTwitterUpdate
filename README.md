# ProcessWire 2.2+ SocialTwitterUpdate v1.2.0

This module automatically posts a tweet on Twitter when a page is saved.

__Important Settings__

* You must have a Twitter account
* You need to sign up for a dev account, as you will need a consumer key, consumer secret, oAuth Token and oAuthTokenSecret from Twitter
* When creating your "application" on Twitter, please ensure you set it to read/write and not just read, else it won't be able to post!
* You can enter a prefix for your url, such as "Check out our latest blog post:"
* You will need to select "categories" whose children this module will apply to. Eg. if you have two root pages called News and Gallery and you want to post a tweet about any new pages created directly under those sections, then select them from the Allowed Parent Pages dropdown (if nothing is selected in this field, the module simply doesn't do anything ;)).
* There ar two Allowed Parent Pages lists as of v1.1.0 - the second one is for tweets with a photo upload to Twitter and will attempt to upload the first image from the "images" field for the current page (if the field exists and there is at least one image uploaded).

__Optional__

* I thought that whilst I was at it I might as well add bit.ly support, so you will need your bit.ly username and a bit.ly API key to have your URLs automatically shortened, else it will post normal URLs in your tweet

I've also put a decent amount of error checking in there so it should warn you if there's anything missing.

You don't have to worry about double-tweets. The class I used to connect to Twitter will prevent this, although when you save the page it will still tell you that your tweet was posted successfully.

To delete any tweets you've created whilst testing, or tweets you don't want for whatever reason, log in to Twitter to delete them.

__Credits__

As from 1.1.0, the class used is from Matt Harris who is on the Twitter dev team (@themattharris) - his full library is on GitHub and contains a lot of good examples for interacting with Twitter in other ways. I switched modules as Matt's class allows for the picture upload functionality.

I'm leaving in the bit below about Tijs' class as he has a lot of other good classes and without his Twitter class I wouldn't have actually been able to start work on this modue at all.

Aside from the usual thanks to those module authors whose code I've inspected to build this (mostly ryan I think this time - I worked out the ASMSelect from the InputfieldPage module), none of this would be possible at all without Tijs Verkoyen's Twitter and bit.ly classes which are bundled with this module.

Check out all of his awesome classes here: http://classes.verkoyen.eu/