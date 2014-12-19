# Background

I have used [Vim](http://www.vim.org) for years. I've also used [Eclipse](https://www.eclipse.org) for my Java needs. As I gain more experience as a software engineer, I find that I'm using more and more languages. Since I'm comfortable with Vim and am a huge fan of the command-line, I've looked into turning Vim into a powerful IDE for all the languages I use because I want my IDE to support me being productive. If all I'm doing is Python or Ruby development, then I can probably get by with Vim as my IDE, but I use way more languages than Python and Ruby. I've looked hard and have been frustrated by the lack of plugins and frustrated that the plugins that do exist usually don't work well together. I saw that Emacs is extremely customisable and supports a lot of what I want and has a great framework for making plugins work well together, so I decided to finally make an effort to learn Emacs. I'm glad I've learned Vim, and I'll still use its ugly step-sister Vi (since it comes with a fresh install of most Unix-like operating systems and is better than ed and nano for system administration needs), but for my daily programming needs, I'm switching to Emacs.

At first, my plan was to try to write down everything I normally do in Vim and Eclipse, and then translate those things into Emacs. Then, I realised that Emacs can probably do much more than those things (people do call it an operating system for a reason). That's when I decided to read the entire GNU Emacs manual, which took me a solid two weeks of reading (I'm a slow reader and take notes when I read; I was reading about 5% per day, and more on the weekend (10% per day)). I also spent another week reading some of the other Info manuals.

The problem with a lot of Emacs guides out there is that they seem be copy-and-pasted from each other and really only cover working with plaintext files. Then there are guides out there that only focus on one programming language. Then there's the GNU Emacs manual, which takes weeks to read. Then there's using Emacs on a daily basis and slowly learning as you go for years. The problem with switching IDEs is that you don't want to sacrifice your productivity. This is where my guide comes in. The purpose of the guide is to get you up to speed on typical things that programmers demand from their IDE while also being useful as a reference for jogging your memory for those things. I don't want the guide to be comprehensive. I just want it to get straight to the point for all the important things. Essentially, I want to develop a conceptual framework, from which you (and I) can build on. You may feel overwhelmed by Emacs's steep learning curve, but consider it a worthwhile investment: you're investing your time in something that you'll use for a lifetime.


# History


The GNU Project was created on 27 September 1983 by Richard Stallman (when he was 30 years old) as a project for developing free software (free as in freedom). The main project was the GNU operating system.

GNU Emacs was first released on 20 March 1985 by Richard Stallman (when he was 32 years old). This was the first program released by the GNU Project.

The Free Software Foundation (FSF) was founded on 04 October 1985 by Richard Stallman (when he was 32 years old) as a non-profit organisation for the free software movement. It helps fund the GNU project.

GNU is a recursive acronym for "GNU's Not Unix!", chosen because GNU's design is Unix-like, but contains no Unix code. The name is also inspired by the 1957 song "The Gnu" from the British comedy duo Flanders and Swann. To avoid confusion with the word "new", the G in GNU is pronounced (like "g-noo", using a hard G like in the word "good"), just like the pronunciation in the Flanders and Swann song. Note that the word gnu (pronounced "noo") refers to the southern African animal that is also known as a wildebeest and is part of the antelope family, hence GNU's logo (created by Etienne Suvasa).

Emacs actually refers to a family of text editors; however, when unqualified, it usually refers to GNU Emacs. Emacs editors are known for their extensibility.

Note that GNU Emacs wasn't the first Emacs, but the first Emacs was also written by Richard Stallman. GNU Emacs was initially created as a free software alternative to the proprietary Gosling Emacs (also known as Gosmacs, gmacs, or Unipress Emacs), which was created by James Gosling (the creator of Java) in 1981. Gosling Emacs was owned by UniPress. Gosling Emacs was written in C and Mocklisp (aka MLisp). It was the first Emacs to run on Unix.

