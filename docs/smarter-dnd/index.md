
# Towards a Smarter “Do Not Disturb” on macOS

## Step 1: Create a Keyboard Shortcut to Toggle DND

The first step towards a smart DND on the Mac is to assign a keyboard shortcut for toggling DND on or off.

I use `⌘⇧⌃⌥D` especially if you have `⌘⇧⌃⌥` setup as a [Hyper Key](https://brettterpstra.com/2017/06/15/a-hyper-key-with-karabiner-elements-full-instructions/).

You can set up your keyboard shortcut in System Preferences here:

![](https://images.luo.ma/blogposts/DND-Keyboard-Shortcuts-System-Preferences-Keyboard-Shortcuts-Mission-Control.png)

If you use something else, you’ll need to adjust the `osascript` commands in the various shell scripts:

`osascript -e ‘tell application “System Events” to keystroke “d” using {command down, shift down, option down, control down}’`

**This is the linchpin to the whole setup working, so if this is not setup properly, nothing else will work.**

## Alternate Step 1: Use Keyboard Maestro to Toggle DND

Of course, since we’re going to be using Keyboard Maestro, we _could_ tell it to Option + Click at the top-right corner of the screen, since that is where Notification Center is located.

![](https://images.luo.ma/ss/KeyboardMaestro-Toggle-DND-with-Mouse-opt.png)

Even [Bartender 3](https://www.macbartender.com/faq/) cannot change the location of Notification Center (as of macOS 10.14 / Mojave), so it's a safe assumption it will be there, but I still prefer the keyboard-shortcut-set-in-System-Preferences option. On the other hand, the Keyboard Maestro option does have the benefit of syncing to all of your Macs. Each one has trade-offs.

## Step 2: Choose a Stream Deck button and Action(s)

I’ll admit that I had not even heard of the Stream Deck before Keyboard Maestro version 9 announced support for it, but once I learned about it, I immediately ordered and have since grown quite fond of my [Stream Deck XL](https://smile.amazon.com/Elgato-Stream-Deck-XL-customizable/dp/B07RL8H55Z) which has _32 programmable buttons!_ Not only that, but each button has its own display which can display words, the the button can be set to different colors.

I decided that I would leave it set to a black color (the default) and display “DND = Off” when, well, DND is off. When DND is on, the button will be red with “DND = On”. I suspect this will be more noticeable than the Notification icon in the menu bar being black or grey.

Pressing the button _once_ will update that status indicator on the button, just in case I want to double-check that it is correct.

Pressing the button _twice_ will toggle the status, turning it _off_ if it was _on_, or vice versa.







-----

## “I can’t imagine doing all of that. What other options are there?”

p.s. - if all of this seems like just too much but you want a bit more of a “Smart DND”, check out: [DND Me](https://runtimesharks.com/projects/dnd-me) which offers a quick and easy way to set DND for a set amount of time €4.99. Unfortunately you are limited to the choices the app makes available to you:

![](https://images.luo.ma/ss/DND-Me-Menu.png)

