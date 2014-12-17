I have used [Vim](http://www.vim.org) for years. I've also used [Eclipse](https://www.eclipse.org) for my Java needs. As I gain more experience as a software engineer, I find that I'm using more and more languages. Since I'm comfortable with Vim and am a huge fan of the command-line, I've looked into turning Vim into a powerful IDE for all the languages I use because I want my IDE to support me being productive. If all I'm doing is Python or Ruby development, then I can probably get by with Vim as my IDE, but I use way more languages than Python and Ruby. I've looked hard and have been frustrated by the lack of plugins and frustrated that the plugins that do exist usually don't work well together. I saw that Emacs is extremely customisable and supports a lot of what I want and has a great framework for making plugins work well together, so I decided to finally make an effort to learn Emacs. I'm glad I've learned Vim, and I'll still use its ugly step-sister Vi (since it comes with a fresh install of most Unix-like operating systems and is better than ed and nano for system administration needs), but for my daily programming needs, I'm switching to Emacs.

At first, my plan was to try to write down everything I normally do in Vim and Eclipse, and then translate those things into Emacs. Then, I realised that Emacs can probably do much more than those things (people do call it an operating system for a reason). That's when I decided to read the entire GNU Emacs manual, which took me a solid two weeks of reading (I'm a slow reader and take notes when I read; I was reading about 5% per day, and more on the weekend (10% per day)). I also spent another week reading some of the other Info manuals.

The problem with a lot of Emacs guides out there is that they seem be copy-and-pasted from each other and really only cover working with plaintext files. Then there are guides out there that only focus on one programming language. Then there's the GNU Emacs manual, which takes weeks to read. Then there's using Emacs on a daily basis and slowly learning as you go for years. The problem with switching IDEs is that you don't want to sacrifice your productivity. This is where my guide comes in. The purpose of the guide is to get you up to speed on typical things that programmers demand from their IDE while also being useful as a reference for jogging your memory for those things. I don't want the guide to be comprehensive. I just want it to get straight to the point for all the important things. Essentially, I want to develop a conceptual framework, from which you (and I) can build on. You may feel overwhelmed by Emacs's steep learning curve, but consider it a worthwhile investment: you're investing your time in something that you'll use for a lifetime.


# Installing [Emacs](https://www.gnu.org/software/emacs/)

At first, I installed Emacs without X support, which meant that I only used Emacs in a terminal. After a lot of reading and after watching experienced users use Emacs, I decided to reinstall Emacs with X support. It's not the most pleasant looking GUI, but I recommend installing with X support (unless you don't have X and don't want it) because then you have the flexibility of starting Emacs in graphical mode (`emacs`) or in terminal mode (`emacs -nw`). Also, there are some things you can do in graphical mode that you can't do in terminal mode, and graphical mode provides conveniences like a menu, which is useful when you're completely lost and don't know what you're doing (like when you're a beginner). Graphical mode also has helpful tooltips when you mouseover things. This guide assumes that you didn't install with X support; I'm sure you have experience with a GUI and can figure out GUI-specific stuff on your own (click, click, click, click, click).

I'm using [dwm](http://dwm.suckless.org) on [Gentoo GNU/Linux](http://www.gentoo.org). I installed with the toolkit-scroll-bars and xft USE flags because the Emacs toolbars didn't look very good and without xft support, Emacs displayed some strings (such as the buffer name in the mode line) in hex.


# Most Important Things to Know First

The most important things to know first are knowing how to quit, cancel, undo, close, and get help, and before you can know that, you need to know how to invoke commands in Emacs.

TODO: keys (for example, <DEL>, <TAB>, etc.).
TODO: how to invoke commands.
TODO: prefix args.

<dl>
  <dt><dfn>C-x C-x</dfn></dt>
  <dt><dfn>M-x save-buffers-kill-terminal</dfn></dt>
  <dd>Quit Emacs.</dd>

  <dt><dfn>C-g</dfn></dt>
  <dt><dfn>&lt;ESC&gt;&lt;ESC&gt;&lt;ESC&gt;</dfn></dt>
  <dd>Cancel something.
    <p>`C-g` and `&lt;ESC&gt;&lt;ESC&gt;&lt;ESC&gt;` are similar, but not exactly.</p>
    <p>`C-g` doesn't execute a command (instead, it sets a variable that Emacs frequently checks, and then acts accordingly), so it can be used to stop commands. If `C-g` executed a command, then Emacs wouldn't notice it until the previous command finished. The downside to `C-g` is that it doesn't cancel a key sequence because it's interpreted as part of the key sequence.</p>
    <p>`&lt;ESC&gt;&lt;ESC&gt;&lt;ESC&gt;` can't stop commands because it invokes a command (which wouldn't be executed until the previous command finished). The good thing is that `&lt;ESC&gt;&lt;ESC&gt;&lt;ESC&gt;` works in most other situations. The annoying thing is that you have to type `&lt;ESC&gt;` exactly 3 times.</p>
  </dd>

  <dt><dfn>C-/</dfn></dt>
  <dt><dfn>C-x u</dfn></dt>
  <dt><dfn>C-_</dfn></dt>
  <dt><dfn>M-x undo</dfn></dt>
  <dt><dfn>M-x undo-only</dfn></dt>
  <dd>Undo one thing.
    <p>`C-/`, `C-x u`, and `C-_` all do the exact same thing (`C-x u` and `C-_` are aliases for `C-/`). According to the Emacs manual, `C-x u` was created as an alias for beginners, since it's easier to remember ('u' stands for "undo"). It's also bound to `C-_` because typing `C-/` on some text terminals actually enters `C-_`.</p>
    <p>If you keep invoking the undo command, then you'll keep undoing earlier and earlier changes. To quote the Emacs manual "Any command other than an undo command breaks the sequence of undo commands. Starting from that moment, the entire sequence of undo commands that you have just performed are themselves placed into the undo record, as a single set of changes. Therefore, to re-apply changes you have undone, type `C-f` or any other command that harmlessly breaks the sequence of undiong; then type `C-/` to undo the undo command[, thus performing a redo]. If you want to resume undoing, without redoing previous undo commands, use `M-x undo-only`. This is like `undo`, but will not redo changes you have just undone."</p>
    <p>Note that you can select a region and undo only the changes within that region. This is called a "selective undo".</p>
  </dd>

  <dt><dfn>M-x revert-buffer</dfn></dt>
  <dd>Undo all changes in the current buffer. Rather than doing this, you could also just quit Emacs without saving your changes.</dd>
</dl>

TODO: how to get help.