The original EMACS was written in 1976 by Richard Stallman (when he was about 23 years old) and Guy L. Steele, Jr. as a set of Editor MACroS for the TECO (Tape Editor and Corrector) editor for the Incompatible Timesharing System (ITS) operating system on the PDP line of computers.

GNU Emacs is written in C and Emacs Lisp (Elisp). LISP 1 was the first implementation of Lisp. LISP 1.5 was the first widely used Lisp implementation. MACLISP appeared in the 1960s; it was developed for MIT's ProjectMAC and was a direct descendent of LISP 1.5. Scheme appeared in 1975 and Common Lisp appeared in 1984. "Richard Stallman chose Lisp as the extension language for his rewrite of Emacs because of its powerful features, including the ability to treat functions as date. Unlike Common Lisp, Scheme existed at the time Stallman was rewriting Gosling Emacs into GNU Emacs, but he chose not to use it because of its comparatively poor performance on workstations, and he wanted to develop a dialect which he thought would be more easily optimized." "In terms of features, Elisp is closely related to the Maclisp dialect, with some later influence from Common Lisp." A scripting language used for scripting an application is called an extension language. Elisp is considered an extension language. Elisp is a scripting language dialect of a general-purpose language.


# Installing [Emacs](https://www.gnu.org/software/emacs/)

At first, I installed Emacs without X support, which meant that I only used Emacs in a terminal. After a lot of reading and after watching experienced users use Emacs, I decided to reinstall Emacs with X support. It's not the most pleasant looking GUI, but I recommend installing with X support (unless you don't have X and don't want it) because then you have the flexibility of starting Emacs in graphical mode (<code>emacs</code>) or in terminal mode (<code>emacs -nw</code>). Also, there are some things you can do in graphical mode that you can't do in terminal mode, and graphical mode provides conveniences like a menu, which is useful when you're completely lost and don't know what you're doing (like when you're a beginner). Graphical mode also has helpful tooltips when you mouseover things. This guide assumes that you didn't install with X support; I'm sure you have experience with a GUI and can figure out GUI-specific stuff on your own (click, click, click, click, click).

I'm using [dwm](http://dwm.suckless.org) on [Gentoo GNU/Linux](http://www.gentoo.org). I installed with the toolkit-scroll-bars and xft USE flags because the Emacs toolbars didn't look very good and without xft support, Emacs displayed some strings (such as the buffer name in the mode line) in hex.

If you really want, you can grab the development version of Emacs from here: https://savannah.gnu.org/projects/emacs/.

An Emacs version number with two components (e.g., 22.1) indicates a released version; three components indicates a development version (e.g., 23.0.50).


# Most Important Things to Know First

The most important things to know first are knowing how to quit, cancel, undo, close, switch and close buffers, and get help, and before you can know that, you need to know how to invoke commands in Emacs.

To invoke a command in Emacs:

1. You can use a key sequence (aka keyboard shortcut, key binding, or key for short).
2. Or you can call the command by name.

## Invoking Commands by Key Sequence

Keys are not commands. Keys are bound to commands. Commands are Emacs Lisp (Elisp) functions.

Simple (printable) characters and control (non-printable) characters, as well as certain non-keyboard inputs such as mouse clicks, are collectively referred to as input events. Some Emacs commands are invoked by just one input event; other commands take two or more input events to invoke. A key sequence is a sequence of one or more input events that is meaningful as a unit. If a key sequence invokes a command, it's called a complete key. If a key sequence isn't long enough to invoke a command, it's called a prefix key. Every key sequence is either a complete key or a prefix key. Prefix keys are combined to form a complete key.

A character is self-inserting if typing that character inserts that character in the buffer. Ordinary printing and whitespace characters are normally self-inserting, except when they're redefined by a major mode. Note that typing a self-inserting character actually invokes an Emacs command called <code>self-insert-command</code>.

A character is electric if in addition to being self-inserting, it also does something else.

