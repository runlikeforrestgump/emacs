# Legal Stuff

You do **not** have permission to make any money off of this document or any version of it (either in its entirety or in parts) or claim any credit for this document or any version of it (either in its entirety or in parts).

You do have permission to share this document, as long as you keep this legal section as is and intact with the copies you share and as long as you honour this legal section.

If you have a copy of the document, you can find the original document at https://github.com/runlikeforrestgump/emacs/README.md.

Copyright 2014 by https://github.com/runlikeforrestgump.


# Background

I have used [Vim](http://www.vim.org) for years. I've also used [Eclipse](https://www.eclipse.org) for my Java needs. As I gain more experience as a software engineer, I find that I'm using more and more languages. Since I'm comfortable with Vim and am a huge fan of the command-line, I've looked into turning Vim into a powerful IDE for all the languages I use because I want my IDE to support me being productive. If all I'm doing is Python or Ruby development, then I can probably get by with Vim as my IDE, but I use way more languages than Python and Ruby. I've looked hard and have been frustrated by the lack of plugins and frustrated that the plugins that do exist usually don't work well together. I saw that Emacs is extremely customisable and supports a lot of what I want and has a great framework for making plugins work well together, so I decided to finally make an effort to learn Emacs. I'm glad I've learned Vim, and I'll still use its ugly step-sister Vi (since it comes with a fresh install of most Unix-like operating systems and is better than ed and nano for system administration needs), but for my daily programming needs, I'm switching to Emacs.

At first, my plan was to try to write down everything I normally do in Vim and Eclipse, and then translate those things into Emacs. Then, I realised that Emacs can probably do much more than those things (people do call it an operating system for a reason). That's when I decided to read the entire GNU Emacs manual, which took me a solid two weeks of reading (I'm a slow reader and take notes when I read; I was reading about 5% per day, and more on the weekend (10% per day)). I also spent another week reading some of the other Info manuals.

The problem with a lot of Emacs guides out there is that they seem to be copy-and-pasted from each other (I think this applies to a lot of guides in general) and really only cover working with plaintext files. Then there are guides out there that only focus on one programming language. Then there's the GNU Emacs manual, which takes weeks to read. Then there's using Emacs on a daily basis and slowly learning as you go for years. The problem with switching IDEs is that you don't want to sacrifice your productivity. This is where my guide comes in. The purpose of the guide is to get you up to speed on typical things that programmers demand from their IDE while also being useful as a reference for jogging your memory for those things. I don't want the guide to be comprehensive. I just want it to get straight to the point for all the important things. Essentially, I want to develop a conceptual framework, from which you (and I) can build on. You may feel overwhelmed by Emacs's steep learning curve, but consider it a worthwhile investment: you're investing your time in something that you'll use for a lifetime.


# History

Richard Stallman joined the MIT Artificial Intelligence Lab in 1971 (when he was about 18 years old).

The GNU Project was created on 27 September 1983 by Richard Stallman (when he was 30 years old) as a project for developing free software (free as in freedom). The main project was the GNU operating system.

GNU Emacs was first released on 20 March 1985 by Richard Stallman (when he was 32 years old). This was the first program released by the GNU Project.

The Free Software Foundation (FSF) was founded on 04 October 1985 by Richard Stallman (when he was 32 years old) as a non-profit organisation for the free software movement. It helps fund the GNU project.

GNU is a recursive acronym for "GNU's Not Unix!", chosen because GNU (the operating system)'s design is Unix-like, but contains no Unix code. The name is also inspired by the 1957 song "The Gnu" from the British comedy duo Flanders and Swann. To avoid confusion with the word "new", the G in GNU is pronounced (like "g-noo", using a hard G like in the word "good"), just like the pronunciation in the Flanders and Swann song. Note that the word gnu (pronounced "noo") refers to the southern African animal that is also known as a wildebeest and is part of the antelope family, hence GNU's logo (created by Etienne Suvasa).

Emacs actually refers to a family of text editors; however, when unqualified, it usually refers to GNU Emacs. Emacs editors are known for their extensibility. A typical Emacs implementation has a small, solid core written in one language (such as C) and often uses some dialect of Lisp for extensibility.

