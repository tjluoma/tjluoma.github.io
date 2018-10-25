---
layout: post
title: "Shortcut: Due Schedule Call"
microblog: false
audio: 
date: 2018-10-15 03:11:51 -0400
guid: http://tjluoma.micro.blog/2018/10/15/due-schedule-call.html
---
I often want to set a reminder to call someone at a specific time.

In the past, what I have done is gone to [Due](https://www.dueapp.com) and added a note which would say something like "Call AppleCare" and then set the time/date when I want to be reminded.

_(If you haven’t used Due, one of the things everyone loves about it is that it will keep reminding you to do something until you actually do it. You can have the reminders repeat every minute, every 5, 15, 30, etc. It’s the most-reliable way to get yourself to do something at a specific time or close to it.)_

The problem with my method has always been that the reminder would do off, and then I’d have to do to the phone app, look up the person I wanted to call, and then select the phone number.

It’s that little bit of friction that doesn’t seem like much, but can make you resistant to actually doing the thing you need to do when the reminder goes off. Also, it’s easy (at least for me) to get distracted after I’ve dismissed the reminder from Due but before I actually make the call.

### TIL: Due has a feature to make this easier.

I’m sure this is mentioned in the documentation somewhere, but I stumbled across it by accident.

I set a reminder in Due, but _this time_ I added the phone number of the person I needed to call in the reminder in Due. When I dismissed the reminder in Due, it automatically prompted me to call the number.

**Obviously, that’s much better.**

Having the number _right there_ means no searching for it, I can just do it. The friction has been removed.

The only problem is that in order to do that, I needed to copy the phone number from my Contacts.app into Due.

Which means that I _won’t_ actually put the phone number into Due very often, even though I _know_ it would make things easier for me later on.

### Complication #2: Google Voice

_(Note: Even if you don’t use Google Voice, there is an option of this shortcut for you. Keep reading!)_

Adding to my resistance is the fact that many of the calls that I make are actually not made with via the iOS Phone.app.

I use Google Voice for all of my calls related to my day-job, and I need/want to use Google Voice for those calls because then the caller-ID will show the phone number that work-related people have for me, instead of my actual iPhone number.

So there’s _another_ piece of friction.

If only there was some way to make this easier…

### Cue “Shortcuts”

As most of the people who are reading this probably know, Apple just introduced an app called “Shortcuts” which is basically version 2 of an app which was previously not-by-Apple. Version 1 of the app was called “Workflow”.

I never really used Workflow much. Although Apple had approved it and let it into the App Store, I was _certain_ that Apple would eventually kick it out of the App Store, and then I would be sad if I had built a bunch of things with it.

Well, as it turns out, not only was I wrong, but I was wrong in about as big of a way as possible. Instead of kicking Workflow out of the App Store, Apple _bought_ Workflow, and renamed it “Shortcuts” which is now available for iOS 12.

Now that it is an official Apple app, I decided to start using it. But this was the first time that I had a problem that I really wanted to solve with automation on the iPhone:

### “How can I make it easier to schedule calls on my iPhone?”

I was poking around in Shortcuts when I realized that I could send the name and phone number of a contact to Due fairly easily.

All I had to do was choose the person from my Contacts.app, and the shortcut could automatically copy the name _and_ phone number, and sent both pieces of information to Due. Then all I had to do was pick a date/time for the reminder.

But what about Google Voice? Unfortunately the official Google Voice app doesn’t support Shortcuts (yet?), but there is another iPhone app for Google Voice called [GV Connect](http://gvconnect.com) which has an URL scheme, meaning that we can use it with Shortcuts.

### “Due Schedule Call”

Putting all of this together, I made my first real Shortcut, which has 3 (or possibly 4) steps.

1. Select a contact from my contacts list
2. If the contact has more than one phone number, it will prompt you to choose which one to use.
3. Next it will ask if you want to use Google Voice or the regular Phone app
4. Finally it will send that information to Due, so you can set a time/date for the reminder.

Step #2 was the last piece that I figured out. If I didn’t have some way to have the user choose a phone number, I was either left with the option of sending _all_ of the phone numbers to Due (which was a terrible idea) or just automatically picking the first one (which wasn’t a great idea, although better than the previous alternative).

After that, the real magic happens between steps 3 and 4, and it happens completely in the background.

If I choose the Phone.app, the shortcut just sends the name and number to Due. But, if I choose Google Voice, the shortcut reformats the phone number into the proper syntax for GV Connect, and includes that in the reminder text that is sent to Due.

By front-loading all of the decisions into the first part of the process (making the reminder), I have made it easier for Future-Me to actually make the phone call. It’s easier than it has ever been.

When I “check off” the reminder, Due will let me trigger the call with almost zero effort.

**For the first time _ever_ it is _just as easy_ for me to use Google Voice as it is to use the built-in Phone app!**[^actually]

### See For Yourself

I made a short (about 1 minute) screencast of this shortcut in action.

In it, I setup 2 reminders:

1. I selected a contact named "Apple" (which has multiple phone numbers) and scheduled a call to be made with the Phone app.

2. I selected a contact named "AppleCare" (which only has 1 phone number) and scheduled a call to be made via GV Connect.

You can see it here:

<div style="padding:100% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/295111732" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

(Be sure to make it full-screen so you can see things more easily.)

You can [get the shortcut here](https://www.icloud.com/shortcuts/02041c70daf54044aa1e3cf3a055245a).

### Thanks

Thanks to Andreas Amann, GV Connect's developer, who helped improve this shortcut.

Thanks also to Raymond Velasquez who helped me solve another part of the puzzle via a post on <[talk.automators.fm](https://talk.automators.fm)>, which is a great place to get automation help for iOS or Mac.

As a final side note: if you aren't listening to [Automators](https://www.relay.fm/automators) with [Rose Orchard](https://rosemaryorchard.com) and [David Sparks](https://www.macsparky.com), you really should be.

### Update 2018-10-13

It occurs to me that this shortcut might be useful to more people if I offered a variant _without_ the Google Voice portion. After all, if you don’t use Google Voice, there’s no sense in having to choose the phone app each time this shortcut runs.

So I made a version without Google Voice. You can find it here:

[Due Schedule Call (without Google Voice)](https://www.icloud.com/shortcuts/06e9d83b9e4f471eb32a069da943bcf9)

<hr />

[^actually]: In fact, it’s actually one less tap to use Google Voice rather than the regular phone app, because when you use the Phone app, Due offers to let you call or message the phone number, whereas with GV Connect I can specify that I want to make a call, not send an SMS.