C = Control = Ctrl = Ctl<br>
M = Meta = Alt<br>
S = Shift<br>
&lt;RET&gt; = Enter or Return<br>
&lt;SPC&gt; = Space<br>
&lt;DEL&gt; = Backspace<br>
&lt;DELETE&gt; = Delete<br>
&lt;LEFT&gt; = left arrow<br>
&lt;RIGHT&gt; = right arrow<br>
&lt;UP&gt; = up arrow<br>
&lt;DOWN&gt; = down arrow

Ctrl, Alt, and Shift are modifiers. <code>&lt;ESC&gt;</code> is a character, not a modifier.

<code>C-&lt;character&gt;</code> means hold the Ctrl key and then press &lt;character&gt;.

<code>C-&lt;character1&gt; C-&lt;character2&gt;</code> means hold the Ctrl key and then press &lt;character1&gt; and then &lt;character2&gt; (<code>C-&lt;character1&gt;&lt;character2&gt;</code>); or hold the Ctrl key, press &lt;character1&gt;, release both keys, and then hold the Ctrl key and press &lt;character2&gt;.

<code>C-&lt;character1&gt; &lt;character2&gt;</code> means hold the Ctrl key, press &lt;character1&gt;, release both keys, and then press &lt;character2&gt;.

<code>M-&lt;character&gt;</code> means hold the Alt key and then press &lt;character&gt;.

<code>M-&lt;character1&gt; M-&lt;character2&gt;</code> means hold the Alt key and then press &lt;character1&gt; and then &lt;character2&gt; (<code>M-&lt;character1&gt;&lt;character2&gt;</code>); or hold the Alt key, press &lt;character1&gt;, release both keys, and then hold the Alt key and press &lt;character2&gt;.

<code>M-&lt;character1&gt; &lt;character2&gt;</code> means hold the Alt key, press &lt;character1&gt;, release both keys, and then press &lt;character2&gt;.

If <code>C-</code> and <code>M-</code> are both used, it doesn't matter which modifier you hold first: <code>C-M-&lt;character&gt;</code> is the same thing as <code>M-C-&lt;character&gt;</code>.

Wherever you see Alt (i.e., M), you can use &lt;ESC&gt; instead. In that case, press &lt;ESC&gt;, but don't hold it.

Multi-character commands are echoed in the echo area if you pause for more than a second in the middle of a command. Emacs then echoes all the characters of the command so far, to prompt you for the rest. Once echoing has started, the rest of the command echoes immediately as you type it.

What some programs call "assigning a keyboard shortcut", Emacs calls "binding a key sequence."

The bindings of key sequences to commands are stored in data structures called keymaps.


## Invoking Commands by Name

It's very easy to invoke a command by name. Just type <code>M-x</code>, followed by the command name, followed by <code>&lt;RET&gt;</code>.

If you invoke a command by name, but it can also be invoked by a key sequence, then Emacs will use the echo area to tell you what key sequence you can use next time you want to invoke the command. If the message disappears too quickly, you can type <code>C-h e</code> to view a log of the echo area messages.

For commands that you don't use often, it's probably easier to remember the command by name rather than by key.

Not all commands are bound to keys.


## Useful Commands to Memorise

<dl>
  <dt><dfn>
C-x C-x<br>
M-x save-buffers-kill-terminal</dfn></dt>
  <dd>Quit Emacs.</dd>

  <dt><dfn>
C-g<br>
&lt;ESC&gt;&lt;ESC&gt;&lt;ESC&gt;</dfn></dt>
  <dd>
<p>Cancel something.</p>

<p><code>C-g</code> and <code>&lt;ESC&gt;&lt;ESC&gt;&lt;ESC&gt;</code> are similar, but not exactly.</p>

<p><code>C-g</code> doesn't invoke a command (instead, it sets a variable that Emacs frequently checks), so it can be used to stop commands. If <code>C-g</code> invoked a command, then Emacs wouldn't execute it until the previous command finished executing. The downside to <code>C-g</code> is that it doesn't cancel a key sequence because it's interpreted as part of the key sequence.</p>

