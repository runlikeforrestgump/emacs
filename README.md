# Background

I have used [Vim](http://www.vim.org) for years. I've also used [Eclipse](https://www.eclipse.org) for my Java needs. As I gain more experience as a software engineer, I find that I'm using more and more languages. Since I'm comfortable with Vim and am a huge fan of the command-line, I've looked into turning Vim into a powerful IDE for all the languages I use because I want my IDE to support me being productive. If all I'm doing is Python or Ruby development, then I can probably get by with Vim as my IDE, but I use way more languages than Python and Ruby. I've looked hard and have been frustrated by the lack of plugins and frustrated that the plugins that do exist usually don't work well together. I saw that Emacs is extremely customisable and supports a lot of what I want and has a great framework for making plugins work well together, so I decided to finally make an effort to learn Emacs. I'm glad I've learned Vim, and I'll still use its ugly step-sister Vi (since it comes with a fresh install of most Unix-like operating systems and is better than ed and nano for system administration needs), but for my daily programming needs, I'm switching to Emacs.

At first, my plan was to try to write down everything I normally do in Vim and Eclipse, and then translate those things into Emacs. Then, I realised that Emacs can probably do much more than those things (people do call it an operating system for a reason). That's when I decided to read the entire GNU Emacs manual, which took me a solid two weeks of reading (I'm a slow reader and take notes when I read; I was reading about 5% per day, and more on the weekend (10% per day)). I also spent another week reading some of the other Info manuals.

The problem with a lot of Emacs guides out there is that they seem to be copy-and-pasted from each other (I think this applies to a lot of guides in general) and really only cover working with plaintext files. Then there are guides out there that only focus on one programming language. Then there's the GNU Emacs manual, which takes weeks to read. Then there's using Emacs on a daily basis and slowly learning as you go for years. The problem with switching IDEs is that you don't want to sacrifice your productivity. This is where my guide comes in. The purpose of the guide is to get you up to speed on typical things that programmers demand from their IDE while also being useful as a reference for jogging your memory for those things. I don't want the guide to be comprehensive. I just want it to get straight to the point for all the important things. Essentially, I want to develop a conceptual framework, from which you (and I) can build on. You may feel overwhelmed by Emacs's steep learning curve, but consider it a worthwhile investment: you're investing your time in something that you'll use for a lifetime.


# History

The GNU Project was created on 27 September 1983 by Richard Stallman (when he was 30 years old) as a project for developing free software (free as in freedom). The main project was the GNU operating system.

GNU Emacs was first released on 20 March 1985 by Richard Stallman (when he was 32 years old). This was the first program released by the GNU Project.

The Free Software Foundation (FSF) was founded on 04 October 1985 by Richard Stallman (when he was 32 years old) as a non-profit organisation for the free software movement. It helps fund the GNU project.

GNU is a recursive acronym for "GNU's Not Unix!", chosen because GNU (the operating system)'s design is Unix-like, but contains no Unix code. The name is also inspired by the 1957 song "The Gnu" from the British comedy duo Flanders and Swann. To avoid confusion with the word "new", the G in GNU is pronounced (like "g-noo", using a hard G like in the word "good"), just like the pronunciation in the Flanders and Swann song. Note that the word gnu (pronounced "noo") refers to the southern African animal that is also known as a wildebeest and is part of the antelope family, hence GNU's logo (created by Etienne Suvasa).

Emacs actually refers to a family of text editors; however, when unqualified, it usually refers to GNU Emacs. Emacs editors are known for their extensibility. A typical Emacs implementation has a small, solid core written in one language (such as C) and often uses some dialect of Lisp for extensibility.

Note that GNU Emacs wasn't the first Emacs, but the first Emacs was also written by Richard Stallman. GNU Emacs was initially created as a free software alternative to the proprietary Gosling Emacs (also known as Gosmacs, gmacs, or UniPress Emacs), which was created by James Gosling (the creator of Java) in 1981. Gosling Emacs was owned by UniPress. Gosling Emacs was written in C and Mocklisp (aka MLisp). It was the first Emacs to run on Unix.

The original EMACS was written in 1976 by Richard Stallman (when he was about 23 years old) and Guy L. Steele, Jr. as a set of **E**ditor **MAC**ro**S** for the TECO (Tape Editor and Corrector) editor for the Incompatible Timesharing System (ITS) operating system on the PDP line of computers in use at MIT at the time.