Note that GNU Emacs wasn't the first Emacs, but the first Emacs was also written by Richard Stallman. GNU Emacs was initially created as a free software alternative to the proprietary Gosling Emacs (also known as Gosmacs, gmacs, or UniPress Emacs), which was created by James Gosling (the creator of Java) in 1981. Gosling Emacs was owned by UniPress. Gosling Emacs was written in C and Mocklisp (aka MLisp). It was the first Emacs to run on Unix.

The original EMACS was written in 1976 by Richard Stallman (when he was about 23 years old) and Guy L. Steele, Jr. as a set of **E**ditor **MAC**ro**S** for the TECO (Tape Editor and Corrector) editor for the Incompatible Timesharing System (ITS) operating system on the PDP line of computers in use at MIT at the time.

GNU Emacs is written in C and Emacs Lisp (Elisp). LISP 1 was the first implementation of Lisp. LISP 1.5 was the first widely used Lisp implementation. MACLISP appeared in the 1960s; it was developed for MIT's ProjectMAC and was a direct descendent of LISP 1.5. Scheme (influenced by LISP 1.5 and MACLISP) appeared in 1975 and Common Lisp appeared in 1984. "Richard Stallman chose Lisp as the extension language for his rewrite of Emacs because of its powerful features, including the ability to treat functions as data. Unlike Common Lisp, Scheme existed at the time Stallman was rewriting Gosling Emacs into GNU Emacs, but he chose not to use it because of its comparatively poor performance on workstations, and he wanted to develop a dialect which he thought would be more easily optimized." "In terms of features, Elisp is closely related to the Maclisp dialect, with some later influence from Common Lisp." A scripting language used for scripting an application is called an extension language. Elisp is considered an extension language. Elisp is a scripting language dialect of a general-purpose language.

If you want to read more about the history of the GNU Project, type <code>C-h g</code> (<code>M-x describe-gnu-project</code>) in Emacs. To paraphrase one of my favourite quotes from that document: "Sharing of software is as old as computers, just as sharing of recipes is as old as cooking." Extremely well articulated, Richard!


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

Some commands are (or can be) disabled, which means that you'll be asked for confirmation when you try to invoke them. The usual reason for disabling a command is that some commands are potentially confusing for beginning users.


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

Multi-character commands are echoed in the echo area if you pause for more than a second in the middle of a command. Emacs then echoes all the characters of the command so far, to prompt you for the rest. Once echoing has started, the rest of the command echoes immediately as you type it. While the minibuffer is in use, key sequences do not echo.

What some programs call "assigning a keyboard shortcut", Emacs calls "binding a key sequence."

The bindings of key sequences to commands are stored in data structures called keymaps.

Typing the help character (<code>C-h</code> or <code>&lt;F1&gt;</code>) after a prefix key displays a list of the commands starting with that prefix. For commands starting with &lt;ESC&gt;, you can use &lt;F1&gt; for help, but not C-h.


## Invoking Commands by Name

It's very easy to invoke a command by name. Just type <code>M-x</code>, followed by the command name, followed by <code>&lt;RET&gt;</code>.

If you invoke a command by name that could also have been invoked by a key sequence, then Emacs will use the echo area to tell you what key sequence you can use next time you want to invoke the command. If the message disappears too quickly, you can type <code>C-h e</code> to view a log of the echo area messages.

For commands that you don't use often, it's probably easier to remember the command by name rather than by key.

Not all commands are bound to keys.

By convention, a command name consists of one or more words, separated by hyphens.


## Key Conflicts

Sometimes you'll notice that a key sequence should invoke a certain command, but doesn't. Or sometimes you'll notice that a key sequence does do something, but it does the wrong thing. In these cases, there's likely a key conflict (or clash or collision, or whatever you want to call it) somewhere, which means that something else (usually your window manager, terminal, or desktop environment) has defined the same key sequence and has higher precedence than Emacs's key sequence. To resolve the conflict, you should either change the key sequence in Emacs (i.e., bind the command to a non-conflicting key sequence) or change the key sequence in whatever is causing the conflict. Unfortunately, I don't know a quick and easy way to debug key conflicts, but your window manager, terminal, or desktop environment are certainly prime suspects. Check their documentation for their keyboard shortcuts. If they have a way to list their key bindings, then do that. Use <code>C-h c</code> in Emacs to describe the key sequence. If you have Emacs compiled with X support and you're in terminal mode, then try launching Emacs in graphical mode to see if that implicates your terminal (if the conflict occurs in terminal mode, but not in graphical mode, then your terminal is causing the conflict). You could also go to an empty desktop or blank terminal and try the key sequence to see what happens; this might give you a clue for what to search for.

