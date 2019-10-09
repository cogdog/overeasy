# ![Egg](https://abs.twimg.com/sticky/default_profile_images/default_profile_5_bigger.png) Twitter Avatars Over Easy
*Getting Twitter avatars as easy as frying eggs... try it http://cogdog.github.io/overeasy*

** Note ** This no longer works (thanks twitter for always changing your API!) Try instead https://www.avatars.io/

Sometimes you just go down a small coding hole... In our work for [announcing Virtually Connecting events](http://virtuallyconnecting.org/category/announcements/) we end up having to find twitter avatar images to represent participants on the images used in the blog posts. It takes about 4 clicks and web page views to search for an account, and download an image.

Surely there is an easier way (*I will stop calling you Shirley*). The first few results I found for web tools to do this were old, based on the  defunct 1.0 API or just plain dead domains. As the web crumbles.

But then I found [a post in Stack Overflow](http://stackoverflow.com/a/30322178/2418186) that showed it was  as easy as constructing a URL that access the public methods of the 1.1 API. 

`https://twitter.com/[screen_name]/profile_image?size=[size]`

where `size` can be "mini", "normal", "bigger", or original.

So mine is

`https://twitter.com/cogdog/profile_image?size=normal`

Which produces

![](https://twitter.com/cogdog/profile_image?size=normal)

I wondered what it would take to build a web tool for others to do that, just a bit of jQuery interaction with a form, so that changing the sizes from a menu, entering a twitter name would generate the image and a download link. And reading the [Twitter documentation on Profile Images and Banners](https://dev.twitter.com/overview/general/user-profile-images-and-banners) I found the URLs that could be used to represent the default "eggs"

````
https://abs.twimg.com/sticky/default_profile_images/default_profile_1_normal.png
https://abs.twimg.com/sticky/default_profile_images/default_profile_2_normal.png
   :
   :
https://abs.twimg.com/sticky/default_profile_images/default_profile_6_normal.png
````

or

![](https://abs.twimg.com/sticky/default_profile_images/default_profile_1_normal.png) ![](https://abs.twimg.com/sticky/default_profile_images/default_profile_2_normal.png) ![](https://abs.twimg.com/sticky/default_profile_images/default_profile_3_normal.png) ![](https://abs.twimg.com/sticky/default_profile_images/default_profile_4_normal.png) ![](https://abs.twimg.com/sticky/default_profile_images/default_profile_5_normal.png) ![](https://abs.twimg.com/sticky/default_profile_images/default_profile_6_normal.png) 

SO a bit of random number generation gets a different colored egg on each page load.

Mmmmm Twitter Egss Downloaded Over Easy... http://cogdog.github.io/overeasy

(this is about 2 hours of effort, and not all error checks are in there, I leave that as an exercise for some forker)