GNU Emacs is written in C and Emacs Lisp (Elisp). LISP 1 was the first implementation of Lisp. LISP 1.5 was the first widely used Lisp implementation. MACLISP appeared in the 1960s; it was developed for MIT's ProjectMAC and was a direct descendent of LISP 1.5. Scheme (influenced by LISP 1.5 and MACLISP) appeared in 1975 and Common Lisp appeared in 1984. "Richard Stallman chose Lisp as the extension language for his rewrite of Emacs because of its powerful features, including the ability to treat functions as data. Unlike Common Lisp, Scheme existed at the time Stallman was rewriting Gosling Emacs into GNU Emacs, but he chose not to use it because of its comparatively poor performance on workstations, and he wanted to develop a dialect which he thought would be more easily optimized." "In terms of features, Elisp is closely related to the Maclisp dialect, with some later influence from Common Lisp." A scripting language used for scripting an application is called an extension language. Elisp is considered an extension language. Elisp is a scripting language dialect of a general-purpose language.


# Installing [Emacs](https://www.gnu.org/software/emacs/)

At first, I installed Emacs without X support, which meant that I only used Emacs in a terminal. After a lot of reading and after watching experienced users use Emacs, I decided to reinstall Emacs with X support. It's not the most pleasant looking GUI (at least on Linux), but I recommend installing with X support (unless you don't have X and don't want it) because then you have the flexibility of starting Emacs in graphical mode (<code>emacs</code>) or in terminal mode (<code>emacs -nw</code>). Also, there are some things you can do in graphical mode that you can't do in terminal mode, and graphical mode provides conveniences like a menu, which is useful when you're completely lost and don't know what you're doing (like when you're a beginner). Graphical mode also has helpful tooltips when you mouseover things. This guide assumes that you didn't install with X support; I'm sure you have experience with a GUI and can figure out GUI-specific stuff on your own (click, click, click, click, click).

I'm using [dwm](http://dwm.suckless.org) on [Gentoo GNU/Linux](http://www.gentoo.org). I installed with the toolkit-scroll-bars and xft USE flags because the Emacs toolbars didn't look very good and without xft support, Emacs displayed some strings (such as the buffer name in the mode line) in hex.

If you really want, you can grab the development version of Emacs from here: https://savannah.gnu.org/projects/emacs/.

An Emacs version number with two components (e.g., 22.1) indicates a released version; three components indicates a development version (e.g., 23.0.50).


# Most Important Things to Know First

The most important things to know first are knowing how to quit, cancel, undo, close, switch and close buffers, and get help, and before you can know that, you need to know how to invoke commands in Emacs.

To invoke a command in Emacs:

1. You can use a key sequence (aka keyboard shortcut, key binding, or key for short).
2. Or you can call the command by name.

Some commands are (or can be) disabled, which means that you'll be asked for confirmation when you try to invoke them.


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

Typing the help character (<code>C-h</code> or <code>&lt;F1&gt;</code>) after a prefix key displays a list of the commands starting with that prefix. For commands starting with &lt;ESC&gt;, you can use &lt;F1&gt; for help, but not C-h.


## Invoking Commands by Name

It's very easy to invoke a command by name. Just type <code>M-x</code>, followed by the command name, followed by <code>&lt;RET&gt;</code>.

If you invoke a command by name that could also have been invoked by a key sequence, then Emacs will use the echo area to tell you what key sequence you can use next time you want to invoke the command. If the message disappears too quickly, you can type <code>C-h e</code> to view a log of the echo area messages.

For commands that you don't use often, it's probably easier to remember the command by name rather than by key.

Not all commands are bound to keys.


## Numeric Arguments (aka Prefix Arguments)

A numeric argument (aka prefix argument) is a number (positive or negative), specified before a command, to change the effect of the command. You can give any Emacs command a numeric argument. Some commands interpret the argument as a repetition count; some commands change their behaviour based on the numeric argument; some commands care whether there is an argument, but ignore its value; some commands treat a plain <code>C-u</code> (a C-u followed by no digits or minus sign) differently from an ordinary argument; some commands treat 0 specially if the numeric argument is treated as a repetition count (because a repetition count of 0 would otherwise be a no-op).

The term "prefix argument" ephasises the fact that the argument is specified before the command. "Prefix argument" is a synonym for "numeric argument."

To specify a numeric argument, you can type a digit and/or a minus sign while holding down the Alt key, followed by the command you want to invoke (you can invoke by key sequence or name). If you enter more than one digit, you don't need to hold down the Alt key for the second and subsequent digits. Numeric arguments are bound to either digit-argument (for positive numbers) or negative-argument (for negative numbers). For example, if you want to move down 25 lines, you could do <code>M-2 5 C-n</code> or <code>M-2 5 M-x next-line</code>.

