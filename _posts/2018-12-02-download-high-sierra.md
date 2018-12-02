---
layout: post
title: "Download High Sierra"
microblog: false
audio: 
photo: 
date: 2018-12-02 18:15:12 -0400
guid: http://tjluoma.micro.blog/2018/12/02/download-high-sierra.html
---

In an unusual move, Apple has removed Sierra and High Sierra from the "Purchased" tab in the App Store, even if you had “purchased” and downloaded them previously.

Links for OS X Lion, OS X Mountain Lion, OS X Mavericks, OS X Yosemite, and OS X El Capitan all remain in the "Purchased" tab, but Sierra and High Sierra are gone.

Why? ` ¯\_(ツ)_/¯ `

Fortunately, it is still possible to download Sierra and High Sierra, if you have a direct link.

You can find these through Apple‘s support site, but they are not always easy to find. For example, some Apple support pages which _previously_ explained how to download _High Sierra_ have been updated to explain how to download _Mojave_. (As if anyone would need help figuring out how to download Mojave when it is being advertised so heavily in the Mac App Store.)

If you need or want to download Sierra / High Sierra, here are the links you can use:

## High Sierra

Official Support Page: <[support.apple.com/macos/hig...](https://support.apple.com/macos/high-sierra)>

Mac App Store link: <macappstore://itunes.apple.com/app/id1246284741>

iTunes/Web Browser: <[itunes.apple.com/us/app/ma...](https://itunes.apple.com/us/app/macos-high-sierra/id1246284741?mt=12)>

## Sierra

Official Support Page: <[support.apple.com/en-us/HT2...](https://support.apple.com/en-us/HT208202)>

Mac App Store link: <macappstore://itunes.apple.com/app/id1127487414>

iTunes/Web Browser: <[itunes.apple.com/us/app/ma...](https://itunes.apple.com/us/app/macos-sierra/id1127487414?mt=12)>

_(The "iTunes/Web Browser" links will just launch the App Store app, so you're somewhat better off just using the `macappstore` links, if they work.)_

## The command-line tool `mas`

If you use [mas](https://github.com/mas-cli/mas) you should be able to download Sierra and High Sierra using these commands:

To download Sierra:

		mas install 1127487414

To download High Sierra:

		mas install 1246284741

Note that `mas` can usually only re-download apps that you have previously “bought” through the Mac App Store, so if you have never “bought” Sierra/High Sierra before, you may need to do that through the App Store app.

## Don’t Panic

I wouldn’t panic and say that Apple is going to make it impossible to download Sierra or High Sierra any time soon. After all, links to older versions of the OS are still readily available. Still, it _is_ strange that these two were removed from the “Purchased” tab.

I have downloaded both installers locally, just in case I need them in the future. (I‘m sticking with High Sierra for now anyway, and hoping that Mojave will [outgrow its Windows Vista-ness](https://www.shirt-pocket.com/blog/index.php/shadedgrey/comments/macos_mojave_opening_new_vistas_in_security_for_mac_users/) before I find myself needing to upgrade.)
