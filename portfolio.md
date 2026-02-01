## Involvement with open source software

<!-- During the university studies, just after learning about Unix, I started to use Unixware (in a family
start-up business, early 1995). Soon after, I heard from a classmate the word Linux (1995), so I
installed Slackware, and started to base all work on that.

Both for my thesis and for the work, I learned Emacs, Tex, Postgres. Later I consciously focused on
tools around Scheme language (Sawfish window manager, Scheme Shell, emacs extensions).
-->
In years 2003-2006 I fixed some bugs, and came up with new features:


##  Sawfish window manager (X11)
* 2003 spontaneous repeated keyboard events (during sync grab)
https://www.mail-archive.com/xfree86@xfree86.org/msg04354.html
* 2004 fixes of Sawfish Window manager & improvements https://mail.gnome.org/archives/sawfish-list/2005-February/msg00010.html
* use an algorithm for restacking windows with minimum requests --  O(nd)-difference algorithm
https://mail.gnome.org/archives/sawfish-list/2004-September/msg00022.html
* I released a custom sawfish with all my improvements:
https://mail.gnome.org/archives/sawfish-list/2004-December/msg00015.html
* many parts were later included in the official release
https://sawfish.fandom.com/wiki/2012_06_26:_Sawfish_1.9.0
* 2005 more sawfish bugs
https://mail.gnome.org/archives/sawfish-list/2005-February/msg00010.html

## Tools to handle scanned documents
* djvulibre threading bugfix: https://sourceforge.net/p/djvu/mailman/message/3231672/
* Gimp bugfix https://bugzilla.gnome.org/show_bug.cgi?id=304814


* procps/top: crash on resize fixed
https://gitlab.com/procps-ng/procps/-/commit/73030f7346f450c8666c52ad1da8cc5e49657abe

## Keyboard driver
At this point I had a good understanding of key-event processing, and got an idea for an original
feature, which required precise timestamps. But no effort was done to have it upstreamed.
https://maruska7.blogspot.com/2014/08/forking-multitouch-on-keyboard.html


* 2005 keyboard-event-handling plugin announced
https://www.mail-archive.com/devel@xfree86.org/msg07273.html

* linux kernel -- evdev timestamping
https://lore.kernel.org/lkml/m2ekayaban.fsf@linux11.maruska.tin.it/
https://lore.kernel.org/lkml/m2slveyflp.fsf@linux11.maruska.tin.it/

* Ongoing maintenance/development for Xorg, libkeyboard/Wetson, and Windows 10 here:
https://github.com/MichalMaruska/fork-plugin/



## Flickering & glyph-matrix display
* reduce flickering in Emacs (X11, by using background NONE)
https://lists.gnu.org/archive/html/emacs-devel/2005-11/msg01164.html

* use Heckel's diff algorithm to detect scrolling and implement smooth scrolling in rxvt

* 2006 more bugs reported in X server:
https://www.spinics.net/lists//xfree86-devel/msg00247.html


## Git tools
In 2011 I created a tool to keep several, intra-dependent improvements of certain open-source
projects, rebase these when needed, use git-build-package to produce debian packages, and
extended apt to make me aware when I need to rebase & build my modified components, to keep
my SID debian systems up-to-date, including my modifications.
https://maruska7.blogspot.com/2017/09/keeping-up-with-debian-sid.html
https://maruska7.blogspot.com/2021/03/on-proof-of-concept-based-on-my-git.html
I made no further attempts to upstream my modifications.

This has been rewritten in [GoLang](https://github.com/MichalMaruska/git-hierarchy-go)
and [Rust](https://github.com/MichalMaruska/git-hierarchy-rust), based on libgit2.