Another way to specify a numeric argument is to type <code>C-u</code> (bound to the universal-argument command) followed by one or more digits, or (for a negative argument) a minus sign followed by one or more digits. C-u alone has the special meaning of "four times": it multiplies the argument for the next command by four; <code>C-u C-u</code> multiplies it by sixteen (4 * 4); and so on.

If you use a numeric argument with M-x, then the argument value will appear in the prompt string.

A minus sign without digits normally means -1.

You can use a numeric argument before a self-inserting character to insert multiple copies of it. If the character is a number, then you need to use <code>C-u</code> to terminate the prefix argument before typing the digit; for example, to append 6 zeros to your paycheque, you can do: <code>M-6 C-u 0</code> or <code>C-u 6 C-u 0</code>.

If you want to repeat a command that prompts for input or repeat a command that doesn't treat a numeric argument as a repetition count, then you need to use the command <code>C-x z</code> (<code>M-x repeat</code>). Repeating a command uses the same arguments that were used before; it does not read new arguments each time. To repeat the command more than once, type additional 'z''s: each 'z' repeats the command one more time. Repetition ends when you type a character other than 'z', or press a mouse button.


## Quoting

Only graphic characters can be inserted by typing the associated key; other keys act as editing commands and do not insert themselves. Quoting means depriving a character of its usual special significance.

To insert a non-graphic character, type <code>C-q</code> and then the character.

<code>C-q</code> (<code>M-x quoted-insert</code>) followed by a sequence of octal digits inserts the character with the specified octal character code. You can use any number of octal digits; any non-digit terminates the octal sequence. To use decimal or hexadecimal instead of octal, set the variable *read-quoted-char-radix* to 10 or 16. If the radix is 16, the letters 'a' to 'f' serve as part of the character code, just like digits. Case is ignored.


## Inserting Non-ASCII Characters

<code>C-x 8</code> (<code>M-x insert-char</code>) prompts for the Unicode name or codepoint of a character. The codepoint can be specified in hexadecimal, octal, binary, or any other radix between 2 and 36. The syntax in Emacs for inserting non-decimal numbers is to insert a '#'; followed by either a 'b' for binary, 'o' for octal, 'x' for hex, or '<num>r' for anything else; followed by the digits written in the specified radix. Case is not significant for the letter that specifies the radix.

An input method is a system for entering non-ASCII text characters by typing sequences of ASCII characters; for example, typing pinyin (romanised Chinese) to enter Chinese characters. I haven't used an input method in Emacs before, so won't go into detail, but here's how you can get started:

<dl>
  <dt><dfn>M-x list-input-methods</dfn></dt>
  <dd>Display a list of all the supported input methods.</dd>

  <dt><dfn>
  C-h I METHOD &lt;RET&gt;<br>
  C-h C-\ METHOD &lt;RET&gt;<br>
  M-x describe-input-method &lt;RET&gt; METHOD</dfn></dt>
  <dd>Describe how to use input method METHOD.</dd>

  <dt><dfn>
  C-x &lt;RET&gt; C-\ METHOD &lt;RET&gt;<br>
  M-x set-input-method &lt;RET&gt; METHOD</dfn></dt>
  <dd>Use input method METHOD for the current buffer.</dd>
</dl>


## Useful Commands to Memorise

<dl>
  <dt><dfn>
C-x C-c<br>
M-x save-buffers-kill-terminal</dfn></dt>
  <dd>Quit Emacs.</dd>

  <dt><dfn>
C-g<br>
&lt;ESC&gt;&lt;ESC&gt;&lt;ESC&gt;</dfn></dt>
  <dd>
<p>Cancel something.</p>

<p>Quitting means cancelling a partially typed command or a running command. Quitting Emacs is called killing it.</p>

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


# Getting Help

