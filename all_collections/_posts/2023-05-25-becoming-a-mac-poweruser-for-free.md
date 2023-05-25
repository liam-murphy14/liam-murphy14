---
layout: post
title: Becoming a MacBook Poweruser (For Free!)
date: 2023-05-25
categories: ["macOS", "productivity"]
---
The MacBook is a subject of some controversy in the techie community. Many Linux enthusiasts and hardcore hardware nerds deem its operating system bloated and inflexible, and its hardware low quality for the price. They're probably right, but I own a MacBook, so here is my brief guide to getting the most out of it without hurting your wallet.

I bought my 2017 MacBook Pro a few months before starting my undergrad degree, and it has been my daily driver since. Recently, I began restoring an old laptop with NixOS, focusing on performance and customization, and I realized that I could be getting a _lot_ more out of my MBP. Here's what I use now.

# Package Management

Use [Homebrew](https://brew.sh/){:target="_blank"}. Enough said. If you already use another package manager, then stick to that, obviously (migrating package managers is a nightmare), but if not, use `brew`. It's easy, customizable, and "just works."

# Keyboard Shortcuts

Mac's built-in keyboard shortcuts aren't great, and the System Preferences interface doesn't allow for a great degree of customization. I use [Karabiner Elements](https://karabiner-elements.pqrs.org/){:target="_blank"} to remap Caps Lock to the so-called Hyper key, which is equivalent to pressing `cmd+ctrl+alt+shift`. This keybinding won't conflict with any app-specific or built-in keybindings, so if you want more shortcuts, remapping Caps to Hyper gives you a ton of flexibility. I use it for my window manager shortcuts, as well as my terminal hotkey.

# Terminal

I spend a ton of time in the terminal, using it as a primary point of entry for most of my apps and files, and there are two pieces of customization I could not live without.

First, as a `zsh` user, [oh my zsh](https://ohmyz.sh/){:target="_blank"} is a beautiful combination of `zsh` plugin management and theming. I use the oh my zsh default theme, robbyrussell, and use it to manage all of two plugins. I have barely scratched the surface of customization with oh my zsh, but its built-in aliases, great themes, and simple plugin management make my terminal-bound life significantly more bearable. Whenever I get some free time, I hope to build up an even more elaborate oh my zsh set up.

Second, [iTerm2](https://iterm2.com){:target="_blank"}. The default MacOS terminal emulator sucks: 8 bit color and terrible customization options make for a bland experience. iTerm is the opposite. Full font and color support, and a never-ending rabbithole of customization options (built-in `tmux` manager, `ssh` management, batteries included). My favorite feature, however, is the dedicated hotkey terminal, a permanently-open terminal window available with a keyboard shortcut of your choosing. For me, `Hyper+enter` brings up this window anytime, anywhere.

Finally, if you're going to spend a lot of time in the terminal, install a good font, and configure iTerm to use it. I am partial to the [FiraCode Nerd Font](https://github.com/tonsky/FiraCode){:target="_blank"}. It has ligatures to improve the readability of common programming constructs, like `=>, ==, !=` and just looks really clean. I have it on both VSCode and iTerm, and love it. Use `brew` or your own package manager to install it.

# App Launching

The default Mac app launcher, Spotlight Search, leaves a lot to be desired, and I honestly didn't use it very much. After switching to [Alfred](https://www.alfredapp.com/){:target="_blank"}, a drop-in spotlight replacement, I now use it for everything. There is a "power pack" expansion available for purchase with loads more features, but I mostly use Alfred as an app launcher, which is included, along with file searching and previewing, web search, and calculator, for free! Some of the features included in the power pack are terminal integrations, clipboard and snipped management, and automated workflows (scripting without the AppleScript). But I'm cheap, so I forego these luxeries.

# Window Management

I'll be the first to admit, I'm no window power user (at least, not on my MBP). I use [Rectangle](https://rectangleapp.com/){:target="_blank"} for my window management needs. I use `Hyper+[h|j|k|l]` to move windows to the Vim-respective halves of my screen, and `Hyper+space` for full screen. That's about all I need, but Rectangle has many more shortcuts available: I recommend using `Hyper` for all your Rectangle keybindings.

# Conclusion

Well, that just about wraps it up. This combo of tools probably increased my productivity by about 10%, which doesn't sound like a lot, but that's almost an hour back per work day! I hope this helps any new poweruser-cheapskates like me!