<p><code>&lt;ESC&gt;&lt;ESC&gt;&lt;ESC&gt;</code> can't stop commands because it invokes a command, which wouldn't be executed until the previous command finished executing. The good thing is that <code>&lt;ESC&gt;&lt;ESC&gt;&lt;ESC&gt;</code> works in most other situations. The annoying thing is that you have to type <code>&lt;ESC&gt;</code> exactly 3 times.</p>
  </dd>

  <dt><dfn>
C-/<br>
C-x u<br>
C-_<br>
M-x undo<br>
M-x undo-only</dfn></dt>
  <dd>
<p>Undo one thing.</p>

<p><code>C-/</code>, <code>C-x u</code>, and <code>C-_</code> all do the exact same thing (<code>C-x u</code> and <code>C-_</code> are aliases for <code>C-/</code>). According to the Emacs manual, <code>C-x u</code> was created as an alias for beginners, since it's easier to remember ('u' stands for "undo"). It's also bound to <code>C-_</code> because typing <code>C-/</code> on some text terminals actually enters <code>C-_</code>.</p>

<p>If you keep invoking the undo command, then you'll keep undoing earlier and earlier changes. To quote the Emacs manual "Any command other than an undo command breaks the sequence of undo commands. Starting from that moment, the entire sequence of undo commands that you have just performed are themselves placed into the undo record, as a single set of changes. Therefore, to re-apply changes you have undone, type <code>C-f</code> or any other command that harmlessly breaks the sequence of undiong; then type <code>C-/</code> to undo the undo command[, thus performing a redo]. If you want to resume undoing, without redoing previous undo commands, use <code>M-x undo-only</code>. This is like <code>undo</code>, but will not redo changes you have just undone."</p>

<p>The undo command applies only to changes in the buffer; you can't use it to undo cursor motion.</p>

<p>Note that you can select a region and undo only the changes within that region. That is called a "selective undo".</p>
  </dd>

  <dt><dfn>M-x revert-buffer</dfn></dt>
  <dd>
<p>Undo all changes in the current buffer.</p>

<p>Rather than doing this, you could also just quit Emacs without saving your changes.</p>
  </dd>
</dl>


# What You See on the Screen

Emacs occupies a frame. A frame refers to either a graphical window (if you're using Emacs in graphical mode) or to a terminal screen (if you're using Emacs in terminal mode). Emacs can use more than one frame, but in terminal mode, you can only see one frame at a time.

Each frame consists of several distinct regions:

* An Emacs frame has an internal border and an external border. The internal border is an extra strip around the text portion of the frame. Emacs itself draws the internal border. The external border is added by your window manager outside the frame. The internal border is 1 pixel wide by default.
* Each frame has a title.
* At the very top of a frame is a menu bar.
* In graphical mode, a tool bar appears right below the menu bar.
* At the very bottom of a frame is an echo area, which is used for showing brief messages.
* Between the menu bar and the echo area is where one or more windows are displayed.
* Each window displays the contents of a buffer.
* A buffer typically contains the contents of a file, but buffers aren't limited to just that use case.
* Each buffer has a name.
* At the very bottom of a window is a mode line, which provides information about the window's buffer.
* Fringes are the narrow strips that appear on the left and right of a window. They are used for displaying symbols that provide information about the buffer text. Fringes are not the same thing as borders.
* A margin is the space between the usable part of a window (including the fringe) and the window edge.
* Blank lines are lines that contain only whitespace (newlines, spaces, and/or tabs).
* The current line is the line that point is on.
* A logical line refers to text that is terminated by a newline (or the end of the file).
* A screen line refers to one row of text that you see on your screen.
* When a logical line is so long that it's displayed as two or more screen lines, this is called line wrapping or line continuation. The long logical line is called a continued line. All screen lines after the first are called continuation lines.