First of all, if something in this guide is unclear and confusing, then please let me know. This guide is not meant to be comprehensive (it's meant to be a starting point for typical daily usage of a programmer who works with more than one programming language), but it's not meant to be confusing.

The Emacs manual (and other Emacs-related manuals) can be read online: https://www.gnu.org/software/emacs/manual/. All those manuals also ship with Emacs, so they can be read in Emacs offline. If you want to support the FSF, you can purchase documentation from http://shop.fsf.org, where you can also buy a mug that has a reference card printed on it.

<dl>
  <dt><dfn>
  C-h r<br>
  &lt;F1&gt; r<br>
  M-x info-emacs-manual</dfn></dt>
  <dd>Display the Emacs manual.</dd>

  <dt><dfn>
  C-h t<br>
  &lt;F1&gt; t<br>
  M-x help-with-tutorial</dfn></dt>
  <dd>Start the Emacs learn-by-doing tutorial.</dd>

  <dt><dfn>
  C-h i h<br>
  &lt;F1&gt; i h<br>
  M-x info-help</dfn></dt>
  <dd>Start the GNU Info learn-by-doing tutorial.</dd>

  <dt><dfn>
  C-h C-f<br>
  &lt;F1&gt; C-f<br>
  M-x view-emacs-FAQ</dfn></dt>
  <dd>Display the Emacs FAQ.</dd>

  <dt><dfn>
  C-h i d m Emacs Lisp Intro &lt;RET&gt; g * &lt;RET&gt;<br>
  &lt;F1&gt; i d m Emacs Lisp Intro &lt;RET&gt; g * &lt;RET&gt;<br>
  M-x info &lt;RET&gt; d m Emacs Lisp Intro &lt;RET&gt; g * &lt;RET&gt;<br>
  M-x menu-bar-read-lispintro</dfn></dt>
  <dd>Display the Emacs Lisp intro.</dd>

  <dt><dfn>
  C-h i d m Elisp &lt;RET&gt; g * &lt;RET&gt;<br>
  &lt;F1&gt; i d m Elisp &lt;RET&gt; g * &lt;RET&gt;<br>
  M-x info &lt;RET&gt; d m &lt;RET&gt; g * &lt;RET&gt;<br>
  M-x menu-bar-read-lispref</dfn></dt>
  <dd>Display the Emacs Lisp reference manual.</dd>

  <dt><dfn>
  C-h a PATTERN<br>
  &lt;F1&gt; a PATTERN<br>
  M-x apropos-command &lt;RET&gt; PATTERN</dfn></dt>
  <dd>TODO</dd>
</dl>

A list of Emacs mailing lists is available here: https://savannah.gnu.org/mail/?group=emacs (help-gnu-emacs@gnu.org or help-emacs-windows@gnu.org are probably the ones you want (if you're looking for help)). You can search the mailing lists at https://lists.gnu.org/archive/html/help-gnu-emacs/ or https://lists.gnu.org/archive/html/help-emacs-windows/.

Some people and companies offer support services and training for Emacs for free or for a fee; you can find a list of them here: https://www.fsf.org/resources/service/. Richard Stallman is even on the list, so I guess you can get help from the inventor himself, which is really cool.

The official Emacs IRC channel is #emacs on freenode, since the GNU Project made freenode its official IRC network in 2002. If you have a question regarding [EmacsWiki](http://www.emacswiki.org), there's a freenode channel for it: #emacswiki.

Emacs comes with reference cards (cheat sheets) in TeX and PDF format. On my machine, they're located in /usr/share/emacs/*/etc/refcards. "refcard" is the name of the file you probably want, but there are other reference cards that are more mode-specific and may also be of interest to you.


## Using GNU Info


# What You See on the Screen

Emacs occupies a frame. A frame refers to either a graphical window (if you're using Emacs in graphical mode) or to a terminal screen (if you're using Emacs in terminal mode). Emacs can use more than one frame, but in terminal mode, you can only see one frame at a time. Each frame has a title.

Each frame consists of several distinct regions:

* An Emacs frame has an **internal border** and an **external border**. The internal border is an extra strip around the text portion of the frame. Emacs itself draws the internal border. The external border is added by your window manager outside the frame. The internal border is 1 pixel wide by default.
* At the very top of a frame is a **menu bar**.
* In graphical mode, a **tool bar** appears right below the menu bar.
* At the very bottom of a frame is an **echo area**, which is used for showing brief messages.
* When the echo area is used for input, it's called the **minibuffer**.
* A **prompt** is text used to ask you for input. Displaying a prompt is called prompting. Emacs prompts always appear in the echo area. One kind of prompting happens when the minibuffer is used to read an argument; the echoing that happens when you pause in the middle of typing a multi-character key sequence is also a kind of prompting.
* Between the menu bar and the echo area is where one or more **window**s are displayed.
* Each window displays the contents of a **buffer**. A buffer typically contains the contents of a file, but buffers aren't limited to just that use case. Each buffer has a name.
* You can limit what text you see in the buffer, making the rest of the text in the buffer temporarily inaccessible and invisible (however, it's still there and you can still save it). This is called **narrowing**. You can think of it as zooming in on something, so that you can focus your attention without distraction (or for easily applying changes to that portion of text). The opposite of narrowing is called **widening**. When narrowed, the text that is still accessible is called the **accessible portion**; the bounds of the narrowed region are called its **restriction**.
* Each window has a **scrollbar**. The echo area and minibuffer also have a scrollbar.
* At the very bottom of each window is a **mode line**, which provides information about the window's buffer.
* **Fringes** are the narrow strips that appear on the left and right of a window. They are used for displaying symbols that provide information about the buffer text. Fringes are not the same thing as borders.
* A **margin** is the space between the usable part of a window (including the fringe) and the window edge.
* A **row** is a horizontal line of text.
* A **column** is a vertical line of text.
* **Blank lines** are lines that contain only whitespace (newlines, spaces, and/or tabs).
* The **current line** is the line that point is on. This type of concept applies to anything: "the current SOMETHING is the SOMETHING that point is in or on".
* A **logical line** refers to text that is terminated by a newline (or the end of the file).
* When a logical line is so long that it's displayed as two or more screen lines, this is called line wrapping or line continuation. The long logical line is called a **continued line**. All screen lines after the first are called **continuation lines**.
* When a logical line is so long that it would be displayed as two or more screen lines but instead it's truncated, it's called a **truncated line**.
* A **screen line** refers to one row of text that you see on your screen.
* A **screenful** is one window's worth of visible text.
* By default, the **cursor** in the selected window is a solid block that appears to be on a character. The cursor shows on the screen where point is located in the text. Cursor and point are not the same thing. You can think of point as the left edge of the cursor. Some characters (such as tabs) are extra wide; when the cursor is positioned over such a character, it normally stretches over the width of the wide character.
* **Point** is the place in the buffer at which insertion and deletion occur. Point is considered to be between two characters, not at or on one character. The cursor indicates the location of point.
* Before point means the character before the cursor.
* After point means the character under the cursor.
* **Mark** points to a position in the text. It specifies one end of the region, point being the other end.
* The **region** is the text between point and the mark. When the region is active, it's highlighted.
* The **empty region** is when mark and point refer to the same spot.
* A **rectangle** consists of the text in a given range of columns on a given range of lines. It's a type of region.
* The **empty rectangle** is when point and mark are in the same column. If they are in the same line, then the rectangle is one line high.
* **Active text** refers to text that does something special in response to mouse clicks or <RET>. You can move your point over the active text, and then type <code>C-h .</code> to display some help text for it in the echo area.
* Sometimes you'll see **hyperlinks**, which you can follow by clicking with your mouse or by moving point over the link and then pressing &lt;RET&gt;.
* **Tooltips** (**balloon help**) are small windows that display text information at the current mouse position. They activate when there is a pause in mouse movement over some significant piece of text in a window, or the mode line, or some other part of the Emacs frame such as a tool bar button or menu item.
* A **page** is a unit of text, delimited by formfeed characters (ASCII control-L: ^L) at the beginning of a line. Traditionally, when printing to hardcopy, each formfeed character forces a page break.
* **Whitespace** refers to any character or series of characters that represent horizontal or vertical space. Whitespace characters are typically spaces, tabs, and newlines; however, the Unicode Character Database defines more whitespace characters than that. The term whitespace is based on the resulting appearance when a hardcopy is printed on ordinary paper, which is usually white.
* Emacs defines certain column numbers (multiples of 8 by default) to be **tab stops**. These are used as stopping points by &lt;TAB&gt; when inserting whitespace.
* **Indentation** refers to the whitespace added to the beginning of a line to indicate the structure of the text.
* **Faces** refer to styles of displaying text or even the cursor. Faces have attributes such as font, height, weight, slant, and colour.
* A **fontset** is a named collection of fonts. A font typically defines shapes for a single alphabet or script; therefore, displaying the entire range of scripts that Emacs supports requires a collection of many fonts, hence the use for fontsets.
* The **speedbar** is a special tall frame for conveniently navigating in or operating on another frame. When the speedbar exists, it's always associated with a specific frame, called its **attached frame**; all speedbar operations act on that frame.

My attempt at an ASCII art Emacs frame (looks kind of like a polaroid):

```
+-----------------------------------------------------+
| menu bar                                            |
+-----------------------------------------------------+
| tool bar                                            |
+-----------------------------------------------------+
| |f|                                               |f|
| |r|                                               |r|
| |i|                                               |i|
| |n|                                               |n|
| |g|                                               |g|
| |e|                                               |e|
| | |                                               | |
|s| |                                               | |
|c| |                window / buffer                | |
|r| |                                               | |
|o| |                                               | |
|l| |                                               | |
|l| |                                               | |
| | |                                               | |
|b| |                                               | |
|a| |                                               | |
|r| |                                               | |
+-----------------------------------------------------+
| mode line                                           |
+-----------------------------------------------------+
| | echo area / minibuffer                            |
+-----------------------------------------------------+
```
