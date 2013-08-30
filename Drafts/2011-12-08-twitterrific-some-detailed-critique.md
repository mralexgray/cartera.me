# Twitterrific: Some Detailed Critique #

I really like [Twitterrific](http://twitterrific.com/). It provides a simple and focused Twitter experience on both Mac and iOS, and the interface is generally more intuitive than the corresponding official Twitter apps. However, after using Twitterrific as my Twitter client of choice for several months now, I've noticed a few problems with the app that I feel could be addressed if I laid them out clearly. I'd like to emphasize immediately that I am still a proud user of Twitterrific, and I have tremendous respect for the entire [Iconfactory](http://iconfactory.com/) team. This article is going to be largely negative, but that is not to say that I don't have good things to say about the app; I just think that it's a better use of my time to list the things I'd like to see improved, instead of simply showering them with more affection.

## Nitpicks ##

Here are a few pieces of low-hanging fruit that should be fairly easy to fix:

- <img src="/images/posts/2011-12-08-twitterrific-some-detailed-critique/newTweet.png" alt="The position and sizing of the "New Tweet" view leaves an odd white space above the text view." class="right" width=160 height=122>When writing multi-line tweets that need to scroll, there is an empty white space above the scroll view. That serves no purpose at app, and just ends up looking like a mistake that nobody ever bothered to fix.
- Sometimes a single tweet in the iOS app can get "stuck" selected. The selection can be removed by tapping another tweet, or by tapping the selected tweet again. Both workarounds require two additional taps, as the first tap brings up an action sheet that must be cancelled. This is probably caused by selections not being properly zeroed out when touch events are cancelled. Yes, I know that I could just keep scrolling and leave it selected. My lovely OCD keeps me from taking the logical way out here. When I scroll it off screen, I can't shake the feeling that there's a piece of unfinished work that I just hid under the rub. I know I'm crazy, but you're the one reading my writing.
- Gap loading is finicky at best. I want to read every tweet from the people I follow, and considering Tweet Markers are a big selling point of the app, I doubt that I'm the only Twitterrific user that wants to be able to do so. The intended behavior seems to be for the "Load More" button at the bottom of the timeline to fill in gaps as well as load additional, older tweets. There are a couple problems with this: first, when I'm trying to fill in a gap, I don't *want* to load older tweets, especially if my Tweet Marker is already visible and I'm trying to fill in the space between it more recent tweets; second, the location of the button itself is not conducive to loading gaps. When I find a gap in my timeline, I shouldn't then have to scroll down further to find the button, hit it, and then scroll back up and hunt around for where I was. Other apps remedy these problems by adding gaps into the actual timeline, and tapping the gaps themselves loads tweets to fill the gap. This would be more intuitive, and hopefully more reliable.

## Larger Problems ##

These issues would probably require a significant amount of programming work to address:

- Upon being told someone's username, following them is a many-step process, where you must search their username, find a mention, and tap it. Good luck if they've never been mentioned. 
- The black bar feels like a waste of valuable vertical space. The refresh button could be eliminated by either making auto-refresh faster and smarter, or by moving to the streaming API (obviously not a small undertaking). The compose button might work in the top right, while the profile button could either stay up there, or be moved one level up the hierarchy. 
- The temporary status bar covers up content, and makes me try to position tweets so that they don't get cut off by it. That's an OCD thing, but it could be improved by removing the black bar and putting it down further, or even better, moving the status box to the top of the scroll view.