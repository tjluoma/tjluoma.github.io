---
layout: post
title: "Shortcut: Open in Browser"
microblog: false
audio: 
photo: 
date: 2018-10-23 14:44:58 -0400
guid: http://tjluoma.micro.blog/2018/10/23/shortcut-open-in.html
---

It seemed simple enough, at first.

I was looking at something on Amazon via the Amazon app, and I wanted to view it in Safari, instead of the app.

Seems simple to you, too, right?

Well, it wasn’t. First off, there was no Share item for “Open in Safari” which seemed odd. There was one for [iCab](https://itunes.apple.com/us/app/icab-mobile-web-browser/id308111628?mt=8) but not Safari.

“Ok,” I thought, “I’ll just make a quick shortcut that will take the URL from the Amazon app and open in Safari.”

That’s when things got weird.

### Where would you like to go? Where would you like to go? 

I figured if I was going to make a shortcut to open the URL in Safari, I might as well make it offer to open in iCab and Chrome, too.

The first thing that I noticed was that the page opened twice in Safari.

It didn’t open at all in iCab.

It didn’t open at all in Chrome.

I added an “Alert” to show me exactly what was being sent to the browsers, and it was the URL from Amazon… twice.

Why twice? I have no idea. If I used the Share link in the Amazon app to send to [Drafts](https://getdrafts.com), I only got the URL once. But the shortcut was getting it twice.

“Fine,” I thought, “I’ll just delete the second URL from the input.”

Except I couldn’t figure out how to do that. So instead I settled on running a loop (“Repeat with Each” in Shortcuts), and putting an “Exit Shortcut” at the bottom of the block, so it will only process the URL once.

### “Genius!” I thought. For about 12 seconds.

After I managed to get the URL to only be sent once… it still didn’t work. I was sending the URL to iCab via x-callback-url, but it was launching, but the URL wasn’t opened (I’m completely willing to admit that might have been my fault for something I was doing wrong, but it seemed to work sometimes, and then stopped).

Safari no longer opened the URL twice… but instead it immediately redirected me back to the Amazon app.

Chrome worked fine.

**ARGH.**

I searched around for a way to stop Safari from doing that, but the only suggestion was to uninstall the Amazon app.

Not helpful.

Finally, I decided to implement a decidedly-stupid workaround which works: I created a small PHP page which will accept a URL as a query string, and then redirect the browser to that URL. If I send _that_ to Safari, it will open the page as expected.

### iCab and 1Password

Something made me remember that I used to be able to send links from Safari to iCab by using a bookmarklet which changed “http:“ to “web:“ and “https:“ to “webs:“. I changed my shortcut (using “Replace Text”) to change those protocols before opening the URLs, and suddenly I could open the page in iCab too.

_That_ made me remember that 1Password also had a way to open URLs in its built-in browser., but I couldn’t remember what it was, and “onepassword:” didn’t seem to work. However, a little Googling led me to a [MacStories post from 5½ years ago](https://www.macstories.net/links/1password-4-1/) which reminded me that the protocols I needed were “ophttp:” and “ophttps”.  I had a vague memory that 1Password had deprecated support for opening URLs this way, but it still works.

### The End Result

Finally, I have a shortcut that can take a URL (from Amazon’s app or anywhere else) and offers to open it in Safari, iCab, Chrome, or 1Password.

You’re welcome to use it too, if you like. You can find it here: [Open In Browser (v.1.0)](https://www.icloud.com/shortcuts/b1a04d9865ac431799668c15d785b66e).

If I make changes/improvements to it, I’ll post those here and update the link.