If you found the key sequence defined outside of Emacs and determined that it's something that you rarely or never use, then redefine the key sequence outside Emacs. If you found the key sequence defined outside of Emacs and determined that it's something you commonly use and the key sequence in Emacs is one that you rarely or never use, or you can't redefine the key sequence outside Emacs, or if you couldn't find out the source of the key conflict, then redefine the key sequence in Emacs. For the cases where you commonly use the same key sequence inside and outside Emacs, then you have a tougher decision.

The quick and easy way to define a key binding is to bind the key to the global keymap in your init file (typically ~/.emacs): <code>(global-set-key (kbd "KEY_SEQUENCE") 'COMMAND)</code>, where KEY_SEQUENCE is written in the same notation that you see in all the Emacs documentation (C- for control, M- for alt, S- for shift, &lt;TAB&gt; for tab, etc.).

The Alt key will sometimes be involved in key conflicts. A way around this is to use &lt;ESC&gt; in place of Alt (you don't need to rebind anything; &lt;ESC&gt; is already an alias for Alt, right out of the box).

Some conflicts that I've run into:

* <code>C-S-&lt;DEL&gt;</code> is supposed to invoke <code>kill-whole-line</code>, but instead it invokes the help prefix (<code>C-h</code>). This was only a problem for me in my terminal ([rxvt-unicode](http://software.schmorp.de/pkg/rxvt-unicode.html)). Note that the key sequence <code>C-&lt;DEL&gt;</code> seems to behave the same as <code>C-S-&lt;DEL&gt;</code> (they both invoke the help prefix). TODO: resolve the conflict and document how I resolved it.
* <code>C-M-v</code> is supposed to invoke <code>scroll-other-window</code>, but instead it pastes text. This was only a problem for me in my terminal. This is because I'm using the rxvt-unicode clipboard extension from [urxvt-perls](https://github.com/muennich/urxvt-perls), which binds <code>C-M-v</code> to paste_escaped by default. To resolve the conflict, I defined a different key binding for paste_escaped in my ~/.Xresources file: <code>URxvt.keysym.C-S-M-V:perl:clipboard:paste_escaped</code> (yes, this is an awkward key binding, but I don't care because I don't use paste_escaped). Another solution you could do is remove the <code>paste_escaped</code> elsif in the on_user_command subroutine in /usr/lib\*/urxvt/perl/clipboard, if paste_escaped is something that you don't use.
* I don't know what <code>C-&lt;TAB&gt;</code> is supposed to do (Emacs tells me <code>C-&lt;TAB&gt;</code> is undefined, but the Emacs manual says that it's bound to the command file-cache-minibuffer-complete); however, I know that if I wanted to use <code>C-&lt;TAB&gt;</code> in my terminal, I currently can't: a plain &lt;TAB&gt; is inserted instead. TODO: resolve the conflict and document how I resolved it.


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

The Emacs manual (and other Emacs-related manuals) can be read online: https://www.gnu.org/software/emacs/manual/. All those manuals also ship with Emacs, so they can be read in Emacs offline. If you want to support the FSF, you can purchase documentation from http://shop.fsf.org, where you can also buy a mug that has a reference card printed on it. They could probably sell more copies of the documentation if the documentation were signed by Richard Stallman, but then he would probably get tired really fast.

<dl>
  <dt><dfn>
  C-h C-h<br>
  M-x help-for-help</dfn></dt>
  <dd>Display a list of help commands.</dd>

  <dt><dfn>
  C-h b<br>
  &lt;F1&gt; b<br>
  M-x describe-bindings</dfn></dt>
  <dd>Display a list of all the active keybindings (minor mode bindings are listed first, followed by major mode, followed by global).</dd>

  <dt><dfn>
  C-h m<br>
  &lt;F1&gt; m<br>
  M-x describe-mode</dfn></dt>
  <dd>Display the documentation for the current major mode, including its commands.</dd>

  <dt><dfn>
  C-h c KEYSEQUENCE<br>
  &lt;F1&gt; c KEYSEQUENCE<br>
  M-x describe-key-briefly &lt;RET&gt; KEYSEQUENCE</dfn></dt>
  <dd>Display the command name that's bound to the specified key sequence.</dd>

  <dt><dfn>
  C-h w COMMAND<br>
  &lt;F1&gt; w COMMAND<br>
  M-x where-is &lt;RET&gt; COMMAND</dfn></dt>
  <dd>Display the key sequence that runs the specified command.</dd>

  <dt><dfn>
  C-h f COMMAND<br>
  C-h k KEYSEQUENCE<br>
  &lt;F1&gt; f COMMAND<br>
  &lt;F1&gt; k KEYSEQUENCE<br>
  M-x describe-function &lt;RET&gt; COMMAND<br>
  M-x describe-key &lt;RET&gt; KEYSEQUENCE</dfn></dt>
  <dd>Display the documentation for the specified command. You can look up the command's documentation by its name or by its key sequence; both ways will take you to the same documentation.</dd>

  <dt><dfn>
  C-h F COMMAND<br>
  C-h K KEYSEQUENCE<br>
  &lt;F1&gt; F COMMAND<br>
  &lt;F1&gt; K KEYSEQUENCE<br>
  M-x Info-goto-emacs-command-node &lt;RET&gt; COMMAND<br>
  M-x Info-goto-emacs-key-command-node &lt;RET&gt; KEYSEQUENCE</dfn></dt>
  <dd>Go to the section in the corresponding manual that documents the specified command or key sequence.</dd>

  <dt><dfn>
  C-h v VARIABLE<br>
  &lt;F1&gt; v VARIABLE<br>
  M-x describe-variable &lt;RET&gt; VARIABLE</dfn></dt>
  <dd>Display the documentation for the given Emacs variable.</dd>

  <dt><dfn>
  C-h a PATTERN<br>
  &lt;F1&gt; a PATTERN<br>
  M-x apropos-command &lt;RET&gt; PATTERN</dfn></dt>
  <dd>
<p>Display a list of commands that match PATTERN.</p>

<p>An apropos pattern means either a word, a space-delimited list of words, or a regular expression. If a list of words is given, the apropos will match anything that contains at least two of the words.</p>
  </dd>

  <dt><dfn>M-x apropos PATTERN</dfn></dt>
  <dd>Display a list of commands and variables that match PATTERN.</dd>

  <dt><dfn>M-x apropos-variable PATTERN</dfn></dt>
  <dd>Display a list of user-customisable variables that match PATTERN. With a prefix argument, search for non-customisable variables too.</dd>

  <dt><dfn>M-x apropos-value</dfn></dt>
  <dd>Display a list of variables whose values match PATTERN.</dd>

  <dt><dfn>
  C-h d TOPICS<br>
  &lt;F1&gt; d TOPICS<br>
  M-x apropos-documentation &lt;RET&gt; TOPICS</dfn></dt>
  <dd>Display the commands and variables whose documentation matches TOPICS.</dd>

  <dt><dfn>
  C-h P PACKAGE<br>
  &lt;F1&gt; P PACKAGE<br>
  M-x describe-package &lt;RET&gt; PACKAGE</dfn></dt>
  <dd>Display the documentation for the specified package.</dd>

  <dt><dfn>
  C-h p<br>
  &lt;F1&gt; p<br>
  M-x finder-by-keyword</dfn></dt>
  <dd>Display a list of package categories. From there, you can select a package category to get a list of packages in that category, and from there, you can select a package name to view the documentation for that package. Use &lt;RET&gt; or your mouse for selection.</dd>

  <dt><dfn>
  C-h l<br>
  &lt;F1&gt; l<br>
  M-x view-lossage</dfn></dt>
  <dd>Display a history of your most recent input keystrokes, ordered from oldest to newest (newest appears near the end of the buffer). This is useful when something surprising happens and you want to figure out what you did.</dd>

  <dt><dfn>
  C-h r<br>
  &lt;F1&gt; r<br>
  M-x info-emacs-manual</dfn></dt>
  <dd>
<p>Display the Emacs manual.</p>

<p>To search the index, use <code>i TOPIC &lt;RET&gt;</code> To search the text, use <code>s TOPIC &lt;RET&gt;</code>. Topic can be a word or a regular expression.</p>
  </dd>

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
  C-h r m Glossary &lt;RET&gt;<br>
  &lt;F1&gt; r m Glossary &lt;RET&gt;<br>
  M-x search-emacs-glossary</dfn></dt>
  <dd>Display the Emacs glossary.</dd>

  <dt><dfn>
  C-h a -mode<br>
  &lt;F1&gt; a -mode</dfn></dt>
  <dd>Display a list of all available major and minor modes.</dd>

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
  C-h I INPUTMETHOD<br>
  &lt;F1&gt; I INPUTMETHOD<br>
  M-x describe-input-method &lt;RET&gt; INPUTMETHOD</dfn></dt>
  <dd>Display the documentation for the specified input method.</dd>

  <dt><dfn>
  C-h C-n<br>
  &lt;F1&gt; C-n<br>
  M-x view-emacs-news</dfn></dt>
  <dd>View the release notes for various versions of Emacs.</dd>

  <dt><dfn>
  C-h r m Antinews<br>
  &lt;F1&gt; r m Antinews</dfn></dt>
  <dd>View hilarious release notes from the perspective of downgrading Emacs and losing features and gaining bugs. It talks about a downgrade as if you are going to a newer version of Emacs.</dd>

  <dt><dfn>
  C-h C-p<br>
  &lt;F1&gt; C-p<br>
  M-x view-emacs-problems</dfn></dt>
  <dd>Display the list of known Emacs problems, sometimes with suggested workarounds.</dd>

  <dt><dfn>
  C-h C-t<br>
  &lt;F1&gt; C-t<br>
  M-x view-emacs-todo</dfn></dt>
  <dd>Display the Emacs to-do list.</dd>

  <dt><dfn>
  C-h C-d<br>
  &lt;F1&gt; C-d<br>
  M-x view-emacs-debugging</dfn></dt>
  <dd>Display help for debugging Emacs.</dd>
</dl>

Note that modes correspond to commands, so if you want to read the documentation for a mode, just look up its documentantation by its command name.

<code>C-h c</code>, <code>C-h k</code>, and <code>C-h K</code> work for any sort of key sequences, including function keys, menus, and mouse events; for example, after <code>C-h k</code>, you can select a menu item from the menu bar, to view the documentation string of the command it runs.

In a help buffer, you can use <code>&lt;SPC&gt;</code> to scroll forward and <code>&lt;DEL&gt;</code> to scroll backward. When a function name, variable name, or face name appears in the documentation in the help buffer, it is normally an underlined hyperlink. To view the associated documentation, move point there and type <code>&lt;RET&gt;</code>, or click on the hyperlink. Doing so replaces the contents of the help buffer; to retrace your steps, type <code>C-c C-b</code> (<code>M-x help-go-back</code>). A help buffer can also contain hyperlinks to Info manuals, source code definitions, and URLs (Web pages). The first two are opened in Emacs, and the third using a Web browser via the browse-url command. To move to the next hyperlink in a help buffer, use <code>&lt;TAB&gt;</code>. To move to the previous hyperlink, use <code>S-&lt;TAB&gt;</code>. <code>&lt;TAB&gt;</code> and <code>S-&lt;TAB&gt;</code> act cyclically, so if you're on the last hyperlink, <code>&lt;TAB&gt;</code> moves to the first hyperlink; if you're on the first hyperlink, <code>S-&lt;TAB&gt;</code> moves to the last hyperlink. If a variable, function, or face name isn't hyperlinked, you can still views its documentation by moving point to the symbol and then typing <code>C-c C-c</code> (<code>M-x help-follow-symbol</code>). To exit a help buffer, press <code>q</code>.

A list of Emacs mailing lists is available here: https://savannah.gnu.org/mail/?group=emacs (help-gnu-emacs@gnu.org or help-emacs-windows@gnu.org are probably the ones you want (if you're looking for help)). You can search the mailing lists at https://lists.gnu.org/archive/html/help-gnu-emacs/ or https://lists.gnu.org/archive/html/help-emacs-windows/.

Some people and companies offer support services and training for Emacs for free or for a fee; you can find a list of them here: https://www.fsf.org/resources/service/. Richard Stallman is even on the list, so I guess you can get help from the inventor himself, which is really cool.

The official Emacs IRC channel is #emacs on freenode, since the GNU Project made freenode its official IRC network in 2002. If you have a question regarding [EmacsWiki](http://www.emacswiki.org), there's a freenode channel for it: #emacswiki.

Emacs comes with reference cards (cheat sheets) in TeX and PDF format. On my machine, they're located in /usr/share/emacs/\*/etc/refcards. "refcard" is the name of the file you probably want, but there are other reference cards that are more mode-specific and may also be of interest to you.


## Using GNU Info

GNU Info is the GNU documentation browser, which uses a hypertext format (a collection of documents with links) called Texinfo. Since a lot of the Emacs documentation is found in Info pages, it's worth learning how to use GNU Info, which can be used as a standalone program or used through Emacs's Info mode.

Each node has a name (for example, Help) and a topic (for example, "How to use Info").

Nodes can have parents or children or both.

The top line of a node is its header. The header says what the next, previous, and parent nodes are. The header doesn't point to subnodes; it only points to nodes at the same level (in the case of next and previuos) or above (in the case of up), relative to the current node.

<dl>
  <dt><dfn>n</dfn></dt>
  <dd>Move to the next node at the same level as the current node.</dd>

  <dt><dfn>p</dfn></dt>
  <dd>Move to the previous node at the same level as the current node.</dd>

  <dt><dfn>
  u<br>
  ^</dfn></dt>
  <dd>Move up to the parent node.</dd>

  <dt><dfn>t</dfn></dt>
  <dd>Move to the top node of the manual.</dd>

  <dt><dfn>l</dfn></dt>
  <dd>Retrace your steps. As you move from node to node, Info records the nodes where you have been in a special history list. The l command revisits nodes in the history list; each successive l command moves one step back through the history.</dd>

  <dt><dfn>r</dfn></dt>
  <dd>r is the opposite of l. It moves forward in the history list.</dd>

  <dt><dfn>]</dfn></dt>
  <dd>Move to the next node regardless of level.</dd>

  <dt><dfn>[</dfn></dt>
  <dd>Move to the previous node regardless of level.</dd>

  <dt><dfn>&lt;SPC&gt;</dfn></dt>
  <dd>Scroll forward if there is still text to scroll forward to; otherwise, move to the next node regardless of level.</dd>

  <dt><dfn>&lt;DEL&gt;</dfn></dt>
  <dd>Scroll backward if there is still text to scroll back to; otherwise, move to the previous node regardless of level.</dd>

  <dt><dfn>C-v</dfn></dt>
  <dd>Scroll forward, but don't move to the next node if the bottom of the node has been reached.</dd>

  <dt><dfn>M-v</dfn></dt>
  <dd>Scroll backward, but don't move to the previous node if the top of the node has been reached.</dd>

  <dt><dfn>b</dfn></dt>
  <dd>Immediately scroll to the top of the current node.</dd>

  <dt><dfn>?</dfn></dt>
  <dd>Display a list of Info commands.</dd>

  <dt><dfn>m NODE_NAME</dfn></dt>
  <dd>
<p>Go to the node that has the specified name.</p>

<p>A menu is a list of other nodes you can move to. The beginning of a menu is always identified by a line which starts with '* Menu:'. A node contains a menu if and only if it has a line in it which starts that way. The only menu you can use at any moment is the one in the node you are in. To use a menu in any other node, you must move to that node first.</p>

<p>You can abbreviate the node name. If the abbreviation is not unique, the first matching node is chosen. Some menus put the shortest possible abbreviation for each node name in capital letters, so you can see how much you need to type. It does not matter whether you use upper case or lower case when you type the node name. If you type &lt;TAB&gt; after entering part of a name, it will fill in more of the name--as much as Info can deduce from the part you have entered. You can also move point over a node name, and then press &lt;RET&gt;. You can type &lt;TAB&gt; to move point to the next item in the menu and type S-&lt;TAB&gt; to move point to the previous item in the menu.</p>

<p>If you type <code>?</code> as the node name, then a list of possible menu items will appear.</p>

<p>Rather than using <code>m</code> and specifying a node name, you can enter a digit from 1 to 9 to access items in the menu.</p>

<p>If you invoke <code>m</code> with a prefix argument (thus, <code>C-u m NODE_NAME</code>), then the node you specify will be opened in a new Info buffer.</p>
  </dd>

  <dt><dfn>f CROSS_REFERENCE</dfn></dt>
  <dd>
<p>Go to the cross reference that has the specified name.</p>

<p>A cross reference is a link that doesn't appear in a menu.</p>

<p>You can type &lt;TAB&gt; to move point to the next cross reference and type S-&lt;TAB&gt; to move point to the previous cross reference.</p>

<p>If you type <code>?</code> as the cross reference name, then a list of possible cross reference names will appear.</p>
  </dd>

  <dt><dfn>g NODE_NAME</dfn></dt>
  <dd>
<p>Go to the node that has the specified name. The difference between this and <code>m</code> is that <code>m</code> only accepts names of nodes that appear in the current node's menu; whereas, <code>g</code> accepts the name of any node whether it's in the menu or not.</p>

<p>If you specify <code>*</code> as the node name, then the whole file will be displayed.</p>

<p>To go to a node in another file, you can include the file name in the node name by putting it at the front, in parentheses; for example, <code>g (emacs)Top &lt;RET&gt;</code> will take you to the top node of the Emacs manual.</p>

<p>If you invoke <code>g</code> with a prefix argument (thus, <code>C-u g NODE_NAME</code>), then the node you specify will be opened in a new Info buffer.</p>
  </dd>

  <dt><dfn>d</dfn></dt>
  <dd>Go to the Directory node, which is a node that lists all the manuals and other Info documents that are installed on your system.</dd>

  <dt><dfn>M-n</dfn></dt>
  <dd>Clone the current Info buffer in another window.</dd>

  <dt><dfn>i TOPIC</dfn></dt>
  <dd>
<p>Search the index for a specified topic and go to the node which is listed in the index for that topic.</p>

<p>To search for keys, use the notation that the Emacs documentation uses; for example, <code>i C-n</code>, where you literally spell out uppercase C, hyphen, lowercase n (rather than holding Ctrl and pressing n).</p>
  </dd>

  <dt><dfn>s STRING</dfn></dt>
  <dd>Search the entire manual for the specified string.</dd>

  <dt><dfn>L</dfn></dt>
  <dd>Display a menu of all the nodes you've visited. You can jump to one of those nodes by selecting it from the menu.</dd>

  <dt><dfn>T</dfn></dt>
  <dd>Go to the table of contents of the current Info file.</dd>

  <dt><dfn>&lt;</dfn></dt>
  <dd>Move to the top node of the current Info file.</dd>

  <dt><dfn>&gt;</dfn></dt>
  <dd>Move to the last node of the current Info file.</dd>

  <dt><dfn>q</dfn></dt>
  <dd>Quit Info.</dd>

  <dt><dfn>C-u C-h i</dfn></dt>
  <dd>Open an Info file that isn't listed in the Directory node.</dd>

  <dt><dfn>M-x info-apropos STRING</dfn></dt>
  <dd>Search for the specified string in the indeces of all the Info files. The <code>i</code> command only searches the index of the current Info file.</dd>
</dl>


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
* You can limit what text you see in the buffer, making the rest of the text in the buffer temporarily inaccessible and invisible (however, it's still there and you can still save it). This is called **narrowing**. You can think of it as zooming in on something, so that you can focus your attention without distraction (or for easily applying changes to a limited portion of the text). The opposite of narrowing is called **widening**. When narrowed, the text that is still accessible is called the **accessible portion**; the bounds of the narrowed region are called its **restriction**.
* Each window has a **scrollbar**. The echo area and minibuffer also have a scrollbar.
* At the very bottom of each window is a **mode line**, which provides information about the window's buffer.
* **Fringes** are the narrow strips that appear on the left and right of a window. They are used for displaying symbols that provide information about the buffer text. Fringes are not the same thing as borders.
* A **margin** is the space between the usable part of a window (including the fringe) and the window edge. I guess you can think of a margin as the window's internal border and think of the window's edge as the window's external border.
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
* A **clipboard** is a buffer provided by your window system for transferring text between applications. Graphical Emacs works with the system clipboard out of the box. If you want to integrate terminal Emacs (emacs -nw) with the system clipboard, then you'll need to use something like [xclip](http://sourceforge.net/projects/xclip/) or [xsel](http://www.vergenet.net/~conrad/software/xsel/).
* A major definition at the top level in the buffer is called a **defun**. The name comes from Lisp, where most such definitions use the construct <code>defun</code>, but in Emacs, the term "defun" applies to all languages.

My attempt at an ASCII art Emacs frame (looks kind of like a polaroid):

```
+---------------------------------------------------------------+
| menu bar                                                      |
+---------------------------------------------------------------+
| tool bar                                                      |
+---------------------------------------------------------------+
| |f|                                                         |f|
| |r|                                                         |r|
| |i|                                                         |i|
| |n|                                                         |n|
| |g|                                                         |g|
| |e|                                                         |e|
| | |                                                         | |
|s| |                                                         | |
|c| |                     window / buffer                     | |
|r| |                                                         | |
|o| |                                                         | |
|l| |                                                         | |
|l| |                                                         | |
| | |                                                         | |
|b| |                                                         | |
|a| |                                                         | |
|r| |                                                         | |
| | |                                                         | |
+---------------------------------------------------------------+
| mode line                                                     |
+---------------------------------------------------------------+
| | echo area / minibuffer                                      |
+---------------------------------------------------------------+
```

## Mode Line

A mode line exists at the bottom of each window to provide information about the contents of the respective window.

In graphical Emacs, you can mouse over items in the mode line to get a rough idea of what the various things in the mode line mean.

The format of the mode line is slightly different for terminal Emacs and graphical Emacs:

* Graphical-Emacs mode line format:
    * The coding system of the text in the buffer.
        * U means utf-8-unix
        * 1 means iso-latin-1-unix
        * = means no-conversion
    * End-of-line convention used in the buffer.
        * : or (Unix) means Unix-style (\\n)
        * / or (Mac) means Mac-style (\\r)
        * \ or (DOS) means DOS-style (\\r\\n)
    * &lt;READ_ONLY_FLAG&gt;
    * &lt;MODIFICATION_STATE&gt;
    * &lt;LOCAL_OR_REMOTE&gt;
    * &lt;BUFFER_NAME&gt;
    * &lt;POSITION&gt;
    * &lt;LINE_NUMBER_OF_POINT&gt;
    * (&lt;MAJOR_MODE&gt; &lt;MINOR_MODES&gt;)
* Terminal-Emacs mode line format:
    * -
    * If an input method is being used, then its name is displayed; otherwise, this field is not included in the mode line.
    * The keyboard input coding system.
    * The terminal output coding system.
    * The coding system of the text in the buffer.
        * U means utf-8-unix
        * 1 means iso-latin-1-unix
        * = means no-conversion
    * End-of-line convention used in the buffer.
        * : or (Unix) means Unix-style (\\n)
        * / or (Mac) means Mac-style (\\r)
        * \ or (DOS) means DOS-style (\\r\\n)
    * &lt;READ_ONLY_FLAG&gt;
    * &lt;MODIFICATION_STATE&gt;
    * &lt;LOCAL_OR_REMOTE&gt;
    * -
    * &lt;SELECTED_FRAME_NAME&gt;
    * &lt;BUFFER_NAME&gt;
    * &lt;POSITION&gt;
    * &lt;LINE_NUMBER_OF_POINT&gt;
    * (&lt;MAJOR_MODE&gt; &lt;MINOR MODES&gt;)
