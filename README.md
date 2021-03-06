TODO: add a table of contents (it would be nice if GitHub's markdown auto-generated this...)

# Legal Stuff

You do **not** have permission to make any money off of this document or any version of it (either in its entirety or in parts), claim any credit for this document or any version of it (either in its entirety or in parts), or modify this document or any version of it.

You do have permission to share this document, as long as you keep this legal section as is and intact with the copies you share and as long as you honour this legal section.

If you have a copy of the document, you can find the original document at https://github.com/runlikeforrestgump/emacs/README.md.

Copyright 2014 - 2015 by https://github.com/runlikeforrestgump.


# Background

I have used [Vim](http://www.vim.org) for years. I've also used [Eclipse](https://www.eclipse.org) for my Java needs. As I gain more experience as a software engineer, I find that I'm using more and more languages. Since I'm comfortable with Vim and am a huge fan of the command-line, I've looked into turning Vim into a powerful IDE for all the languages I use because I want my IDE to support me being productive. If all I'm doing is Python or Ruby development, then I can probably get by with Vim as my IDE, but I use way more languages than Python and Ruby. I've looked hard and have been frustrated by the lack of plugins and frustrated that the plugins that do exist usually don't work well together. I saw that Emacs is extremely customisable and supports a lot of what I want and has a great framework for making plugins work well together, so I decided to finally make an effort to learn Emacs. I'm glad I've learned Vim, and I'll still use its ugly step-sister Vi (since it comes with a fresh install of most Unix-like operating systems and is better than ed and nano for system administration needs), but for my daily programming needs, I'm switching to Emacs.

At first, my plan was to try to write down everything I normally do in Vim and Eclipse, and then translate those things into Emacs. Then, I realised that Emacs can probably do much more than those things (people do call it an operating system for a reason). That's when I decided to read the entire GNU Emacs manual, which took me a solid two weeks of reading (I'm a slow reader and take notes when I read; I was reading about 5% per day, and more on the weekend (10% per day)). I also spent another week reading some of the other Info manuals.

The problem with a lot of Emacs guides out there is that they seem to be copy-and-pasted from each other (I think this applies to a lot of guides in general, which you can often find on people's blogs) and really only cover the basics of working with plaintext files. Then there are guides out there that only focus on one programming language, which means you'll have to depend on different guides (assuming you use more than one language), which likely differ in their quality. Then there's the GNU Emacs manual, which takes weeks to read and doesn't cover everything that a programmer would want to know. Then there's using Emacs on a daily basis and very slowly learning as you go for years. The problem with switching IDEs is that you don't want to sacrifice your productivity. This is where my guide comes in. The purpose of the guide is to get you up to speed on typical things that programmers demand from their IDE while also being useful as a reference for jogging your memory for those things. I don't want the guide to be comprehensive. I just want it to get straight to the point for all the important things. Essentially, I want to develop a conceptual framework, from which you (and I) can build on. You may feel overwhelmed by Emacs's steep learning curve, but consider it a worthwhile investment: you're investing your time in something that you'll use for a lifetime.

Another problem with a lot of guides in general is that the trend these days seems to be that guides try hard (often too hard) to be cute and funny (and sometimes come off as condescending and overly simplistic). I value humour, but I very rarely come across a guide that uses humour well. In most cases, the humour is noisy and distracting and doesn't even serve its purpose of being funny; I've even run into cases where the humour introduced confusion and ambiguity. Remember, if your primary goal is to teach something, then focus your efforts on teaching, not telling jokes.

From the Eshell manual: "Any tool you use often deserves the time spent learning to master it."


# History

Richard Stallman joined the MIT Artificial Intelligence Lab in 1971 (when he was about 18 years old).

The original EMACS was written in 1976 by Richard Stallman (when he was about 23 years old) and Guy L. Steele, Jr. as a set of **E**ditor **MAC**ro**S** for the TECO (Tape Editor and Corrector) editor for the Incompatible Timesharing System (ITS) operating system on the PDP line of computers in use at MIT at the time.

The GNU Project was created on 27 September 1983 by Richard Stallman (when he was 30 years old) as a project for developing free software (free as in freedom). The main project was the GNU operating system.

GNU Emacs was first released on 20 March 1985 by Richard Stallman (when he was 32 years old). This was the first program released by the GNU Project.

The Free Software Foundation (FSF) was founded on 04 October 1985 by Richard Stallman (when he was 32 years old) as a non-profit organisation for the free software movement. It helps fund the GNU project.

GNU is a recursive acronym for "GNU's Not Unix!", chosen because GNU (the operating system)'s design is Unix-like, but contains no Unix code. The name is also inspired by the 1957 song "The Gnu" from the British comedy duo Flanders and Swann. To avoid confusion with the word "new", the G in GNU is pronounced (like "g-noo", using a hard G like in the word "good"), just like the pronunciation in the Flanders and Swann song. Note that the word gnu (pronounced "noo") refers to the southern African animal that is also known as a wildebeest and is part of the antelope family, hence GNU's logo (created by Etienne Suvasa).

Emacs actually refers to a family of text editors; however, when unqualified, it usually refers to GNU Emacs. Emacs editors are known for their extensibility. A typical Emacs implementation has a small, solid core written in one language (such as C) and often uses some dialect of Lisp for extensibility.

Note that GNU Emacs wasn't the first Emacs, but the first Emacs was also written by Richard Stallman. GNU Emacs was initially created as a free software alternative to the proprietary Gosling Emacs (also known as Gosmacs, gmacs, or UniPress Emacs), which was created by James Gosling (the creator of Java) in 1981. Gosling Emacs was owned by UniPress. Gosling Emacs was written in C and Mocklisp (aka MLisp). It was the first Emacs to run on Unix.

GNU Emacs is written in C and Emacs Lisp (Elisp). LISP 1 was the first implementation of Lisp. LISP 1.5 was the first widely used Lisp implementation. MACLISP appeared in the 1960s; it was developed for MIT's ProjectMAC and was a direct descendent of LISP 1.5. Scheme (influenced by LISP 1.5 and MACLISP) appeared in 1975 and Common Lisp appeared in 1984. "Richard Stallman chose Lisp as the extension language for his rewrite of Emacs because of its powerful features, including the ability to treat functions as data. Unlike Common Lisp, Scheme existed at the time Stallman was rewriting Gosling Emacs into GNU Emacs, but he chose not to use it because of its comparatively poor performance on workstations, and he wanted to develop a dialect which he thought would be more easily optimized." "In terms of features, Elisp is closely related to the Maclisp dialect, with some later influence from Common Lisp." A scripting language used for scripting an application is called an extension language. Elisp is considered an extension language. Elisp is a scripting language dialect of a general-purpose language (Lisp).

If you want to read more about the history of the GNU Project, type <code>C-h g</code> (<code>M-x describe-gnu-project</code>) in Emacs. To paraphrase one of my favourite quotes from that document: "Sharing of software is as old as computers, just as sharing of recipes is as old as cooking."


# Installing [Emacs](https://www.gnu.org/software/emacs/)

At first, I installed Emacs without X support, which meant that I only used Emacs in a terminal. After a lot of reading and after watching experienced users use Emacs, I decided to reinstall Emacs with X support. It's not the most pleasant looking GUI (at least on Linux), but I recommend installing with X support (unless you don't have X and don't want it) because then you have the flexibility of starting Emacs in graphical mode (<code>emacs</code>) or in terminal mode (<code>emacs -nw</code>). Also, there are some things you can do in graphical mode that you can't do in terminal mode, and graphical mode provides conveniences like a menu, which is useful when you're completely lost and don't know what you're doing (like when you're a beginner). Graphical mode also has helpful tooltips when you mouseover things. Another benefit of graphical mode is that you're less likely to encounter key conflicts (most key conflicts are caused by your terminal). This guide assumes that you didn't install with X support; I'm sure you have experience with a GUI and can figure out GUI-specific stuff on your own (click, click, click, click, click).

I'm using [dwm](http://dwm.suckless.org) on [Gentoo GNU/Linux](http://www.gentoo.org). I installed with the toolkit-scroll-bars and xft USE flags because the Emacs toolbars didn't look very good and without xft support, Emacs displayed some strings (such as the buffer name in the mode line) in hex.

If you really want, you can grab the development version of Emacs from here: https://savannah.gnu.org/projects/emacs/.

An Emacs version number with two components (e.g., 22.1) indicates a released version; three components indicates a development version (e.g., 23.0.50).


# Starting Emacs

If you installed Emacs with X support, then invoking Emacs with <code>emacs &</code> will launch graphical Emacs and invoking Emacs with <code>emacs -nw</code> will launch terminal Emacs. If you installed Emacs without X support, then invoking Emacs with either <code>emacs</code> or <code>emacs -nw</code> will launch terminal Emacs.

The recommended way to use Emacs is to start it just once and do all your editing in the same Emacs session rather than starting a new instance each time you want to edit a file.

Additionally, you can tell Emacs to load one or more specified files after launching:

<dl>
  <dt><dfn>
  emacs FILENAME</dfn></dt>
  <dd>Launch Emacs and then load the specified file.</dd>

  <dt><dfn>
  emacs +LINE_NUMBER FILENAME</dfn></dt>
  <dd>Launch Emacs, load the specified file, and then move point to the specified line number in the specified file.</dd>

  <dt><dfn>
  emacs +LINE_NUMBER:COLUMN_NUMBER FILENAME</dfn></dt>
  <dd>Launch Emacs, load the specified file, and then move the cursor to the specified column number on the specified line number in the specified file.</dd>
</dl>

The optional <code>+LINE_NUMBER:COLUMN_NUMBER</code> applies only to the next file specified.

If you specify more than one file, then you'll only see the last file that you specified; however, the other files will also have been loaded and are available in the buffer list.

If you want to see how long Emacs has been running, type <code>M-x emacs-uptime</code>.


# Most Important Things to Know First

The most important things to know first are knowing how to quit, cancel, undo, switch and close buffers, and get help, and before you can know that, you need to know how to invoke commands in Emacs.

To invoke a command in Emacs:

1. You can use a key sequence (aka keyboard shortcut, key binding, or key for short).
2. Or you can call the command by name.

Some commands are (or can be) disabled, which means that you'll be asked for confirmation when you try to invoke them. The usual reason for disabling a command is that some commands are potentially confusing for beginning users.

You'll notice that some commands are grouped by similar prefix keys or prefix or suffix names; for example, a lot of window-based key sequences start with <code>C-x 4</code> and a lot of frame-based key sequences start with <code>C-x 5</code>. This makes it a little easier to remember things.

To repeat a command, you can use <code>C-x z</code> (<code>M-x repeat</code>). Repeating a command uses the same arguments that were used before; it does not read new arguments each time. To repeat the command more than once, type additional 'z''s: each 'z' repeats the command one more time. Repetition ends when you type a character other than 'z', or press a mouse button.


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

It's very easy to invoke a command by name. Just type <code>M-x</code>, followed by the command name, followed by <code>&lt;RET&gt;</code>. By convention, a command name consists of one or more words, separated by hyphens.

If you invoke a command by name that could also have been invoked by a key sequence, then Emacs will use the echo area to tell you what key sequence you can use next time you want to invoke the command. If the message disappears too quickly, you can type <code>C-h e</code> to view a log of the echo area messages.

For commands that you don't use often, it's probably easier to remember the command by name rather than by key. Also, not all commands are bound to keys.


## Key Conflicts

Sometimes you'll notice that a key sequence should invoke a certain command, but doesn't. Or sometimes you'll notice that a key sequence does do something, but it does the wrong thing. In these cases, there's likely a key conflict (or clash or collision, or whatever you want to call it) somewhere, which means that something else (usually your window manager, terminal, or desktop environment) has defined the same key sequence and has higher precedence than Emacs's key sequence. To resolve the conflict, you should either change the key sequence in Emacs (i.e., bind the command to a non-conflicting key sequence) or change the key sequence in whatever is causing the conflict. Unfortunately, I don't know a quick and easy way to debug key conflicts, but your window manager, terminal, or desktop environment are certainly prime suspects. Check their documentation for their keyboard shortcuts. If they have a way to list their key bindings, then do that. Use <code>C-h c</code> in Emacs to describe the key sequence. If you have Emacs compiled with X support and you're in terminal mode, then try launching Emacs in graphical mode to see if that implicates your terminal (if the conflict occurs in terminal mode, but not in graphical mode, then your terminal is causing the conflict). You could also go to an empty desktop or blank terminal and try the key sequence to see what happens; this might give you a clue for what to search for.

If you found the key sequence defined outside of Emacs and determined that it's something that you rarely or never use, then redefine the key sequence outside Emacs. If you found the key sequence defined outside of Emacs and determined that it's something you commonly use and the key sequence in Emacs is one that you rarely or never use, or you can't redefine the key sequence outside Emacs, or if you couldn't find out the source of the key conflict, then redefine the key sequence in Emacs. For the cases where you commonly use the same key sequence inside and outside Emacs, then you have a tougher decision.

The quick and easy way to define a key binding is to bind the key to the global keymap in your init file (typically ~/.emacs): <code>(global-set-key (kbd "KEY_SEQUENCE") 'COMMAND)</code>, where KEY_SEQUENCE is written in the same notation that you see in all the Emacs documentation (C- for control, M- for alt, S- for shift, &lt;TAB&gt; for tab, etc.).

The Alt key will sometimes be involved in key conflicts. A way around this is to use &lt;ESC&gt; in place of Alt (you don't need to rebind anything; &lt;ESC&gt; is already an alias for Alt, right out of the box).

Some conflicts that I've run into:

* <code>C-S-&lt;DEL&gt;</code> is supposed to invoke <code>kill-whole-line</code>, but instead it invokes the help prefix (<code>C-h</code>). This was only a problem for me in my terminal ([rxvt-unicode](http://software.schmorp.de/pkg/rxvt-unicode.html)). Note that the key sequence <code>C-&lt;DEL&gt;</code> seems to behave the same as <code>C-S-&lt;DEL&gt;</code> (they both invoke the help prefix). TODO: resolve the conflict and document how I resolved it.
* <code>C-M-v</code> is supposed to invoke <code>scroll-other-window</code>, but instead it pastes text. This was only a problem for me in my terminal. This is because I'm using the rxvt-unicode clipboard extension from [urxvt-perls](https://github.com/muennich/urxvt-perls), which binds <code>C-M-v</code> to paste_escaped by default. To resolve the conflict, you can define a different key binding for paste_escaped in your ~/.Xresources file: <code>URxvt.keysym.CHANGEME:perl:clipboard:paste_escaped</code>. Don't bind to <code>C-M-S-v</code> because that will conflict with <code>scroll-other-window-down</code>. Another solution you could do is remove the <code>paste_escaped</code> elsif in the on_user_command subroutine in /usr/lib\*/urxvt/perl/clipboard, if paste_escaped is something that you don't use; it's not something that I use, so it's the solution that I went with.
* <code>C-M-s</code> is supposed to invoke <code>isearch-forward-regexp</code>, but instead it invokes a urxvtperl scrollback search. This was only a problem for me in my terminal. I never use it, so I simply removed "searchable-scrollback" from the URxvt.perl-ext-common line in my ~/.Xresources.
* I don't know what <code>C-&lt;TAB&gt;</code> is supposed to do (Emacs tells me <code>C-&lt;TAB&gt;</code> is undefined, but the Emacs manual says that it's bound to the command file-cache-minibuffer-complete); however, I know that if I wanted to use <code>C-&lt;TAB&gt;</code> in my terminal, I currently can't: a plain &lt;TAB&gt; is inserted instead. TODO: resolve the conflict and document how I resolved it.


## Numeric Arguments (aka Prefix Arguments)

A numeric argument (aka prefix argument) is a number (positive or negative or 0), specified before a command, to change the effect of the command. You can give any Emacs command a numeric argument. Some commands interpret the argument as a repetition count; some commands change their behaviour based on the numeric argument; some commands care whether there is an argument, but ignore its value; some commands treat a plain <code>C-u</code> (a C-u followed by no digits or minus sign) differently from an ordinary argument; some commands treat 0 specially if the numeric argument is treated as a repetition count (because a repetition count of 0 would otherwise be a no-op).

The term "prefix argument" ephasises the fact that the argument is specified before the command. "Prefix argument" is a synonym for "numeric argument."

To specify a numeric argument, you can type a digit and/or a minus sign while holding down the Alt key, followed by the command you want to invoke (you can invoke by key sequence or name). If you enter more than one digit, you don't need to hold down the Alt key for the second and subsequent digits. Numeric arguments are bound to either digit-argument (for positive numbers) or negative-argument (for negative numbers). For example, if you want to move down 25 lines, you could do <code>M-2 5 C-n</code> or <code>M-2 5 M-x next-line</code>.

Another way to specify a numeric argument is to type <code>C-u</code> (bound to the universal-argument command) followed by one or more digits, or (for a negative argument) a minus sign followed by one or more digits. C-u alone has the special meaning of "four times": it multiplies the argument for the next command by four; <code>C-u C-u</code> multiplies it by sixteen (4 * 4); and so on.

If you use a numeric argument with M-x, then the argument value will appear in the prompt string.

A minus sign without digits normally means -1.

You can use a numeric argument before a self-inserting character to insert multiple copies of it. If the character is a number, then you need to use <code>C-u</code> to terminate the prefix argument before typing the digit; for example, to append 6 zeros to your paycheque, you can do: <code>M-6 C-u 0</code> or <code>C-u 6 C-u 0</code>.

If you want to repeat a command that prompts for input or repeat a command that doesn't treat a numeric argument as a repetition count, then you need to use the command <code>C-x z</code> (<code>M-x repeat</code>). Repeating a command uses the same arguments that were used before; it does not read new arguments each time. To repeat the command more than once, type additional 'z''s: each 'z' repeats the command one more time. Repetition ends when you type a character other than 'z', or press a mouse button.


## Keyboard Macros

Keyboard macros are a way of defining new Emacs commands from sequences of existing ones, with no need to write a Lisp program. You can use a macro to record a sequence of commands, then play them back as many times as you like.

Basically, you invoke a command (typically via <code>&lt;F3&gt;</code>) to start recording a keyboard macro. From that point forward, everything you type will be recorded until you either end the macro definition (typically via <code>&lt;F4&gt;</code>) or cancel it (<code>C-g</code>). To invoke the most recently defined macro, you use the same key that you used to end the definition: <code>&lt;F4&gt;</code>. If you want to invoke the macro repeatedly, then use a prefix argument with <code>&lt;F4&gt;</code>.

After you've defined a keyboard macro, there are a few ways you can edit its definition: you can append a new definition to the end of the existing definition; edit the macro in a buffer with a specialised major mode for editing macros; or interactively edit the macro's definition one command at a time.

After you've defined a keyboard macro, you can optionally bind it to a name or a key sequence. If you change the macro's definition after you bind it, then you'll have to rebind it to get the updated definition on your command or key sequence. Once you've at least bound the macro to a name, then you can insert its definition (optionally with its key binding) into a buffer (usually your init file), so that you can save the macro for future Emacs sessions.

<dl>
  <dt><dfn>
  &lt;F3&gt;<br>
  M-x kmacro-start-macro-or-insert-counter<br>
  C-x (<br>
  M-x kmacro-start-macro</dfn></dt>
  <dd>
<p>Start the definition of a keyboard macro. Your keys will continue to be executed, but will also become part of the definition of the macro; this means that the first time you define a keyboard macro is also the first time you execute it. 'Def' appears in the mode line to remind you that you're defining a keyboard macro.</p>

<p>Most keyboard commands work as usual in a keyboard macro definition; however, typing <code>C-g</code> (<code>keyboard-quit</code>) quits the keyboard macro definition.</p>

<p>When a command reads an argument with the minibuffer, your minibuffer input becomes part of the macro along with the command, so when you replay the macro, the command gets the same argument as when you entered the macro.</p>

<p>Each keyboard macro has an associated counter, which is initialised to 0 when you start defining the macro. Each time &lt;F3&gt; appears in the macro definition, the counter's value is inserted into the buffer and then the counter's value is incremented. You can change what the increment is (default is 1) by using a numeric prefix argument. You can use this type of behaviour for doing things like making numbered lists.</p>

<p>If you use <code>C-x q</code> (or <code>M-x kbd-macro-query</code>) in your macro definition, then whenever <code>C-x q</code> is encountered when the macro is executed, the macro will pause and prompt you asking you how you'd like to proceed (continue executing; skip the remainder of this repetition of the macro and start right away with the next repetition; skip the remainder of this repetition and cancel further repetitions; enter a recursive editing level, in which you can perform editing which is not part of the macro).</p>
  </dd>

  <dt><dfn>
  &lt;F4&gt;<br>
  M-x kmacro-end-or-call-macro<br>
  C-x )<br>
  M-x kmacro-end-macro<br>
  C-x e<br>
  M-x kmacro-end-and-call-macro</dfn></dt>
  <dd>
<p>If a keyboard macro is being defined, end the definition; otherwise, execute the most recent keyboard macro.</p>

<p>You can supply a numeric prefix argument to invoke the macro a specified number of numbers. An argument of zero repeats the macro until it gets an error or until you type <code>C-g</code>.</p>
  </dd>

  <dt><dfn>
  C-u &lt;F3&gt;<br>
  C-u M-x kmacro-start-macro-or-insert-counter</dfn></dt>
  <dd>Start the definition of a keyboard macro by recording the execution of the previous macro, and then recording anything else you type before you end the macro definition.</dd>

  <dt><dfn>
  C-u C-u &lt;F3&gt;<br>
  C-u C-u M-x kmacro-start-macro-or-insert-counter</dfn></dt>
  <dd>Start the definition of a keyboard macro based on the previous macro, but without executing the previous macro. Anything else you type will be recorded and appended to the definition until you end the macro definition.</dd>

  <dt><dfn>
  C-x C-k n<br>
  M-x kmacro-name-last-macro</dfn></dt>
  <dd>Bind the most recently defined keyboard macro to a command name for the duration of the Emacs session.</dd>

  <dt><dfn>
  C-x C-k b<br>
  M-x kmacro-bind-to-key</dfn></dt>
  <dd>
<p>Bind the most recently defined keyboard macro to a key sequence for the duration of the Emacs session.</p>

<p>To avoid problems caused by overriding existing bindings, the key sequences <code>C-x C-k 0</code> through <code>C-x C-k 9</code> and <code>C-x C-k A</code> through <code>C-x C-k Z</code> are reserved for your own keyboard macro bindings (or any other custom bindings). To bind to one of those key sequences, you only need to type the digit or letter rather than the whole key sequence; for example, <code>C-x C-k b 4</code> instead of <code>C-x C-k b C-x C-k 4</code>, although either way will work.</p>
  </dd>

  <dt><dfn>
  M-x insert-kbd-macro &lt;RET&gt; MACRO-NAME</dfn></dt>
  <dd>If a macro is bound to the specified name (use <code>C-x C-k n</code> before you invoke <code>M-x insert-kbd-macro</code>), then insert its definition in Lisp code into the current buffer. If you use a prefix argument, then any key bindings for the macro will also be inserted into the buffer. The reason for being able to insert the macro's definition into the buffer, is so that you can persist the macro across Emacs sessions. You would typically insert the macro's definition and key bindings into your init file or into a Lisp file that you would then load with <code>M-x load-file</code>.</dd>

  <dt><dfn>
  C-x C-k C-e<br>
  M-x kmacro-edit-macro</dfn></dt>
  <dd>Enter a buffer with a specialised major mode for editing the most recently defined keyboard macro. Press <code>C-h m</code> for help once in that buffer.</dd>

  <dt><dfn>
  C-x C-k e MACRO-NAME-OR-KEY<br>
  M-x edit-kbd-macro &lt;RET&gt; MACRO-NAME-OR-KEY</dfn></dt>
  <dd>Enter a buffer with a specialised major mode for editing the specified keyboard macro. Press <code>C-h m</code> for help once in that buffer.</dd>

  <dt><dfn>
  C-x C-k l<br>
  M-x kmacro-edit-lossage</dfn></dt>
  <dd>Enter a buffer with a specialised major mode for editing your last 300 keystrokes as a keyboard macro. Press <code>C-h m</code> for help once in that buffer.</dd>

  <dt><dfn>
  C-x C-k &lt;SPC&gt;<br>
  M-x kmacro-step-edit-macro</dfn></dt>
  <dd>Interactively replay and edit the most recently defined keyboard macro, one command at a time (remember, a keyboard macro is made up of one or more commands). Press <code>?</code> for help.</dd>
</dl>


## Quoting

Only graphic characters can be inserted by typing the associated key; other keys act as editing commands and do not insert themselves. Quoting means depriving a character of its usual special significance.

To insert a non-graphic character, type <code>C-q</code> and then the character.

<code>C-q</code> (<code>M-x quoted-insert</code>) followed by a sequence of octal digits inserts the character with the specified octal character code. You can use any number of octal digits; any non-digit terminates the octal sequence. To use decimal or hexadecimal instead of octal, set the variable <code>read-quoted-char-radix</code> to 10 or 16. If the radix is 16, the letters 'a' to 'f' serve as part of the character code, just like digits. Case is ignored.

Quoting a file name turns off the special significance of constructs such as <code>$</code>, <code>~</code>, and <code>:</code>.

<dl>
  <dt><dfn>
  C-q C-S-2</dfn></dt>
  <dd>Null (caret notation: ^@; C escape code: \0).</dd>

  <dt><dfn>
  C-q C-g</dfn></dt>
  <dd>Bell (caret notation: ^G; C escape code: \a).</dd>

  <dt><dfn>
  C-q C-h</dfn></dt>
  <dd>Backspace (caret notation: ^H; C escape code: \b).</dd>

  <dt><dfn>
  C-q C-i</dfn></dt>
  <dd>Horizontal tab (caret notation: ^I; C escape code: \t).</dd>

  <dt><dfn>
  C-q C-j</dfn></dt>
  <dd>Line feed (caret notation: ^J; C escape code: \n).</dd>

  <dt><dfn>
  C-q C-k</dfn></dt>
  <dd>Vertical tab (caret notation: ^K; C escape code: \v).</dd>

  <dt><dfn>
  C-q C-l</dfn></dt>
  <dd>Form feed (caret notation: ^L; C escape code: \f).</dd>

  <dt><dfn>
  C-q C-m</dfn></dt>
  <dd>Carriage return (caret notation: ^M; C escape code: \r).</dd>

  <dt><dfn>
  C-q C-[</dfn></dt>
  <dd>Escape (caret notation: ^[; C escape code: \e).</dd>
</dl>

If you want to insert ASCII control characters literally, then look up their value in caret notation (the caret stands for the Ctrl key); for example, end of file is ^D, which means C-d, so to insert that control character literally, type <code>C-q</code> to quote the following character, and then type <code>C-d</code> as the character you want to quote and insert literally. To find the caret notation for ASCII control characters, search for something like "C0 control codes."

Caret notation is used for the 33 ASCII control characters. The notation consists of a caret (^) followed by a character in the ASCII range from ? to \_ (look at an ASCII table); this digraph stands for the ASCII control character that has the numerical equivalent to the characters's position in the range from ? to \_: ? is -1 (for ASCII control character 127), @ is 0 (for ASCII control character 0), A is 1, Z is 26, \[ is 27, and \_ is 31. For the letters, it's easy, because it's the position in the alphabet (A is the first, M is the 13th letter, Z is the 26th letter). ASCII control character 10 is the line feed (\\n) character. The 10th letter of the alphabet is J, so the caret notation for \\n is ^J. ASCII control character 27 is the escape (\\e) character. The first character after Z ("letter 27") in the ASCII table is \[, so the caret notation for escape is ^\[.


## Inserting Non-ASCII Characters

<code>C-x 8</code> (<code>M-x insert-char</code>) prompts for the Unicode name or codepoint of a character. The codepoint can be specified in hexadecimal, octal, binary, or any other radix between 2 and 36. The syntax in Emacs for inserting non-decimal numbers is to insert a '#'; followed by either a 'b' for binary, 'o' for octal, 'x' for hex, or '<num>r' for anything else; followed by the digits written in the specified radix. Case is not significant for the letter that specifies the radix.

An input method is a system for entering non-ASCII text characters by typing sequences of ASCII characters; for example, typing pinyin (romanised Chinese) to enter Chinese characters. I haven't used an input method in Emacs before, so won't go into detail, but here's how you can get started:

<dl>
  <dt><dfn>
  M-x list-input-methods</dfn></dt>
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

  <dt><dfn>
  C-\<br>
  M-x toggle-input-method</dfn></dt>
  <dd>Toggle the use of the selected input method.</dd>
</dl>


## Useful Commands to Memorise

<dl>
  <dt><dfn>
  C-x C-c<br>
  M-x save-buffers-kill-terminal</dfn></dt>
  <dd>
<p>Exit/quit/terminate/kill Emacs.</p>

<p>If there are any unsaved buffers, Emacs will ask you if you'd like to save them before exiting.</p>

<p>If there are any running subprocesses, Emacs will tell you and ask you if you'd still like to kill Emacs (and thus also kill any of its subprocesses).</p>

<p>All frames will be closed.</p>
  </dd>

  <dt><dfn>
  C-g<br>
  &lt;ESC&gt; &lt;ESC&gt; &lt;ESC&gt;</dfn></dt>
  <dd>
<p>Cancel something.</p>

<p>Quitting means cancelling a partially typed command or a running command. Quitting Emacs is called killing it.</p>

<p><code>C-g</code> and <code>&lt;ESC&gt; &lt;ESC&gt; &lt;ESC&gt;</code> are similar, but not exactly.</p>

<p><code>C-g</code> doesn't invoke a command (instead, it sets a variable that Emacs frequently checks), so it can be used to stop commands.</p>

<p><code>&lt;ESC&gt; &lt;ESC&gt; &lt;ESC&gt;</code> can't stop commands because it invokes a command, which wouldn't be executed until the previous command finished executing. The good thing is that <code>&lt;ESC&gt; &lt;ESC&gt; &lt;ESC&gt;</code> works in most other situations. The annoying thing is that you have to type <code>&lt;ESC&gt;</code> exactly 3 times.</p>
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

<p>If you keep invoking the undo command, then you'll keep undoing earlier and earlier changes. To quote the Emacs manual "Any command other than an undo command breaks the sequence of undo commands. Starting from that moment, the entire sequence of undo commands that you have just performed are themselves placed into the undo record, as a single set of changes. Therefore, to re-apply changes you have undone, type <code>C-f</code> or any other command that harmlessly breaks the sequence of undoing; then type <code>C-/</code> to undo the undo command[, thus performing a redo]. If you want to resume undoing, without redoing previous undo commands, use <code>M-x undo-only</code>. This is like <code>undo</code>, but will not redo changes you have just undone."</p>

<p>Basically, to redo something, you undo its corresponding undo.</p>

<p>The undo command applies only to changes in the buffer; you can't use it to undo cursor motion.</p>

<p>Note that you can select a region and undo only the changes within that region. That is called a "selective undo". When the region is active, then <code>C-/</code> will undo changes in the region; when the region is not active, then <code>C-u C-/</code> will undo changes in the region.</p>
  </dd>

  <dt><dfn>
  M-x revert-buffer</dfn></dt>
  <dd>
<p>Undo all changes in the current buffer.</p>

<p>Rather than doing this, you could also just quit Emacs without saving your changes.</p>
  </dd>

  <dt><dfn>
  C-x o<br>
  M-x other-window</dfn></dt>
  <dd>
<p>Switch windows.</p>

<p><code>C-x o</code> cycles through the windows generally top to bottom and left to right. When the minibuffer is active, the minibuffer is the last window in the cycle.</p>

<p><code>M-x windmove-default-keybindings</code> makes it much easier for you to move to the window you want by binding some convenience commands to <code>S-&lt;left&gt;</code>, <code>S-&lt;right&gt;</code>, <code>S-&lt;up&gt;</code>, and <code>S-&lt;down&gt;</code> (you only need to run <code>M-x windmove-default-keybindings</code> once). Unfortunately, those key bindings will break shift selection. If you want shift selection and a convenient way to select windows, then you should bind the <code>windmove-left</code>, <code>windmove-right</code>, <code>windmove-up</code>, and <code>windmove-down</code> commands to keys that won't conflict with anything else.</p>
  </dd>

  <dt><dfn>
  C-x 0<br>
  M-x delete-window</dfn></dt>
  <dd>Delete the selected window, but not its buffer.</dd>

  <dt><dfn>
  C-x 4 0<br>
  M-x kill-buffer-and-window</dfn></dt>
  <dd>Delete the selected window and its buffer.</dd>

  <dt><dfn>
  C-x 1<br>
  M-x delete-other-windows</dfn></dt>
  <dd>
<p>Delete all the windows (but not their buffers) in the selected frame except for the selected window.</p>

<p>You cannot use the command while in the minibuffer.</p>
  </dd>

  <dt><dfn>
  C-x &lt;left&gt;<br>
  M-x previous-buffer</dfn></dt>
  <dd>Select the previous buffer.</dd>
</dl>


# Killing or Suspending Emacs

Emacs uses the term "quitting" for what you probably think of as "cancelling." Emacs defines a couple meanings for the term "killing", one of which means to exit Emacs (what you might think of as "quitting").

<dl>
  <dt><dfn>
  C-x C-c<br>
  M-x save-buffers-kill-terminal</dfn></dt>
  <dd>
<p>Exit/quit/terminate/kill Emacs.</p>

<p>If there are any unsaved buffers, Emacs will ask you if you'd like to save them before exiting.</p>

<p>If there are any running subprocesses, Emacs will tell you and ask you if you'd still like to kill Emacs (and thus also kill any of its subprocesses).</p>

<p>All frames will be closed.</p>
  </dd>

  <dt><dfn>
  M-x kill-emacs</dfn></dt>
  <dd>Exit/quit/terminate/kill Emacs without being prompted about saving.</dd>

  <dt><dfn>
  C-z<br>
  C-x C-z<br>
  M-x suspend-frame</dfn></dt>
  <dd>
<p>In terminal Emacs, suspend Emacs; in graphical Emacs, minimise the selected frame.</p>

<p>In terminal Emacs, in most shells, you can resume Emacs using the shell command <code>%emacs</code>. If that doesn't work, try <code>jobs emacs</code>, and then use the number in brackets as the arg to <code>fg</code>, or if Emacs is the job that was most recently suspended, placed in the background, or run as a background job, then a simple <code>fg</code> with no args should work.
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
  <dd>Display the documentation for the given Emacs variable. If you specify "?" as the variable name, then all variables are listed.</dd>

  <dt><dfn>
  C-h a PATTERN<br>
  &lt;F1&gt; a PATTERN<br>
  M-x apropos-command &lt;RET&gt; PATTERN</dfn></dt>
  <dd>
<p>Display a list of commands that match PATTERN.</p>

<p>An apropos pattern means either a word, a space-delimited list of words, or a regular expression. If a list of words is given, the apropos will match anything that contains at least two of the words.</p>
  </dd>

  <dt><dfn>
  M-x apropos PATTERN</dfn></dt>
  <dd>Display a list of commands and variables that match PATTERN.</dd>

  <dt><dfn>
  M-x apropos-variable PATTERN</dfn></dt>
  <dd>Display a list of user-customisable variables that match PATTERN. With a prefix argument, search for non-customisable variables too.</dd>

  <dt><dfn>
  M-x apropos-value</dfn></dt>
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
  <dd>
<p>Display the Emacs Lisp reference manual.</p>

<p>The Elisp reference manual looks really useful, but I think it's okay to just read the Emacs Lisp Intro for now and come to the Elisp reference when you actually need it; otherwise, it's just too many details that will probably all go over your head.</p>
  </dd>

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

  <dt><dfn>
  C-u C-h a .*<br>
  C-h f ?</dfn></dt>
  <dd>Display a list of all commands.</dd>

  <dt><dfn>
  C-u C-h a .*-mode<br>
  C-h f -mode?</dfn></dt>
  <dd>Display a list of all modes.</dd>

  <dt><dfn>
  C-u M-x apropos-variable .*<br>
  C-h v ?</dfn></dt>
  <dd>Display a list of all variables.</dd>

  <dt><dfn>
  C-u M-x apropos-variable .*-hook<br>
  C-h v -hook?</dfn></dt>
  <dd>Display a list of all hooks.</dd>
</dl>

Note that modes correspond to commands, so if you want to read the documentation for a mode, just look up its documentantation by its command name.

<code>C-h c</code>, <code>C-h k</code>, and <code>C-h K</code> work for any sort of key sequences, including function keys, menus, and mouse events; for example, after <code>C-h k</code>, you can select a menu item from the menu bar, to view the documentation string of the command it runs.

In a help buffer, you can use <code>&lt;SPC&gt;</code> to scroll forward and <code>&lt;DEL&gt;</code> to scroll backward. When a function name, variable name, or face name appears in the documentation in the help buffer, it is normally an underlined hyperlink. To view the associated documentation, move point there and type <code>&lt;RET&gt;</code>, or click on the hyperlink. Doing so replaces the contents of the help buffer; to retrace your steps, type <code>C-c C-b</code> (<code>M-x help-go-back</code>). A help buffer can also contain hyperlinks to Info manuals, source code definitions, and URLs (Web pages). The first two are opened in Emacs, and the third using a Web browser via the browse-url command. To move to the next hyperlink in a help buffer, use <code>&lt;TAB&gt;</code>. To move to the previous hyperlink, use <code>S-&lt;TAB&gt;</code>. <code>&lt;TAB&gt;</code> and <code>S-&lt;TAB&gt;</code> act cyclically, so if you're on the last hyperlink, <code>&lt;TAB&gt;</code> moves to the first hyperlink; if you're on the first hyperlink, <code>S-&lt;TAB&gt;</code> moves to the last hyperlink. If a variable, function, or face name isn't hyperlinked, you can still views its documentation by moving point to the symbol and then typing <code>C-c C-c</code> (<code>M-x help-follow-symbol</code>). To exit a help buffer, press <code>q</code>.

When you're in a buffer that's not meant for inserting text, you can usually press <code>h</code> or <code>?</code> for help. If you're in a buffer that's meant for inserting text, then you could use <code>C-h m</code> instead.

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
  <dt><dfn>
  n</dfn></dt>
  <dd>Move to the next node at the same level as the current node.</dd>

  <dt><dfn>
  p</dfn></dt>
  <dd>Move to the previous node at the same level as the current node.</dd>

  <dt><dfn>
  u<br>
  ^</dfn></dt>
  <dd>Move up to the parent node.</dd>

  <dt><dfn>
  t</dfn></dt>
  <dd>Move to the top node of the manual.</dd>

  <dt><dfn>
  l</dfn></dt>
  <dd>Retrace your steps. As you move from node to node, Info records the nodes where you have been in a special history list. The l command revisits nodes in the history list; each successive l command moves one step back through the history.</dd>

  <dt><dfn>
  r</dfn></dt>
  <dd>r is the opposite of l. It moves forward in the history list.</dd>

  <dt><dfn>
  ]</dfn></dt>
  <dd>Move to the next node regardless of level.</dd>

  <dt><dfn>
  [</dfn></dt>
  <dd>Move to the previous node regardless of level.</dd>

  <dt><dfn>
  &lt;SPC&gt;</dfn></dt>
  <dd>Scroll forward if there is still text to scroll forward to; otherwise, move to the next node regardless of level.</dd>

  <dt><dfn>
  &lt;DEL&gt;</dfn></dt>
  <dd>Scroll backward if there is still text to scroll back to; otherwise, move to the previous node regardless of level.</dd>

  <dt><dfn>
  C-v</dfn></dt>
  <dd>Scroll forward, but don't move to the next node if the bottom of the node has been reached.</dd>

  <dt><dfn>
  M-v</dfn></dt>
  <dd>Scroll backward, but don't move to the previous node if the top of the node has been reached.</dd>

  <dt><dfn>
  b</dfn></dt>
  <dd>Immediately scroll to the top of the current node.</dd>

  <dt><dfn>
  ?</dfn></dt>
  <dd>Display a list of Info commands.</dd>

  <dt><dfn>
  m NODE_NAME</dfn></dt>
  <dd>
<p>Go to the node that has the specified name.</p>

<p>A menu is a list of other nodes you can move to. The beginning of a menu is always identified by a line which starts with '* Menu:'. A node contains a menu if and only if it has a line in it which starts that way. The only menu you can use at any moment is the one in the node you are in. To use a menu in any other node, you must move to that node first.</p>

<p>You can abbreviate the node name. If the abbreviation is not unique, the first matching node is chosen. Some menus put the shortest possible abbreviation for each node name in capital letters, so you can see how much you need to type. It does not matter whether you use upper case or lower case when you type the node name. If you type &lt;TAB&gt; after entering part of a name, it will fill in more of the name--as much as Info can deduce from the part you have entered. You can also move point over a node name, and then press &lt;RET&gt;. You can type &lt;TAB&gt; to move point to the next item in the menu and type S-&lt;TAB&gt; to move point to the previous item in the menu.</p>

<p>If you type <code>?</code> as the node name, then a list of possible menu items will appear.</p>

<p>Rather than using <code>m</code> and specifying a node name, you can enter a digit from 1 to 9 to access items in the menu.</p>

<p>If you invoke <code>m</code> with a prefix argument (thus, <code>C-u m NODE_NAME</code>), then the node you specify will be opened in a new Info buffer.</p>
  </dd>

  <dt><dfn>
  f CROSS_REFERENCE</dfn></dt>
  <dd>
<p>Go to the cross reference that has the specified name.</p>

<p>A cross reference is a link that doesn't appear in a menu.</p>

<p>You can type &lt;TAB&gt; to move point to the next cross reference and type S-&lt;TAB&gt; to move point to the previous cross reference.</p>

<p>If you type <code>?</code> as the cross reference name, then a list of possible cross reference names will appear.</p>
  </dd>

  <dt><dfn>
  g NODE_NAME</dfn></dt>
  <dd>
<p>Go to the node that has the specified name. The difference between this and <code>m</code> is that <code>m</code> only accepts names of nodes that appear in the current node's menu; whereas, <code>g</code> accepts the name of any node whether it's in the menu or not.</p>

<p>If you specify <code>*</code> as the node name, then the whole file will be displayed.</p>

<p>To go to a node in another file, you can include the file name in the node name by putting it at the front, in parentheses; for example, <code>g (emacs)Top &lt;RET&gt;</code> will take you to the top node of the Emacs manual.</p>

<p>If you invoke <code>g</code> with a prefix argument (thus, <code>C-u g NODE_NAME</code>), then the node you specify will be opened in a new Info buffer.</p>
  </dd>

  <dt><dfn>
  d</dfn></dt>
  <dd>Go to the Directory node, which is a node that lists all the manuals and other Info documents that are installed on your system.</dd>

  <dt><dfn>
  M-n</dfn></dt>
  <dd>Clone the current Info buffer in another window.</dd>

  <dt><dfn>
  i TOPIC</dfn></dt>
  <dd>
<p>Search the index for a specified topic and go to the node which is listed in the index for that topic.</p>

<p>To search for keys, use the notation that the Emacs documentation uses; for example, <code>i C-n</code>, where you literally spell out uppercase C, hyphen, lowercase n (rather than holding Ctrl and pressing n).</p>
  </dd>

  <dt><dfn>
  s STRING</dfn></dt>
  <dd>Search the entire manual for the specified string.</dd>

  <dt><dfn>
  L</dfn></dt>
  <dd>Display a menu of all the nodes you've visited. You can jump to one of those nodes by selecting it from the menu.</dd>

  <dt><dfn>
  T</dfn></dt>
  <dd>Go to the table of contents of the current Info file.</dd>

  <dt><dfn>
  &lt;</dfn></dt>
  <dd>Move to the top node of the current Info file.</dd>

  <dt><dfn>
  &gt;</dfn></dt>
  <dd>Move to the last node of the current Info file.</dd>

  <dt><dfn>
  q</dfn></dt>
  <dd>Quit Info.</dd>

  <dt><dfn>
  C-u C-h i</dfn></dt>
  <dd>Open an Info file that isn't listed in the Directory node.</dd>

  <dt><dfn>
  M-x info-apropos STRING</dfn></dt>
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
* In graphical mode, each window has a **scrollbar**. The echo area and minibuffer also have a scrollbar.
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
* After point means the character at or on the cursor.
* **Mark** points to a position in the text. It specifies one end of the region, point being the other end.
* The **region** is the text between point and the mark. When the region is active, it's highlighted.
* The **empty region** is when mark and point refer to the same spot.
* A **rectangle** consists of the text in a given range of columns on a given range of lines. It's a type of region.
* The **empty rectangle** is when point and mark are in the same column. If they are in the same line, then the rectangle is one line high.
* **Active text** refers to text that does something special in response to mouse clicks or &lt;RET&gt;. You can move your point over the active text, and then type <code>C-h .</code> to display some help text for it in the echo area.
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
        * <code>U</code> means utf-8-unix.
        * <code>1</code> means iso-latin-1-unix.
        * <code>=</code> means no-conversion (usually used for binary files).
    * End-of-line convention used in the buffer.
        * <code>:</code> or (Unix) means Unix-style (\\n).
        * <code>/</code> or (Mac) means Mac-style (\\r).
        * <code>\\</code> or (DOS) means DOS-style (\\r\\n).
    * Read-only flag.
        * <code>-</code> means that the buffer is writable and unmodified.
        * <code>*</code> means that the buffer is writable and modified.
        * <code>%</code> means that the buffer is read-only.
    * Modification state.
        * <code>-</code> means that the buffer is unmodified.
        * <code>*</code> means that the buffer is modified.
        * <code>%</code> means that the read-only buffer is unmodified.
    * Directory location flag.
        * <code>-</code> means that the buffer's current directory is local.
        * <code>@</code> means that the buffer's current directory is remote.
    * The name of the buffer, which is usually the same name as the file you are editing. For buffers that aren't associated with files, the buffer name is surrounded by asterisks.
    * Position in the file.
        * <code>All</code> means that the entire buffer is visible.
        * <code>Top</code> means that the very beginning of the buffer is visible and that there is text that can be scrolled down to.
        * <code>Bot</code> means that the very end of the buffer is visible and that there is text that can be scrolled up to.
        * <code>nn%</code> means that nn% of the buffer is above the top of the window and that there is text that can be scrolled up or down to.
    * The character 'L' followed by the line number at point.
    * (
    * The name of the major mode being used. Some major modes also display additional information after the major mode name.
    * A list of the minor mode names and feature names (such as Narrow) being used.
    * )
* Terminal-Emacs mode line format:
    * -
    * If an input method is being used, then its name is displayed; otherwise, this field is not included in the mode line.
    * The keyboard input coding system.
    * The terminal output coding system.
    * The coding system of the text in the buffer.
        * <code>U</code> means utf-8-unix.
        * <code>1</code> means iso-latin-1-unix.
        * <code>=</code> means no-conversion (usually used for binary files).
    * End-of-line convention used in the buffer.
        * <code>:</code> or (Unix) means Unix-style (\\n).
        * <code>/</code> or (Mac) means Mac-style (\\r).
        * <code>\\</code> or (DOS) means DOS-style (\\r\\n).
    * Read-only flag.
        * <code>-</code> means that the buffer is writable and unmodified.
        * <code>*</code> means that the buffer is writable and modified.
        * <code>%</code> means that the buffer is read-only.
    * Modification state.
        * <code>-</code> means that the buffer is unmodified.
        * <code>*</code> means that the buffer is modified.
        * <code>%</code> means that the read-only buffer is unmodified.
    * Directory location flag.
        * <code>-</code> means that the buffer's current directory is local.
        * <code>@</code> means that the buffer's current directory is remote.
    * -
    * The name of the selected frame. The initial frame's name is F1, and subsequent frames are usually named F2, F3, and so on.
    * The name of the buffer, which is usually the same name as the file you are editing. For buffers that aren't associated with files, the buffer name is surrounded by asterisks.
    * Position in the file.
        * <code>All</code> means that the entire buffer is visible.
        * <code>Top</code> means that the very beginning of the buffer is visible and that there is text that can be scrolled down to.
        * <code>Bot</code> means that the very end of the buffer is visible and that there is text that can be scrolled up to.
        * <code>nn%</code> means that nn% of the buffer is above the top of the window and that there is text that can be scrolled up or down to.
    * The character 'L' followed by the line number at point.
    * (
    * The name of the major mode being used. Some major modes also display additional information after the major mode name.
    * A list of the minor mode names and feature names (such as Narrow) being used.
    * )

If Emacs is inside a recursive editing level, square brackets appear around the parentheses that surround the modes. If Emacs is in one recursive editing level within another, double square brackets appear, and so on. Since recursive editing levels affects Emacs globally, the square brackets appear in the mode line of every window.

When reading Info pages, I noticed that there's some additional stuff after the buffer name in the mode line: <code>(FILENAME) NODE_NAME</code>. This suggests to me that some modes customise the mode line format.

There are different things that you can optionally add to the mode line, each of which can usually be displayed by enabling a mode; for example, size of the buffer (<code>size-indication-mode</code>), column number of point (<code>column-number-mode</code>), current time (<code>display-time-mode</code>), and battery charge (<code>display-battery-mode</code>). If you don't want to the see the line number of point, then you can toggle the line-number-mode off. There are several Emacs packages out there that provide additional mode line features; two common ones are [Power Line](http://www.emacswiki.org/emacs/PowerLine) and [Smart Mode Line](https://github.com/Bruce-Connor/smart-mode-line).

When only line-number-mode is enabled, then you'll see L followed by the line number. When only column-number-mode is enabled, then you'll see C followed by the column number. When both line-number-mode and column-number-mode are enabled, you'll see two numbers in parentheses: <code>(LineNumber, ColumnNumber)</code>.


## Menu Bar


### GUI

You can use the mouse to choose a command from the menu bar. An arrow on the right edge of a menu item means it leads to a submenu. A '...' at the end of a menu item means that the command will prompt you for further input before it actually does anything. Some menu items show what key sequence you can use for invoking the corresponding command.

To view the full command name and documentation for a menu item, type <code>C-h k</code>, and then select the menu bar with the mouse in the usual way. You can't do this in terminal Emacs.

Instead of using the mouse, you can also invoke the first menu bar item by pressing <code>&lt;F10&gt;</code> (to run the command <code>menu-bar-open</code>). You can then navigate the menus with the arrow keys. To activate a selected menu item, press <code>&lt;RET&gt;</code>. To cancel menu navigation, press <code>&lt;ESC&gt;</code>.


### Terminal

You can use the menu bar by typing <code>M-`</code> or <code>&lt;F10&gt;</code> (both of which run the command <code>tmm-menubar</code>). You can use the up and down arrow keys to move through the menu to different items, and then you can type <code>&lt;RET&gt;</code> to select the item. Each menu item is also designated by a letter or digit (usually the initial of some word in the item's name). This letter or digit is separated from the item name by '==>'. You can type the item's letter or digit to select the item.

When you're in the menu bar's minibuffer, you can press <code>&lt;PageUp&gt;</code> to move to the Completions buffer, where you can move point to the menu item you want and then press <code>&lt;RET&gt;</code> to select it.


## Minibuffer

The minibuffer is where Emacs commands read complicated arguments, such as file names, buffer names, command names, or Lisp expressions. When the minibuffer is in use, it appears in the echo area with a cursor. The minibuffer starts with a prompt string, which states what kind of input is expected. The prompt string usually ends with a colon and stands out from the input text. Sometimes, the prompt shows a default argument, inside parentheses before the colon. This default will be used as the argument if you just type <code>&lt;RET&gt;</code> without entering anything else (in other words, when you submit an empty string).

The minibuffer doesn't have a mode line.

If an error message or an informative message is emitted while the minibuffer is active, the message hides the minibuffer for a few seconds, or until you type something; then the minibuffer comes back.

Normally, the minibuffer window occupies a single screen line; however, if you add two or more lines' worth of text into the minibuffer, it expands automatically to accomodate the text (see the <code>resize-mini-windows</code> variable).

Since the minibuffer is just a buffer (with a small amount of screen space), you can use the usual basic Emacs keys for moving around (for example, <code>C-a</code> and <code>C-e</code>) and editing (for example, <code>C-k</code> and <code>C-/</code>) a line of text. You can also switch to another window and then come back to the minibuffer later. <code>C-a</code> in a minibuffer moves point to the beginning of the argument text, not the beginning of the prompt.

By default, you can't invoke anything that invokes the minibuffer (you can't use a minibuffer within another minibuffer); however, you can set the <code>enable-recursive-minibuffers</code> variable to 't', so that you can use a minibuffer within another minibuffer.

Since &lt;RET&gt; in the minibuffer submits the argument, you can't use it to insert a newline. Instead, you can use <code>C-q C-j</code> or <code>C-o</code>. This applies to other characters as well: if a character has a special meaning in the minibuffer, then quote it using <code>C-q</code>.

The minibuffer prompt string is read-only and cannot be changed. If you try to change it, then "Text is read-only" will briefly appear in the echo area.

When the minibuffer displays a password prompt, you are more limited in what you can do. Most of the features and commands associated with the minibuffer can not be used when entering a password. There is no history or completion, and you cannot change windows or perform any other actions with Emacs until you have submitted the password. While you are typing the password, you may press <code>&lt;DEL&gt;</code> to delete backwards, removing the last character entered. <code>C-u</code> deletes everything you have typed so far. <code>C-g</code> quits the password prompt. <code>C-y</code> inserts the current kill into the password. You may type either <code>&lt;RET&gt;</code> or <code>&lt;ESC&gt;</code> to submit the password. Any other self-inserting character key inserts the associated character into the password, and all other input is ignored. To prevent others from seeing your password, every password character you type is displayed as a dot ('.').

Sometimes, the minibuffer prompts you with a question with a list of possible values; these are called "yes or no" queries. There are two main types of "yes or no" queries:

1. The prompt ends with "(y or n)". Such a query does not actually use the minibuffer; the prompt appears in the echo area, and you answer by typing either 'y' or 'n', which immediately delivers the response. Because this query does not actually use the minibuffer, the usual minibuffer editing commands cannot be used.
2. The second type of "yes or no" prompt is typically used if giving the wrong answer could have serious consequences. It uses the minibuffer and features a prompt ending with "(yes or no)". To answer, you must type either 'yes' or 'no' into the minibuffer, followed by <code>&lt;RET&gt;</code>. Since this type of query uses the minibuffer, you can use the usual minibuffer commands.

Every argument that you enter with the minibuffer is saved in a minibuffer history list, so that you can easily reuse the argument next time you use the minibuffer. Emacs actually keeps separate history lists for several different kinds of arguments: file names, buffer names, command names, and command arguments.

<dl>
  <dt><dfn>
  M-p<br>
  &lt;Up&gt;</dfn></dt>
  <dd>Replace the contents of the minibuffer with the previous history item (cycle backwards).</dd>

  <dt><dfn>
  M-n<br>
  &lt;Down&gt;</dfn></dt>
  <dd>
<p>Replace the contents of the minibuffer with the next history item (cycle forwards).</p>

<p>If you type <code>M-n</code> (or <code>&lt;Down&gt;</code>) in the minibuffer when you're on the last item in the history list, then Emacs will start cycling through a list of default arguments (values that you are likely to enter). You can think of the list of default arguments as a "future history" list.
  </dd>
</dl>

If you edit the text inserted by <code>M-p</code> or <code>M-n</code>, this does not change its entry in the history list; however, the edited argument does go at the end of the history list when you submit it.

Every command that uses the minibuffer is saved in a command history list, together with the value of its arguments, so that you can repeat the entire command. You won't see your previous incremental searches in the minibuffer, unless you set <code>isearch-resume-in-command-history</code> to true.

<dl>
  <dt><dfn>
  C-x &lt;ESC&gt; &lt;ESC&gt;</dfn></dt>
  <dd>
<p>Turn the previous command into a Lisp expression and then enter a minibuffer initialised with the text for that expression. If you type just &lt;RET&gt;, that repeats the command unchanged. You can also change the command by editing the Lisp expression before you execute it.</p>

<p>A numeric argument to <code>C-x &lt;ESC&gt; &lt;ESC&gt;</code> specifies which command to repeat; 1 means the last one, 2 the previous, and so on.</p>

<p>Once inside the minibuffer for <code>C-x &lt;ESC&gt; &lt;ESC&gt;</code>, you can use the usual minibuffer history commands to move through the history list.</p>
  </dd>

  <dt><dfn>
  M-x list-command-history</dfn></dt>
  <dd>Display a list of the entire command history.</dd>
</dl>


## Frames

All frames created in the same Emacs session have access to the same underlying buffers and other data.

It's possible to create multiple frames on text terminals; such frames are displayed one at a time, filling the entire terminal screen.

If you don't give a frame a name, then the default name is of the form FN, where N is an integer indicating the frame number (first frame is F1, second frame is F2, and so on).

<dl>
  <dt><dfn>
  C-x 5 2<br>
  M-x make-frame-command</dfn></dt>
  <dd>Create a new frame.</dd>

  <dt><dfn>
  C-x 5 0<br>
  M-x delete-frame</dfn></dt>
  <dd>Delete the selected frame.</dd>

  <dt><dfn>
  C-x 5 o<br>
  M-x other-frame</dfn></dt>
  <dd>Switch frames.</dd>

  <dt><dfn>
  C-x 5 1<br>
  M-x delete-other-frames</dfn></dt>
  <dd>Delete all the frames except for the selected one.</dd>
  
  <dt><dfn>
  M-x set-frame-name &lt;RET&gt; FRAME_NAME</dfn></dt>
  <dd>Rename the selected frame.</dd>

  <dt><dfn>
  M-x select-frame-by-name &lt;RET&gt; FRAME_NAME</dfn></dt>
  <dd>Select the specified frame by its name.</dd>

  <dt><dfn>
  M-x fit-frame-to-buffer</dfn></dt>
  <dd>Adjust the selected frame's height to display its buffer's contents exactly (if it can fit in the maximum height of the frame); otherwise, adjust the selected frame's height to the maximum height that your window manager will allow.</dd>

  <dt><dfn>
  M-x make-frame<br>
  M-x new-frame</dfn></dt>
  <dd>Clone the selected buffer into a new frame.</dd>
</dl>


## Windows

Each window belongs to one and only one frame and each window displays only one buffer at any time. Multiple windows can display parts of different buffers, or different parts of one buffer. If a single buffer appears in more than one window, then any changes in its text are displayed in all the windows where it appears.

The minibuffer is special. Don't expect all the window commands to work in the minibuffer; for example, you cannot split the minibuffer. You also can't make the minibuffer the only remaining window and you cannot delete the minibuffer.

Remember, each window is associated with one buffer. Instead of switching windows, you can switch buffers. Also, if you're already visiting a file in a buffer, then you can switch to that buffer by visiting the file again (<code>C-x C-f</code>): when you try visiting a file that is already in a buffer, then Emacs will switch to that buffer rather than opening a new buffer.

<dl>
  <dt><dfn>
  C-x 2<br>
  M-x split-window-below</dfn></dt>
  <dd>Split the selected window horizontally into two separate windows, one above the other. After splitting, the selected window is the top one and both windows have the same value of point as before.</dd>

  <dt><dfn>
  C-x 3<br>
  M-x split-window-right</dfn></dt>
  <dd>
<p>Split the selected window vertically into two separate windows, positioned side by side. After splitting, the selected window is the one on the left and both windows have the same value of point as before.</p>

<p>If the windows are too narrow, then long lines will be truncated (see the <code>truncate-partial-width-windows</code> variable).</p>
  </dd>

  <dt><dfn>
  C-x o<br>
  M-x other-window</dfn></dt>
  <dd>
<p>Switch windows.</p>

<p><code>C-x o</code> cycles through the windows generally top to bottom and left to right. When the minibuffer is active, the minibuffer is the last window in the cycle.</p>

<p><code>M-x windmove-default-keybindings</code> makes it much easier for you to move to the window you want by binding some convenience commands to <code>S-&lt;left&gt;</code>, <code>S-&lt;right&gt;</code>, <code>S-&lt;up&gt;</code>, and <code>S-&lt;down&gt;</code> (you only need to run <code>M-x windmove-default-keybindings</code> once). Unfortunately, those key bindings will break shift selection. If you want shift selection and a convenient way to select windows, then you should bind the <code>windmove-left</code>, <code>windmove-right</code>, <code>windmove-up</code>, and <code>windmove-down</code> commands to keys that won't conflict with anything else.</p>
  </dd>

  <dt><dfn>
  M-v<br>
  &lt;PageUp&gt;</dfn></dt>
  <dd>Select the completion list window.</dd>

  <dt><dfn>
  C-M-v<br>
  &lt;ESC&gt; C-v<br>
  M-x scroll-other-window</dfn></dt>
  <dd>
<p>Scroll up the next window that <code>C-x o</code> would select.</p>

<p>In the minibuffer, <code>C-M-v</code> scrolls the help window associated with the minibuffer, if any, rather than the next window in the standard cyclic order.</p>
  </dd>

  <dt><dfn>
  C-M-S-v<br>
  &lt;ESC&gt; C-S-v<br>
  M-x scroll-other-window-down</dfn></dt>
  <dd>Scroll down the next window that <code>C-x o</code> would select.</dd>

  <dt><dfn>
  C-x 0<br>
  M-x delete-window</dfn></dt>
  <dd>Delete the selected window, but not its buffer.</dd>

  <dt><dfn>
  C-x 4 0<br>
  M-x kill-buffer-and-window</dfn></dt>
  <dd>Delete the selected window and its buffer.</dd>

  <dt><dfn>
  C-x 1<br>
  M-x delete-other-windows</dfn></dt>
  <dd>
<p>Delete all the windows (but not their buffers) in the selected frame except for the selected window.</p>

<p>You cannot use this command while in the minibuffer.</p>

<p>When there are multiple windows open, <code>&lt;ESC&lt; &lt;ESC&lt; &lt;ESC&lgt;</code> acts like <code>C-x 1</code>.</p>
  </dd>

  <dt><dfn>
  C-x ^<br>
  M-x enlarge-window</dnf></dt>
  <dd>
<p>Make the selected window one line taller.</p>

<p>If you supply a positive numeric argument, then make the selected window that many lines taller. If you supply a negative argument, then make the selected window that many lines shorter.</p>
  </dd>

  <dt><dfn>
  C-x }<br>
  M-x enlarge-window-horizontally</dfn></dt>
  <dd>
<p>Make the selected window one column wider.</p>

<p>If you supply a positive numeric argument, then make the selected window that many columns wider. If you supply a negative argument, then make the selected window that many lines narrower.</p>
  </dd>

  <dt><dfn>
  C-x {<br>
  M-x shrink-window-horizontally</dfn></dt>
  <dd>
<p>Make the selected window one column narrower.</p>

<p>If you supply a positive numeric argument, then make the selected window that many columns narrower. If you supply a negative argument, then make the selected window that many lines wider.</p>
  </dd>

  <dt><dfn>
  M-x maximize-window</dfn></dt>
  <dd>Make the selected window as tall and wide as possible.</dd>

  <dt><dfn>
  M-x minimize-window</dfn></dt>
  <dd>Make the selected window as short and narrow as possible.</dd>

  <dt><dfn>
  C-x +<br>
  M-x balance-windows</dfn></dt>
  <dd>Even out the heights of all the windows in the selected frame, making their sizes as similar as possible.</dd>

  <dt><dfn>
  M-x balance-windows-area</dfn></dt>
  <dd>Adjust the area of all the windows in the selected frame, making their sizes as similar as possible.</dd>

  <dt><dfn>
  M-x fit-window-to-buffer</dfn></dt>
  <dd>Adjust the selected window's height to display its buffer's contents exactly (if it can fit in the height of the frame); otherwise, adjust the selected window's height to the height of the frame.</dd>

  <dt><dfn>
  M-x delete-windows-on &lt;RET&gt; BUFFER_NAME</dfn></dt>
  <dd>Delete all windows showing the specified buffer.</dd>
</dl>

If you enable Winner mode (<code>M-x winner-mode</code>), then you can undo and redo the windows-related changes that you make (such as splitting, killing, or resizing windows):

<dl>
  <dt><dfn>
  C-c &lt;left&gt;<br>
  M-x winner-undo</dfn></dt>
  <dd>Undo windows-related changes (such as splits, kills, and resizes). Selecting windows doesn't count as a change.</dd>

  <dt></dfn>
  C-c &lt;right&gt;<br>
  M-x winner-redo</dfn></dt>
  <dd>Redo windows-related changes (such as splits, kills, and resizes). Selecting windows doesn't count as a change.</dd>
</dl>

If you enable Follow mode (<code>M-x follow-mode</code>), then if you have two or more windows showing the same buffer, then when you scroll, the buffers are adjusted so that they always show adjacent portions of the buffer's text. This means that if one buffer were showing lines 1 to 50, then another buffer would show lines 51 to 100, and another buffer would show lines 101 to 150, and so on (assuming all those windows have the same height). If you are at the very first line in a window and then you scroll up, either point will move to the adjacent window showing the same buffer on the left (if there is one) or if you're already on the leftmost window showing the same buffer, then scrolling up will scroll all windows up. Same idea applies when scrolling down: if you are at the very last line in a window and then you scroll down, either point will move to the adjacent window showing the same buffer on the right (if there is one) or if you're already on the rightmost window showing the same buffer, then scrolling down will scroll all windows down. <code>M-x follow-delete-other-windows-and-split</code> command will create two side-by-side windows and then enter Follow mode.

If you enable Scroll All mode (<code>M-x scroll-all-mode</code>), then all scrolling commands and point motion commands apply to every single window, even if they display different buffers.


## Buffers

The text you are editing in Emacs resides in an object called a buffer.

The buffer is the basic editing unit; one buffer corresponds to one text being edited. You normally have several buffers, but at any time you are editing only one, the current buffer, though several can be visible when you are using multiple windows or frames. Most buffers are visiting some file.

Each buffer has its own value of point. A buffer that is not currently displayed remembers its value of point if you later display it again. Furthermore, if a buffer is displayed in multiple windows, each of those windows has its own value of point.

Emacs keeps a buffer selection history that records how recently each Emacs buffer has been selected. This is used for choosing a buffer to select.

Each buffer has a unique name, which can be of any length. The distinction between upper and lower case matters in buffer names. Most buffers are made by visiting files, and their names are derived from the files' names. Emacs normally constructs the buffer name from the file name, omitting the directory name. If there is already a buffer with that name, Emacs constructs a unique name.

If a buffer contains changes that have not been saved, the buffer is considered modified. This implies that some changes will be lost if the buffer is not saved.

An indirect buffer shares the text of some other buffer, which is called the base buffer of the indirect buffer. The text of the indirect buffer is always identical to the text of its base buffer; changes made by editing either one are visible immediately in the other, but in all other respects, the indirect buffer and its base buffer are completely separate. They can have different names, different values of point, different narrowing, different markers, different major modes, and different local variables. An indirect buffer cannot visit a file, but its base buffer can. If you try to save the indirect buffer, that actually works by saving the base buffer. Killing the base buffer effectively kills the indirect buffer, but killing an indirect buffer has no effect on its base buffer. To create an indirect buffer, you can do any of the following: <code>C-x 4 c</code> (or <code>M-x clone-indirect-buffer-other-window</code>0, <code>M-x clone-indirect-buffer</code>, or <code>M-x make-indirect-buffer &lt;RET&gt; BASE-BUFFER &lt;RET&gt; INDIRECT-NAME</code>.

A split buffer is not the same thing as an indirect buffer. When you split a buffer, no new buffers are created; however, when you make an indirect buffer, the indirect buffer is a new buffer. An indirect buffer setup is special because any changes you make in the base buffer or indirect buffer are reflected in both buffers.

<code>C-x 4</code> is a prefix key for a variety of commands that switch to a buffer in another window. <code>C-x 5</code> is a prefix key for a variety of commands that switch to a buffer in another frame.

<dl>
  <dt><dfn>
  C-x b BUFFER_NAME<br>
  M-x switch-to-buffer</dfn></dt>
  <dd>Select or create a buffer named BUFFER_NAME.</dd>

  <dt><dfn>
  C-x 4 b BUFFER_NAME<br>
  M-x switch-to-buffer-other-window</dfn></dt>
  <dd>Select or create a buffer named BUFFER_NAME in another window.</dd>

  <dt><dfn>
  C-x 5 b BUFFER_NAME<br>
  M-x switch-to-buffer-other-frame</dfn></dt>
  <dd>Select or create a buffer named BUFFER_NAME in another frame.</dd>

  <dt><dfn>
  C-x &lt;left&gt;<br>
  M-x previous-buffer</dfn></dt>
  <dd>Select the previous buffer in the buffer list.</dd>

  <dt><dfn>
  C-x &lt;right&gt;<br>
  M-x next-buffer</dfn></dt>
  <dd>Select the next buffer in the buffer list.</dd>

  <dt><dfn>
  C-x C-b<br>
  M-x list-buffers</dfn></dt>
  <dd>
<p>Display a list of the existing buffers.</p>

<p>"CRM" means "Current, Read-only, and Modified." A period ('.') under C means that that buffer is the current one. A percent sign ('%') means that that buffer is read-only. An asterisk ('*') means that that buffer is modified. The Buffer column displays the buffer's name. The Size column displays the buffer's size. The Mode column displays the buffer's major mode. The File column displays the file that the buffer is visiting, if any. The buffers are listed in the order that they were last used (most recent at the top; least recent at the bottom).</p>

<p>What <code>C-x C-b</code> displays is actually an interactive menu. Switch to the menu and press <code>h</code> for help. Instead of opening the buffer menu and then manually switching to it, you can open the buffer menu and automatically switch to it: use <code>M-x buffer-menu</code> or <code>M-x buffer-menu-other-window</code>.</p>
  </dd>

  <dt><dfn>
  C-u C-x C-b</dfn></dt>
  <dd>Display only a list of the existing buffers that are visiting files.</dd>

  <dt><dfn>
  C-x C-q<br>
  M-x read-only-mode</dfn></dt>
  <dd>Toggle the read-only status of a buffer.</dd>

  <dt><dfn>
  M-x rename-buffer &lt;RET&gt; BUFFER_NAME</dfn></dt>
  <dd>Rename the current buffer to BUFFER_NAME.</dd>

  <dt><dfn>
  M-x rename-uniquely</dfn></dt>
  <dd>Rename the current buffer by appending a unique number to its current name.</dd>

  <dt><dfn>
  C-x k BUFFER_NAME<br>
  M-x kill-buffer &lt;RET&gt; BUFFER_NAME</dfn></dt>
  <dd>Kill buffer BUFFER_NAME. If you don't specify a name and just immediately press <code>&lt;RET&gt;</code>, then the current buffer will be killed by default.</dd>

  <dt><dfn>
  M-x kill-some-buffers</dfn></dt>
  <dd>Offer to kill each buffer, one by one.</dd>

  <dt><dfn>
  M-x kill-matching-buffers</dfn></dt>
  <dd>Offer to kill all buffers matching a regular expression.</dd>

  <dt><dfn>
  M-x clean-buffer-list</dfn></dt>
  <dd>
<p>By default, kill any unmodified buffers that haven't been displayed in the past three days.</p>

<p>If you enable Midnight mode (<code>M-x midnight-mode</code>), then <code>clean-buffer-list</code> will be run automatically for you every midnight.</p>
  </dd>
</dl>

Enabling Iswitchb mode (<code>M-x iswitchb-mode</code>) makes it much easier to switch buffers. It redefines what <code>C-x b</code>, <code>C-x 4 b</code>, and <code>C-x 5 b</code> do. When you enter one of those commands, they will prompt you with a list of possible buffer names. You can do one of two things: you can either start typing the name of the buffer you want to switch to it, until it appears first in the list, or you can press <code>C-s</code> (rotate left) or <code>C-r</code> (rotate right) until the buffer you want to switch to appears first in the list. Once the buffer you want to switch to appears first in the list (or is the only buffer listed), then press <code>&lt;RET&gt;</code>.


# Modes

Modes alter the functionality of buffers; for example, by introducing new commands and variables, altering key sequences, or altering various variables. Major modes tailor a buffer for a specific type of task.

Major modes are mutually exclusive; each buffer has one and only one major mode at any time. Minor modes are optional features which you can turn on or off, not necessarily specific to a type of file or buffer. Minor modes are independent of one another, and of the selected major mode.

The least specialised major mode is called "Fundamental mode". This mode has no mode-specific redefinitions or variable settings, so that each Emacs commands behaves in its most general manner, and each user option variable is in its default state.

Modes are either major or minor. Minor modes are either buffer-local (can be selectively enabled on a per-buffer basis) or global (always applies to all buffers).

Each mode is associated with a mode command, whose name consists of the mode name followed by "-mode". To toggle a minor mode (if it's enabled, then disable it; if it's disabled, then enable it) or switch to a major mode, you simply invoke its mode command: <code>M-x MODENAME-mode</code>. Since a buffer must have a major mode and can't have more than one major mode, you can't toggle a major mode on and off. Enabling a major mode disables the previous major mode. If you don't want to use the current major mode, then switch to a different one.

The major mode is chosen for you automatically based on the contents of the buffer; for example, if Emacs sees that you are visiting a Java file, then Emacs will use the cc-mode major mode. If you'd like to use a different major mode, you can always switch it to whatever you want.

If you have changed the major mode of a buffer, you can return to the major mode Emacs would have chosen automatically, by typing <code>M-x normal-mode</code>.


# How Text is Displayed

Most characters are printing characters; when they appear in a buffer, they are displayed literally on the screen. Printing characters include ASCII numbers, letters, and punctuation characters, as well as many non-ASCII characters.

The newline character is displayed by starting a newline.

The tab character is displayed as one big space that extends a certain number of columns (8 by default).

The ASCII character set contains non-printing control characters. ASCII control characters whose codes are below U+0020 (octal 40, decimal 32) are displayed as a caret (^) followed by the non-control version of the character. The raw bytes width codes U+0080 (octal 200) through U+009F (octal 237) are displayed as a backslash followed by the octal value.

Some non-ASCII characters have the same appearance as an ASCII space or hyphen (minus) character. Such characters can cause problems if they are entered into a buffer without your realisation, e.g., by yanking; for instance, source code compilers typically do not treat non-ASCII spaces as whitespace characters. To deal with this problem, Emacs displays such characters specially.

On graphical displays, some characters may have no glyphs in any of the fonts available to Emacs. These glyphless characters are normally displayed as boxes containing the hexadecimal character code. Similarly, on text terminals, characters that cannot be displayed using the terminal encoding are normally displayed as question signs.


# Reverting

Reverting something means returning it to its original state.

<dl>
  <dt><dfn>
  M-x revert-buffer<br>
  g</dfn></dt>
  <dd>
<p>Replace the current buffer text with the text of the visited file on disk; mark the buffer as "not modified"; and clear the buffer's undo history (thus, the reversion cannot be undone).</p>

<p>Some kinds of buffers that are not associated with files, such as Dired buffers, can also be reverted. For them, reverting means recalculating their contents.</p>

<p>Some buffers map <code>g</code> to <code>M-x revert-buffer</code>.</p>
  </dd>

  <dt><dfn>
  M-x auto-revert-mode<br>
  M-x global-auto-revert-mode</dfn></dt>
  <dd>
<p>Auto-Revert mode is a minor mode that automatically reverts buffers every five seconds. <code>M-x auto-revert-mode</code> enables it in the current buffer; <code>M-x global-auto-revert-mode</code> enables it in all buffers.</p>

<p>Global Auto Revert mode normally only reverts file buffers. To auto-revert certain non-file buffers, you can use <code>M-x auto-revert-mode</code> in that buffer, or you can set <code>global-auto-revert-non-file-buffers</code> to a non-nil value. The latter enables Auto Reverting for all types of buffers for which it is implemented.</p>

<p>Buffers that are modified aren't auto-reverted.</p>

<p>Auto-Revert mode won't revert remote files.</p>
  </dd>

  <dt><dfn>
  M-x auto-revert-tail-mode</dfn></dt>
  <dd>
<p>Auto-Revert Tail mode is a variant of Auto-Revert mode that is tailored to reverting buffers that only grow at the end (such as log files). For files that only grow at the end, it's more efficient to use Auto-Revert Tail mode than it is to use Auto-Revert mode.</p>

<p>Buffers that are modified aren't auto-reverted.</p>

<p>Auto-Revert Tail mode can revert remote files.</p>
  </dd>
</dl>


# Files

When editing a file in Emacs, you're actually working with a copy of the file: Emacs inserts the contents of the file into a buffer, which is called "visiting the file." Your changes last only as long as the Emacs session. To keep your changes permanently, you must save the buffer back into the file.

Each buffer is associated with a different default directory (typically the directory of the file that's being visited in the buffer). Entering a file name without a directory specifies a file in the default directory. Entering a file name with a relative path specifies a file relative to the default directory. When you create a new buffer that is not visiting a file, its default directory is usually copied from the buffer that was current at the time. To see the default directory, type <code>M-x pwd</code>. To set the default directory explicitly, type <code>M-x cd</code>.

Saving a buffer in Emacs means writing its contents back into the file that the buffer is visiting.

A backup file records the contents that a file had before the current editing session. The first time you save a file from a buffer, a backup file will automatically be created for you consisting of the contents of the file before your changes. The backup will be overwritten next time you visit the file and then save. A backup filename will appear as <code>FILENAME~</code>, <code>%FILENAME%~</code>, or <code>FILENAME.~NUMBER~</code>. To prevent excessive consumption of disk space, Emacs will automatically keep the first few backups and the latest few backups, and delete any in between, each time a new backup is made.

Auto saving is the practice of periodically saving the contents of an Emacs buffer in a separate file, so that the information will be preserved if the buffer is lost due to a system error or user error. By default, when visiting a file, Emacs will auto-save the buffer into a separate file after 300 or more characters have been typed in the buffer or after Emacs has been idle for 30 seconds and the buffer has been modified. Emacs will also automatically auto save whenever it gets a fatal error. To explicitly auto save a buffer, type <code>M-x do-auto-save</code>. The auto-save file name is of the form <code>#FILENAME#</code> or <code>#FILENAME#UNIQUESTRING</code>. When you delete a substantial part of the text in a large buffer, auto save turns off temporarily in that buffer. To reenable auto-saving after this happens, save the buffer with <code>C-x C-s</code>, or use <code>C-u 1 M-x auto-save-mode</code>. A buffer's auto-save file is deleted when you save the buffer of the visited file. Changing the visited file name with <code>C-x C-w</code> or <code>set-visited-file-name</code> renames any auto-save file to go with the new visited name. If you want to recover a file from an auto save file, then do <code>M-x recover-file &lt;RET&gt; FILENAME &lt;RET&gt;</code>, where FILENAME is the official file's name, not the auto save file's name; note that this alone doesn't recover the file on disk. To recover the file on disk, you should save the buffer (after you invoke <code>M-x recover-file</code>). If Emacs or the computer crashes, you can recover all the files you were editing from their auto save files with the command <code>M-x recover-session</code>.

Shadow files are files that are identical to each other and exist in more than one place and possibly on different machines. A shadow file group consists of one or more shadow files. The shadow file group persists across Emacs sessions, so you don't need to set it up every time you start Emacs. Once the group is set up, every time you exit Emacs or type <code>M-x shadow-copy-files</code>, it will copy the file you edited to the other files in its group. Before you start shadowing files, you need to set Emacs up for file shadowing. To do that, type <code>M-x shadow-initialize</code>. It'll seem like that command didn't do anything; however, you should see "(New file)" in the echo area. If you look at the buffer list (<code>C-x C-b</code>), then you should see two new empty files: ~/.shadows and ~/.shadow_todo. Visit and save both those buffers. To set up a shadow file group, type <code>M-x shadow-define-literal-group</code> or <code>M-x shadow-define-regexp-group</code>. I assume that all the files you specify during one shadow-define-literal-group session will be added to the same group and that each separate invocation of shadow-define-literal-group defines a new group. A shadow cluster is a group of hosts that share directories, so that copying to or from one of the hosts is sufficient to update the file on all of them. To define a shadow cluster, type <code>M-x shadow-define-cluster</code>. TODO: how to edit shadow file groups?

A fileset is a group of files that can be treated as a unit. You can use <code>M-x filesets-open</code> to open all the files in the fileset; <code>M-x filesets-close</code> to close them; and <code>M-x filesets-run-cmd</code> to run a shell command against them. TODO: expand this section.

If you want to view the current buffer in a Web browser (for example, if the buffer is HTML), you can type <code>M-x browse-url-of-file</code>.

Dired is the Emacs directory browser. It enables you to list files in a directory (and optional its subdirectories), move around that list, visit, rename, delete, and otherwise operate on the files. To invoke Dired, type <code>C-x d</code> or <code>M-x dired</code>; you can also invoke Dired by giving <code>C-x C-f</code> a directory name. There are actually many ways to invoke Dired. The Dired buffer is read-only. Press <code>h</code> for help.

Wdired is a special mode that allows you to perform file operations by editing the Dired buffer directly (the W in Wdired stands for Writable). To enter Wdired mode, type <code>C-x C-q</code> or <code>M-x wdired-change-to-wdired-mode</code> while in a Dired buffer. After you are done making changes, type <code>C-c C-c</code> to apply your changes and switch back to ordinary Dired mode.

Image-Dired is a special mode for viewing a directory that contains images. To enter Image-Dired mode, type <code>C-t d</code> while in a Dired buffer or by typing <code>M-x image-tired</code>.

A dribble file is a file into which Emacs writes all the characters that you type on the keyboard. Dribble files can be used to make a record for debugging Emacs bugs. Emacs does not make a dribble file unless you tell it to. To start writing all keyboard characters to a dribble file called FILENAME, type <code>M-x open-dribble-file &lt;RET&gt; FILENAME</code>. From then on, Emacs copies all your input to the specified dribble file until the Emacs process is killed.

<dl>
  <dt><dfn>
  C-x C-f FILENAME<br>
  M-x find-file &lt;RET&gt; FILENAME</dfn></dt>
  <dd>
<p>Visit the specified file (copy the file's contents into an Emacs buffer, so that you can view or edit the file) in the current frame and window. If the file doesn't exist, then an empty buffer is created.</p>

<p>If you visit a file that is already in Emacs, <code>C-x C-f</code> switches to the existing buffer instead of making another copy. Before doing so, it checks whether the file has changed since you last visited for saved it. If the file has changed, Emacs offers to reread it.</p>

<p>When the minibuffer is used to read a file name, it typically starts out with some initial text ending in a slash. This is the default directory. If you don't want the prompt to display the default directory, then add the following to your ~/.emacs.d/init.el: <code>(setq insert-default-directory nil)</code>. If you set insert-default-directory to nil, then file names you specify will still be relative to the default directory; you just won't see the default directory in the prompt. If you insert a double slash ('//') or a tilde ('~') in the file name prompt, then everything before the double slash or tilde will be ignored. This provides a convenient way for you to enter a file name without having to kill the entire line.</p>

<p>You can specify environment variables in file names; Emacs will expand them. Just write them like you normally would in the terminal: preceded by a dollar sign (<code>$ENVAR</code>) and optionally surrounded by braces (<code>${ENVAR}</code>). You can enter file names, just as you would in a terminal: <code>~/</code> means your home directory; <code>~/USERNAME/</code> or <code>~USERNAME/</code> means the home directory of the specified user; <code>.</code> means the current directory; and <code>..</code> means the parent directory. You can also use the '?' and '*' wildcard characters; Emacs will visit all the files that match the wildcard.</p>

<p>If you want to specify a file name literally, without having special characters being interpreted, then start the line with <code>/:</code>. Note that you can still use relative paths.</p>

<p>If the specified filename is actually a directory, then Emacs will invoke Dired, the Emacs directory browser.</p>

<p>If you visit a file that the operating system won't let you modify, or that is marked read-only, Emacs makes the buffer read-only too.</p>

<p>Emacs automatically uncompresses compressed files when you visit them, and automatically recompresses them if you alter them and save them.</p>

<p>If you visit a file archive, then Emacs will use Tar mode or Archive mode to provide a Dired-like list of the contents of the archive. You can edit or delete files in an archive. When you save your changes, the archive will automatically be recreated with your changes.</p>

<p>The TRAMP package (comes with Emacs and works right out of the box) provides a way to edit remote files (files that are stored on a system other than your own) or edit files as another user (the package also allows you to do other things, but the gist of the package is that it allows you to do things remotely). All you have to do is prepend some stuff to the file name you want to visit: <code>/METHODNAME:USERNAME@HOST.DOMAINNAME#PORTNUMBER:/PATH/TO/FILE</code>. Only the initial forward slash ('/'), host, colon (':'), and filename are required. Note that the host can be specified by name, IPv4 address, or IPv6 address. If you use IPv6, then you must surround the IPv6 address with square brackets. There are many possibilities for method name: rsh, ssh, telnet, su, sudo, sshx, krlogin, ksu, plink, plinkx, rcp, scp, sftp, rsync, scpx, scpc, rsyncc, pscp, psftp, fcp, ftp, and smb. If you don't specify a directory path, then the default directory that is searched for file is the home directory on the remote machine. TRAMP is supposed to make editing a remote file seem just like editing a local file, so all the commands you normally you use for local files can also be used with remote files. Minibuffer killing via a double slash or tilde works a bit differently with remote files. If a double slash ('//') appears immediately after the colon, then everything before the double slash is ignored. If the double slash appears somewhere after the colon, but not immediately after, then only the text between the colon and the double slash will be ignored. If a triple slash appears somewhere after the colon, but not immediately after, then everything before the triple slash is ignored.</p>

<p>In graphical Emacs, if you visit an image, the image will be displayed in Emacs. You can type <code>C-c C-c</code> to toggle between viewing the image and viewing the image's file contents. If the image is animated, then <code>&lt;RET&gt;</code> can toggle animation on and off.</p>

<p>In graphical Emacs, if you visit a PDF, the PDF will be displayed in Emacs. You can type <code>C-c C-c</code> to toggle between viewing the PDF and viewing the PDF's file contents. Press <code>h</code> for help and press <code>q</code> to close the PDF.</p>
  </dd>

  <dt><dfn>
  C-x C-f /sudo::/PATH/TO/FILENAME</dfn></dt>
  <dd>Open a file via sudo.</dd>

  <dt><dfn>
  C-x C-v FILENAME<br>
  M-x find-alternate-file &lt;RET&gt; FILENAME</dfn></dt>
  <dd>
<p>Kill the current buffer (after first offering to save it if it's modified) and then visit the specified file.</p>

<p>When <code>C-x C-v</code> reads the file name to visit, it inserts the entire default file name in the buffer, with point just after the directory part; this is convenient if you made a slight error in typing the name.</p>
  </dd>

  <dt><dfn>
  C-x C-r FILENAME<br>
  M-x find-file-read-only &lt;RET&gt; FILENAME</dfn></dt>
  <dd>Visit the specified file in read-only mode.</dd>

  <dt><dfn>
  C-x 4 f FILENAME<br>
  C-x 4 C-f FILENAME<br>
  M-x find-file-other-window &lt;RET&gt; FILENAME</dfn></dt>
  <dd>Visit the specified file in another window.</dd>

  <dt><dfn>
  C-x 4 r<br>
  M-x find-file-read-only-other-window &lt;RET&gt; FILENAME</dfn></dt>
  <dd>Visit the specified file in read-only mode in another window.</dd>

  <dt><dfn>
  C-x 5 f FILENAME<br>
  C-x 5 C-f FILENAME<br>
  M-x find-file-other-frame &lt;RET&gt; FILENAME</dfn></dt>
  <dd>Visit the specified file in another frame.</dd>

  <dt><dfn>
  C-x 5 r FILENAME<br>
  M-x find-file-read-only-other-frame &lt;RET&gt; FILENAME</dfn></dt>
  <dd>Visit the specified file in read-only mode in another frame.</dd>

  <dt><dfn>
  C-x C-s<br>
  M-x save-buffer</dfn></dt>
  <dd>
<p>Save the current buffer to its file. If the current buffer is not modified (no changes have been made in it since the buffer was created or last saved), saving is not really done, because it would have no effect. Instead, a message is displayed in the echo area: "(No changes need to be saved)".</p>

<p>If you want to request for a backup to be created next time you save, then invoke save-buffer with a prefix argument: <code>C-u C-x C-s</code>.</p>

<p>If you want to make a backup immediately, and then save your changes, then invoke save-buffer with two prefix arguments: <code>C-u C-u C-x C-s</code>.</p>

<p>If you want to make a backup immediately, save your changes, and then request for a backup to be created next time you save, then invoke save-buffer with three prefix arguments: <code>C-u C-u C-u C-x C-s</code>.</p>
  </dd>

  <dt><dfn>
  C-x s<br>
  M-x save-some-buffers</dfn></dt>
  <dd>For each modified buffer, answer whether you want to save the buffer or not. Note that <code>C-x C-c</code> invokes <code>save-some-buffers</code> before killing Emacs.</dd>

  <dt><dfn>
  M-~<br>
  M-x not-modified</dfn></dt>
  <dd>
<p>Mark the current buffer as "not modified" to protect it from being saved. This is useful if you made changes to the buffer, but don't want to save those changes (and don't want to risk saving those changes).</p>

<p>To mark a buffer as modified, type <code>C-u M-~</code>.</p>
  </dd>

  <dt><dfn>
  M-x set-visited-file-name &lt;RET&gt; FILENAME</dfn></dt>
  <dd>Change the name of the file that the buffer is visiting; this doesn't visit the new file name and doesn't save the buffer changes to the new file name. If you want to save the buffer's contents to the new file name, then use <code>C-x C-s</code>.</dd>

  <dt><dfn>
  C-x C-w FILENAME<br>
  M-x write-file &lt;RET&gt; FILENAME</dfn></dt>
  <dd>Change the name of the file that the buffer is visiting, and then save the current buffer under that file name. This is equivalent to <code>M-x set-visited-file-name &lt;RET&gt; FILENAME &lt;RET&gt; C-x C-s</code>.</dd>

  <dt><dfn>
  C-x C-d DIR-OR-PATTERN<br>
  M-x list-directory &lt;RET&gt; DIR-OR-PATTERN</dfn></dt>
  <dd>Display a brief directory listing (like <code>ls -CF</code>).</dd>

  <dt><dfn>
  C-u C-x C-d DIR-OR-PATTERN<br>
  C-u M-x list-directory &lt;RET&gt; DIR-OR-PATTERN</dfn></dt>
  <dd>Display a verbose directory listing (like <code>ls -l</code>).</dd>

  <dt><dfn>
  M-x make-directory &lt;RET&gt; DIRNAME</dfn></dt>
  <dd>Create a new directory using the specified name.</dd>

  <dt><dfn>
  M-x delete-file &lt;RET&gt; FILENAME</dfn></dt>
  <dd>Delete the specified file.</dd>

  <dt><dfn>
  M-x delete-directory &lt;RET&gt; DIRNAME</dfn></dt>
  <dd>Delete the specified directory.</dd>

  <dt><dfn>
  M-x copy-file &lt;RET&gt; OLD &lt;RET&gt; NEW</dfn></dt>
  <dd>Copy the specified file into a file named NEW.</dd>

  <dt><dfn>
  M-x copy-directory &lt;RET&gt; OLD &lt;RET&gt; NEW</dfn></dt>
  <dd>Copy the specified directory into a directory named NEW.</dd>

  <dt><dfn>
  M-x rename-file &lt;RET&gt; OLD &lt;RET&gt; NEW</dfn></dt>
  <dd>Rename the specified file from OLD to NEW. If NEW is a directory name, then use that directory, and move OLD into it.</dd>

  <dt><dfn>
  M-x make-symbolic-link &lt;RET&gt; TARGET &lt;RET&gt; LINKNAME</dfn></dt>
  <dd>Create a symbolic link named LINKNAME, which points to TARGET.</dd>

  <dt><dfn>
  C-x i<br>
  M-x insert-file</dfn></dt>
  <dd>Insert a copy of the contents of the specified file into the current buffer at point, leaving point unchanged, but moving mark to the end of the inserted contents.</dd>

  <dt><dfn>
  M-x write-region</dfn></dt>
  <dd>Copy the contents of region into the specified file.</dd>

  <dt><dfn>
  M-x append-to-file</dfn></dt>
  <dd>Append the contents of region to the end of the specified file.</dd>

  <dt><dfn>
  M-x set-file-modes<br>
  M-x chmod</dfn></dt>
  <dd>Change the file modes (file permissions) of the specified file. Specify the arguments in the same format that chmod would expect.</dd>
</dl>


# Moving Around a Buffer

Very often, Alt (M-) is used for operations related to the units defined by language (words, sentences, paragraphs, etc.), while Ctrl (C-) is used for operations on basic units that are independent of what you are editing (characters, lines, etc.).

The sentence commands assume that you follow the convention of putting two spaces at the end of a sentence. A sentence ends wherever there is a '.', '?', or '!' followed by two spaces or the end of the line. Between a '.', '?', or '!' and two spaces or the end of the line can be any number or mixture of '.', '?', '!', ']', '}', ')', ''', or '"'. If you want to use just one space between sentences, you can put the following in your ~/.emacs.d/init.el: <code>(setq sentence-end-double-space nil)</code>; the downside to using one space to end sentences is that Emacs can't distinguish between periods that end sentences and periods that indicate abbreviations.

<dl>
  <dt><dfn>
  C-f<br>
  &lt;right&gt;<br>
  M-x forward-char</dfn></dt>
  <dd>Move forward one character. If you're at the end of a line, <code>C-f</code> will take you to the first character on the next line.</dd>

  <dt><dfn>
  C-d<br>
  M-x delete-char<br>
  &lt;Delete&gt;<br>
  M-x delete-forward-char</dfn></dt>
  <dd>Delete forward one character. If you're at the end of a line, <code>C-d</code> will delete the newline.</dd>

  <dt><dfn>
  C-b<br>
  &lt;left&gt;<br>
  M-x backward-char</dfn></dt>
  <dd>Move backward one character. If you're at the beginning of a line, <code>C-b</code> will take you to the last character on the previous line.</dd>

  <dt><dfn>
  &lt;DEL&gt;<br>
  M-x delete-backward-char</dfn></dt>
  <dd>Delete backward one character. If you're at the beginning of a line, <code>&lt;DEL&gt;</code> will delete the newline.</dd>

  <dt><dfn>
  M-f<br>
  M-&lt;right&gt;<br>
  M-x forward-word</dfn></dt>
  <dd>Move forward one word.</dd>

  <dt><dfn>
  M-d<br>
  C-&lt;Delete&gt;<br>
  M-x kill-word</dfn></dt>
  <dd>Kill forward one word.</dd>

  <dt><dfn>
  M-b<br>
  M-&lt;left&gt;<br>
  M-x backward-word</dfn></dt>
  <dd>Move backward one word.</dd>

  <dt><dfn>
  M-&lt;DEL&gt;<br>
  C-&lt;DEL&gt;<br>
  M-x backward-kill-word</dfn></dt>
  <dd>Kill backward one word.</dd>

  <dt><dfn>
  M-e<br>
  M-x forward-sentence</dfn></dt>
  <dd>Move forward one sentence.</dd>

  <dt><dfn>
  M-k<br>
  M-x kill-sentence</dfn></dt>
  <dd>Kill forward from point to the end of one sentence.</dd>

  <dt><dfn>
  M-a<br>
  M-x backward-sentence</dfn></dt>
  <dd>Move backward one sentence.</dd>

  <dt><dfn>
  C-x &lt;DEL&gt;<br>
  M-x backward-kill-sentence</dfn></dt>
  <dd>Kill backward from point to the beginning of one sentence.</dd>

  <dt><dfn>
  C-e<br>
  &lt;End&gt;<br>
  M-x move-end-of-line</dfn></dt>
  <dd>Move to the end of one logical line.</dd>

  <dt><dfn>
  C-k<br>
  M-x kill-line</dfn></dt>
  <dd>
<p>If there are visible (non-whitespace) characters after point, kill forward from point to the end of the current logical line (not including the newline). Press C-k again to kill the newline.</p>

<p>If point is after the last visible character in the line, <code>C-k</code> will kill all the whitespace (including the newline).</p>
  </dd>

  <dt><dfn>
  C-a<br>
  &lt;Home&gt;<br>
  M-x move-beginning-of-line</dfn></dt>
  <dd>Move to the beginning of one logical line.</dd>

  <dt><dfn>
  M-0 C-k<br>
  C-u 0 C-k<br>
  C-u C-0 C-k</dfn></dt>
  <dd>Kill backward from point to the beginning of one logical line.</dd>

  <dt><dfn>
  C-S-&lt;DEL&gt;<br>
  C-a C-k C-k<br>
  M-x kill-whole-line</dfn></dt>
  <dd>Kill one whole logical line, regardless of where point is in it.</dd>

  <dt><dfn>
  C-x C-o<br>
  M-x delete-blank-lines</dfn></dt>
  <dd>
<p>If point is on a blank line that is surrounded by one or more blank lines on either side, then delete all the surrounding blank lines, leaving just one blank line.</p>

<p>If point is on a blank line that is not surrounded by any blank lines on either side, then delete the current blank line.</p>

<p>If point is on a nonblank line that precedes one or more blank lines, then delete all following blank lines up to the next nonblank line.</p>

<p>If point is on a nonblank line that is not followed by any blank lines, then do nothing.</p>
  </dd>

  <dt><dfn>
  C-n<br>
  &lt;down&gt;<br>
  M-x next-line</dfn></dt>
  <dd>Move down one screen line.</dd>

  <dt><dfn>
  C-p<br>
  &lt;up&gt;<br>
  M-x previous-line</dfn></dt>
  <dd>Move up one screen line.</dd>

  <dt><dfn>
  M-g &lt;TAB&gt;<br>
  M-x move-to-column</dfn></dt>
  <dd>Move to the specified column number in the current line (the first column is column 0).</dd>

  <dt><dfn>
  M-g M-g LINE-NUMBER<br>
  M-g g LINE-NUMBER<br>
  C-u LINE-NUMBER M-g M-g<br>
  C-u LINE-NUMBER M-g g<br>
  M-LINE-NUMBER M-g M-g<br>
  M-LINE-NUMBER M-g g</dfn></dt>
  <dd>Move to the specified line number (the first line is line 1).</dd>

  <dt><dfn>
  M-}<br>
  C-&lt;down&gt;<br>
  M-x forward-paragraph</dfn></dt>
  <dd>Move forward one paragraph.</dd>

  <dt><dfn>
  M-x kill-paragraph</dfn></dt>
  <dd>Kill forward from point to the end of one paragraph.</dd>

  <dt><dfn>
  M-{<br>
  C-&lt;up&gt;<br>
  M-x backward-paragraph</dfn></dt>
  <dd>Move backward one paragraph.</dd>

  <dt><dfn>
  M-x backward-kill-paragraph</dfn></dt>
  <dd>Kill backward from point to the beginning of one paragraph.</dd>

  <dt><dfn>
  C-v<br>
  &lt;PageDown&gt;<br>
  M-x scroll-up-command</dfn></dt>
  <dd>Scroll the text up one screenful (or you can think of this as scrolling the scrollbar down one screenful).</dd>

  <dt><dfn>
  M-v<br>
  &lt;PageUp&gt;<br>
  M-x scroll-down-command</dfn></dt>
  <dd>Scroll the text down one screenful (or you can think of this as scrolling the scrollbar up one screenful).</dd>

  <dt><dfn>
  C-x ]<br>
  M-x forward-page</dfn></dt>
  <dd>Move forward one page (move to previous ^L).</dd>

  <dt><dfn>
  C-x [<br>
  M-x backward-page</dfn></dt>
  <dd>Move backward one page (move to next ^L).</dd>

  <dt><dfn>
  C-x C-p C-w<br>
  C-x C-p S-&lt;DEL&gt;</dfn></dt>
  <dd>Kill one whole page (up to and including ^L) regardless of where point is in the page. If you simply press <code>&lt;DEL&gt;</code> instead of <code>S-&lt;DEL&gt;</code> or <code>C-w</code>, then that will delete the text instead of killing it.</dd>

  <dt><dfn>
  C-M-f<br>
  C-M-&lt;right&gt;<br>
  &lt;ESC&gt; C-&lt;right&gt;<br>
  M-x forward-sexp</dfn></dt>
  <dd>Move forward across one expression (could be an identifier, literal, keyword, or whatever) that is at the same nesting level as point.</dd>

  <dt><dfn>
  C-M-k<br>
  M-x kill-sexp</dfn></dt>
  <dd>Kill forward from point to the end of one expression (could be an identifier, literal, keyword, or whatever) that is at the same nesting level as point.</dd>

  <dt><dfn>
  C-M-b<br>
  C-M-&lt;left&gt;<br>
  &lt;ESC&gt; C-&lt;left&gt;<br>
  M-x backward-sexp</dfn></dt>
  <dd>Move backward across one expression (could be an identifier, literal, keyword, or whatever) that is at the same nesting level as point.</dd>

  <dt><dfn>
  &lt;ESC&gt; C-&lt;Delete&gt;<br>
  &lt;ESC&gt; C-&lt;DEL&gt;<br>
  M-x backward-kill-sexp</dfn></dt>
  <dd>Kill backward from point to the beginning of one expression (could be an identifier, literal, keyword, or whatever) that is at the same nesting level as point.</dd>

  <dt><dfn>
  C-M-n<br>
  M-x forward-list</dfn></dt>
  <dd>Move forward across one balanced pair of delimiters (often "()", "[]", or "{}", but there could be more or less, depending on the buffer's mode) that are at the same nesting level as point.</dd>

  <dt><dfn>
  C-M-p<br>
  M-x backward-list</dfn></dt>
  <dd>Move backward across one balanced pair of delimiters (often "()", "[]", or "{}", but there could be more or less, depending on the buffer's mode) that are at the same nesting level as point.</dd>

  <dt><dfn>
  C-M-d<br>
  C-M-&lt;down&gt;<br>
  &lt;ESC&gt; C-&lt;down&gt;<br>
  M-x down-list</dfn></dt>
  <dd>Move down into one nested balanced pair of delimiters (often "()", "[]", or "{}", but there could be more or less, depending on the buffer's mode).</dd>

  <dt><dfn>
  M-x up-list</dfn></dt>
  <dd>Move forward up out of one nested balanced pair of delimiters (often "()", "[]", or "{}", but there could be more or less, depending on the buffer's mode).</dd>

  <dt><dfn>
  C-M-u<br>
  C-M-&lt;up&gt;<br>
  &lt;ESC&gt; C-&lt;up&gt;<br>
  M-x backward-up-list</dfn></dt>
  <dd>Move backward up out of one nested balanced pair of delimiters (often "()", "[]", or "{}", but there could be more or less, depending on the buffer's mode).</dd>

  <dt><dfn>
  M-x kill-backward-up-list</dfn></dt>
  <dd>Kill any expression within a balanced pair of delimiters, other than the expression that point is on, and kill the balanced pair of delimiters; for example, if you have "(foo bar baz)" with point on "bar" and you invoke <code>M-x kill-backward-up-list</code>, then you will be left with "bar".</dd>

  <dt><dfn>
  C-M-e<br>
  C-M-&lt;End&gt;<br>
  &lt;ESC&gt; C-&lt;End&gt;<br>
  M-x end-of-defun</dfn></dt>
  <dd>Move forward to the end of the next defun (function, class, template, struct, or any other major definition) at the same nesting level as point.</dd>

  <dt><dfn>
  C-M-a<br>
  C-M-&lt;Home&gt;<br>
  &lt;ESC&gt; C-&lt;Home&gt;<br>
  M-x beginning-of-defun</dfn></dt>
  <dd>Move backward to the beginning of the previous defun (function, class, template, struct, or any other major definition).</dd>

  <dt><dfn>
  C-M-h &lt;DEL&gt;</dfn></dt>
  <dd>Delete the current defun (function, class, template, struct, or any other major definition).</dd>

  <dt><dfn>
  M-&gt;<br>
  C-&lt;End&gt;<br> 
  M-x end-of-buffer</dfn></dt>
  <dd>Move forward to the end of the buffer.</dd>

  <dt><dfn>
  M-&lt;<br>
  C-&lt;Home&gt;<br>
  M-x beginning-of-buffer</dfn></dt>
  <dd>Move backward to the beginning of the buffer.</dd>

  <dt><dfn>
  M-x erase-buffer</dfn></dt>
  <dd>Delete the entire contents of the current buffer.</dd>
</dl>


# Marks and Regions

A lot of commands can operate on a block of text called a region. The region is the text between point and mark. The empty region is when mark and point refer to the same spot. The region always extends from the point to the mark, no matter which one comes earlier in the text; each time you move point, the region changes. To create a region, you set mark first, then point.

In Vim, you might be used to working with ranges of lines. In Emacs, the convention is to work with regions instead of ranges of lines.

When the mark is active, the region is active. When the region is active, it's highlighted. Some commands require the region to be active in order to work; other commands don't have that requirement (they can operate on an inactive region). To deactive the region, type <code>C-g</code>. Most commands will deactivate the region when they're done operating on it.

When multiple windows show the same buffer, they can have different values of point, but they all share one common mark position.

Some commands set mark without activating it (usually commands that move point will set the mark at the current point before moving point). You can tell that a command sets a mark when it shows "Mark set" in the echo area.

Some commands can set mark without moving point.

Some commands only operate on regions (they usually contain the word "region" in their name).

The commands that mark objects (words, sentences, paragraphs, etc.) extend the region further each time they're called.

The default behaviour of the mark and region, in which setting the mark activates it and highlights the region, is called Transient Mark mode. This is a minor mode that is enabled by default. It makes many Emacs commands operate on the region when the mark is active. It can be toggled with <code>M-x transient-mark-mode</code>. While Transient Mark mode is off, you can activate it temporarily using <code>C-&lt;SPC&gt; C-&lt;SPC&gt;</code> (set the mark at point and enable Transient Mark mode until the mark is deactivated) or using <code>C-u C-x C-x</code> (exchange point and mark and enable Transient Mark mode until the mark is deactivated).

Marks aren't just used to help define regions. They can also be used as a way to remember a position in the buffer (<code>C-&lt;SPC&gt; C-&lt;SPC&gt;</code>), so that you can jump back to it (<code>C-u C-&lt;SPC&lt;</code>).

If you enable Delete Selection mode, then inserting text while the mark is active causes the text in the region to be deleted first. To toggle Delete Selection mode on or off, type <code>M-x delete-selection-mode</code>.

<dl>
  <dt><dfn>
  C-&lt;SPC&gt;<br>
  C-@<br>
  M-x set-mark-command</dfn></dt>
  <dd>Set the mark at point and activate it.</dd>

  <dt><dfn>
  C-x C-x<br>
  M-x exchange-point-and-mark</dfn></dt>
  <dd>Set the mark at point, activate it, and then move point to where the previous mark used to be. If you keep invoking <code>exchange-point-and-mark</code>, then you can keep swapping point and mark. You can use this command to reactivate mark.</dd>

  <dt><dfn>
  M-@<br>
  M-x mark-word</dfn></dt>
  <dd>Set mark from point to the end of the current or next word without moving point.</dd>

  <dt><dfn>
  M-x mark-end-of-sentence</dfn></dt>
  <dd>Set mark from point to the end of the current or next sentence without moving point.</dd>

  <dt><dfn>
  C-M-&lt;SPC&gt;<br>
  C-M-@<br>
  M-x mark-sexp</dfn></dt>
  <dd>Set mark from point to the end of the current or next expression (could be an identifier, literal, keyword, or whatever) that is at the same nesting level as point without moving point.</dd>

  <dt><dfn>
  M-h<br>
  M-x mark-paragraph</dfn></dt>
  <dd>Set mark after the end of the current paragraph and move point to the beginning of the current paragraph.</dd>

  <dt><dfn>
  C-M-h<br>
  M-x mark-defun</dfn></dt>
  <dd>Set mark after the end of the current defun (function, class, template, struct, or any other major definition) and move point to the beginning of the current defun.</dd>

  <dt><dfn>
  C-x C-p<br>
  M-x mark-page</dfn></dt>
  <dd>Set mark after the end of the current page (^L) and move point to the beginning of the current page.</dd>

  <dt><dfn>
  C-x h<br>
  M-x mark-whole-buffer</dfn></dt>
  <dd>Set mark at the end of the current buffer and move point to the beginning of the current buffer (essentially, this is a Select All).</dd>
</dl>


## Shift Selection

If you hold down the shift key while typing a cursor motion command (i.e., any command that moves point without doing anything else), this sets the mark before moving point, so that the region extends from the original position of point to its new position. In addition to the usual ways of deactivating the mark (such as changing the buffer text or typing <code>C-g</code>), the mark is deactivated by any unshifted cursor motion command. Any subsequent shifted cursor motion command avoids setting the mark anew; therefore, a series of shifted cursor motion commands will continuously adjust the region.


## Narrowing and Widening

Narrowing means focusing in on some portion of the buffer, making the rest of the buffer temporarily inaccessible. When you have narrowed down to a part of the buffer, that part appears to be all there is. You can't see the rest, you can't move into it (motion commands won't go outside the accessible part), you can't change it in any way; however, it is not gone, and if you save the file, all the inaccessible text will be saved. The word "Narrow" appears in the mode line whenever narrowing is in effect.

Widening is the opposite of narrowing. When a buffer is widened, all its text is accessible and visible.

<dl>
  <dt><dfn>
  C-x n n<br>
  M-x narrow-to-region</dfn></dt>
  <dd>
<p>Narrow buffer down to the region (the area that point and mark delineate).</p>

<p>You can narrow a narrowed region, but when you widen, the entire buffer will be made accessible (rather than undoing the most recent narrow).</p>
</dd>

  <dt><dfn>
  C-x n d<br>
  M-x narrow-to-defun</dfn></dt>
  <dd>Narrow buffer down to the current defun (function, class, template, struct, or any other major definition).</dd>

  <dt><dfn>
  C-x n p<br>
  M-x narrow-to-page</dfn></dt>
  <dd>Narrow buffer down to the current page.</dd>

  <dt><dfn>
  C-x n w<br>
  M-x widen</dfn></dt>
  <dd>Widen the current buffer (make the entire buffer accessible again). You can also think of this as cancelling a narrow.</dd>

  <dt><dfn>
  C-x =<br>
  M-x what-cursor-position</dfn></dt>
  <dd>Display information about where point is relative to the entire buffer (not just the narrowed region). The numbers in angle brackets are the first line number in the narrowed region (relative to the entire buffer) and the last line number in the narrowed region (also relative to the entire buffer).</dd>

  <dt><dfn>
  M-x what-line</dfn></dt>
  <dd>Display the line number of point relative to the entire buffer, and then in parentheses, display the line number of point relative to the narrowed region.</dd>
</dl>


## Rectangles

A given combination of point and mark values can be interpreted either as a region or as a rectangle, depending on the command that uses them. A rectangle is a subset of a region; when you make a region, the rectangle is considered to be the area from point in one corner to mark in the diagonally opposite corner. If point and mark are in the same column, the region-rectangle is empty. If they are in the same line, the region-rectangle is one line high. It's important to remember that the cursor is not the same thing as point.

<dl>
  <dt><dfn>
  C-x r o<br>
  M-x open-rectangle</dfn></dt>
  <dd>Fill the entire rectangle with blank space, pushing the previous contents outside to the right of the rectangle.</dd>

  <dt><dfn>
  C-x r N<br>
  M-x rectangle-number-lines</dfn></dt>
  <dd>Prepend line numbers to the lines in the rectangle. By default, the first line number in the rectangle is line 1, the second line number in the rectangle is line 2, and so on. The line numbers have nothing to do with the line numbers in the rest of the buffer. With a prefix argument, the command prompts for a number to begin from and for a format string with which to print the numbers.</dd>

  <dt><dfn>
  M-x string-insert-rectangle &lt;RET&gt; STRING &lt;RET&gt;</dfn></dt>
  <dd>Insert the specified string on each line of the rectangle.</dd>
</dl>


# Searching and Replacing


## Search

Incremental searching (Isearch or I-search) begins searching as soon as you type the first character of the search string. As you type in the search string, Emacs shows you where the string (as you have typed it so far) would be found by highlighting all the matches.

A nonincremental search requires you to type the entire search string before searching begins.

A word search finds a sequence of words without regard to the type of punctuation between them; for example, if you enter a search string that consists of two words separated by a single space, the search matches any sequence of those two words separated by one or more spaces, newlines, or other punctuation characters. Incremental and nonincremental word searches differ slightly in the way they find a match. In a nonincremental word search, the last word in the search string must exactly match a whole word. In an incremental word search, the matching is more lax: the last word in the search string can match part of a word, so that the matching proceeds incrementally as you type.

A symbol search is much like an ordinary search, except that the boundaries of the search must match the boundaries of a symbol. The meaning of "symbol" in this context depends on the major mode and usually refers to a source code token. Symbol search is useful for searching source code. In incremental symbol search, only the beginning of the search string is required to match the beginning of a symbol. In nonincremental symbol search, the beginning and end of the search string are required to match the beginning and end of a symbol.

Emacs supports incremental and nonincremental regular expression (regexp) searches. The annoying thing about GNU's regular expressions is that some characters need to be escaped in order for them to have special meaning (this is backwards because usually you would escape something to remove its special meaning); pipes ('|') and parentheses both need to be escaped for them to have their special meaning (if they're not escaped, then they're matched literally). In most other cases, the regular expression syntax is pretty standard. If you need help with regular expressions, then consult the "Syntax of Regular Expressions" section in the Emacs manual or the "Regular Expressions" section in the Elisp manual.

If a search string contains only lowercase letters, the search is case-insensitive. If a search string contains any uppercase letters, then the search is case-sensitive. If you delete all the uppercase characters from the search string, then it becomes case-insensitive again. This behaviour also applies to incremental regexp searches; for example "[ab]" matches 'a', 'A', 'b', or 'B', but "[AB]" only matches 'A' or 'B'.

To search for a newline character, type <code>C-j</code>. To search for other control characters, quote it by typing <code>C-q</code> first. To search for non-ASCII characters, you can either use <code>C-q</code> and enter its octal code, or use an input method. If an input method is enabled in the current buffer when you begin the search, you can use it in the search string also. While typing the search string, you can toggle the input method with the command <code>C-\</code>. You can also turn on a non-default input method with <code>C-^</code>, which prompts for the name of the input method. When an input method is active during incremental search, the search prompt includes the input method mnemonic. Any input method you enable during incremental search remains enabled in the current buffer afterwards.

If you begin an incremental search while the minibuffer is active, Emacs searches the contents of the minibuffer. Unlike searching an ordinary buffer, the search string is not shown in the echo area, because that is used to display the minibuffer. If an incremental search fails in the minibuffer, it tries searching the minibuffer history. You can visualise the minibuffer and its history as a series of "pages", with the earliest history element on the first page and the current minibuffer on the last page. A forward search, <code>C-s</code>, searches forward to later pages; a reverse search, <code>C-r</code>, searches backwards to earlier pages. Like in ordinary buffer search, a failing search can wrap around, going from the last page to the first page or vice versa. When the current match is on a history element, that history element is pulled into the minibuffer. If you exit the incremental search normally (for example, by typing <code>&lt;RET&gt;</code>), it remains in the minibuffer afterwards. Canceling the search, with <code>C-g</code>, restores the contents of the minibuffer when you began the search.

<dl>
  <dt><dfn>
  &lt;RET&gt;</dfn></dt>
  <dd>
<p>Terminate a search and leave the cursor where it is. Actually, any command not specially meaningful in searches will also terminate the search. When you exit the incremental search, it adds the original value of point to the mark ring, without activating the mark; you can thus use <code>C-u C-&lt;SPC&gt;</code> to return to where you were before beginning the search. It only does this if the mark was not already active.</p>

<p>If the search string is empty, then <code>&lt;RET&gt;</code> will launch a nonincremental search.</p>
  </dd>

  <dt><dfn>
  C-g</dfn></dt>
  <dd>Cancel a search and move the cursor back to where it was before the search began. If the search prompt says "Failing I-search", then <code>C-g</code> will remove all the characters from the search string that are causing the search to fail, so in the case of a failing I-search, you need to press <code>C-g</code> twice in order to cancel the search.</dd>

  <dt><dfn>
  C-s<br>
  M-x isearch-forward<br>
  C-u C-M-s</dfn></dt>
  <dd>
<p>Begin an incremental search forward, or if already in a forward incremental search, then move to the next occurrence of the search string. If you're at the last match in the buffer, then typing <code>C-s</code> will begin the search again from the beginning of the buffer. This is called wrapping around, and "Wrapped" appears in the search prompt once this has happened. If you wrap more than once, then "Overwrapped" appears in the search prompt, which means that you are revisiting matches that you have already seen.</p>

<p>On the first match, you can press <code>&lt;DEL&gt;</code> to edit the search string. If you type <code>C-s</code> or <code>C-r</code> to move to the next or previous occurrence, then pressing <code>&lt;DEL&gt;</code> will move you one match closer to the first match. When you press &lt;DEL&gt; enough times to get back to the first match, then &lt;DEL&gt; can be used again to edit the search string. An easier way to edit the search string is to press <code>M-e</code> followed by <code>C-s</code> or <code>C-r</code> to resume the search.</p>

<p><code>C-r</code> in a forward search switches to a backward search.</p>

<p>After exiting a search, you can search for the same string again by typing just <code>C-s C-s</code>. The first <code>C-s</code> is the key that invokes incremental search, and the second <code>C-s</code> means "search again". It doesn't matter if the last search string was searched for with <code>C-s</code> or <code>C-r</code>.</p>
  </dd>

  <dt><dfn>
  C-r<br>
  M-x isearch-backward<br>
  C-u C-M-r</dfn></dt>
  <dd>
<p>Begin an incremental search backward, or if already in a backward incremental search, then move to the next occurrence of the search string. If you're at the first match in the buffer, then typing <code>C-r</code> will begin the search again from the end of the buffer. This is called wrapping around, and "Wrapped" appears in the search prompt once this has happened. If you wrap more than once, then "Overwrapped" appears in the search prompt, which means that you are revisiting matches that you have already seen.</p>

<p>On the first match, you can press <code>&lt;DEL&gt;</code> to edit the search string. If you type <code>C-s</code> or <code>C-r</code> to move to the previous or next occurrence, then pressing <code>&lt;DEL&gt;</code> will move you one match closer to the first match. When you press &lt;DEL&gt; enough times to get back to the first match, then &lt;DEL&gt; can be used again to edit the search string. An easier way to edit the search string is to press <code>M-e</code> followed by <code>C-s</code> or <code>C-r</code> to resume the search.</p>

<p><code>C-s</code> in a backward search switches to a forward search.</p>

<p>After exiting a search, you can search for the same string again by typing just <code>C-r C-r</code>. The first <code>C-r</code> is the key that invokes incremental search, and the second <code>C-r</code> means "search again". It doesn't matter if the last search string was searched for with <code>C-s</code> or <code>C-r</code>.</p>
  </dd>

  <dt><dfn>
  M-e</dfn></dt>
  <dd>Edit a search string. To resume searching, press <code>C-s</code> or <code>C-r</code> after you're done editing.</dd>

  <dt><dfn>
  M-s &lt;SPC&gt;<br>
  M-x isearch-toggle-lax-whitespace</dfn></dt>
  <dd>
<p>Toggle lax space matching.</p>

<p>By default, incremental search performs "lax space matching": each space, or sequence of spaces, matches any sequence of one or more spaces in the text. When lax space matching is disabled, then each space in the search string matches exactly one space. This applies to regexp and non-regexp searches.</p>
  </dd>

  <dt><dfn>
  M-c</dfn></dt>
  <dd>Within an incremental search, <code>M-c</code> toggles the case-sensitivity of that search.</dd>

  <dt><dfn>
  C-s &lt;RET&gt; SEARCH_STRING &lt;RET&gt;<br>
  M-x search-forward</dfn></dt>
  <dd>Begin a nonincremental search forward, which will simply jump to the first match and then terminate the search. I guess if you want to move to the next match, then type <code>C-s C-s</code> to begin an incremental search forward using the previous search string. If you want to move to the next match, then type <code>C-r C-r</code> to begin an incremental search backward using the previous search string.</dd>

  <dt><dfn>
  C-r &lt;RET&gt; SEARCH_STRING &lt;RET&gt;<br>
  M-x search-backward</dfn></dt>
  <dd>Begin a nonincremental search backward, which will simply jump to the first match and then terminate the search. I guess if you want to move to the next match, then type <code>C-r C-r</code> to begin an incremental search backward using the previous search string. If you want to move to the previous match, then type <code>C-s C-s</code> to begin an incremental search forward using the previous search string.</dd>

  <dt><dfn>
  M-s w<br>
  M-x isearch-toggle-word<br>
  M-x isearch-forward-word</dfn></dt>
  <dd>If incremental search is active, toggle word search mode (keeping the same direction of the search); otherwise, begin an incremental forward word search. To disable word search, type <code>M-s w</code> again.</dd>

  <dt><dfn>
  M-s w C-r<br>
  C-r M-s w</dfn></dt>
  <dd>Begin an incremental backward word search.</dd>

  <dt><dfn>
  M-s w &lt;RET&gt; SEARCH_WORDS &lt;RET&gt;<br>
  M-x word-search-forward</dfn></dt>
  <dd>Begin a nonincremental word search forward, which will simply jump to the first match and then terminate the search.</dd>

  <dt><dfn>
  M-s w C-r &lt;RET&gt; SEARCH_WORDS &lt;RET&gt;<br>
  M-x word-search-backward</dfn></dt>
  <dd>Begin a nonincremental word search backward, which will simply jump to the first match and then terminate the search.</dd>

  <dt><dfn>
  M-s _<br>
  M-x isearch-toggle-symbol<br>
  M-x isearch-forward-symbol</dfn></dt>
  <dd>If incremental search is active, toggle symbol search mode (keeping the same direction of the search); otherwise, begin an incremental forward symbol search. To disable symbol search, type <code>M-s _</code> again.</dd>

  <dt><dfn>
  M-s _ C-r<br>
  C-r M-s _</dfn></dt>
  <dd>Begin an incremental backward symbol search.</dd>

  <dt><dfn>
  M-s _ &lt;RET&gt; SYMBOL &lt;RET&gt;</dfn></dt>
  <dd>Begin a nonincremental symbol search forward, which will simply jump to the first match and then terminate the search.</dd>

  <dt><dfn>
  M-s _ C-r &lt;RET&gt; SYMBOL &lt;RET&gt;</dfn></dt>
  <dd>Begin a nonincremental symbol search backward, which will simply jump to the first match and then terminate the search.</dd>

  <dt><dfn>
  C-M-s<br>
  M-x isearch-forward-regexp<br>
  C-u C-s<br>
  C-s M-r</dfn></dt>
  <dd>Begin an incremental regexp search forward. To search using the previous regexp search string, press <code>C-s</code> immediately.</dd>

  <dt><dfn>
  C-M-r<br>
  M-x isearch-backward-regexp<br>
  C-u C-r<br>
  C-r M-r</dfn></dt>
  <dd>Begin an incremental regexp search backward. To search using the previous regexp search string, press <code>C-r</code> immediately.</dd>

  <dt><dfn>
  C-M-s &lt;RET&gt;<br>
  M-x re-search-forward</dfn></dt>
  <dd>Begin a nonincremental regexp search forward.</dd>

  <dt><dfn>
  C-M-r &lt;RET&gt;<br>
  M-x re-search-backward</dfn></dt>
  <dd>Begin a nonincremental regexp search backward.</dd>

  <dt><dfn>
  M-x multi-isearch-buffers</dfn></dt>
  <dd>Prompt for one ore more buffer names. Then, begin an incremental search forward in the first buffer specified. If the search fails in that buffer (or reaches the end of it), then the next <code>C-s</code> tries searching the next specified buffer, and so forth.</dd>

  <dt><dfn>
  M-x multi-isearch-files</dfn></dt>
  <dd>Prompt for one ore more file names. Then, begin an incremental search forward in the first file specified. If the search fails in that file (or reaches the end of it), then the next <code>C-s</code> tries searching the next specified file, and so forth.</dd>

  <dt><dfn>
  M-x multi-isearch-buffers-regexp</dfn></dt>
  <dd>Prompt for one ore more buffer names. Then, begin an incremental regexp search forward in the first buffer specified. If the search fails in that buffer (or reaches the end of it), then the next <code>C-s</code> tries searching the next specified buffer, and so forth.</dd>

  <dt><dfn>
  M-x multi-isearch-files-regexp</dfn></dt>
  <dd>Prompt for one ore more file names. Then, begin an incremental regexp search forward in the first file specified. If the search fails in that file (or reaches the end of it), then the next <code>C-s</code> tries searching the next specified file, and so forth.</dd>

  <dt><dfn>
  M-x occur<br>
  M-x list-matching-lines</dfn></dt>
  <dd>
<p>Prompt for a regexp, and display a list showing each line in the buffer that contains a match for it. A numeric argument N specifies that N lines of context are to be displayed before and after each matching line.</p>

<p>In the *Occur* buffer, you can click on each entry, or move point there and type &lt;RET&gt;, to visit the corresponding position in the buffer that was search. <code>o</code> displays the match in another window; <code>C-o</code> opens the match in another window, but doesn't select that window. Alternatively, you can use the <code>C-x `</code> command to visit the occurrences one by one.</p>

<p>Typing <code>e</code> in the *Occur* buffer switches to Occur Edit mode, in which edits made to the entries are also applied to the text in the originating buffer. Type <code>C-c C-c</code> to return to Occur mode.</p>
  </dd>

  <dt><dfn>
  M-s o</dfn></dt>
  <dd>Run <code>occur</code> using the search string of the last incremental string search. You can also run <code>M-s o</code> when an incrmental search is active; this uses the current search string.</dd>

  <dt><dfn>
  M-x multi-occur</dfn></dt>
  <dd>This command is just like <code>occur</code>, except it is able to search through multiple buffers. It asks you to specify the buffer names one by one.</dd>

  <dt><dfn>
  M-x multi-occur-in-matching-buffers</dfn></dt>
  <dd>This command is similar to <code>multi-occur</code>, except the buffers to search are specified by a regular expression that matches visited file names. With a prefix argument, it uses the regular expression to match buffer names instead.</dd>

  <dt><dfn>
  M-x how-many</dfn></dt>
  <dd>Prompt for a regular expression and print the number of matches for it in the buffer after point. If the region is active, this operates on the region instead.</dd>

  <dt><dfn>
  M-x grep<br>
  M-x lgrep</dfn></dt>
  <dd>
<p>Run <code>grep</code> asynchronously under Emacs, listing matching lines in the buffer named *grep*. Use the same arguments you would give grep when running it normally. Your command need not simply run <code>grep</code>; you can use any shell command that produces output in the same format as grep. You can also chain together <code>grep</code> commands.</p>

<p>"lgrep" means "local grep."</p>

<p>If you specify a prefix argument for <code>M-x grep</code>, it finds the tag in the buffer around point, and puts that into the default <code>grep</code> command.</p>
  </dd>

  <dt><dfn>
  M-x grep-find<br>
  M-x find-grep<br>
  M-x rgrep</dfn></dt>
  <dd>
<p>Run <code>grep</code> via <code>find</code>, and collect output in the *grep* buffer.</p>

<p>"rgrep" means "recursive grep."</p>
  </dd>

  <dt><dfn>
  M-x zrgrep<br>
  M-x rzgrep</dfn></dt>
  <dd>
<p>Run <code>zgrep</code> and collect output in the *grep* buffer.</p>

<p>"zrgrep" and "rzgrep" both mean recursive grep for gzipped files.</p>
  </dd>

  <dt><dfn>
  M-x kill-grep</dfn></dt>
  <dd>Kill the running <code>grep</code> subprocess.</dd>

  <dt><dfn>
  M-.<br>
  M-x find-tag</dfn></dt>
  <dd>Prompt for a tag name and jump to its source definition. When you want to go back to where you jumped from, type <code>M-*</code> (<code>M-x pop-tag-mark</code>).</dd>

  <dt><dfn>
  M-x tags-search &lt;RET&gt; REGEXP &lt;RET&gt;</dfn></dt>
  <dd>Search for the specified regular expression through the files in the selected tags table. As soon as it finds an occurrence, the search terminates. To find the next match, type <code>M-,</code> (<code>M-x tags-loop-continue</code>).</dd>

  <dt><dfn>
  M-x find-dired</dfn></dt>
  <dd>Run <code>find</code> and then populate a Dired buffer with the output.</dd>

  <dt><dfn>
  M-x find-grep-dired</dfn></dt>
  <dd>Find files in the specified directory that contain the specified regular expression, and then populate a Dired buffer with those files.</dd>

  <dt><dfn>
  M-x find-name-dired</dfn></dt>
  <dd>Find file names recursively starting from the specified directory that match the specified globbing pattern, and then populate a Dired buffer with the matching files.</dd>

  <dt><dfn>
  M-x locate</dfn></dt>
  <dd>Use the <code>locate</code> command to find files, and then populate a *Locate* buffer with the output of the command.</dd>
</dl>


## Replace

The replace commands normally operate on the text from point to the end of the buffer. When the region is active, they operate on it instead.

Unlike incremental search, the replacement commands do not use lax space matching by default.

If the first argument of a replace command is all lowercase, the command ignores case while searching for occurrences to replace. When the NEW_STRING argument is all lowercase, replacement commands try to preserve the case pattern of each occurrence as long as the occurrence is all lowercase, all uppercase, or capitalised. If uppercase letters are used in the replacement string, they remain uppercase every time that text is inserted. If uppercase letters are used in the first argument, the second argument is always substituted exactly as given, with no case conversion.

To restart a query replace once it is exited, use <code>C-x &lt;ESC&gt; &lt;ESC&gt;</code>.

<dl>
  <dt><dfn>
  M-x replace-string &lt;RET&gt; OLD_STRING &lt;RET&gt; NEW_STRING &lt;RET&gt;</dfn></dt>
  <dd>Unconditionally replace every occurrence of OLD_STRING after point with NEW_STRING. If you want to replace all occurrences in the buffer, then you need to go to the beginning of the buffer first. If you want to limit the replacement to part of the buffer, then activate the region around that part (when the region is active, replacement is limited to the region) or narrow the buffer to that part. When <code>replace-string</code> exits, it leaves point at the last occurrence replaced. It adds the prior position of point (where the <code>replace-string</code> command was issued) to the mark ring, without activating the mark; use <code>C-u C-&lt;SPC&gt;</code> to move back there.</dd>

  <dt><dfn>
  M-x replace-regexp &lt;RET&gt; REGEXP &lt;RET&gt; NEW_STRING &lt;RET&gt;</dfn></dt>
  <dd>
<p>Unconditionally replace every occurrence of REGEXP after point with NEW_STRING.</p>

<p>\& in NEW_STRING stands for the entire match being replaced.</p>

<p>\N in NEW_STRING, where N is a digit, stands for whatever matched the Nth parenthesized grouping in REGEXP. This is called a back reference.</p>

<p>\# in NEW_STRING stands for the count of replacements already made in this command. In the first replacement, \# stands for 0; in the second, for 1; and so on.</p>

<p>If you want to enter part of the replacement string by hand each time, use <code>\?</code> in the replacement string. Each replacement will ask you to edit the replacement string in the minibuffer, putting point where the <code>\?</code> was.</p>
  </dd>

  <dt><dfn>
  M-% OLD_STRING &lt;RET&gt; NEW_STRING &lt;RET&gt;<br>
  M-x query-replace</dfn></dt>
  <dd>
<p>Replace some occurrences of OLD_STRING after point with NEW_STRING. This command finds occurrences of OLD_STRING one by one, displaying the occurrence and asking you whether to replace it. Type <code>C-h</code> for help.</p>

<p>If you're in an incremental search, you can type <code>M-%</code> to invoke <code>query-replace</code> or <code>query-replace-regexp</code> (depending on the search mode) with the search string used as the string to replace.</p>
  </dd>

  <dt><dfn>
  C-M-% REGEXP &lt;RET&gt; NEW_STRING &lt;RET&gt;<br>
  M-x query-replace-regexp</dfn></dt>
  <dd>Replace some occurrences of REGEXP after point with NEW_STRING. This command finds occurrences of REGEXP one by one, displaying the occurrence and asking you whether to replace it. By default, query-replace-regexp will show the substituted replacement string for the current match in the minibuffer. Type <code>C-h</code> for help.</dd>

  <dt><dfn>
  M-x tags-query-replace &lt;RET&gt; REGEXP &lt;RET&gt; REPLACEMENT &lt;RET&gt;</dfn></dt>
  <dd>Perform a <code>query-replace-regexp</code> on each file in the selected tags table.</dd>

  <dt><dfn>
  M-x isearch-query-replace</dfn></dt>
  <dd>Begin <code>query-replace</code> with the string used in the last incremental search.</dd>

  <dt><dfn>
  M-x isearch-query-replace-regexp</dfn></dt>
  <dd>Begin <code>query-replace-regexp</code> with the regular expression used in the last incremental regexp search. You can use back references and such, just like you normally could.</dd>

  <dt><dfn>
  C-x r t NEW_STRING<br>
  M-x replace-rectangle</dfn></dt>
  <dd>Replace the contents of the region-rectangle with the specified string. It doesn't matter if the string is smaller or bigger than the rectangle; the rectangle will be resized appropriately.</dd>
</dl>


# Killing, Deleting, Copying, and Yanking


## Kill (Cut)

"Killing" means erasing text and copying it into the kill ring; some applications use the term "cutting" for a similar operation. There are commands for killing many different types of syntactic units (words, sentences, lines, paragraphs, etc.). Commands that kill normally contain the word "kill" in their name.

Normally, each kill command pushes a new entry onto the kill ring; however, any sequence of two or more kill commands in a row combine their text into a single entry, so that a single <code>C-y</code> yanks all the text as a unit. Any non-kill commands breaks the sequence; if you break the sequence, but you still want to append to the kill ring, then press <code>C-M-w</code> (<code>M-x append-next-kill</code>) before you kill. Commands that kill forward from point add onto the end of the previous killed text. Commands that kill backward from point add text onto the beginning. This way, any sequence of mixed forward and backward kill commands puts all the killed text into one entry without rearrangement. The text in the kill ring entry always has the same order that it had in the buffer before you killed it. A kill command following <code>M-w</code> (<code>M-x kill-ring-save</code>) does not append to the text that <code>M-w</code> copied into the kill ring.

When you undo a kill command, that brings the killed text back into the buffer, but does not remove it from the kill ring.

The kill commands work specially in a read-only buffer: they copy instead of cut.

<dl>
  <dt><dfn>
  M-d<br>
  C-&lt;Delete&gt;<br>
  M-x kill-word</dfn></dt>
  <dd>Kill forward one word.</dd>

  <dt><dfn>
  M-&lt;DEL&gt;<br>
  C-&lt;DEL&gt;<br>
  M-x backward-kill-word</dfn></dt>
  <dd>Kill backward one word.</dd>

  <dt><dfn>
  M-k<br>
  M-x kill-sentence</dfn></dt>
  <dd>Kill forward from point to the end of one sentence.</dd>

  <dt><dfn>
  C-x &lt;DEL&gt;<br>
  M-x backward-kill-sentence</dfn></dt>
  <dd>Kill backward from point to the beginning of one sentence.</dd>

  <dt><dfn>
  C-k<br>
  M-x kill-line</dfn></dt>
  <dd>
<p>If there are visible (non-whitespace) characters after point, kill forward from point to the end of the current logical line (not including the newline). Press C-k again to kill the newline.</p>

<p>If point is after the last visible character in the line, <code>C-k</code> will kill all the whitespace (including the newline).</p>
  </dd>

  <dt><dfn>
  M-0 C-k<br>
  C-u 0 C-k<br>
  C-u C-0 C-k</dfn></dt>
  <dd>Kill backward from point to the beginning of one logical line.</dd>

  <dt><dfn>
  C-S-&lt;DEL&gt;<br>
  C-a C-k C-k<br>
  M-x kill-whole-line</dfn></dt>
  <dd>Kill one whole logical line, regardless of where point is in it.</dd>

  <dt><dfn>
  M-x kill-paragraph</dfn></dt>
  <dd>Kill forward from point to the end of one paragraph.</dd>

  <dt><dfn>
  M-x backward-kill-paragraph</dfn></dt>
  <dd>Kill backward from point to the beginning of one paragraph.</dd>

  <dt><dfn>
  C-x C-p C-w<br>
  C-x C-p S-&lt;DEL&gt;</dfn></dt>
  <dd>Kill one whole page (up to and including ^L) regardless of where point is in the page. If you simply press <code>&lt;DEL&gt;</code> instead of <code>S-&lt;DEL&gt;</code> or <code>C-w</code>, then that will delete the text instead of killing it.</dd>

  <dt><dfn>
  C-M-k<br>
  M-x kill-sexp</dfn></dt>
  <dd>Kill forward from point to the end of one expression (could be an identifier, literal, keyword, or whatever) that is at the same nesting level as point.</dd>

  <dt><dfn>
  &lt;ESC&gt; C-&lt;Delete&gt;<br>
  &lt;ESC&gt; C-&lt;DEL&gt;<br>
  M-x backward-kill-sexp</dfn></dt>
  <dd>Kill backward from point to the beginning of one expression (could be an identifier, literal, keyword, or whatever) that is at the same nesting level as point.</dd>

  <dt><dfn>
  M-x kill-backward-up-list</dfn></dt>
  <dd>Kill any expression within a balanced pair of delimiters, other than the expression that point is on, and kill the balanced pair of delimiters; for example, if you have "(foo bar baz)" with point on "bar" and you invoke <code>M-x kill-backward-up-list</code>, then you will be left with "bar".</dd>

  <dt><dfn>
  C-w<br>
  S-&lt;DEL&gt;<br>
  M-x kill-region</dfn></dt>
  <dd>Kill the region.</dd>

  <dt><dfn>
  M-z CHARACTER<br>
  M-x zap-to-char</dfn></dt>
  <dd>Kill forward from point to the next occurrence of CHARACTER. With a negative prefix argument (<code>C-u - M-z CHARACTER</code> or <code>M-- M-z CHARACTER), kill backward from point to the next occurrence of CHARACTER.</dd>

  <dt><dfn>
  C-x r k<br>
  M-x kill-rectangle</dfn></dt>
  <dd>Kill the text of the region-rectangle.</dd>

  <dt><dfn>
  M-x clipboard-kill-region</dfn></dt>
  <dd>Kill the region, and save it in the X clipboard.</dd>
</dl>


## Delete

"Deleting" means erasing text, but not copying it into the kill ring. Commands that can erase significant amounts of nontrivial data generally do a kill operation instead of a delete. For the most part, the Emacs commands that delete text are those that erase just one character or only whitespace. Commands that delete normally contain the word "delete" in their name.

<dl>
  <dt><dfn>
  C-d<br>
  M-x delete-char<br>
  &lt;Delete&gt;<br>
  M-x delete-forward-char</dfn></dt>
  <dd>Delete forward one character. If you're at the end of a line, <code>C-d</code> will delete the newline. If a region is active, delete the text in the region instead of deleting a single character.</dd>

  <dt><dfn>
  &lt;DEL&gt;<br>
  M-x delete-backward-char</dfn></dt>
  <dd>Delete backward one character. If you're at the beginning of a line, <code>&lt;DEL&gt;</code> will delete the newline. If a region is active, delete the text in the region instead of deleting a single character.</dd>

  <dt><dfn>
  M-\<br>
  M-x delete-horizontal-space</dfn></dt>
  <dd>Delete spaces and tabs around point.</dd>

  <dt><dfn>
  M-&lt;SPC&gt;<br>
  M-x just-one-space</dfn></dt>
  <dd>Delete spaces and tabs around point, leaving one space.</dd>

  <dt><dfn>
  C-x C-o<br>
  M-x delete-blank-lines</dfn></dt>
  <dd>
<p>If point is on a blank line that is surrounded by one or more blank lines on either side, then delete all the surrounding blank lines, leaving just one blank line.</p>

<p>If point is on a blank line that is not surrounded by any blank lines on either side, then delete the current blank line.</p>

<p>If point is on a nonblank line that precedes one or more blank lines, then delete all following blank lines up to the next nonblank line.</p>

<p>If point is on a nonblank line that is not followed by any blank lines, then do nothing.</p>
  </dd>

  <dt><dfn>
  M-^<br>
  M-x delete-indentation</dfn></dt>
  <dd>Join two lines by deleting the intervening newline, along with any indentation following it.</dd>

  <dt><dfn>
  C-M-h &lt;DEL&gt;</dfn></dt>
  <dd>Delete the current defun (function, class, template, struct, or any other major definition).</dd>

  <dt><dfn>
  M-x erase-buffer</dfn></dt>
  <dd>Delete the entire contents of the current buffer.</dd>

  <dt><dfn>
  M-x flush-lines<br>
  M-x delete-matching-lines</dfn></dt>
  <dd>Delete any line after point that contains a match for the specified regular expression.</dd>

  <dt><dfn>
  M-x keep-lines<br>
  M-x delete-non-matching-lines</dfn></dt>
  <dd>Delete any line after point that doesn't contain a match for the specified regular expression.</dd>

  <dt><dfn>
  M-x delete-pair</dfn></dt>
  <dd>Delete a pair of characters enclosing the sexp that follows point.</dd>

  <dt><dfn>
  C-x r d<br>
  M-x delete-rectangle</dfn></dt>
  <dd>Delete the text in the region-rectangle.</dd>

  <dt><dfn>
  M-x delete-region</dfn></dt>
  <dd>Delete the text in the region.</dd>

  <dt><dfn>
  M-x delete-trailing-whitespace</dfn></dt>
  <dd>Delete trailing whitespace in the region.</dd>

  <dt><dfn>
  M-x delete-whitespace-rectangle</dfn></dt>
  <dd>Delete all whitespace following a specified column in each line.</dd>

  <dt><dfn>
  C-M-w<br>
  M-x isearch-del-char</dfn></dt>
  <dd>Delete the last character from the search string.</dd>

  <dt><dfn>
  C-x r c<br>
  M-x clear-rectangle</dfn></dt>
  <dd>Black out the region-rectangle.</dd>

  <dt><dfn>
  C-e C-k<br>
  C-e &lt;Delete&gt;</dfn></dt>
  <dd>Merge the current line with the next line (delete the newline at the end of the current line).</dd>

  <dt><dfn>
  C-a &lt;DEL&gt;</dfn></dt>
  <dd>Merge the current line with the previous line.</dd>
</dl>


## Copy

<dl>
  <dt><dfn>
  M-w<br>
  M-x kill-ring-save</dfn></dt>
  <dd>Copy the region into the kill ring.</dd>

  <dt><dfn>
  M-x clipboard-kill-ring-save</dfn></dt>
  <dd>Copy the region into the kill ring, and save it in the X clipboard.</dd>

  <dt><dfn>
  C-x r M-w<br>
  M-x copy-rectangle-as-kill</dfn></dt>
  <dd>Copy the region-rectangle and save it as the last killed one.</dd>

  <dt><dfn>
  M-x copy-region-as-kill</dfn></dt>
  <dd>Copy the region and save it as the last killed one.</dd>
</dl>


## Yank (Paste)

"Yanking" means reinserting text that was previously killed (you can think of it as yanking back, or pulling back, some text that was taken away); some applications use the term "pasting" for a similar operation. Note that Vim uses the term "yank" to mean "copy".

<dl>
  <dt><dfn>
  C-y<br>
  M-x yank</dfn></dt>
  <dd>Yank (paste) the last kill into the buffer at point.</dd>

  <dt><dfn>
  M-x append-to-buffer</dfn></dt>
  <dd>Append region to the contents of the specified buffer wherever point is in that buffer, and then place point after the appended region in that buffer. If you specify a nonexistent buffer, the buffer will be created.</dd>

  <dt><dfn>
  M-x prepend-to-buffer</dfn></dt>
  <dd>Prepend region to the contents of the specified buffer wherever point is in that buffer, and tehn place point before the prepended region in that buffer. If you specify a nonexistent buffer, the buffer will be created.</dd>

  <dt><dfn>
  M-x copy-to-buffer</dfn></dt>
  <dd>Copy region into the specified buffer, deleting that buffer's old contents.</dd>

  <dt><dfn>
  M-x insert-buffer</dfn></dt>
  <dd>Insert the contents of the specified buffer into the current buffer at point, leaving point at the beginning of the inserted text. It also adds the position of the end of the inserted text to the mark ring, without activating the mark.</dd>

  <dt><dfn>
  M-x append-to-file</dfn></dt>
  <dd>Append region to the contents of the specified file. The file is changed immediately on disk. You should use <code>append-to-file</code> only with files that are not being visited in Emacs.</dd>

  <dt><dfn>
  C-y<br>
  M-x isearch-yank-kill</dfn></dt>
  <dd>Yank into an incremental search.</dd>

  <dt><dfn>
  M-x clipboard-yank</dfn></dt>
  <dd>Yank the clipboard contents.</dd>

  <dt><dfn>
  C-M-y<br>
  M-x isearch-yank-char</dfn></dt>
  <dd>Yank the next character from the buffer into the search string.</dd>

  <dt><dfn>
  M-s C-e<br>
  M-x isearch-yank-line</dfn></dt>
  <dd>Yank the rest of the line from the buffer into the search string.</dd>

  <dt><dfn>
  M-x isearch-yank-word</dfn></dt>
  <dd>Yank the next word from the buffer into the search string.</dd>

  <dt><dfn>
  C-w<br>
  M-x isearch-yank-word-or-char</dfn></dt>
  <dd>Yank the next character, subword, or word from the buffer into the search string.</dd>

  <dt><dfn>
  M-x isearch-yank-x-selection</dfn></dt>
  <dd>Yank the current X selection into the search string.</dd>

  <dt><dfn>
  C-x r y<br>
  M-x yank-rectangle</dfn></dt>
  <dd>Yank the last killed rectangle with upper left corner at point.</dd>
</dl>


## Clipboard

In most grahpical desktop environments, you can transfer data (usually text) between different applications using a system facility called the "clipboard." On X, two other similar facilities are available: the primary selection and the secondary selection. In graphical Emacs, the kill and yank commands integrate with these facilities, so that you can easily transfer text between Emacs and other graphical applications.

By default, Emacs uses UTF-8 as the coding system for inter-program text transfers.

When you kill or copy something to the kill ring, that text is also put in the system clipboard.

If another application "owns" the clipboard (i.e., if you cut or copied text there more recently than your last kill command in Emacs), then Emacs yanks from the clipboard instead of the kill ring.

Many X desktop environments support a feature called the "clipboard manager." If you exit Emacs while it is the current "owner" of the clipboard data, and there is a clipboard manager running, Emacs transfers the clipboard data to the clipboard manager so that it is not lost. In some circumstances, this may cause a delay when exiting Emacs.

Under the X Window System, there exists a "primary selection" containing the last stretch of text selected in an X application (usually by dragging the mouse). Typically, this text can be inserted into other X applications by mouse-2 clicks (middle clicks). The primary selection is separate from the clipboard. Its contents are more fragile; they are overwritten each time you select text with the mouse, whereas the clipboard is only overwritten by explicit cut or copy commands. Under X, whenever the region is active, the text in the region is saved in the primary selection. This applies regardless of whether the region was made by dragging or clicking the mouse, or by keyboard commands. To insert the primary selection into an Emacs buffer, click <code>mouse-2</code> (middle click) (<code>M-x mouse-yank-primary</code>) where you want to insert it.

In addition to the primary selection, the X Window System provides a second similar facility known as the secondary selection. Nowadays, few X applications make use of the secondary selection. I assume the secondary selection is a lot like the primary selection, except it can be used for the cases where you don't want to overwrite the clipboard selection or the primary selection. To set the secondary selection, press and hold <code>Alt</code> (<code>M-</code>), drag mouse-1 (the left mouse button) to highlight the text you want, and then release <code>Alt</code> (<code>M-</code>). Alternatively, press <code>M-Mouse-1</code> (the left mouse button) (<code>M-x mouse-start-secondary</code>) at one end of the text and press <code>M-Mouse-3</code> (the right mouse button) (<code>M-x mouse-secondary-save-then-kill</code>) at the other end. To insert the secondary selection where you click, press <code>M-Mouse-2</code> (the middle mouse button) (<code>M-x mouse-yank-secondary</code>).


# Completion

"Completion" means that Emacs can fill in the rest of what you're typing, or some of it, based on what you've typed so far. Suggestions for possible completions are called "completion alternatives" or simply "completions."

When a command reads an argument using the minibuffer with completion, it also controls what happens when you type <code>&lt;RET&gt;</code> (<code>M-x minibuffer-complete-and-exit</code>) to submit the argument. There are four types of behaviour:

<ol>
  <li>"Strict completion" accepts only exact completion matches. Typing <code>&lt;RET&gt;</code> exits the minibuffer only if the minibuffer text is an exact match, or completes to one.</li>
  <li>"Cautious completion" is like strict completion, except <code>&lt;RET&gt;</code> exits only if the text is already an exact match. If the text completes to an exact match, <code>&lt;RET&gt;</code> performs that completion but does not exit yet; you must type a second &lt;RET&gt; to exit.</li>
  <li>"Permissive completion" allows any input; the completion candidates are just suggestions. Typing <code>&lt;RET&gt;</code> does not complete, it just submits the argument as you have entered it.</li>
  <li>"Permissive completion with confirmation" is like permissive completion, with an exception: if you typed <code>&lt;TAB&gt;</code> and this completed the text up to some intermediate state (i.e., one that is not yet an exact completion match), typing <code>&lt;RET&gt;</code> right afterward does not submit the argument. Instead, Emacs asks for confirmation. Type <code>&lt;RET&gt;</code> again to confirm and submit the text. This catches a common mistake, in which one types <code>&lt;RET&gt;</code> before realising that <code>&lt;TAB&gt;</code> did not complete as far as desired.</li>
</ol>

Completion commands work by narrowing a large list of possible completion alternatives to a smaller subset that matches what you have typed in the minibuffer. Emacs performs completion using one or more "completion styles"--sets of criteria for matching minibuffer text to completion alternatives. During completion, Emacs tries each completion style in turn. If a style yields one or more matches, that is used as the list of completion alternatives. If a style produces no matches, Emacs falls back to the next style.

The default completion styles are (in order):

<ol>
  <li>"basic": A matching completion alternative must have the same beginning as the text in the minibuffer before point. Furthermore, if there is any text in the minibuffer after point, the rest of the completion alternative must contain that text as a substring.</li>
  <li>"partial-completion": This aggressive completion style divides the minibuffer text into words separated by hyphens or spaces, and completes each word separately; for example, when completing command names, <code>em-l-m</code> completes to <code>emacs-lisp-mode</code>. furthermore, a <code>*</code> in the minibuffer text is treated as a wildcard--it matches any character at the corresponding position in the completion alternative.</li>
  <li>"emacs22": This completion style is similar to "basic", except that is ignores the text in the minibuffer after point. It is so-named because it corresponds to the completion behaviour in Emacs 22.</li>
</ol>

The following additional completion styles are also defined, and you can add them to the <code>completion-styles</code> variable if you want to use them:

<ol>
  <li>"substring": A matching completion alternative must contain the text in the minibuffer before point, and the text in the minibuffer after point, as substrings (in that same order).</li>
  <li>"initials": This very aggressive completion style attempts to complete acronyms and initialisms; for example, when completing command names, it matches <code>lch</code> to <code>list-command-history</code>.</li>
  <li>"emacs21": A matching completion alternative must start with the text in the minibuffer.</li>
</ol>

Case is significant when completing case-sensitive arguments, such as command names. Case differences are ignored when completing arguments in which case does not matter.

Normally, if there is more than one completion alternative for the text in the minibuffer, a completion command completes up to the longest common substring.

Icomplete mode (<code>M-x icomplete-mode</code>) displays an indication of available completions when you are in the minibuffer and completion is active. The completion alternatives are listed in the minibuffer in curly braces after point.

File name completion ignores file names whose extensions appear in the variable <code>completion-ignored-extensions</code>.

File name completion works with TRAMP for completion of method names, of user names, and of machine names as well as for completion of file names on remote machines.

Dynamic abbreviations allow the meanings of abbreviations to be determined automatically from the contents of the buffer, but dynamic abbrev expansion happens only when you request it explicitly. In this context, think of any abbreviation as any word-size unit of text that can expand into a longer string.

<dl>
  <dt><dfn>
  &lt;TAB&gt;<br>
  M-x minibuffer-complete<br>
  M-x gud-gdb-complete-command</dfn></dt>
  <dd>
<p>In the minibuffer, complete the text in the minibuffer as much as possible; if unable to complete, display a list of possible completions.</p>

<p>In GDB, complete a symbol name.</p>
  </dd>

  <dt><dfn>
  &lt;SPC&gt;<br>
  M-x minibuffer-complete-word</dfn></dt>
  <dd>Complete up to one word (up to the next hyphen or space) from the minibuffer text before point. This command is not available for arguments that often include spaces, such as file names.</dd>

  <dt><dfn>
  &lt;RET&gt;<br>
  M-x minibuffer-complete-and-exit<br>
  M-x choose-completion</dfn></dt>
  <dd>
<p>In the minibuffer, submit the text in the minibuffer as the argument, possibly completing first.</p>

<p>In the completion list buffer, choose the completion at point.</p>
  </dd>

  <dt><dfn>
  ?<br>
  M-x minibuffer-completion-help</dfn></dt>
  <dd>Display a list of completions.</dd>

  <dt><dfn>
  M-v<br>
  &lt;PageUp&gt;<br>
  M-x switch-to-completions</dfn></dt>
  <dd>Typing <code>M-v</code>, while in the minibuffer, selects the window showing the completion list.</dd>

  <dt><dfn>
  &lt;right&gt;<br>
  M-x next-completion</dfn></dt>
  <dd>In the completion list buffer, move point to the next completion alternative.</dd>

  <dt><dfn>
  &lt;left&gt;<br>
  M-x previous-completion</dfn></dt>
  <dd>In the completion list buffer, move point to the previous completion alternative.</dd>

  <dt><dfn>
  M-&lt;TAB&gt;<br>
  &lt;ESC&gt; &lt;TAB&gt;<br>
  M-x isearch-complete<br>
  M-x ispell-complete-word<br>
  M-x completion-at-point<br>
  M-x widget-complete</dfn></dt>
  <dd>
<p>In incremental search, attempt to complete the search string using the search ring as a list of completion alternatives.</p>

<p>In a buffer, complete the word before point based on the spelling dictionary. You can also use <code>C-M-i</code>.</p>

<p>In programming language modes, type <code>C-M-i</code>, <code>M-&lt;TAB&gt;</code>, or <code>&lt;ESC&gt; &lt;TAB&gt;</code> to complete the partial symbol before point. If Semantic mode is enabled, it tries to use the Semantic parser data for completion. If Semantic mode is not enabled or fails at performing completion, it tries to complete using the selected tags table. If in Emacs Lisp mode, it performs completion using the function, variable, or property names defined in the current Emacs session.</p>
  </dd>

  <dt><dfn>
  C-&lt;TAB&gt;<br>
  M-x file-cache-minibuffer-complete</dfn></dt>
  <dd>You can use the file name cache to make it easy to locate a file by name, without having to remember exactly where it is located. When typing a file name in the minibuffer, <code>C-&lt;TAB&gt;</code> completes it using the file name cache. If you repeat <code>C-&lt;TAB&gt;</code>, that cycles through the possible completions of what you had originally typed. The file name cache does not fill up automatically. Also, the file name cache is not persistent: it is kept and maintained only for the duration of the Emacs session.</dd>

  <dt><dfn>
  C-c , &lt;SPC&gt;<br>
  M-x semantic-complete-analyze-inline</dfn></dt>
  <dd>In Semantic mode, display a list of possible completions for the symbol at point. This also activates a set of special key bindings for choosing a completion: <code>&lt;RET&gt;</code> accepts the current completion, <code>M-n</code> and <code>M-p</code> cycle through possible completions, <code>&lt;TAB&gt;</code> completes as far as possible and then cycles, and <code>C-g</code> or any other key aborts completion.</dd>

  <dt><dfn>
  C-c , l<br>
  M-x semantic-analyze-possible-completions</dfn></dt>
  <dd>Display a list of the possible completions of the symbol at point, in another window.</dd>

  <dt><dfn>
  M-?<br>
  M-x comint-dynamic-list-filename-completions</dfn></dt>
  <dd>In Shell mode, display temporarily a list of the possible completions of the file name before point.</dd>

  <dt><dfn>
  M-/<br>
  M-x dabbrev-expand</dfn></dt>
  <dd>Expand the word in the buffer before point by searching backward in the buffer for the first word that starts with the word before point as a prefix. Repeating <code>M-/</code> searches for an alternative expansion by looking farther back. After scanning all the text before point, the search continues after point. After scanning the current buffer, <code>M-/</code> normally searches other buffers.</dd>

  <dt><dfn>
  C-M-/<br>
  M-x dabbrev-completion</dfn></dt>
  <dd>Perform completion of a dynamic abbreviation. Instead of trying the possible expansions one by one, it finds all of them, then inserts the text that they have in common. If they have nothing in common, <code>C-M-/</code> displays a list of completions, from which you can select a choice in the usual manner.</dd>
</dl>


# Rings

A ring is so-named because it can be visualised as a set of things arranged in a ring, which you can access in cyclic order (when you're at the end and you access the next item, you go back to the beginning; when you're at the beginning and you access the previous item, you go back to the end). There are several types of rings.

The mark ring is used to hold several recent previous locations of the mark, in case you want to move back to them. Each buffer has its own mark ring; in addition, there is a single global mark ring. The global mark ring records the series of buffers you have recently set a mark in. In many cases you can use this to backtrack through buffers you have been editing, or in which you have found tags. When you use a command that sets mark (such as <code>C-&lt;SPC&gt; C-&lt;SPC&gt;</code>), the command will push the old mark onto the mark ring. The mark will also be pushed onto the global mark ring, where the buffer associated with the mark is also pushed onto the ring. By default, a buffer's mark ring can only store 16 marks; when the mark ring is full, a subsequent push will cause the oldest mark to be discarded. By default, the global mark ring can only store 16 marks.

The kill ring is where all text you have killed recently is saved. You can reinsert any of the killed text still in the ring; this is called yanking. There is only one kill ring, shared by all buffers, so you can kill text in one buffer and yank it in another buffer. By default, the kill ring can only store 60 kills; when the kill ring is full, a subsequent kill will cause the oldest kill to be discarded. The actual contents of the kill ring are stored in a variable named <code>kill-ring</code>; you can view the entire contents of the kill ring with <code>C-h v kill-ring</code>.

The keyboard macro ring (or macro ring for short) stores all the keyboard macros you have defined. There is only one keyboard macro ring, shared by all buffers. By default, the keyboard macro ring can only store 8 keyboard macros; when the keyboard macro ring is full, a subsequent push will cause the oldest keyboard macro to be discarded. All commands that operate on the keyboard macro ring use the same <code>C-x C-k</code> prefix; these commands can be executed and repeated immediately after each other without needing you to type the <code>C-x C-k</code> prefix each time. When you move to the next or previous item in the keyboard macro ring, the definition of the new head macro is displayed in the echo area. Emacs treats the head of the macro ring as the last defined keyboard macro.

The shell history ring (or shell ring for short) stores all the previously entered shell commands and their arguments. Outside Emacs, some shells store their command histories in files so that you can refer to commands from previous shell sessions. Emacs reads the command history file for your chosen shell, to initialise its own command history. The file name is usually "~/.bash_history" for bash, "~/.zsh_history" for zsh, "~/.sh_history" for ksh, and "~/.history" for other shells.

The search ring stores all your previous searches. String-based searches and regexp-based searches have separate search rings.

TODO: tag ring

For each type of ring, you can think of moving through the ring as moving a pointer through it. If you move through a ring and then start doing other things, the pointer will still be pointing to the same position you were in the ring, so you can pick up from where you left off once you start moving through the ring again.

<dl>
  <dt><dfn>
  C-u C-&lt;SPC&gt;<br>
  C-u C-@<br>
  C-u M-x set-mark-command</dfn></dt>
  <dd>Move to the previous mark in the current buffer's mark ring.</dd>

  <dt><dfn>
  C-x C-&lt;SPC&gt;<br>
  C-x C-@<br>
  M-x pop-global-mark</dfn></dt>
  <dd>Move to the previous mark in the global mark ring.</dd>

  <dt><dfn>
  M-y<br>
  M-x yank-pop</dfn></dt>
  <dd>
<p>If the previous command was a yank command, <code>M-y</code> takes the text that was yanked and replaces it with the text from an earlier kill. <code>M-y</code> is allowed only after a <code>C-y</code> or another <code>M-y</code>; the first time you use <code>M-y</code>, you have to use <code>C-y</code> first.</p>

<p>With a negative numeric argument, move forward through the kill ring instead of backward.</p>
  </dd>

  <dt><dfn>
  C-x C-k C-k<br>
  M-x kmacro-end-or-call-macro-repeat</dfn></dt>
  <dd>Execute the keyboard macro at the head of the keyboard macro ring.</dd>

  <dt><dfn>
  C-x C-k C-n<br>
  M-x kmacro-cycle-ring-next</dfn></dt>
  <dd>Rotate the keyboard macro ring to the next macro.</dd>

  <dt><dfn>
  C-x C-k C-p<br>
  M-x kmacro-cycle-ring-previous</dfn></dt>
  <dd>Rotate the keyboard macro ring to the previous macro.</dd>

  <dt><dfn>
  M-p<br>
  C-&lt;Up&gt;</dfn></dt>
  <dd>
<p>In a search, rotate the search ring to the previous search string.</p>

<p>In a shell buffer, rotate the shell history ring to the previous shell command and its arguments.</p>
  </dd>

  <dt><dfn>
  M-n<br>
  C-&lt;Down&gt;</dfn></dt>
  <dd>
<p>In a search, rotate the search ring to the next search string.</p>

<p>In a shell buffer, rotate the shell history ring to the next shell command and its arguments.</p>
  </dd>

  <dt><dfn>
  M-r</dfn></dt>
  <dd>In a shell buffer, begin an incremental regexp search of previous shell commands. Incremental search commands have their usual effects--for instance, <code>C-s</code> and <code>C-r</code> search forward and backward for the next match. <code>&lt;RET&gt; terminates the search.</dd>

  <dt><dfn>
  C-c C-x</dfn></dt>
  <dd>In a shell buffer, fetch the next subsequent command from the history.</dd>

  <dt><dfn>
  C-c .<br>
  M-x comint-input-previous-argument</dfn></dt>
  <dd>In a shell buffer, fetch the last argument from the previous command. With a numeric prefix, fetch the Nth argument instead. Repeating <code>C-c .</code> fetches from an earlier shell command, always using the same value of N (if you used a prefix argument).</dd>

  <dt><dfn>
  C-c C-l<br>
  M-x comint-dynamic-list-input-ring</dfn></dt>
  <dd>In a shell buffer, display the buffer's history of shell commands in another window.</dd>
</dl>


# Registers

Registers can store positions, pieces of text, rectangles, numbers, window configurations, or file names, but each register can only store one thing at any given time. Whatever you store in a register remains there until you store something else in that register.

Each register has a case-sensitive name (register 'r' is different from register 'R') that consists of a single character (a letter or a number).

When a register stores a position, you can think of that position as a named mark.

Registers don't persist across Emacs sessions.

<dl>
  <dt><dfn>
  M-x view-register &lt;RET&gt; REGISTER_NAME</dfn></dt>
  <dd>Display a description of what the specified register contains.</dd>

  <dt><dfn>
  M-x list-registers</dfn></dt>
  <dd>Display a list of nonempty registers saying briefly what they contain.</dd>

  <dt><dfn>
  C-x r &lt;SPC&gt; REGISTER_NAME<br>
  C-x r C-&lt;SPC&gt; REGISTER_NAME<br>
  C-x r C-@ REGISTER_NAME<br>
  M-x point-to-register</dfn></dt>
  <dd>Record the position of point and the current buffer in the specified register.</dd>

  <dt><dfn>
  C-x r j REGISTER_NAME<br>
  M-x jump-to-register</dfn></dt>
  <dd>Jump to the register and buffer or restore the window or frame configuration, depending on whether a position or a window configuration is stored in the register.</dd>

  <dt><dfn>
  C-x r s REGISTER_NAME<br>
  C-x r x REGISTER_NAME<br>
  M-x copy-to-register</dfn></dt>
  <dd>Copy the region into the specified register. With a prefix argument, delete the region from the buffer after copying it to the register.</dd>

  <dt><dfn>
  C-x r i REGISTER_NAME<br>
  C-x r g REGISTER_NAME<br>
  M-x insert-register</dfn></dt>
  <dd>Copy the text, rectangle, or number from the specified register into the current buffer.</dd>

  <dt><dfn>
  M-x append-to-register &lt;RET&gt; REGISTER_NAME</dfn></dt>
  <dd>Append the region to the existing text in the specified register. With a prefix argument, delete the region from the buffer after appending it to the register.</dd>

  <dt><dfn>
  M-x prepend-to-register &lt;RET&gt; REGISTER_NAME</dfn></dt>
  <dd>Prepend the region to the existing text in the specified register. With a prefix argument, delete the region from the buffer after prepending it to the register.</dd>

  <dt><dfn>
  C-x r r REGISTER_NAME<br>
  M-x copy-rectangle-to-register</dfn></dt>
  <dd>Copy the region-rectangle into the specified register. With a prefix argument, delete the region-rectangle from the buffer after copying it to the register.</dd>

  <dt><dfn>
  C-x r w REGISTER_NAME<br>
  M-x window-configuration-to-register</dfn></dt>
  <dd>Save the state of the selected frame's windows in the specified register.</dd>

  <dt><dfn>
  C-x r f REGISTER_NAME<br>
  M-x frame-configuration-to-register</dfn></dt>
  <dd>Save the state of all frames, including all their windows, in the specified register.</dd>

  <dt><dfn>
  C-u NUMBER C-x r n REGISTER_NAME<br>
  C-u NUMBER M-x number-to-register</dfn></dt>
  <dd>Store the specified number in the specified register. With no prefix argument (i.e., no <code>C-u NUMBER</code>), store a 0.</dd>

  <dt><dfn>
  C-u NUMBER C-x r + REGISTER_NAME<br>
  C-u NUMBER M-x increment-register</dfn></dt>
  <dd>If the specified register contains a number, increment that number by the specified amount. With no prefix argument (i.e., no <code>C-u NUMBER</code>), increment by 1.</dd>
</dl>


# Bookmarks

Bookmarks are somewhat like registers in that they can record positions in buffers you can jump to. Unlike registers, they have long names and they persist automatically from one Emacs session to the next (your bookmarks are automatically saved when you kill Emacs). By default, bookmarks are saved to ~/.emacs.d/bookmarks or to ~/.emacs.bmk. The bookmark commands load your default bookmark file automatically. This saving and loading is how bookmarks persist from one Emacs session to the next.

<dl>
  <dt><dfn>
  C-x r m BOOKMARK_NAME<br>
  M-x bookmark-set</dfn></dt>
  <dd>Set a bookmark named BOOKMARK at point. If you don't specify a bookmark name, then the name will be taken from the name of the file.</dd>

  <dt><dfn>
  C-x r b BOOKMARK_NAME<br>
  M-x bookmark-jump</dfn></dt>
  <dd>Jump to the bookmark named BOOKMARK.</dd>

  <dt><dfn>
  C-x r l<br>
  M-x list-bookmarks</dfn></dt>
  <dd>List all the bookmarks.</dd>

  <dt><dfn>
  M-x bookmark-save</dfn></dt>
  <dd>Explicitly save the current bookmark values in the default bookmark file.</dd>

  <dt><dfn>
  M-x bookmark-load &lt;RET&gt; FILENAME</dfn></dt>
  <dd>Load the specified bookmark file.</dd>

  <dt><dfn>
  M-x bookmark-write &lt;RET&gt; FILENAME</dfn></dt>
  <dd>Save all the current bookmark values in the specified file.</dd>

  <dt><dfn>
  M-x bookmark-delete &lt;RET&gt; BOOKMARK_NAME</dfn></dt>
  <dd>Delete the specified bookmark.</dd>

  <dt><dfn>
  M-x bookmark-insert-location &lt;RET&gt; BOOKMARK_NAME</dfn></dt>
  <dd>Insert in the buffer the name of the file that the specified bookmark points to.</dd>

  <dt><dfn>
  M-x bookmark-insert &lt;RET&gt; BOOKMARK_NAME</dfn></dt>
  <dd>Insert in the buffer the contents of the file that the specified bookmark points to.</dd>

  <dt><dfn>
  M-x bookmark-rename</dfn></dt>
  <dd>Rename a bookmark from OLD_NAME to NEW_NAME.</dd>
</dl>


# Saving Emacs's State

You can save the Emacs desktop (the buffers, their file names, major modes, buffer positions, and some other things), so that you can persist that state across Emacs sessions.

You can save the desktop manually with the command <code>M-x desktop-save</code>. You can also enable automatic saving of the desktop when you exit Emacs, and automatic restoration of the last saved desktop when Emacs starts; add the following to your ~/.emacs.d/init.el for automatic saving and restoration: <code>(desktop-save-mode 1)</code>.

When Emacs loads a saved desktop, it looks for saved desktops in the directories specified by DESKTOP-PATH and then loads the first desktop it finds.

<dl>
  <dt><dfn>
  M-x desktop-change-dir</dfn></dt>
  <dd>Load the first desktop found in the specified directory.</dd>

  <dt><dfn>
  M-x desktop-clear</dfn></dt>
  <dd>Empty the current desktop.</dd>

  <dt><dfn>
  M-x desktop-remove</dfn></dt>
  <dd>Delete a desktop file.</dd>

  <dt><dfn>
  M-x desktop-revert</dfn></dt>
  <dd>Revert to the last loaded desktop.</dd>

  <dt><dfn>
  M-x desktop-save</dfn></dt>
  <dd>Save the current desktop in a desktop file.</dd>

  <dt><dfn>
  M-x desktop-save-in-desktop-dir</dfn></dt>
  <dd>Save the current desktop in a desktop file in the specified directory.</dd>

  <dt><dfn>
  M-x desktop-save-mode</dfn></dt>
  <dd>Toggle desktop saving.</dd>
</dl>


# Spell Checking

Emacs's spell checking depends on a separate (non-Emacs) spell checker program: Aspell, Ispell, or Hunspell.

When the spell checker encounters a misspelled word, you will be prompted for what to do. Press <code>?</code> for help.

Ispell, Aspell, and Hunspell look up spelling in two dictionaries: the standard dictionary and your personal dictionary. The standard dictionary is specified by the variable <code>ispell-local-dictionary</code> or, if that is <code>nil</code>, by the variable <code>ispell-dictionary</code>. If both are <code>nil</code>, the spelling program's default dictionary is used. The command <code>M-x ispell-change-dictionary</code> sets the standard dictionary for the buffer and then restarts the subprocess, so that it will use a different standard dictionary. Your personal dictionary is specified by the variable <code>ispell-personal-dictionary</code>. If that is <code>nil</code>, the spelling program looks for a personal dictionary in a default location.

A separate dictionary is used for word completion. The variable <code>ispell-complete-word-dict</code> specifies the file name of this dictionary. The completion dictionary must be different because it cannot use root and affix information. For some languages, there is a spell checking dictionary but no word completion dictionary.

<dl>
  <dt><dfn>
  M-$<br>
  M-x ispell-word</dfn></dt>
  <dd>
<p>If the region is inactive, then check and optionally correct the spelling of the word at point.</p>

<p>If the region is active, then check and optionally correct the spelling of all the words in the region.</p>
  </dd>

  <dt><dfn>
  M-x ispell</dfn></dt>
  <dd>
<p>If the region is inactive, then check and optionally correct the spelling of all the words in the buffer.</p>

<p>If the region is active, then check and optionally correct the spelling of all the words in the region.</p>
  </dd>

  <dt><dfn>
  M-x ispell-buffer</dfn></dt>
  <dd>Check and optionally correct the spelling of all the words in the buffer, regardless if the region is active or not.</dd>

  <dt><dfn>
  M-x ispell-region</dfn></dt>
  <dd>Check and optionally correct the spelling of all the words in the region, regardless if the region is active or not.</dd>

  <dt><dfn>
  M-x ispell-comments-and-strings</dfn></dt>
  <dd>Check and optionally correct the spelling of all the words in any comments or string literals.</dd>

  <dt><dfn>
  M-x ispell-change-dictionary &lt;RET&gt; DICT</dfn></dt>
  <dd>Restart the Aspell/Ispell/Hunspell process, using DICT as the dictionary.</dd>

  <dt><dfn>
  M-x ispell-kill-ispell</dfn></dt>
  <dd>
<p>Kill the Aspell/Ispell/Hunspell subprocess.</p>

<p>Once started, the Aspell or Ispell or Hunspell subprocess continues to run, waiting for something to do, so that subsequent spell checking commands complete more quickly. If you want to get rid of the process, use <code>M-x ispell-kill-ispell</code>. This is not usually necessary, since the process uses no processor time except when you do spelling correction.</p>
  </dd>

  <dt><dfn>
  M-x flyspell-mode</dfn></dt>
  <dd>Enable Flyspell mode, which highlights all misspelled words.</dd>

  <dt><dfn>
  M-x flyspell-prog-mode</dfn></dt>
  <dd>Enable Flyspell mode for source code, which only highlights misspelled words in comments or string literals.</dd>

  <dt><dfn>
  M-&lt;TAB&gt;<br>
  &lt;ESC&gt; &lt;TAB&gt;<br>
  M-x ispell-complete-word</dfn></dt>
  <dd>Complete the word before point based on the spelling dictionary. If you keep invoking <code>ispell-complete-word</code>, it'll cycle through other suggestions.</dd>

  <dt><dfn>
  C-M-i<br>
  C-.<br>
  M-x flyspell-auto-correct-word</dfn></dt>
  <dd>When Flyspell mode is enabled, complete the word before point based on the spelling dictionary. If you keep invoking <code>flyspell-auto-correct-word</code>, it'll cycle through other suggestions.</dd>

  <dt><dfn>
  M-x flyspell-buffer</dfn></dt>
  <dd>Using Flyspell, highlight all the words in the buffer that are misspelled.</dd>

  <dt><dfn>
  M-x flyspell-region</dfn></dt>
  <dd>Using Flyspell, highlight all the words in the region that are misspelled, regardless if the region is active or not.</dd>
</dl>


# Calendar (Dates and Times)

<dl>
  <dt><dfn>
  M-x calendar</dfn></dt>
  <dd>
<p>Display a three-month calendar centred on the current month, with point on the current date.</p>

<p>With a numeric argument, prompt for the month and year to be the centre of the three-month calendar.</p>
  </dd>

  <dt><dfn>
  q<br>
  M-x calendar-exit</dfn></dt>
  <dd>Close the calendar.</dd>

  <dt><dfn>
  C-f<br>
  M-x calendar-forward-day</dfn></dt>
  <dd>Move point one day forward.</dd>

  <dt><dfn>
  C-b<br>
  M-x calendar-backward-day</dfn></dt>
  <dd>Move point one day backward.</dd>

  <dt><dfn>
  C-n<br>
  M-x calendar-forward-week</dfn></dt>
  <dd>Move point one week forward.</dd>

  <dt><dfn>
  C-p<br>
  M-x calendar-backward-week</dfn></dt>
  <dd>Move point one week backward.</dd>

  <dt><dfn>
  M-}<br>
  M-x calendar-forward-month</dfn></dt>
  <dd>Move point one month forward.</dd>

  <dt><dfn>
  M-{<br>
  M-x calendar-backward-month</dfn></dt>
  <dd>Move point one month backward.</dd>

  <dt><dfn>
  C-x ]<br>
  M-x calendar-forward-year</dfn></dt>
  <dd>Move point one year forward.</dd>

  <dt><dfn>
  C-x [<br>
  M-x calendar-backward-year</dfn></dt>
  <dd>Move point one year backward.</dd>

  <dt><dfn>
  &gt;<br>
  M-x calendar-scroll-left</dfn></dt>
  <dd>Scroll one month forward.</dd>

  <dt><dfn>
  &lt;<br>
  M-x calendar-scroll-right</dfn></dt>
  <dd>Scroll one month backward.</dd>

  <dt><dfn>
  C-v<br>
  M-x calendar-scroll-left-three-months</dfn></dt>
  <dd>Scroll three months forward.</dd>

  <dt><dfn>
  M-v<br>
  M-x calendar-scroll-right-three-months</dfn></dt>
  <dd>Scroll three months backward.</dd>

  <dt><dfn>
  C-u C-v<br>
  C-u M-x calendar-scroll-left-three-months</dfn></dt>
  <dd>Scroll one year forward (C-u multiplies the following command by 4, thus 4 * 3 months, which is one year).</dd>

  <dt><dfn>
  C-u M-v<br>
  C-u M-x calendar-scroll-right-three-months</dfn></dt>
  <dd>Scroll one year backward (C-u multiplies the following command by 4, thus 4 * 3 months, which is one year).</dd>

  <dt><dfn>
  C-a<br>
  M-x calendar-beginning-of-week</dfn></dt>
  <dd>Move point to the start of the week.</dd>

  <dt><dfn>
  C-e<br>
  M-x calendar-end-of-week</dfn></dt>
  <dd>Move point to the end of the week.</dd>

  <dt><dfn>
  M-a<br>
  M-x calendar-beginning-of-month</dfn></dt>
  <dd>Move point to the start of the month.</dd>

  <dt><dfn>
  M-e<br>
  M-x calendar-end-of-month</dfn></dt>
  <dd>Move point to the end of the month.</dd>

  <dt><dfn>
  M-&lt;<br>
  M-x calendar-beginning-of-year</dfn></dt>
  <dd>Move point to the start of the year.</dd>

  <dt><dfn>
  M-&gt;<br>
  M-x calendar-end-of-year</dfn></dt>
  <dd>Move point to the end of the year.</dd>

  <dt><dfn>
  g d<br>
  M-x calendar-goto-date</dfn></dt>
  <dd>Move point to the specified date (year, month, day).</dd>

  <dt><dfn>
  g D<br>
  M-x calendar-goto-day-of-year</dfn></dt>
  <dd>Move point to the specified day (a number between 1 and 365 inclusive) of the specified year.</dd>

  <dt><dfn>
  g w<br>
  M-x calendar-iso-goto-week</dfn></dt>
  <dd>Move point to the specified week (a number between 1 and 52 inclusive) of the specified year.</dd>

  <dt><dfn>
  o<br>
  M-x calendar-other-month</dfn></dt>
  <dd>Centre calendar around the specified month of the specified year.</dd>

  <dt><dfn>
  .<br>
  M-x calendar-goto-today</dfn></dt>
  <dd>Move point to today's date.</dd>

  <dt><dfn>
  C-&lt;SPC&gt;<br>
  C-@<br>
  M-x calendar-set-mark</dfn></dt>
  <dd>Mark the date under the cursor.</dd>

  <dt><dfn>
  C-x C-x<br>
  M-x calendar-exchange-point-and-mark</dfn></dt>
  <dd>Exchange the current cursor position with the mark date.</dd>

  <dt><dfn>
  M-=<br>
  M-x calendar-count-days-region</dfn></dt>
  <dd>Display the number of days in the current region. If you haven't set a region, then you will see "No mark set in this buffer" in the echo area.</dd>

  <dt><dfn>
  p d<br>
  M-x calendar-print-day-of-year</dfn></dt>
  <dd>Display the day of the year (a number between 1 and 365 inclusive) for the selected day, and display how many days are left in the year from that day.</dd>

  <dt><dfn>
  &lt;SPC&gt;<br>
  M-x scroll-other-window</dfn></dt>
  <dd>Scroll the other window's text up.</dd>

  <dt><dfn>
  &lt;DEL&gt;<br>
  M-x scroll-other-window-down</dfn></dt>
  <dd>Scroll the other window's text down.</dd>

  <dt><dfn>
  h<br>
  M-x calendar-cursor-holidays</dfn></dt>
  <dd>Display the holidays for the selected date.</dd>

  <dt><dfn>
  x<br>
  M-x calendar-mark-holidays</dfn></dt>
  <dd>Highlight all the days that contain holidays, regardless if they're currently visible in the calendar or not.</dd>

  <dt><dfn>
  u<br>
  M-x calendar-unmark</dfn></dt>
  <dd>Remove all highlights from the calendar.</dd>

  <dt><dfn>
  a<br>
  M-x calendar-list-holidays</dfn></dt>
  <dd>List all the holidays in another window for the displayed three months.</dd>

  <dt><dfn>
  M-x holidays</dfn></dt>
  <dd>
<p>List all the holidays in another window for the three months around today's date (i.e., the previous, current, and next months relative to today's date).</p>

<p>With a numeric argument, you can specify a different month to centre on.</p>
  </dd>

  <dt><dfn>
  M-x list-holidays</dfn></dt>
  <dd>List all the holidays in another window for a specified range of years.</dd>

  <dt><dfn>
  M-x sunrise-sunset</dfn></dt>
  <dd>Display the local times of sunrise and sunset for today's date.</dd>

  <dt><dfn>
  S<br>
  M-x calendar-sunrise-sunset</dfn></dt>
  <dd>Display the local times of sunrise and sunset for the selected date.</dd>

  <dt><dfn>
  C-u M-x sunrise-sunset</dfn></dt>
  <dd>Display the local times of sunrise and sunset for a specified date.</dd>

  <dt><dfn>
  M-x calendar-sunrise-sunet-month</dfn></dt>
  <dd>Display the local times of sunrise and sunset for the selected month.</dd>

  <dt><dfn>
  M<br>
  M-x calendar-lunar-phases</dfn></dt>
  <dd>Display the dates and times for all the quarters of the moon for the selected three-month period.</dd>

  <dt><dfn>
  M-x lunar-phases</dfn></dt>
  <dd>
<p>Display the dates and times for all the quarters of the moon for the three months around today's date (i.e., the previous, current, and next months relative to today's date).</p>

<p>With a numeric argument, you can specify a different month and year to centre on.</p>
  </dd>

  <dt><dfn>
  p o<br>
  M-x calendar-print-other-dates</dfn></dt>
  <dd>Display the selected date in various other calendar systems.</dd>

  <dt><dfn>
  M-x european-calendar</dfn></dt>
  <dd>Set the interpretation and display of dates to the European style.</dd>
</dl>


# Editing Plaintext

<dl>
  <dt><dfn>
  C-o<br>
  M-x open-line</dfn></dt>
  <dd>Insert a newline at point, but don't move point. This command is most useful when point is at the beginning of a line, in which case, point will be left at the beginning of a blank line.</dd>
</dl>


## Case Conversion

If a word case conversion command is given in the middle of a word, it applies only to the part of the word that follows point.

<dl>
  <dt><dfn>
  M-l<br>
  M-x downcase-word</dfn></dt>
  <dd>Convert the following word to all lowercase. With a negative prefix argument, convert the previous word to all lowercase.</dd>

  <dt><dfn>
  M-u<br>
  M-x upcase-word</dfn></dt>
  <dd>Convert the following word to all uppercase. With a negative prefix argument, convert the previous word to all uppercase.</dd>

  <dt><dfn>
  M-c<br>
  M-x capitalize-word</dfn></dt>
  <dd>Capitalise the following word. With a negative prefix argument, capitalise the previous word.</dd>

  <dt><dfn>
  C-x C-l<br>
  M-x downcase-region</dfn></dt>
  <dd>Convert the entire region to all lowercase.</dd>

  <dt><dfn>
  C-x C-u<br>
  M-x upcase-region</dfn></dt>
  <dd>Convert the entire region to all uppercase.</dd>

  <dt><dfn>
  M-x capitalize-region</dfn></dt>
  <dd>Capitalise the entire region.</dd>
</dl>


## Filling

Filling text means adjusting the positions of line-breaks to shift text between consecutive lines, so that all the lines are approximately the same length.

Auto Fill mode is a buffer-local mind mode in which lines are broken automatically when they become too wide. Breaking only happens when you type a <code>&lt;SPC&gt;</code> or <code>&lt;RET&gt;</code>.

By default, the fill commands will not break a line after a period followed by just one space.

The fill prefix feature allows paragraphs to be filled so that each line starts with a special string of characters. You can specify a fill prefix explicitly, or you can let Emacs try to deduce on automatically (Adaptive Fill). To specify a fill prefix for the current buffer, move to a line that starts with the desired prefix, put point at the end of the prefix, and type <code>C-x .</code> (<code>M-x set-fill-prefix</code>). To turn off the fill prefix, specify an empty prefix by typing <code>C-x .</code> with point at the very beginning of a line.

When a fill prefix is in effect, the fill commands remove the fill prefix from each line of the paragraph before filling, and insert it on each line after filling. The beginning of the first line of the paragraph is left unchanged, since often that is intentionally different. Auto Fill mode also inserts the fill prefix automatically when it makes a new line. The <code>C-o</code> command inserts the fill prefix on new lines it creates, when you use it at the beginning of a line. Conversely, the command <code>M-^</code> deletes the prefix (if it occurs) after the newline that it deletes.

<dl>
  <dt><dfn>
  M-x auto-fill-mode</dfn></dt>
  <dd>Toggle Auto Fill mode.</dd>

  <dt><dfn>
  &lt;SPC&gt;<br>
  &lt;RET&gt;</dfn></dt>
  <dd>In Auto Fill mode, break lines when appropriate. If you want to insert a space or newline without permitting line-breaking, type <code>C-q &lt;SPC&gt;</code> for a space or type <code>C-q C-j</code> or <code>C-o</code> for a newline.</dd>

  <dt><dfn>
  M-q<br>
  M-x fill-paragraph</dfn></dt>
  <dd>Fill the current paragraph using the current fill prefix. If the region is active, then fill each paragraph in the region.</dd>

  <dt><dfn>
  M-x fill-region</dfn></dt>
  <dd>Fill each paragraph in the region.</dd>

  <dt><dfn>
  M-x fill-region-as-paragraph</dfn></dt>
  <dd>Fill the region, considering it as one paragraph.</dd>

  <dt><dfn>
  C-x f<br>
  M-x set-fill-column</dfn></dt>
  <dd>Set the maximum line width for filling. With a prefix argument of <code>C-u</code>, set <code>fill-column</code> to the current column of point.</dd>

  <dt><dfn>
  M-x fill-individual-paragraphs</dfn></dt>
  <dd>Fill the region, considering each change of identation as starting a new paragraph.</dd>

  <dt><dfn>
  M-x fill-nonuniform-paragraphs</dfn></dt>
  <dd>Fill the region, considering only paragraph-separator lines as starting a new paragraph.</dd>
</dl>


# Transposing

Transposing two units (characters, words, expressions, lines, etc.) of text means putting each unit into the place formerly occupied by the other. You can also think of it as "swapping".

<dl>
  <dt><dfn>
  C-t<br>
  M-x transpose-chars</dfn></dt>
  <dd>Transpose the characters before and after point (the character before the cursor and the character on the cursor). When point is at the end of the line, then transpose the last two characters on the line before the newline. With a numeric argument of zero, transpose the character ending after point with the one ending after mark.</dd>

  <dt><dfn>
  M-t<br>
  M-x transpose-words</dfn></dt>
  <dd>Transpose the word before or containing point with the word after point. The punctuation characters between the words do not move; for example, "foo, bar" transposes into "bar, foo" rather than "bar foo,". With a numeric argument of zero, transpose the word ending after point with the one ending after mark.</dd>

  <dt><dfn>
  C-M-t<br>
  M-x transpose-sexps</dfn></dt>
  <dd>Transpose the expression (could be an identifier, literal, keyword, or whatever) before or containing point with the expression after point. With a numeric argument of zero, transpose the expression ending after point with the one ending after mark.</dd>

  <dt><dfn>
  C-x C-t<br>
  M-x tranpose-lines</dfn></dt>
  <dd>Transpose the current line with the previous line. With a numeric argument of zero, transpose the current line with the line containing mark.</dd>

  <dt><dfn>
  M-x transpose-sentences</dfn></dt>
  <dd>Transpose the current sentence with the next one. With a numeric argument of zero, transpose the current sentence with the sentence containing mark.</dd>

  <dt><dfn>
  M-x transpose-paragraphs</dfn></dt>
  <dd>Transpose the current paragraph with the next one. With a numeric argument of zero, transpose the current paragraph with the paragraph containing mark.</dd>
</dl>


# Sorting

Emacs provides several commands for sorting text in the buffer. All operate on the contents of the region. They divide the text of the region into many "sort records", identify a "sork key" for each record, and then reorder the records into the order determined by the sort keys. The records are ordered so that their keys are in alphabetical order, or, for numeric sorting, in numeric order. In alphabetic sorting, all uppercase letters 'A' through 'Z' come before lowercase 'a', in accord with the ASCII character sequence.

The various sort commands differ in how they divide the text into sort records and in which part of each record is used as the sort key. Most of the sort commands use each entire sort record as its own sort key, but some use only a portion of the record as the sort key.

If you want case-insensitive sorting, then set the <code>sort-fold-case</code> variable to <code>t</code> before you sort: <code>M-x set-variable &lt;RET&gt; sort-fold-case &lt;RET&gt; t &lt;RET&gt;</code>. You could also add the following to your init file: <code>(setq sort-fold-case t)</code>.

<dl>
  <dt><dfn>
  M-x sort-lines</dfn></dt>
  <dd>Divide the region into lines, and sort by comparing the entire text of a line. A numeric argument means sort into descending order.</dd>

  <dt><dfn>
  M-x sort-paragraphs</dfn></dt>
  <dd>Divide the region into paragraphs, and sort by comparing the entire text of a paragraph (except for leading blank lines). A numeric argument means sort into descending order.</dd>

  <dt><dfn>
  M-x sort-pages</dfn></dt>
  <dd>Divide the region into pages, and sort by comparing the entire text of a page (except for leading blank lines). A numeric argument means sort into descending order.</dd>

  <dt><dfn>
  M-x sort-fields</dfn></dt>
  <dd>
<p>Divide the region into lines, and sort by comparing the conents of one field in each line. Fields are defiend as separated by whitespace, so the first run of consecutive non-whitespace characters in a line constitutes field 1, the second such run constitutes field 2, etc.</p>

<p>Specify which field to sort by with a numeric argument: 1 to sort by field 1, etc. A negative argument means count fields from the right instead of from the left; thus, minus 1 means sort by the last field. If several lines have identical contents in the field being sorted, they keep the same relative order that they had in the original buffer.</p>
  </dd>

  <dt><dfn>
  M-x sort-numeric-fields</dfn></dt>
  <dd>Like <code>M-x sort-fields</code>, except the specified field is converted to an integer for each line, and the numbers are compared (rather than their string representations). By default, numbers are interpreted according to <code>sort-numeric-base</code>, but numbers beginning with "0x" or "0" are interpreted as hexadecimal and octal, respectively.</dd>

  <dt><dfn>
  M-x sort-columns</dfn></dt>
  <dd>Like <code>M-x sort-fields</code>, except that the text within each line used for comparison comes from a fixed range of columns. You specify the columns by putting point at one of the columns and the mark at the other column. All of the line point is in is considered part of the region, and so is all of the line the mark is in, as well as all the lines in between. Sorting columns can be thought of as sorting the rectangle specified by point and the mark, except that the text on each line to the left or right of the rectangle moves along with the text inside the rectangle.</dd>

  <dt><dfn>
  M-x reverse-region</dfn></dt>
  <dd>Reverse the order of the lines in the region. This is useful for sorting into descending order by fields or columns, since those sort commands do not have a feature for doing that. Basically, you would sort by fields or columns (<code>M-x sort-fields</code>, <code>M-x sort-numeric-fields</code>, or <code>M-x sort-columns</code>), and then you would reverse the order of the lines (<code>M-x reverse-region</code>).</dd>
</dl>


# Describing a Buffer, Region, or Character

<dl>
  <dt><dfn>
  M-=<br>
  M-x count-words-region<br>
  M-x count-lines-region</dfn></dt>
  <dd>Display a message in the echo area reporting the number of lines, words, and characters that are present in the region.</dd>

  <dt><dfn>
  C-u M-=<br>
  M-x count-words</dfn></dt>
  <dd>Display a message in the echo area reporting the number of lines, words, and characters that are present in the buffer. If the region is active, display the numbers for the region instead.</dd>

  <dt><dfn>
  C-x l<br>
  M-x count-lines-page</dfn></dt>
  <dd>Display a message in the echo area reporting the number of lines in the current page. The numbers in parentheses are the lines before point + the lines after point.</dd>

  <dt><dfn>
  C-x =<br>
  M-x what-cursor-position</dfn></dt>
  <dd>
<p>Describe the character that's after point (i.e., on the cursor).</p>

<p>
  <ul>
    <li>Char:</li>
    <li>CHARACTER</li>
    <li>(</li>
    <li>DECIMAL_VALUE_OF_CHARACTER,</li>
    <li>OCTAL_VALUE_OF_CHARACTER,</li>
    <li>HEXADECIMAL_VALUE_OF_CHARACTER</li>
    <li>)</li>
    <li>point=</li>
    <li>NUMBER_OF_CHARACTERS_ON_OR_BEFORE_CURSOR</li>
    <li>of</li>
    <li>TOTAL_NUMBER_OF_CHARACTERS_IN_BUFFER</li>
    <li>(</li>
    <li>POSITION_OF_POINT_IN_THE_BUFFER_REPRESENTED_AS_A_PERCENTAGE</li>
    <li>)</li>
    <li>column=</li>
    <li>COLUMN_NUMBER_OF_CURSOR_ON_THE_CURRENT_LINE</li>
  </ul>
</p>
  </dd>
</dl>


# Syntax Highlighting (Font Lock)

Font Lock mode is a minor mode, always local to a particular buffer, which assigns faces to various bits of text in the buffer. Each buffer's major mode tells Font Lock mode which text to fontify; for instance, programming language modes fontify syntactically relevant constructs like comments, strings, and function names. Font Lock mode is enabled by default.

Most other editors refer to font locking as syntax highlighting.

In most cases, you'll find that syntax highlighting works out of the box.

<dl>
  <dt><dfn>
  M-x font-lock-mode</dfn></dt>
  <dd>Toggle Font Lock mode in the current buffer.</dd>

  <dt><dfn>
  M-x global-font-lock-mode</dfn></dt>
  <dd>Toggle Font Lock mode in all buffers.</dd>
</dl>


# Comments

You can enable spell checking for comments by using Flyspell Prog mode (<code>M-x flyspell-prog-mode</code>).

<dl>
  <dt><dfn>
  M-;<br>
  M-x comment-dwim</dfn></dt>
  <dd>
<p>If the region is active, either add comment delimiters to the region (if there aren't any comment delimiters) or remove comment delimiters from the region (if there are comment delimiters).</p>

<p>If the region is not active, either add a new comment to the current line (if there is no comment) or realign the existing comment on the current line to the conventional alignment (unless the comment starts in column 0, in which case it isn't moved at all). For blank lines, the comment is indented to the same position where &lt;TAB&gt; would indent to. For non-blank lines, the comment is placed after the last non-whitespace character on the line; normally, at the column specified by the variable <code>comment-column</code>, but if the line already extends beyond that column, then the comment is usually separated from the non-comment text by at least one space. When a comment is added or realigned, point is moved to one space after the opening delimiter, so that you can start typing a comment right away. Even if an existing comment is properly aligned, <code>M-;</code> is still useful for moving directly to the start of the comment text.</p>
  </dd>

  <dt><dfn>
  C-u M-;<br>
  M-x comment-kill<br>
  M-x kill-comment</dfn></dt>
  <dd>Kill any comment on the current line, along with the whitespace before it.</dd>

  <dt><dfn>
  M-x comment-region<br>
  C-c C-c</dfn></dt>
  <dd>Add comment delimiters to the region, whether the region is active or not.</dd>

  <dt><dfn>
  M-x uncomment-region</dfn></dt>
  <dd>Remove comment delimiters from the region, whether the region is active or not.</dd>

  <dt><dfn>
  M-x comment-or-uncomment-region</dfn></dt>
  <dd>Whether the region is active or not, add comment delimiters to the region if the region isn't fully commented; otherwise, remove the comment delimiters from the region.</dd>

  <dt><dfn>
  M-j<br>
  C-M-j<br>
  M-x comment-indent-new-line<br>
  M-x indent-new-comment-line</dfn></dt>
  <dd>Break the current line and insert the necessary comment delimiters and indentation to continue the comment on the next line. When Auto Fill mode is enabled, going past the fill column while typing a comment will have the same effect as the <code>comment-indent-new-line</code> command.</dd>

  <dt><dfn>
  M-x comment-indent<br>
  M-x indent-for-comment</dfn></dt>
  <dd>If there is a comment on the current line, indent it to <code>comment-column</code>; otherwise, add a new empty comment to the current line.</dd>

  <dt><dfn>
  C-x ;<br>
  M-x comment-set-column<br>
  M-x set-comment-column</dfn></dt>
  <dd>Set the value of <code>comment-column</code> in the current buffer to the column where point is currently located. <code>C-u C-x ;</code> sets the comment column to match the last comment before point in the buffer, and then does a <code>M-;</code> to align the current line's comment under the previous one.</dd>

  <dt><dfn>
  M-x ispell-comments-and-strings</dfn></dt>
  <dd>Check comments and strings in the current buffer for spelling errors.</dd>
</dl>


# Indentation

Indentation refers to the whitespace added to the beginning of a line to indicate the structure of the text.

By default, indentation commands insert (or remove) an optimal mix of space characters and tab characters to align to the desired column.

A tab width refers to the number of columns between two adjacent tab stops (i.e., how wide a single tab character is); it only applies to tab characters. An indentation offset refers to the number of columns that a line is shifted to the right when it's indented.

<dl>
  <dt><dfn>
  C-x $<br>
  M-x set-selective-display</dfn></dt>
  <dd>Hide lines indented more than the specified number of columns. The only indication of their presence is that three dots ('...') appear at the end of each visible line that is followed by one or more hidden lines. To make all lines visible again, type <code>C-x $</code> with no argument.</dd>

  <dt><dfn>
  &lt;TAB&gt;<br>
  M-x indent-for-tab-command</dfn></dt>
  <dd>Indent the current line, in a mode-appropriate and context-aware way. If the region is active, indent all the lines within it. If you want to insert a literal tab, type <code>C-q &lt;TAB&gt;</code>.</dd>

  <dt><dfn>
  C-j<br>
  M-x newline-and-indent</dfn></dt>
  <dd>Perform &lt;RET&gt; followed by &lt;TAB&gt;.</dd>

  <dt><dfn>
  C-M-o<br>
  M-x split-line</dfn></dt>
  <dd>Insert a newline at point and indent the next line.</dd>

  <dt><dfn>
  M-m<br>
  M-x back-to-indentation</dfn></dt>
  <dd>Move to the first non-whitespace character on the current line. If you want to jump to the last non-whitespace character on a line, you should delete all trailing whitespace, and then this becomes a nonissue (i.e., if there is no trailing whitespace, then a simple <code>C-e</code> will take you to the last non-whitespace character on a line).</dd>

  <dt><dfn>
  M-i<br>
  M-x tab-to-tab-stop</dfn></dt>
  <dd>Indent whitespace at point, up to the next tab stop.</dd>

  <dt><dfn>
  M-x indent-relative</dfn></dt>
  <dd>Insert whitespace at point, until point is aligned with the first non-whitespace character on the previous non-blank line. If point is already farther right than that, run <code>tab-to-tab-stop</code> instead--unless called with a numeric argument, in which case do nothing.</dd>

  <dt><dfn>
  M-^<br>
  M-x delete-indentation</dfn></dt>
  <dd>Delete the indentation from the current line, and replace the newline from the end of the previous line with a space, thus merging the two lines.</dd>

  <dt><dfn>
  C-M-\<br>
  M-x indent-region</dfn></dt>
  <dd>Indent all the lines in the region, as though you had typed <code>&lt;TAB&gt;</code> at the beginning of each line, whether the region is active or not.</dd>

  <dt><dfn>
  C-x &lt;TAB&gt;<br>
  M-x indent-rigidly</dfn></dt>
  <dd>Shift each line in the region by a fixed distance to the right or left. The distance to move is determined by the numeric argument (positive to move rightward, negative to move leftware). This command can be used to remove all indentation from the lines in the region, by invoking it with a large negative argument.</dd>

  <dt><dfn>
  M-x tabify</dfn></dt>
  <dd>Convert sequences of at least two spaces to tabs if that can be done without changing indentation.</dd>

  <dt><dfn>
  M-x untabify</dfn></dt>
  <dd>Convert all tabs to the appropriate number of spaces.</dd>

  <dt><dfn>
  &lt;DEL&gt;<br>
  M-x backward-delete-char-untabify</dfn></dt>
  <dd></dd>

  <dt><dfn>
  M-j<br>
  C-M-j<br>
  M-x indent-new-comment-line</dfn></dt>
  <dd>Break line at point and then indent the next line, continuing the comment if within one.</dd>

  <dt><dfn>
  C-x h C-M-\</dfn></dt>
  <dd>Reindent the whole buffer.</dd>
</dl>


# Documentation

<dl>
  <dt><dfn>
  C-h S<br>
  M-x info-lookup-symbol</dfn></dt>
  <dd>For major modes that apply to languages that have documentation in Info, view the Info documentation for a symbol. You specify the symbol with the minibuffer; the default is the symbol appearing in the buffer at point. For example, in C mode, this looks for the symbol in the C Library Manual. The command only works if the appropriate manual's Info files are installed. The major mode determines where to look for documentation for the symbol--which Info files to look in, and which indices to search.</dd>

  <dt><dfn>
  M-x man</dfn></dt>
  <dd>
<p>Read the man page for the specified topic; the default topic is the symbol appearing in the buffer at point. You can specify <code>TOPIC</code>, <code>SECTION TOPIC</code>, or <code>TOPIC(SECTION)</code>. If you don't specify a section, then the first section found that contains the specified topic will be returned.</p>

<p>The section numbers are often along the lines of:
  <ul>
    <li><b>1</b>: Executable programs or shell commands</li>
    <li><b>2</b>: System calls (functions provided by the kernel)</li>
    <li><b>3</b>: Library calls (functions within program libraries)</li>
    <li><b>4</b>: Special files (usually found in /dev)</li>
    <li><b>5</b>: File formats and conventions (e.g., /etc/passwd)</li>
    <li><b>6</b>: Games</li>
    <li><b>7</b>: Miscellaneous (including macro packages and conventions)</li>
    <li><b>8</b>: System administration commands (usually only for root)</li>
    <li><b>9</b>: Kernel routines</li>
  </ul>
</p>
  </dd>

  <dt><dfn>
  C-h f<br>
  M-x describe-function</dfn></dt>
  <dd>When editing Emacs Lisp code, view the built-in documentation for the specified function.</dd>

  <dt><dfn>
  C-h v<br>
  M-x describe-variable</dfn></dt>
  <dd>When editing Emacs Lisp code, view the built-in documentation for the specified variable.</dd>

  <dt><dfn>
  M-x eldoc-mode</dfn></dt>
  <dd>Eldoc is a buffer-local minor mode for Elisp code. When it is enabled, the echo area displays some useful information whenever there is a Lisp function or variable at point; for a function, it shows the argument list, and for a variable it shows the first line of the variable's documentation string.</dd>
</dl>


# Diff

When differences are found between two or more things (files, buffers, regions, etc.), the output is called a "diff" or a "patch." When you do a diff in Emacs, the output is displayed in a "\*diff\*" buffer, which uses Diff mode.

A diff consists of one or more hunks, which are contiguous chunks of text that contain one or more changed lines and possibly any number of unchanged lines to provide context for the changes. Each hunk is preceded by a hunk header, which specifies the old and new line numbers at which the hunk occurs. Whenever you change a hunk, Diff mode attempts to automatically correct the line numbers in the hunk headers, to ensure that the patch remains correct.

Diff mode treats each hunk as an "error message", similar to Compilation mode. Thus, you can use commands such as <code>C-x '</code> to visit the corresponding source locations.

Emacs has a few different ways to work with diffs: Diff, Emerge, and Ediff. Diff only handles a few things (comparing two files; comparing a file with its most recent backup; comparing a buffer with its corresponding file; and comparing the text in two windows). Emerge is mainly for doing merges. Ediff replaces and extends Emerge. Ediff can do cool stuff like diffing regions in a buffer.

<dl>
  <dt><dfn>
  M-x diff</dfn></dt>
  <dd>Prompt for two file names, and then display the differences between the two specified files in a buffer named "*diff*". The two files are compared using the diff program. By default, the diff will be a context diff.</dd>

  <dt><dfn>
  M-x diff-backup</dfn></dt>
  <dd>Compare the specified file with its most recent backup.</dd>

  <dt><dfn>
  M-x diff-buffer-with-file</dfn></dt>
  <dd>Compare the specified buffer with its corresponding file. This shows you what changes you would make to the file if you save the buffer.</dd>

  <dt><dfn>
  M-x compare-windows</dfn></dt>
  <dd>Compare the text in the current window with that in the next window. Comparison starts at point in each window. The command sets mark at point in each buffer, then moves point forward in each window, one character at a time, until it reaches characters that don't match. Then the command exits. If point in the two windows is followed by non-matching text when the command starts, <code>M-x compare-windows</code> tries heuristically to advance up to matching text in the two windows, and then exits. With a numeric argument, changes in whitespace are ignored.</dd>

  <dt><dfn>
  M-x ediff<br>
  M-x ediff-files</dfn></dt>
  <dd>Compare two files.</dd>

  <dt><dfn>
  M-x ediff-backup</dfn></dt>
  <dd>Compare a file with its backup. If there are several numerical backups, use the latest. If the file is itself a backup, then compare it with its original.</dd>

  <dt><dfn>
  M-x ediff-current-file</dfn></dt>
  <dd>Compare the buffer with its file on disk.</dd>

  <dt><dfn>
  M-x ediff-buffers</dfn></dt>
  <dd>Compare two buffers.</dd>

  <dt><dfn>
  M-x ediff3<br>
  M-x ediff-files3</dfn></dt>
  <dd>Compare three files.</dd>

  <dt><dfn>
  M-x ediff-buffers3</dfn></dt>
  <dd>Compare three buffers.</dd>

  <dt><dfn>
  M-x ediff-windows-wordwise</dfn></dt>
  <dd>Compare two windows word-by-word.</dd>

  <dt><dfn>
  M-x ediff-windows-linewise</dfn></dt>
  <dd>Compare two windows line-by-line.</dd>

  <dt><dfn>
  M-x ediff-regions-wordwise</dfn></dt>
  <dd>Compare two regions word-by-word. The regions can come from the same buffer and they can even overlap. You will be asked to specify the buffers that contain the regions, which you want to compare. For each buffer, you will also be asked to mark the regions to be compared. Pay attention to the messages that appear in the minibuffer.</dd>

  <dt><dfn>
  M-x ediff-regions-linewise</dfn></dt>
  <dd>Similar to <code>ediff-windows-linewise</code>, but compares the regions line-by-line.</dd>

  <dt><dfn>
  M-x ediff-patch-buffer</dfn></dt>
  <dd>Patch the specified buffer.</dd>

  <dt><dfn>
  M-x ediff-patch-file</dfn></dt>
  <dd>Patch the specified file.</dd>
</dl>

Diff mode commands:

<dl>
  <dt><dfn>
  M-n<br>
  M-x diff-hunk-next</dfn></dt>
  <dd>Move to the start of the next hunk.</dd>

  <dt><dfn>
  M-p<br>
  M-x diff-hunk-prev</dfn></dt>
  <dd>Move to the start of the previous hunk.</dd>

  <dt><dfn>
  M-}<br>
  M-x diff-file-next</dfn></dt>
  <dd>In a multi-file patch, move to the start of the next file.</dd>

  <dt><dfn>
  M-{<br>
  M-x diff-file-prev</dfn></dt>
  <dd>In a multi-file patch, move to the start of the previous file.</dd>

  <dt><dfn>
  M-k<br>
  M-x diff-hunk-kill</dfn></dt>
  <dd>Kill the hunk at point.</dd>

  <dt><dfn>
  M-K<br>
  M-x diff-file-kill</dfn></dt>
  <dd>In a multi-file patch, kill the current file.</dd>

  <dt><dfn>
  C-c C-a<br>
  M-x diff-apply-hunk</dfn></dt>
  <dd>Apply the current hunk to its target file. With a prefix argument of <code>C-u</code>, revert the current hunk.</dd>

  <dt><dfn>
  C-c C-b<br>
  M-x diff-refine-hunk</dfn></dt>
  <dd>Highlight the changes of the current hunk with finer granularity. This allows you to see exactly which parts of each change line were actually changed.</dd>

  <dt><dfn>
  C-c C-c<br>
  M-x diff-goto-source</dfn></dt>
  <dd>Go to the source file and line corresponding to the current hunk.</dd>

  <dt><dfn>
  C-c C-e<br>
  M-x diff-ediff-patch</dfn></dt>
  <dd>Start an Ediff session with the current patch.</dd>

  <dt><dfn>
  C-c C-n<br>
  M-x diff-restrict-view</dfn></dt>
  <dd>Restrict the view to the current hunk. With a prefix argument of <code>C-u</code>, restrict the view to the current file of a multi-file patch. To widen again, use <code>C-x n w</code> (<code>M-x widen</code>).</dd>

  <dt><dfn>
  C-c C-r<br>
  M-x diff-reverse-direction</dfn></dt>
  <dd>Reverse the direction of comparison for the entire buffer (<code>diff bar foo</code> instead of <code>diff foo bar</code>).</dd>

  <dt><dfn>
  C-c C-s<br>
  M-x diff-split-hunk</dfn></dt>
  <dd>Split the hunk at point. This is far manually editing patches, and only works with the unified diff format produced by the "-u" or "--unified" options to the diff program. If you need to split a hunk in the context diff format produced by the "-c" or "--context" options to diff, first convert the buffer to the unified diff format with <code>C-c C-u</code>.</dd>

  <dt><dfn>
  C-c C-d<br>
  M-x diff-unified-&gt;context</dfn></dt>
  <dd>Convert the entire buffer to the context diff format. With a prefix argument, convert only the text within the region.</dd>

  <dt><dfn>
  C-c C-u<br>
  M-x diff-context-&gt;unified</dfn></dt>
  <dd>Convert the entire buffer to the unified diff format. With a prefix argument, convert unified format to context format. When the mark is active, convert only the text within the region.</dd>

  <dt><dfn>
  C-c C-w<br>
  M-x diff-refine-hunk</dfn></dt>
  <dd>Refine the current hunk so that it disregards changes in whitespace.</dd>

  <dt><dfn>
  M-x diff-delete-trailing-whitespace</dfn></dt>
  <dd>Search for trailing whitespace in the lines modified by the patch, and remove that whitespace in both the patch and the patched source file(s). This command does not save the modifications that it makes. With a prefix argument, it tries to modify the original source files rather than the patched source files.</dd>

  <dt><dfn>
  C-c C-t<br>
  M-x diff-test-hunk</dfn></dt>
  <dd>See whether it's possible to apply the current hunk.</dd>
</dl>


# Source Code Management (Version Control)

The Emacs version control interface is called "VC". VC commands work with several different version control systems: GNU Arch, Bazaar, CVS, Git, Mercurial, Monotone, RCS, SCCS/CSSC, and Subversion. VC allows you to use a version control system from within Emacs, integrating the version control operations smoothly with editing.

When you tell VC to commit a change, it pops up a buffer named "\*vc-log\*". In this buffer, you should write a commit message. You can use the <code>M-n</code> and <code>M-p</code> commands to cycle through previous commit messages.

<dl>
  <dt><dfn>
  C-x v v<br>
  M-x vc-next-action</dfn></dt>
  <dd>Perform the next appropriate version control operation on the current file. If the file is not under version control, then register it with a version control system. If the file is under version control and there are changes to it, then commit it.</dd>

  <dt><dfn>
  C-c C-c<br>
  M-x log-edit-done</dfn></dt>
  <dd>Accept the current commit message.</dd>

  <dt><dfn>
  C-c C-f<br>
  M-x log-edit-show-files</dfn></dt>
  <dd>Show what files are being committed.</dd>

  <dt><dfn>
  C-c C-d<br>
  M-x log-edit-show-diff</dfn></dt>
  <dd>Show a diff for changes you are committing.</dd>

  <dt><dfn>
  C-x v i<br>
  M-x vc-register</dfn></dt>
  <dd>Place a file under version control.</dd>

  <dt><dfn>
  C-x v =<br>
  M-x vc-diff</dfn></dt>
  <dd>Display a diff between two file revisions.</dd>

  <dt><dfn>
  M-x vc-ediff</dfn></dt>
  <dd>Display a diff between two file revisions using Ediff.</dd>

  <dt><dfn>
  C-x v D<br>
  M-x vc-root-diff</dfn></dt>
  <dd>Display diffs for the whole repository.</dd>

  <dt><dfn>
  C-x v ~<br>
  M-x vc-revision-other-window</dfn></dt>
  <dd>Visit the specified revision of the current file in another window.</dd>

  <dt><dfn>
  C-x v g<br>
  M-x vc-annotate</dfn></dt>
  <dd>Open the file in another buffer and annotate each line in the file with revision information (who last edited the line; when; what commit).</dd>

  <dt><dfn>
  C-x v l<br>
  M-x vc-print-log</dfn></dt>
  <dd>Display the log for the current file.</dd>

  <dt><dfn>
  C-x v L<br>
  M-x vc-print-root-log</dfn></dt>
  <dd>Display the log for the current repository.</dd>

  <dt><dfn>
  C-x v I<br>
  M-x vc-log-incoming</dfn></dt>
  <dd>Display the changes that a pull operation will retrieve.</dd>

  <dt><dfn>
  C-x v O<br>
  M-x vc-log-outgoing</dfn></dt>
  <dd>Display the changes that will be sent by the next push operation.</dd>

  <dt><dfn>
  C-x v u<br>
  M-x vc-revert<br>
  M-x vc-revert-buffer</dfn></dt>
  <dd>Revert the current file.</dd>

  <dt><dfn>
  M-x vc-delete-file</dfn></dt>
  <dd>Delete the current file and mark it as such in the version control system.</dd>

  <dt><dfn>
  C-x v d<br>
  M-x vc-dir</dfn></dt>
  <dd>Show the VC status for "interesting" files in and below the current directory.</dd>

  <dt><dfn>
  C-x v m<br>
  M-x vc-merge</dfn></dt>
  <dd>Perform a version control merge operation.</dd>

  <dt><dfn>
  C-x v +<br>
  M-x vc-pull<br>
  M-x vc-update</dfn></dt>
  <dd>Update the current branch by pulling.</dd>

  <dt><dfn>
  M-x vc-rename-file</dfn></dt>
  <dd>Rename a file under version control.</dd>
</dl>

Annotation commands:

<dl>
  <dt><dfn>
  p</dfn></dt>
  <dd>Annotate the revision before the one currently annotated.</dd>

  <dt><dfn>
  n</dfn></dt>
  <dd>Annotate the revision after the one currently annotated.</dd>

  <dt><dfn>
  j</dfn></dt>
  <dd>Annotate the revision indicated by the current line.</dd>

  <dt><dfn>
  a</dfn></dt>
  <dd>Annotate the revision before the one indicated by the current line. This is useful to see the state the file was in before the change on the current line was made.</dd>

  <dt><dfn>
  f</dfn></dt>
  <dd>Show in a buffer the file revision indicated by the current line.</dd>

  <dt><dfn>
  d</dfn></dt>
  <dd>Display a diff between the current line's revision and the previous revision. This is useful to see what the current line's revision actually changed in the file.</dd>

  <dt><dfn>
  D</dfn></dt>
  <dd>Display the diff between the current line's revision and the previous revision for all files in the commit. This is useful to see what the current line's revision actually changed in the repo.</dd>

  <dt><dfn>
  l</dfn></dt>
  <dd>Show the log of the current line's revision.</dd>

  <dt><dfn>
  w</dfn></dt>
  <dd>If you used <code>p</code> or <code>n</code> to browse to other revisions, use this key to return to your working revision.</dd>

  <dt><dfn>
  v</dfn></dt>
  <dd>Toggle the annotation visibility.</dd>
</dl>

Log commands:

<dl>
  <dt><dfn>
  p</dfn></dt>
  <dd>Move point to the previous log entry.</dd>

  <dt><dfn>
  n</dfn></dt>
  <dd>Move point to the next log entry.</dd>

  <dt><dfn>
  a</dfn></dt>
  <dd>Annotate the revision on the current line.</dd>

  <dt><dfn>
  f</dfn></dt>
  <dd>Visit the revision indicated at the current line.</dd>

  <dt><dfn>
  d</dfn></dt>
  <dd>Display a diff between the revision at point and the next earlier revision, for the specific file.</dd>

  <dt><dfn>
  D</dfn></dt>
  <dd>Display a diff between the revision at point and the next earlier revision, for all files in that revision.</dd>

  <dt><dfn>
  &lt;RET&gt;</dfn></dt>
  <dd>In the log buffer created by <code>C-x v L</code>, toggle the the display of the commit message for the revision at point.</dd>
</dl>


# Remote Collaboration (Collaborative Editing; Pair Programming)

There are a few ways you can do remote collaboration. I'll describe two of them.

One way is for one person to start a GNU Screen session that's running Emacs, and then have other people connect to that Screen session.

The programmer hosting the session should do the following:

1. <code>screen -S SESSION_NAME</code>.
2. Start Emacs in terminal mode.

The remote programmers should do the following:

1. <code>ssh -t REMOTE_HOSTNAME screen -S SESSION_NAME -x</code>

Another way is for one person to run an Emacs server, and then have other people connect to it with <code>emacsclient</code> over an SSH connection, and then use something like [lockstep](https://github.com/tjim/lockstep) to synchronise what everyone is seeing.

The programmer hosting the session should do the following:

1. If Emacs is already running, then type <code>M-x server-start</code>. If Emacs is not already running, then you can start an Emacs server by executing <code>emacs -f server-start</code> (<code>emacs --funcall server-start</code>) or <code>emacs --daemon</code>. If you start Emacs as a daemon, then you'll need to connect to the server with <code>emacsclient</code>; otherwise, when you use server-start, your Emacs session is both a client and a server.
2. If you want to allow people to see what you see, then type <code>M-x lockstep</code>. Their session won't be synchronised with yours unless they also type <code>M-x lockstep</code> in their session.
3. Optionally, you can give a name to your server: <code>M-x set-variable &lt;RET&gt; server-name &lt;RET&gt; SERVER_NAME &lt;RET&gt;</code>.

The remote programmers should do the following:

1. <code>ssh -X REMOTE_HOSTNAME -f emacsclient -c --display=$DISPLAY</code> for creating a new graphical frame on your local display (or <code>ssh -X REMOTE_HOSTNAME -f emacsclient -nw --display=$DISPLAY</code> for creating a new terminal frame on your local display). You could also do <code>ssh -X REMOTE_HOSTNAME -f emacsclient --eval '"(make-frame-on-display \"$DISPLAY\")"'</code>.
2. If you want to synchronise your session with the host's session, type <code>M-x lockstep</code>.

If you're the one hosting the pair programming session, you should probably set up a separate user account on your machine for the purpose of pair programming. Rather than sharing a password with everyone, ask each person for their public SSH key. Add each person's public SSH key to ~/.ssh/authorized_keys, so that they can connect to your machine. You might also want to create a chroot jail for SSH users, so that you can further restrict what people can do on your machine. Follow the principle of least privilege.

To kill a daemon session, type <code>M-x kill-emacs</code>, or kill the Emacs daemon from the command-line, like you would kill any daemon.


# Shells

Thanks to TRAMP, you can open an interactive shell on a remote host and run commands from there.

Note that "comint" is an abbreviation for "**Com**mand **int**erpreter".

<dl>
  <dt><dfn>
  M-!<br>
  M-x shell-command</dfn></dt>
  <dd>Run the specified shell command.</dd>

  <dt><dfn>
  M-|<br>
  M-x shell-command-on-region</dfn></dt>
  <dd>Run the specified shell command with region contents as input; optionally replace the region with the output.</dd>

  <dt><dfn>
  M-&<br>
  M-x async-shell-command</dfn></dt>
  <dd>Run the specified shell command asynchronously, and display the output.</dd>

  <dt><dfn>
  M-x shell</dfn></dt>
  <dd>Run a subshell with input and output through an Emacs buffer. You can then give commands interactively.</dd>

  <dt><dfn>
  M-x term</dfn></dt>
  <dd>Run a subshell with input and output through an Emacs buffer. You can then give commands interactively. Full terminal emulation is available.</dd>

  <dt><dfn>
  M-x eshell</dfn></dt>
  <dd>Invoke a shell implemented entirely in Emacs.</dd>

  <dt><dfn>
  C-g</dfn></dt>
  <dd>Abort a long-running command (just like typing <code>C-c</code> in a normal shell).</dd>

  <dt><dfn>
  </dfn></dt>
  <dd></dd>

  <dt><dfn>
  </dfn></dt>
  <dd></dd>

</dl>

Eshell is the Emacs Shell, which is a shell-like command interpreter implemented in Emacs Lisp. It invokes no external processes except for those requested by the user. It is intended to be a functional replacement for command shells, such as bash, zsh, rc, or 4dos; since Emacs itself is capable of handling the sort of tasks accomplished by those tools. Everything it does, it uses Emacs's facilities to do.

Several commands are built-in in Eshell. In order to call the external variant of a built-in command <code>foo</code>, you could call <code>*foo</code>. Usually, this should not be necessary.

Eshell's globbing syntax is very similar to that of Zsh.

Since Eshell does not communicate with a terminal like most command shells, I/O is a little different. If you try to run programs from within Eshell that are not line-oriented, such as programs that use ncurses, you will just get garbage output, since the Eshell buffer is not a terminal emulator. Eshell solves this problem by running specified commands in Emacs's terminal emulator; to let Eshell know which commands need to be run in a terminal, add them to the list <code>ESHELL-VISUAL-COMMANDS</code>.


# Emacs Lisp

Most of Emacs is written in a dialect of Lisp, called Emacs Lisp, which is extended with special features that make it especially suitable for text editing tasks. It's also the language that's used for customising and extending Emacs.

Emacs Lisp code is stored in files whose names conventionally end in ".el".

Emacs Lisp code can be compiled into byte-code, which loads faster, takes up less space, and executes faster. By convention, compiled Emacs Lisp code goes in a separate file whose name ends in ".elc". Do **not** compile your init files into byte-code!

If you want to try out an expression for any of the below, but you don't know Emacs Lisp, then try a simple expression like <code>(* 2 3)</code>, which should evaluate to <code>6</code>.

<dl>
  <dt><dfn>
  M-x eval-buffer<br>
  M-x eval-current-buffer</dfn></dt>
  <dd>Evaluate the current buffer as Emacs Lisp code.</dd>

  <dt><dfn>
  C-M-x<br>
  M-x eval-defun</dfn></dt>
  <dd>Evaluate the top-level form containing point, or after point.</dd>

  <dt><dfn>
  M-:<br>
  M-&lt;ESC&gt; :<br>
  M-x eval-expression</dfn></dt>
  <dd>Evaluate the specified expression and print its value in the echo area.</dd>

  <dt><dfn>
  C-x C-e<br>
  M-x eval-last-sexp<br>
  M-x eval-print-last-sexp</dfn></dt>
  <dd>Evaluate the sexp before point and print its value in the minibuffer.</dd>

  <dt><dfn>
  M-x eval-region</dfn></dt>
  <dd>Execute the region as Emacs Lisp code.</dd>

  <dt><dfn>
  M-x pp-eval-last-sexp</dfn></dt>
  <dd>Evaluate the specified expression and pretty-print its value.</dd>

  <dt><dfn>
  M-x pp-eval-last-sexp</dfn></dt>
  <dd>Evaluate the sexp before point and pretty-print its value.</dd>

  <dt><dfn>
  M-x load-file</dfn></dt>
  <dd>Execute the contents of the specified Emacs Lisp file. It is not necessary to visit the file first; this command reads the file directly from disk, not from an existing Emacs buffer.</dd>

  <dt><dfn>
  M-x load-library</dfn></dt>
  <dd>If an Emacs Lisp file is installed in the Emacs Lisp load path, you can execute its contents by typing <code>M-x load-library</code> instead of <code>M-x load-file</code>.</dd>

  <dt><dfn>
  </dfn></dt>
  <dd></dd>

</dl>

The <code>*scratch*</code> buffer is a special buffer that can be used to evaluate Emacs Lisp expression interactively. Its major mode is Lisp Interaction mode (<code>M-x lisp-interaction-mode</code>).

<dl>
  <dt><dfn>
  C-j<br>
  M-x eval-print-last-sexp</dfn></dt>
  <dd>Evaluate the expression before point, and insert the value at point. Note that point doesn't have to appear immediately after the expression. You could have an expression followed by several blank lines, and then type <code>C-j</code> to insert the value of the expression on the current line.</dd>
</dl>

An alternative way of evaluating Emacs Lisp expressions interactively is to use Inferior Emacs Lisp mode, which provides an interface rather like Shell mode for evaluating Emacs Lisp expressions. To create an <code>*ielm*</code> buffer, which uses Inferior Emacs Lisp mode, type <code>M-x ielm</code>.

<code>t</code> means true; <code>nil</code> means false. When you want to set a variable to a non-nil value, the convention is to use <code>t</code> as the non-nil value when all that matters is that the variable is non-nil.

An association list, or alist for short, records a mapping from keys to values. It is a list of cons cells called associations: the CAR of each cons cell is the key, and the CDR is the associated value: <code>((KEY1 . VALUE1) (KEY2 . VALUE2) (KEY3 . VALUE3))</code>.


# Line Wrapping

If you want to line truncation rather than line continuation for long lines, you can type <code>M-x toggle-truncate-lines</code>. When lines are truncated, you can scroll horizontally to reveal more of the line.


# Recursive Editing Levels

A recursive edit is a situation in which you are using Emacs commands to perform arbitrary editing while in the middle of another Emacs command. Exiting the recursive edit means returning to the unfinished command, which continues execution. The command to exit is <code>C-M-c</code> (<code>M-x exit-recursive-edit</code>). You can also abort the recursive edit. This is like exiting, but also quits the unfinished command immediately. Use the command <code>C-]</code> (<code>M-x abort-recursive-edit</code>) to do this.

It is possible to be in recursive edits within recursive edits. Exiting a recursive editing level applies to the innermost level only. Aborting also gets out of only one level of recursive edit; it returns immediately to the command level of the previous recursive edit. The command <code>M-x top-level</code> aborts all levels of recursive edits, returning immediately to the top-level command reader. It also exits the minibuffer, it it is active.

You **can't** use <code>C-g</code> to exit a recursive editing level (like <code>C-]</code> can), but you can use <code>&lt;ESC&gt; &lt;ESC&gt; &lt;ESC&gt;</code>.


# Hideshow

Hideshow mode is a buffer-local minor mode that allows you to selectively display portions of a program, which are referred to as blocks. Type <code>M-x hs-minor-mode</code> to toggle this minor mode. When you use Hideshow mode to hide a block, the block disappears from the screen, to be replaced by an ellipsis (three periods in a row). Just what constitutes a block depends on the major mode. In C mode and related modes, blocks are delimited by braces, while in Lisp mode they are delimited by parentheses. Multi-line comments also count as blocks.

<dl>
  <dt><dfn>
  C-c @ C-h<br>
  M-x hs-hide-block</dfn></dt>
  <dd>Hide the current block.</dd>

  <dt><dfn>
  C-c @ C-s<br>
  M-x hs-show-block</dfn></dt>
  <dd>Show the current block.</dd>

  <dt><dfn>
  C-c @ C-c<br>
  M-x hs-toggle-hiding</dfn></dt>
  <dd>Toggle the current block (hide it if it's shown; show it if it's hidden).</dd>

  <dt><dfn>
  C-c @ C-M-h<br>
  M-x hs-hide-all</dfn></dt>
  <dd>Hide all top-level blocks.</dd>

  <dt><dfn>
  C-c @ C-M-s<br>
  M-x hs-show-all</dfn></dt>
  <dd>Show all blocks in the buffer.</dd>

  <dt><dfn>
  C-c @ C-l<br>
  M-x hs-hide-level</dfn></dt>
  <dd>Hide all blocks N levels below this block.</dd>

  <dt><dfn>
  M-x hs-hide-initial-comment-block</dfn></dt>
  <dd>Hide the first block of comments in a file.</dd>
</dl>

To hide lines in the current buffer, type <code>C-x $</code> (<code>M-x set-selective-display</code>) with a numeric argument N. Then lines with at least N columns of indentation disappear from the screen. To make all lines visible again, type <code>C-x $</code> with no argument.


# Delimiters

You can use <code>M-x check-parens</code> to find any unbalanced parentheses and unbalanced string quotes in the buffer.


# Imenu

To jump to function definitions within a buffer, you can use <code>M-x imenu</code>; you'll be prompted for a function name. If you type <code>&lt;TAB&gt;</code>, you'll see a list of possible completions. 

If you add or delete definitions, then you need to update the buffer's index (rescan). If you set <code>imenu-auto-rescan</code> to a non-nil value, then rescanning will happen automatically. Add the following to your init file: <code>(setq imenu-auto-rescan t)</code>.

You can customise the way the menus are sorted by setting the variable <code>imenu-sort-function</code>. By default, names are ordered as they occur in the buffer; if you want alphabetic sorting, use the symbol <code>imenu--sort-by-name</code> as the value. To sort the menu by name, add teh following to your init file: <code>(setq imenu-sort-function 'imenu--sort-by-name)</code>.


# Smartparens

You may have heard of packages such autopair, electric-pair-mode, or paredit. Smartparens combines the functionality of all of them into a single package and provides improvements and new features.

To install smartparens: <code>M-x package-install &lt;RET&gt; smartparens</code>.

To enable smartparens, add the following to your init file: <code>(smartparens-global-mode t)</code>.

By default, smartparens will highlight the delimited region when you're editing it. The default highlighting colour is ugly; to disable the highlighting feature, add the following to your init file: <code>(setq sp-highlight-pair-overlay nil)</code>.

Bind sp-rewrap-sexp and sp-unwrap-sexp:
<code>
(global-set-key (kbd "C-x C-k C") 'sp-rewrap-sexp)
(global-set-key (kbd "C-x C-k D") 'sp-unwrap-sexp)
</code>

TODO: file a bug regarding single quotes and backtick quotes with sp-rewrap-sexp
TODO: file a bug regarding quotes (single, double, or backtick) with sp-unwrap-sexp


# Projects

The <code>Projectile</code> package makes working with projects much easier; for example, you can type <code>C-c p f</code> to display a list of all the files in the project, and then you can start typing the name of a file to narrow the search results. <code>C-c p f</code> feels kind of similar to Eclipse's <code>C-S-r</code>. You can also type <code>C-c p s g</code> to run grep on all the files in the project. Good news: Projectile automatically detects your project's root!

To install Projectile: <code>M-x package-install &lt;RET&gt; projectile</code>.

To enable Projectile for programming modes, add the following to your init file: <code>(add-hook 'prog-mode-hook 'projectile-mode)</code>.

Use Projectile even for paths that don't contain a project file: <code>(setq projectile-require-project-root nil)</code>.

Regenerate tags whenever Emacs is idle: <code>(setq projectile-enable-idle-timer t)</code>. If you don't want to be bombarded with a prompt asking if you'd like to reload the tags file, add the following to your init file: <code>(setq tags-revert-without-query t)</code>. Tag files can be pretty large. You may want to raise the large-file-warning-threshold (the default is 10 MB): <code>(setq large-file-warning-threshold SIZE_IN_BYTES)</code>.

Install helm-projectile: <code>M-x package-install &lt;RET&gt; helm-projectile</code>.

Enable helm-projectile: <code>(add-hook 'prog-mode-hook 'helm-projectile-on)</code>.

Use helm with Projectile: <code>(setq projectile-completion-system 'helm)</code>.

Find file in project: <code>C-c p f</code>.

Find buffer in project: <code>C-c p b</code>.

Find directory in project: <code>C-c p d</code>.

Find in project: <code>C-c p h</code>.

Switch project: <code>C-c p p</code>.

<dl>
  <dt><dfn>
  C-c p s s<br>
  M-x projectile-ag</dfn></dt>
  <dd>Run an ag search on the project using the specified search string.</dd>

  <dt><dfn>
  C-c p c<br>
  M-x projectile-compile-project</dfn></dt>
  <dd>Compile the project.</dd>

  <dt><dfn>
  C-c p D<br>
  M-x projectile-dired</dfn></dt>
  <dd>Open dired at the root of the project.</dd>

  <dt><dfn>
  C-c p d<br>
  M-x projectile-find-dir</dfn></dt>
  <dd>Jump to a project's directory using completion.</dd>

  <dt><dfn>
  C-c p f<br>
  M-x project-file-find-file</dfn></dt>
  <dd>Jump to a project's file using completion.</dd>

  <dt><dfn>
  C-c p a<br>
  M-x projectile-find-other-file</dfn></dt>
  <dd>Switch between files with the same name but different extensions.</dd>

  <dt><dfn>
  C-c p j<br>
  M-x projectile-find-tag</dfn></dt>
  <dd>Find tag in project.</dd>

  <dt><dfn>
  C-c p T<br>
  M-x projectile-find-test-file</dfn></dt>
  <dd>Jump to a project's test file using completion.</dd>

  <dt><dfn>
  C-c p s g<br>
  M-x projectile-grep</dfn></dt>
  <dd>Perform rgrep in the project.</dd>

  <dt><dfn>
  C-c p I<br>
  M-x projectile-ibuffer</dfn></dt>
  <dd>Open an IBuffer window showing all buffers in the current project.</dd>

  <dt><dfn>
  C-c p k<br>
  M-x projectile-kill-buffers</dfn></dt>
  <dd>Kill all project buffers.</dd>

  <dt><dfn>
  C-c p o<br>
  M-x projectile-multi-occur</dfn></dt>
  <dd>Do a multi-occur in the project's buffers.</dd>

  <dt><dfn>
  C-c p &lt;ESC&gt;<br>
  M-x projectile-project-buffers-other-buffer</dfn></dt>
  <dd>Switch to the most recently selected project buffer.</dd>

  <dt><dfn>
  C-c p e<br>
  M-x projectile-recentf</dfn></dt>
  <dd>Show a list of recently visited files in the project.</dd>

  <dt><dfn>
  C-c p R<br>
  M-x projectile-regenerate-tags</dfn></dt>
  <dd>Regenerate the project's tags.</dd>

  <dt><dfn>
  C-c p r<br>
  M-x projectile-replace</dfn></dt>
  <dd>Replace a string in the project using tags-query-replace.</dd>

  <dt><dfn>
  C-c p S<br>
  M-x projectile-save-project-buffers</dfn></dt>
  <dd>Save all project buffers.</dd>

  <dt><dfn>
  C-c p P<br>
  M-x projectile-test-project</dfn></dt>
  <dd>Run project test command.</dd>

  <dt><dfn>
  C-c p v<br>
  M-x projectile-vc</dfn></dt>
  <dd>Open vc-dir at the root of the project.</dd>
</dl>


# Searching a Codebase

Install ag (the silver searcher): <code>M-x package-install &lt;RET&gt; ag</code>.

To search a project (from the project root), you can type <code>M-x ag-project</code>, or if you have Projectile, you can type <code>C-c p s s</code>.

In the ag buffer, you can type <code>C-c C-f</code> to enable next-error-follow-minor-mode, so that moving through the search results automatically displays the search result in another window.

To highlight the search string in the search results, add the following to your init file: <code>(setq ag-highlight-search t)</code>.


# Flycheck

<dl>
  <dt><dfn>
  C-c ! n<br>
  M-x flycheck-next-error</dfn></dt>
  <dd>Jump to the next Flycheck error.</dd>

  <dt><dfn>
  C-c ! p<br>
  M-x flycheck-previous-error</dfn></dt>
  <dd>Jump to the previous Flycheck error.</dd>

  <dt><dfn>
  C-c ! l<br>
  M-x flycheck-list-errors</dfn></dt>
  <dd>View a list of Flycheck errors.</dd>
</dl>


# Java

Install malabar-mode: <code>M-x package-install &lt;RET&gt; malabar-mode</code>. TODO: how to get working (I'm running into an eieio issue)?


# Scala

"Although it's not required, ENSIME is designed to complement an existing Scala major mode; scala-mode2 is an excellent Scala mode."

Install SBT outside Emacs. Once you install SBT, you should run <code>sbt</code> on the command-line, which should create <code>~/.sbt/VERSION</code> for you. Create a plugins directory there: <code>mkdir ~/.sbt/VERSION/plugins</code>. Then, create a <code>plugins.sbt</code> file with the following contents:
<code>
resolvers += Resolver.sonatypeRepo("snapshots")
addSbtPlugin("org.ensime" % "ensime-sbt" % "ENSIME-SBT-VERSION")
</code>

Replace ENSIME-SBT-VERSION with the latest version of the plugin, available at https://github.com/aemoncannon/ensime-sbt-cmd. To find the version, look at the build.sbt file (you should see the version in that file).

Install scala-mode2: <code>M-x package-install &lt;RET&gt; scala-mode2</code>.

Install ENSIME: <code>M-x package-install &lt;RET&gt; ensime</code>. Add the following to your init file:
<code>
(require 'ensime)
(add-hook 'scala-mode-hook 'ensime-scala-mode-hook)
</code>

TODO: generate an ENSIME project (<code>ensime generate</code>).


# Ruby

Install ruby-refactor: <code>M-x package-install &lt;RET&gt; ruby-refactor</code>. Add the following to your init file: <code>add-hook 'ruby-mode-hook 'ruby-refactor-mode-launch)</code>.

Install rspec-mode: <code>M-x package-install &lt;RET&gt; rspec-mode</code>.

Install ruby-tools: <code>M-x package-install &lt;RET&gt; ruby-tools</code>. Add the following to your init file: <code>add-hook 'ruby-mode-hook 'ruby-tools-mode)</code>. I've found that ruby-tools-mode doesn't work very well in terminal Emacs, but it does work well in graphical Emacs.

Install ruby-end: <code>M-x package-install &lt;RET&gt; ruby-end</code>.

Install rake: <code>M-x package-install &lt;RET&gt; rake</code>.

Install ruby-block: <code>M-x package-install &lt;RET&gt; ruby-block</code>. Add the following to your init file:
<code>
(require 'ruby-block)
(add-hook 'ruby-mode-hook 'ruby-block-mode)
(setq ruby-block-highlight-toggle 'overlay)
</code>

Install rubocop: <code>M-x package-install &lt;RET&gt; rubocop</code>. Add the following to your init file: <code>(add-hook 'ruby-mode-hook 'rubocop-mode)</code>. To make RuboCop even better, install flycheck, so that problems are detected on the fly: <code>M-x package-install &lt;RET&gt; flycheck</code>. Add the following to your init file: <code>(add-hook 'ruby-mode-hook 'flycheck-mode)</code>.

Install inf-ruby: <code>M-x package-install &lt;RET&gt; inf-ruby</code>. Add the following to your init file: <code>(add-hook 'inf-ruby-mode-hook 'company-mode)</code>. To run irb: <code>M-x inf-ruby</code> or <code>M-x run-ruby</code>.

Install robe: <code>M-x package-install &lt;RET&gt; robe</code>. Add the following to your init file: <code>(add-hook 'ruby-mode-hook 'robe-mode)</code>. There are some Ruby gems you'll also need to install: <code>gem install pry pry-doc method_source</code>. TODO: how to jump to definition (I keep getting "Method not found")? Also, I don't like how I have to start an inf-ruby process, and then run ruby-start, before I can even use completion.

<dl>
  <dt><dfn>
  C-c C-d<br>
  M-x robe-doc</dfn></dt>
  <dd>Show the documentation for the object at point.</dd>

  <dt><dfn>
  M-.<br>
  M-x robe-jump</dfn></dt>
  <dd>Go to the definition of the object at point.</dd>

  <dt><dfn>
  M-,<br>
  M-x pop-tag-mark</dfn></dt>
  <dd>Go back to where you jumped from.</dd>

  <dt><dfn>
  C-;<br>
  M-x ruby-tools-clear-string</dfn></dt>
  <dd>Clear the string at point.</dd>

  <dt><dfn>
  #<br>
  M-x ruby-tools-interpolate</dfn></dt>
  <dd>When point is in a place where interpolation is applicable, <code>#</code> will insert <code>#{}</code> with point between the braces.</dd>

  <dt><dfn>
  C-"<br>
  M-x ruby-tools-to-double-quote-string</dfn></dt>
  <dd>Convert single quote string at point to double quote string.</dd>

  <dt><dfn>
  C-'<br>
  M-x ruby-tools-to-single-quote-string</dfn></dt>
  <dd>Convert symbol or double quote string at point to single quote string.</dd>

  <dt><dfn>
  C-:<br>
  M-x ruby-tools-to-symbol</dfn></dt>
  <dd>Convert string at point to symbol.</dd>
</dl>


# Python

To run the Python interpreter: <code>M-x run-python</code>.

Install python-environment: <code>M-x package-install &lt;RET&gt; python-environment</code>.

Install jedi: <code>M-x package-install &lt;RET&gt; jedi</code>. Install the Jedi EPC server: <code>M-x jedi:install-server</code>. Add the following to your init file:
<code>
(add-hook 'python-mode-hook 'jedi:setup)
(setq jedi:use-shortcuts t)
</code>

Install rope (outside Emacs): <code>pip install rope</code> for Python 2 or <code>pip install rope_py3k</code> for Python 3.

Install ropemode (outside Emacs): <code>pip install ropemode</code> for Python 2 or <code>pip install ropemode_py3k</code> for Python 3.

Install ropemacs (outside Emacs): <code>pip install ropemacs</code> for Python 2 or <code>pip install ropemacs_py3k</code> for Python 3.

Install flake8 (outside Emacs): <code>pip install flake8</code>.

Install importmagic (outside Emacs): <code>pip install importmagic</code>.

Install elpy: <code>M-x package-install &lt;RET&gt; elpy</code>. Add the following to your init file: <code>(elpy-enable)</code>.

<dl>
  <dt><dfn>
  C-c ?<br>
  M-x jedi:show-doc</dfn></dt>
  <dd>Show the documentation of the object at point.</dd>

  <dt><dfn>
  M-.<br>
  C-c .<br>
  M-x jedi:goto-definition</dfn></dt>
  <dd>Go to the definition of the object at point.</dd>

  <dt><dfn>
  M-,<br>
  C-c ,<br>
  M-x jedi:goto-definition-pop-marker</dfn></dt>
  <dd>Go back to where you jumped from.</dd>
</dl>


# Perl

To use cperl-mode instead of perl-mode, add the following to your init file: <code>(defalias 'perl-mode 'cperl-mode)</code>.


# JavaScript

Install js2-mode: <code>M-x package-install &lt;RET&gt; js2-mode</code>. Add the following to your init file: <code>(add-hook 'js-mode-hook 'js2-minor-mode)</code>.

Install ac-js2: <code>M-x package-install &lt;RET&gt; ac-js2</code>. Add the following to your init file: <code>(add-hook 'js2-mode-hook 'ac-js2-mode)</code>. You can use ac-js2 for jumping to definitions via <code>M-.</code> and jumping back to where you came from via <code>M-,</code>.

Install js2-refactor: <code>M-x package-install &lt;RET&gt; js2-refactor</code>. TODO: how to set up key bindings?


# HTML

Install web-mode: <code>M-x package-install &lt;RET&gt; web-mode</code>.

To use web-mode for HTML files, add the following to your init file: <code>(add-to-list 'auto-mode-list '("\\.html?\\'" . web-mode))</code>

In terminal Emacs, auto-closing of tags is disabled by default; to enable it, add the following to your init file: <code>(setq web-mode-enable-auto-closing t)</code>.

I'm not sure what auto-pairing is supposed to do; my guess is that if I type an opening tag, then the closing tag will automatically be inserted. I'm not seeing this happen, even when I set web-mode-enable-auto-pairing to <code>t</code>.

I don't see any packages in MELPA, ELPA, or Marmalade for checking HTML syntax on the fly. There's an Emacs package called <code>tidy</code> that sends a buffer or region to an external tidy program, but it looks like a pain to set up and it hasn't been updated since 2011. For now, I'm just going to use the tidy program outside Emacs. Having an HTML validator in Emacs would be great.

To configure the indentation offsets:
<code>
(setq web-mode-code-indent-offset 2)
(setq web-mode-css-indent-offset 2)
(setq web-mode-markup-indent-offset 2)
(setq web-mode-sql-indent-offset 2)
</code>

<dl>
  <dt><dfn>
  M-;</dfn></dt>
  <dd>Comment/uncomment lines.</dd>

  <dt><dfn>
  C-c C-f</dfn></dt>
  <dd>Expand/collapse a tag.</dd>

  <dt><dfn>
  C-c C-i</dfn></dt>
  <dd>Reindent the entire buffer.</dd>

  <dt><dfn>
  C-c C-e a</dfn></dt>
  <dd>Select element content.</dd>

  <dt><dfn>
  C-c C-e b</dfn></dt>
  <dd>Element beginning.</dd>

  <dt><dfn>
  C-c C-e c</dfn></dt>
  <dd>Element clone.</dd>

  <dt><dfn>
  C-c C-e d</dfn></dt>
  <dd>Child element (down).</dd>

  <dt><dfn>
  C-c C-e e</dfn></dt>
  <dd>Element end.</dd>

  <dt><dfn>
  C-c C-e i</dfn></dt>
  <dd>Element insert.</dd>

  <dt><dfn>
  C-c C-e k</dfn></dt>
  <dd>Element kill (kill the element but leave the newline).</dd>

  <dt><dfn>
  C-c C-e n</dfn></dt>
  <dd>Next element.</dd>

  <dt><dfn>
  C-c C-e p</dfn></dt>
  <dd>Previous element.</dd>

  <dt><dfn>
  C-c C-e r</dfn></dt>
  <dd>Rename element.</dd>

  <dt><dfn>
  C-c C-e s</dfn></dt>
  <dd>Select element.</dd>

  <dt><dfn>
  C-c C-e u</dfn></dt>
  <dd>Parent element (up).</dd>

  <dt><dfn>
  C-c C-e v</dfn></dt>
  <dd>Element vanish (kill the element and the newline).</dd>

  <dt><dfn>
  C-c C-d d</dfn></dt>
  <dd>Show any tag mismatches.</dd>

  <dt><dfn>
  C-c C-d e</dfn></dt>
  <dd>Replace HTML entities with the characters that they represent.</dd>

  <dt><dfn>
  C-c C-d n</dfn></dt>
  <dd>Normalise.</dd>

  <dt><dfn>
  C-c C-d x</dfn></dt>
  <dd>Show the xpath for the element at point.</dd>

  <dt><dfn>
  C-c C-t a</dfn></dt>
  <dd>Sort attributes.</dd>

  <dt><dfn>
  C-c C-t b</dfn></dt>
  <dd>Tag beginning.</dd>

  <dt><dfn>
  C-c C-t e</dfn></dt>
  <dd>Tag end.</dd>

  <dt><dfn>
  C-c C-t m</dfn></dt>
  <dd>Fetch matching tag.</dd>

  <dt><dfn>
  C-c C-t s</dfn></dt>
  <dd>Select tag.</dd>

  <dt><dfn>
  C-c C-t p</dfn></dt>
  <dd>Previous tag.</dd>

  <dt><dfn>
  C-c C-t n</dfn></dt>
  <dd>Next tag.</dd>

  <dt><dfn>
  C-c C-a b</dfn></dt>
  <dd>Attribute beginning.</dd>

  <dt><dfn>
  C-c C-a e</dfn></dt>
  <dd>Attribute end.</dd>

  <dt><dfn>
  C-c C-a i</dfn></dt>
  <dd>Attribute insert.</dd>

  <dt><dfn>
  C-c C-a s</dfn></dt>
  <dd>Attribute select.</dd>

  <dt><dfn>
  C-c C-a t</dfn></dt>
  <dd>Attribute transpose.</dd>

  <dt><dfn>
  C-c C-a n</dfn></dt>
  <dd>Attribute next.</dd>
</dl>


# JSON

To associate JSON files with js2-mode, add the following to your init file: <code>(add-to-list 'auto-mode-alist '("\\.json$" . js2-mode))</code>.


# XML

A lot of people recommend nXML-mode, which is built into Emacs and is already the default major mode for XML files.


# CSS

If you have a string that represent a colour (for example, "white" or "#ffffff"), rainbow-mode will set the background colour of the string to the colour that the string represents; for example, the string "white" or "#ffffff" will be displayed with a white background.

To install rainbow-mode: <code>M-x package-install &lt;RET&gt; rainbow-mode</code>.

To automatically enable rainbow-mode for CSS files, add the following to your init file: <code>(add-hook 'css-mode-hook 'rainbow-mode)</code>.

To configure the indentation offset: <code>(setq css-indent-offset 2)</code>.


# YAML

Install yaml-mode: <code>M-x package-install &lt;RET&gt; yaml-mode</code>.

yaml-mode doesn't get along with electric-indent-mode, so you should disable electric-indent mode for YAML files: <code>(add-hook 'yaml-mode-hook (lambda () (electric-indent-mode -1)))</code>.


# Elisp

TODO


# Scheme

TODO


# Bash

TODO


# C

TODO


# C++

TODO


# Prolog

TODO


# Forth

TODO


# Pascal

TODO


# Customisation

Emacs has many settings which you can change. Most settings are customisable variables, which are also called user options. A separate class of settings are the faces, which determine the fonts, colours, and other attributes of text.

Customisation is done by setting variables and faces; rebinding key sequences; enabling modes; installing packages; adding hooks; adding Emacs Lisp code to an init file; etc.

A default is a value that's used when you don't explicitly specify a value to use.

For a lot of the modes where you can jump to the definition of the object at point, you can use <code>M-.</code> to jump there and <code>M-,</code> or <code>M-*</code> to jump back.


## Init File

An initialisation file is a file that gets loaded when Emacs starts. It's used to customise Emacs.

The init file contains one or more Emacs Lisp expressions.

Emacs looks for your personal init file using the filenames <code>~/.emacs</code>, <code>~/.emacs.el</code>, or <code>~/.emacs.d/init.el</code>. I recommend using <code>~/.emacs.d/init.el</code> because then you can split your init file into multiple files in ~/.emacs.d. Note that once Emacs finds an init file, it loads it, and then stops searching for any other personal init file.

Before loading your personal init file, Emacs looks for a site startup file named <code>site-start.el</code> located in any of the directories listed in Emacs's <code>load-path</code> variable. The site startup file is useful for defining overridable customisations for all users. Note that users can ignore the site startup file altogether by starting Emacs with the <code>--no-site-file</code> option.

After loading your personal init file, Emacs looks for a default init file named <code>default.el</code> located in any of the directories listed in Emacs's <code>load-path</code> variable. The default init file is useful for defining customisations that you want to apply to all users and that you don't want them to override. Note that users can still override default.el by adding the following to their personal init file: <code>(setq inhibit-default-init t)</code>.

If you run Emacs via the <code>su</code> command, Emacs tries to find your own init file, not that of the user you are currently pretending to be. The idea is that you should get your own editor customisations even if you are running as the super user.

If you run Emacs with the <code>--no-init-file</code> (<code>-q</code>) option, then Emacs won't load your personal init file or the default init file.

If you want to start Emacs using another user's init file, then use the <code>--user USERNAME</code> (<code>-u USERNAME</code>) option when starting Emacs.

If your init file has any problems, then start Emacs with the <code>--debug-init</code> option. Also, check the <code>*Messages*</code> buffer: <code>C-h e</code> (<code>M-x view-echo-area-messages</code>).

If your init files are completely broken, then start Emacs with <code>--quick</code> (<code>-Q</code>); this is similar to doing <code>--no-init-file --no-site-file --no-splash</code> (<code>-q --no-site-file --no-splash</code>).

If you made changes to your init file while you're already in an Emacs session, then you can switch to the init file's buffer and type <code>M-x eval-buffer</code> to evaluate the whole file, or you can highlight the changes that you made and then type <code>M-x eval-region</code>. Whether you edited the init file inside or outside of Emacs, you can type <code>M-x load-file</code> rather than evaluating a buffer or region.

If you want to see how long your init file took to load, type <code>M-x emacs-init-time</code>.


## Easy Customisation

Rather than manually editing an init file, Emacs provides a special buffer for browsing and editing settings; type <code>M-x customize</code>.

Customisation settings are organised into customisation groups. These groups are collected into bigger groups, all the way up to a master group called "Emacs". <code>M-x customize</code> creates a customisation buffer that shows the top-level Emacs group. Each group may contain settings and other subgroups.

Most of the customisation buffer is read-only, but it includes some editable fields, such as a field for searching for settings. There are also buttons and links, which you can activate by either clicking with the mouse, or moving point there and typing <code>&lt;RET&gt;</code>. In the customisation buffer, you can type <code>&lt;TAB&gt;</code> (<code>M-x widget-forward</code>) to move forward to the next button or editable field. <code>S-&lt;TAB&gt;</code> (<code>M-x widget-backward</code>) moves back to the previous button or editable field.

If you are interested in customising a particular setting or customisation group, you can go straight there with the commands <code>M-x customize-option</code>, <code>M-x customize-face</code>, or <code>M-x customize-group</code>.

The search field accepts one or more words separated by spaces, or a regular expression. Type <code>&lt;RET&gt;</code> in the field to submit the search. Note that this feature only finds groups and settings that are already loaded in the current Emacs session. The commad <code>M-x customize-apropos</code> is similar to using the search field, except that it reads the search term(s) using the minibuffer.

<code>M-x customize-browse</code> is another way to browse the available settings. This command creates a special customisation buffer which shows only the names of groups and settings, in a structured layout.

For each variable, you'll see its name, value, state, and description. The <code>STANDARD</code> state means that the variable is set to its default value. To edit the value of the variable, just move point to the value and edit it; the state will change to <code>EDITED</code>. Editing the value does not make it take effect right away. To do that, you must set the variable by activating the <code>[State]</code> button and choosing an appropriate option. You can set for the current session for save for future sessions.

<code>C-c C-c</code> (<code>M-x Custom-set</code>) is equivalent to using the <code>[Set for Current Session]</code> button. The command <code>C-x C-s</code> (<code>M-x Custom-save</code>) is like using the <code>[Save for Future Sessions]</code> button.

If Emacs was invoked with the <code>-q</code> or <code>--no-init-file</code> options, it will not let you save your customisations in your init file.

Saving works by writing appropriate code to your init file. If you want to save to a different file, then you'll need to add a couple lines to your init file: <code>(setq custom-file "~/.emacs-custom.el")</code> (you don't have to use ~./emacs-custom.el as the file you want to save to; it's just a suggestion); followed by <code>(load custom-file)</code>.

Typing <code>&lt;RET&gt;</code> on an editable value field moves point forward to the next field or button, like <code>&lt;TAB&gt;</code>.

To insert a newline within an editable field, use <code>C-o</code> or <code>C-q C-j</code>.

While editing certain kinds of values, such as file names, directory names, and Emacs command names, you can perform completion with <code>C-M-i</code> (<code>M-x widget-complete</code>), or the equivalent keys <code>M-&lt;TAB&gt;</code> or <code>&lt;ESC&gt; &lt;TAB&gt;</code>.

For some variables, there is only a fixed set of legitimate values, and you are not allowed to edit the value directly. Instead, a <code>[Value Menu]</code> button appears before the value; activating this button presents a choice of values. For a boolean "on or off" value, the button says <code>[Toggle]</code> and flips the value.

The State button has four reset operations: Undo Edits, Reset to Saved, Erase Customisation, and Set to Backup Value.

<dl>
  <dt><dfn>
  M-x customize-option<br>
  M-x customize-variable</dfn></dt>
  <dd>Set up a customisation buffer for just the specified variable.</dd>

  <dt><dfn>
  M-x customize-face</dfn></dt>
  <dd>Set up a customisation buffer for just the specified faced.</dd>

  <dt><dfn>
  M-x customize-group</dfn></dt>
  <dd>Set up a customisation buffer for just the specified group.</dd>

  <dt><dfn>
  M-x customize-apropos</dfn></dt>
  <dd>Set up a customisation buffer for all the settings and groups that match the specified search string.</dd>

  <dt><dfn>
  M-x customize-changed</dfn></dt>
  <dd>Set up a customisation buffer with all the settings and groups whose meaning have changed since the specified Emacs version.</dd>

  <dt><dfn>
  M-x customize-saved</dfn></dt>
  <dd>Set up a customisation buffer containing all settings that you have saved with customisation buffers.</dd>

  <dt><dfn>
  M-x customize-unsaved</dfn></dt>
  <dd>Set up a customisation buffer containing all settings that you have set but not saved.</dd>
</dl>


## Variables

A variable is a Lisp symbol that has a value.

Setting a variable from within Emacs only affects the current Emacs session. The only way to alter the variable in future sessions is to put something in your init file.

One way to set a variable in Emacs is to go to the <code>*scratch*</code> buffer, type the necessary Lisp expression, and then type <code>C-j</code>. An easier way to set a variable is to use <code>M-x set-variable</code> in any buffer.

<dl>
  <dt><dfn>
  C-h v<br>
  M-x describe-variable</dfn></dt>
  <dd>Display the value and documentation of the specified variable.</dd>

  <dt><dfn>
  M-x set-variable</dfn></dt>
  <dd>Change the value of the specified variable to the specified value.</dd>
</dl>


## Binding New Keys

You can define a key binding in your init file (typically ~/.emacs): <code>(global-set-key (kbd "KEY_SEQUENCE") 'COMMAND)</code>, where KEY_SEQUENCE is written in the same notation that you see in all the Emacs documentation (C- for control, M- for alt, S- for shift, &lt;TAB&gt; for tab, etc.). You can also do <code>(define-key global-map (kbd "KEY_SEQUENCE") 'COMMAND)</code>.

If you want to define a local key binding (local to a particular mode) in your init file, then you need to define the key in the mode's map in the mode's hook: <code>(add-hook 'FOOBAR-mode-hook (lambda() (define-key FOOBAR-mode-map (kbd "KEY_SEQUENCE") 'COMMAND)</code>.

If you want to globally unset a key: <code>(global-unset-key (kbd "KEY_SEQUENCE"))</code>.

To avoid problems caused by overriding existing bindings, the key sequences <code>C-x C-k 0</code> through <code>C-x C-k 9</code> and <code>C-x C-k A</code> through <code>C-x C-k Z</code> are reserved for users (that's you!) to define.

<dl>
  <dt><dfn>
  M-x global-set-key</dfn></dt>
  <dd>Define the specified key globally to run the specified command.</dd>

  <dt><dfn>
  M-x local-set-key</dfn></dt>
  <dd>Define the specified key in the major mode now in effect to run the specified command.</dd>

  <dt><dfn>
  M-x global-unset-key</dfn></dt>
  <dd>Make the specified key undefined in the global key map.</dd>

  <dt><dfn>
  M-x local-unset-key</dfn></dt>
  <dd>Make the specified key undefined in the major mode now in effect.</dd>
</dl>

If you have redefined (or undefined) a key and you subsequently wish to revert the change, undefining the key will not do the job--you need to redefine the key with its standard definition. To find the name of the standard definition of a key, go to a Fundamental mode buffer in a fresh Emacs and use <code>C-h c</code>. The documentation of keys in the Emacs manual also lists their command names.


## Disabling and Enabling Commands

You can make a command disabled either by editing the initialization file directly, or with the command <code>M-x disable-command</code>, which edits the initialisation file for you. Likewise, <code>M-x enable-command</code> edits the initialisation file to enable a command permanently.

To manually disable a command in your init file, you need to put a non-nil <code>disabled</code> property on the Lisp symbol for the command: <code>(put 'COMMAND 'disabled t)</code>. If the value of the <code>disabled</code> property is a string, that string is included in the message displayed when the command is used: <code>(put 'COMMAND 'disabled "MESSAGE")</code>.

To manually enable a command in your init file, you need to put a nil <code>disabled</code> property on the Lisp symbol for the command: <code>(put 'COMMAND 'disabled nil)</code>.

Whether a command is disabled is independent of what key is used to invoke it; disabling also applies if the command is invoked using M-x. Disabling a command has no effect on calling it as a function from Lisp programs.

If you want to enable all disabled commands, then put the following in your init file: <code>(setq disabled-command-function nil)</code>.


## Hooks

A hook is a list of functions to be called on specific occassions, such as saving a file or enabling a mode.

Using hooks, you can apply styles to specific things; for example, if your team were developing a product which required a Linux driver, you'd probably want to use the linux style for the driver, and your own team's style for the rest of the code.

Most hooks are normal hooks. This means that when Emacs runs the hook, it calls each hook function in turn, with no arguments. Every variable whose name ends in "-hook" is a normal hook.

A few hooks are abnormal hooks. Their names end in "-functions" (or sometimes "-hooks") instead of "-hook". What makes these hooks abnormal is that their functions accept arguments or their functions return a value that gets used.

Most major modes run one or more mode hooks as the last step of initialisation.

Major mode hooks also apply to other major modes derived from the original mode.

Every major mode apart from Fundamental mode defines a mode hook. Each mode hook is named after its major mode (append "-hook" to the end of the mode's name; for example, text-mode's hook would be called text-mode-hook). All text-based major modes run text-mode-hook and all programming language modes run prog-mode-hook prior to running their own mode hooks.

Enable Flyspell in all text modes: <code>(add-hook 'text-mode-hook 'flyspell-mode)</code>.

Enable Flyspell Prog in all programming modes: <code>(add-hook 'prog-mode-hook 'flyspell-prog-mode)</code>.

Clean up whitespace before saving a file: <code>(add-hook 'before-save-hook 'whitespace-cleanup)</code>. A less obtrusive way to clean up whitespace is to install the ws-butler package (<code>M-x package-install &lt;RET&gt; ws-butler</code>). To enable ws-butler: <code>(add-hook 'prog-mode-hook 'ws-butler-mode)</code>.


## Packages

A package is a collection of Lisp code that you download and automatically install from within Emacs. Packages provide a convenient way to add new features. In the past, if you liked some third party Lisp code, you would have to manually add it to your init file.

Most optional features in Emacs are grouped into packages. Emacs contains several hundred built-in packages, and more can be installed over the network.

The official Emacs package repository is [GNU ELPA](http://elpa.gnu.org) (Emacs Lisp Package Archive). Another popular Emacs package repository is [MELPA](http://melpa.org) (Milkpostman's Emacs Lisp Package Archive). [Marmalade](https://marmalade-repo.org) is yet another package repository. The [Emacs Lisp List](http://www.damtp.cam.ac.uk/user/sje30/emacs/ell.html) (ELL) aims to provide one compact list of packages with links to all the current Emacs Lisp files on the Internet. The ELL can be browsed over the Web, or from Emacs with the [ell.el](http://www.damtp.cam.ac.uk/user/sje30/emacs/ell.el). As of 2013-06-07, the list is no longer maintained.

To use MELPA and Marmalade, add the following to your init file:

<code>
(require 'package)
(package-initialize)
(add-to-list 'package-archives '("melpa" . "http://melpa.milkbox.net/packages/") t)
(add-to-list 'package-archives '("marmalade" . "https://marmalade-repo.org/packages/") t)
</code>

The <code>(package-initialize)</code> is necessary if you install any packages; otherwise, you won't be able to refer to packages in your init file (for example, to enable their mode).

<code>M-x list-packages</code> brings up a buffer named <code>*Packages*</code> with a list of all packages. You can install or uninstall packages via this buffer. The command accesses the network to retrieve the list of available packages from the package archive server. If the network is unavailable, it falls back on the most recently retrieved list.

The <code>*Packages*</code> buffer seems to sort packages by their status and then by their name.

The command <code>C-h P</code> (<code>M-x describe-package</code>) prompts for the name of a package, and displays a help buffer describing the attributes of the package and the feaures that it implements.

To make it easier to find packages related to a topic, most packages are associated with one or more keywords based on what they do. Type <code>C-h p</code> (<code>M-x finder-by-keyword</code>) to bring up a list of package keywords, together with a description of what the keywords mean. To view a list of packages for a given keyword, type <code>&lt;RET&gt;</code> on that line; this displays the list of packages in a Package Menu buffer.

By default, Emacs downloads packages from a package archive maintained by the Emacs developers and hosted by the GNU Project. Optionally, you can also download packages from archives maintained by third parties.

Each package is downloaded from the package archive in the form of a single package file--either an Emacs Lisp source file or a tar file containing multiple Emacs Lisp source and other files. Package files are automatically retrieved, processed, and disposed of by the Emacs commands that install packages.

Packages are most conveniently installed using the package menu, but you can also use the commad <code>M-x package-install</code>, which prompts for the name of a package with the "available" status. Another way to install a package is to get the package file from somewhere and then type <code>M-x package-install-file</code>.

Once installed, the contents of a package are placed in a subdirectory of ~/.emacs.d/elpa/.

A package may require certain other packages to be installed, because it relies on functionality provided by them. When Emacs installs such a package, it also automatically downloads and installs any required package that is not already installed. If a required package is somehow unavailable, Emacs signals an error and stops installation. A package's requirements list is shown in its help buffer.

By default, packages are downloaded from a single package archive maintained by the Emacs developers. This is controlled by the variable <code>package-archives</code>, whose value is a list of package archives known to Emacs. Each list element must have the form <code>(ID . LOCATION)</code>, wheere ID is the name of a package archive and LOCATION is the HTTP address or directory name of the package archive. You can alter this list if you wish to use third party package archives.

Once a package is downloaded and installed, it is loaded into the current Emacs session. By default, Emacs also automatically loads all installed packages in subsequent Emacs sessions. For finer control over package loading, you can use the variable <code>package-load-list</code>. Its value should be a list. A list element of the form <code>(NAME VERSION)</code> tells Emacs to load version VERSION of the package named NAME. Here, VERSION should be a version string corresponding to a specific version of the package, or <code>t</code> to load any installed version, or <code>nil</code> to disable the package. A list element can also be the symbol <code>all</code>, which means to load the latest installed version of any package not named by the other list elements. The default value is just <code>'(all)</code>.

If you encounter "Error during download request: Not Found" after trying to install a package, try typing <code>M-x package-refresh-contents</code> and then reattempt the install.

Package Menu commands:

<dl>
  <dt><dfn>
  i<br>
  M-x package-menu-mark-install</dfn></dt>
  <dd>Mark the package on the current line for installation.</dd>

  <dt><dfn>
  d<br>
  M-x package-menu-mark-delete</dfn></dt>
  <dd>Mark the package on the current line for deletion.</dd>

  <dt><dfn>
  u</dfn></dt>
  <dd>Remove any installation or deletion marks from the current line.</dd>

  <dt><dfn>
  U<br>
  M-x package-menu-mark-upgrades</dfn></dt>
  <dd>Mark all packages with a newer available version for upgrading.</dd>

  <dt><dfn>
  x<br>
  M-x package-menu-execute</dfn></dt>
  <dd>Download and install all packages marked with <code>i</code> and their dependencies; also, delete all packages marked with <code>d</code>. This also removes the marks.</dd>

  <dt><dfn>
  r<br>
  M-x package-menu-refresh</dfn></dt>
  <dd>Fetch the list of available packages from the package archive and recompute the package list.</dd>
</dl>


## Themes

Custom themes are collections of settings that can be enabled or disabled as a unit. You can use custom themes to swich easily between various collections of settings.

A custom theme is stored as an Emacs Lisp source file. If the name of the custom theme is NAME, the theme file is named NAME-theme.el. By default, Emacs looks for theme files in ~/.emacs.d/ and in etc/themes in your Emacs installation directory.

Type <code>M-x customize-themes</code> to switch to a buffer named <code>*Custom Themes*</code>, which lists known themes and let's you enable or disable themes.

Any customizations that you make through the customization buffer take precedence over theme settings.

You can enable a specific custom theme in the current Emacs session by typing <code>M-x load-theme</code>. To disable a theme, type <code>M-x disable-theme</code>. To enable a theme, type <code>M-x enable-theme</code>. To describe a theme, type <code>M-x describe-theme</code>.

To create or modify custom themes, type <code>M-x customize-create-theme</code>.

If you want to use a custom colour scheme, save the THEME.el file into a directory that is in Emacs's load path (such as <code>~/.emacs.d</code>). Then, in Emacs, run <code>M-x load-theme &lt;RET&gt; THEME</code>; you will be asked whether you'd really like like to load the file or not and if you'd like to consider the theme file to be considered safe for future sessions. If you answer yes to both questions, then some Elisp will be written to your init file. To set the custom colour scheme for all Emacs sessions, add the following to your init file, anywhere **after** where custom-safe-themes is set: <code>(load-theme 'THEME)</code>.


## Colour

By default, Emacs automatically picks an appropriate colour scheme based on whether your background is dark or light. In my case, Emacs didn't detect detect that my terminal's background is dark, so I had to tell it explicitly by adding the following to my init file: <code>(setq-default frame-background-mode 'dark)</code>.

In graphical Emacs, my mouse pointer was black (by default) and my background was black, so it was very hard to see the mouse pointer. To change the colour of the mouse pointer, add the following to your init file: <code>(set-mouse-color "COLOUR")</code> ("orchid" seems like a nice colour for a mouse pointer on a black background; "white" would also be a safe bet).

You can specify a colour as a name or as an RGB triplet. A colour name is a pre-defined name, such as "dark orange" or "medium sea green". To see a list of colour names, RGB triplets, and what the colours look like, type <code>M-x list-colors-display</code>. Emacs understands X11 colour names even on text terminals; if a face is given a colour specified by an X11 colour name, it is displayed using the closest-matching terminal colour. An RGB triplet is a string of the form <code>#RRGGBB</code>. Each of the R, G, and B components is a hexadecimal number. For hexadecimal values A to F, case doesn't matter.

You can also see a list of colours in X11's rgb.txt file (on my computer, it's <code>/usr/share/X11/rgb.txt</code>).


## Fonts

There are several different ways to specify a default font for Emacs:

<ul>
  <li>Add the following to your init file: <code>(add-to-list 'default-frame-alist '(font . "FONT"))</code>.</li>
  <li>Add the following to your ~/.Xresources: <code>emacs.font: FONT</code>.</li>
  <li>Specify the font when you start Emacs by using the <code>-fn</code> (or <code>--font</code>) command-line option.</li>
</ul>

To check what font you're currently using, the <code>C-u C-x =</code> command can be helpful. It describes the character at point, and names the font that it's rendered in. If you're using terminal Emacs, then <code>C-u C-x =</code> probably won't show you what font is being used; however, the font that Emacs uses is likely the font that your terminal uses. In graphical Emacs, <code>C-u C-x =</code> should show the font.

On X, there are four different ways to express a font name:

<ol>
  <li>Fontconfig Pattern</li>
  <li>GTK font pattern (also called a Pango font name)</li>
  <li>X Logical Font Description (XLFD)</li>
  <li>font nicknames</li>
</ol>

Fontconfig patterns have the following form: <code>FONTNAME[-FONTSIZE][:NAME1=VALUES1][:NAME2=VALUES2]...</code>. FONTNAME is the family name of the font, such as "Monospace" or "DejaVu Sans Mono"; FONTSIZE is the point size of the font; and the NAME=VALUES pairs specify settings such as the slant, weight, style, width, or spacing of the font. Each VALUES may be a single value, or a list of values separated by commas. For a more detailed description of Fontconfig patterns, see http://fontconfig.org/fontconfig-user.html.

GTK font patterns have the following form: <code>FONTNAME [PROPERTIES] [FONTSIZE]</code>. FONTNAME is the family name of the font; PROPERTIES is a list of property values separated by spaces; FONTSIZE is the point size of the font.

An X Logical Font Description (XLFD) is the traditional method for specifying fonts under X. Each XLFD consists of fourteen words or numbers, separated by dashes. XLFD patterns have the following form: <code>-MAKER-FAMILY-WEIGHT-SLANT-WIDTHTYPE-STYLE-PIXELS-HEIGHT-HORIZ-VERT-SPACING-WIDTH-REGISTRY-ENCODING</code>. A wildcard character (<code>*</code>) in an XLFD matches any sequence of characters (including none), and <code>?</code> matches any single character; however, matching is implementation-dependent, and can be inaccurate when wildcards match dashes in a long name. For reliable results, supply all 14 dashes and use wildcards only within a field. Case is insignificant in an XLFD. For a more detailed description of XLFD, see http://www.x.org/releases/X11R7.6/doc/xorg-docs/specs/XLFD/xlfd.html.

Certain fonts have shorter nicknames, which you can use instead of a normal font specification.

On X, Emacs recognizes two types of fonts: client-side fonts, which are provided by the Xft and Fontconfig libraries, and server-side fonts, which are provided by the X server itself. Most client-side fonts support advanced font features such as antialiasing and subpixel hinting, while server-side fonts do not. Fontconfig and GTK patterns match only client-side fonts.

You will probably want to use a fixed-width default font--that is, a font in which all characters have the same width. For Xft and Fontconfig fonts, you can use the <code>fc-list</code> command to list the available fixed-width fonts. For server-side X fonts, you can use the <code>xlsfonts</code> program to list the available fixed-width fonts. Any font with "m" or "c" in the SPACING field of the XLFD is a fixed-width font.

To see what a particular font looks like, use the <code>xfd</code> command.

Emacs can display variable-width fonts, but some Emacs commands, particularly indentation commands, do not account for variable character display widths.

A fontset is a named collection of fonts. A font typically defines shapes for a single alphabet or script; therefore, displaying the entire range of scripts that Emacs supports requires a collection of many fonts, hence the use for fontsets.

In graphical Emacs, you can resize the font on the fly. To increase the height of the default font in the current buffer, type <code>C-x C-+</code> or <code>C-x C-=</code>. To decrease it, type <code>C-x C--</code>. To restore the default (global) font height, type <code>C-x C-0</code>. Once you type <code>C-x</code> once, you can repeatedly press any resize key any number of times; for example, <code>C-x C-= C-= C-= C-- C-- C-=</code>.

To see what faces are currently defined and what they look like, type <code>M-x list-faces-display</code>.


## Coding System

Prefer UTF-8 and Unix newlines: <code>(prefer-coding-system 'utf-8-unix)</code>.


## Indentation

Only use spaces for indentation: <code>(setq indent-tabs-mode nil)</code>.

Define the default style for various modes: <code>(setq c-default-style '((java-mode . "java") (awk-mode . "awk") (other . "linux")))</code>. If your team doesn't use any of the built-in styles, you can define your own style. If your team's style is close to one of the built-in styles, you can use that style as the base style, and then override what you need.


## Calendar

Set the date and time style:
<code>
(require 'calendar')

(setq calendar-date-display-form calendar-iso-date-display-form)
(setq calendar-date-style 'iso)
(setq calendar-time-display-form
    '(24-hours ":" minutes (if time-zone " (") time-zone (if time-zone ")")))
</code>

Set your location (for <code>M-x sunrise-sunset</code>):
<code>
(setq calendar-latitude LATITUDE)
(setq calendar-longitude LONGITUDE)
(setq calendar-location-name LOCATION_NAME)
</code>

Latitude and longtidue should be positive or negative decimal numbers (one decimal place is enough). The location name should be a string. For example, if you live in London, you would put <code>51.5</code> for the latitude, <code>-0.1</code> for the longitude, and "London" (or "London, England" or "London, UK" or whatever; the name is arbitrary) for the location name.


### Holidays

If you were only interested in seeing country-specific holidays, then you should start by adding the following to your init file:

<code>
(setq holiday-bahai-holidays nil)
(setq holiday-christian-holidays nil)
(setq holiday-general-holidays nil)
(setq holiday-hebrew-holidays nil)
(setq holiday-islamic-holidays nil)
(setq holiday-oriental-holidays nil)
(setq holiday-other-holidays nil)
</code>

As an example of defining country-specific holidays, here are some Canadian holidays and other observances (if I missed any or made a mistake, please let me know):

<code>
(setq holiday-local-holidays
    '((holiday-fixed 1 1 "New Year's Day")
      (holiday-fixed 1 2 "Bank holiday (Quebec only)")
      (holiday-fixed 1 17 "Raoul Wallenberg Day")
      (holiday-fixed 2 2 "Groundhog Day")
      (holiday-fixed 2 14 "Valentine's Day")
      (holiday-fixed 2 15 "National Flag of Canada Day")
      (holiday-float 2 1 2 "Family Day (British Columbia only)")
      (holiday-float 2 1 3 "Family Day (Alberta, Ontario, and Saskatchewan only); Louis Riel Day (Manitoba only); Islander Day (Prince Edward Island only)")
      (holiday-float 3 1 2 "Commonwealth Day")
      (holiday-fixed 3 17 "Saint Patrick's Day")
      (holiday-fixed 4 1 "April Fool's Day")
      (holiday-fixed 4 6 "Tartan Day")
      (holiday-fixed 4 9 "Vimy Ridge Day")
      (holiday-easter-etc -2 "Good Friday")
      (holiday-easter-etc +1 "Easter Monday")
      (holiday-fixed 4 22 "Earth Day")
      (holiday-fixed 4 23 "Saint George's Day (Newfoundland only)")
      (holiday-fixed 5 4 "Anti-Bullying Day")
      (holiday-float 5 0 2 "Mother's Day")
      (holiday-fixed 6 2 "Decoration Day")
      (holiday-fixed 6 11 "William Davis Miners' Memorial Day (Nova Scotia only)")
      (holiday-float 6 0 3 "Father's Day")
      (holiday-fixed 6 19 "Loyalist Day")
      (holiday-fixed 6 21 "National Aboriginal Day (Northwest Territories only)")
      (holiday-fixed 6 24 "Discovery Day (Newfoundland only); St. Jean Baptiste Day (Quebec only)")
      (holiday-fixed 6 27 "Canadian Multiculturalism Day")
      (holiday-fixed 7 1 "Canada Day")
      (holiday-fixed 7 9 "Nunavut Day (Nunavut only)")
      (hoilday-fixed 7 12 "Orangemen's Day (Newfoundland only)")
      (holiday-fixed 8 9 "National Peacekeepers' Day")
      (holiday-float 8 1 1 "Civic Holiday (All except Quebec and Yukon)")
      (holiday-float 8 1 3 "Discovery Day (Yukon only)")
      (holiday-float 8 3 1 "Regatta Day (Newfoundland only)")
      (holiday-float 8 5 3 "Gold Cup Parade Day (Prince Edward Island only)")
      (hoilday-fixed 8 23 "Black Ribbon Day")
      (holiday-float 9 1 1 "Labour Day")
      (holiday-float 9 0 2 "Grandparents' Day")
      (holiday-float 10 1 2 "Thanksgiving")
      (holiday-fixed 10 31 "Halloween")
      (holiday-fixed 11 11 "Remembrance Day")
      (holiday-fixed 12 6 "National Day of Remembrance and Action on Violence Against Women")
      (holiday-fixed 12 24 "Christmas Eve")
      (holiday-fixed 12 25 "Christmas Day")
      (holiday-fixed 12 26 "Boxing Day")
      (holiday-fixed 12 31 "New Year's Eve")))
</code>

The date when Daylight Savings Time begins and the date when Daylight Savings Time ends are both defined in holiday-solar-holidays.

I think it would be nice if Emacs provided a set of commonly observed international holidays (such as International Women's Day).

TODO: how to properly add Canada Day? (Canada Day normally falls on July 1, but when July 1 is a Sunday, then Canada Day is officially on July 2, although it's still observed on July 1.)
TODO: how to add Victoria Day and National Patriots' Day? (Both holidays fall on the last Monday before May 25.)
TODO: how to add Yukon's Heritage Day? (Yukon's Heritage Day falls on the Friday before the last Sunday in February.)

In Emac's calendar, you can type <code>x</code> to mark all the visible days that have holidays. If you move point to a day that contains a holiday, you can type <code>h</code> to list the holidays for that day.

To see a list of all the holidays in the current year, type <code>M-x list-holidays &lt;RET&gt; &lt;RET&gt; &lt;RET&gt; &lt;RET&gt;</code>.


## World Clock

Use <code>M-x display-time-world</code> to display the current time around the world. Note that the <code>*wclock*</code> auto-refreshes.

<code>
(setq display-time-world-time-format "%R %5Z (UTC%z) - %d %3h - %A")
(setq display-time-world-list
    '(("Europe/London" "London, UK")
      ("Atlantic/Cape_Verde" "Praia, Cape Verde")
      ("Atlantic/South_George" "South Georgia")
      ("Atlantic/Sao_Paulo" "Nuuk, Greenland")
      ("Canada/Newfoundland" "St John's, Canada")
      ("Canada/Atlantic" "Halifax, Canada")
      ("America/Caracas" "Caracas, Venezuela")
      ("Canada/Eastern" "Toronto, Canada")
      ("Canada/Central" "Winnipeg, Canada")
      ("Canada/Mountain" "Edmonton, Canada")
      ("Canada/Pacific" "Vancouver, Canada")
      ("US/Alaska" "Anchorage, USA")
      ("Pacific/Marquesas" "Marquesas Islands")
      ("US/Hawaii" "Honoloulu, USA")
      ("Pacific/Tongatapu" "Tonga")
      ("Pacific/Chatham" "Chatham")
      ("Pacific/Auckland" "Auckland, New Zealand")
      ("Pacific/Norfolk" "Norfolk Island")
      ("Pacific/Noumea" "Noumea, New Caledonia")
      ("Australia/Lord_Howe" "Lord Howe Island")
      ("Australia/Melbourne" "Melbourne, Australia")
      ("Australia/Adelaide" "Adelaide, Australia")
      ("Asia/Tokyo" "Tokyo, Japan")
      ("Australia/Eucla" "Eucla, Australia")
      ("Asia/Shanghai" "Beijing, China")
      ("Asia/Ho_Chi_Minh" "Hanoi, Vietnam")
      ("Asia/Rangoon" "Yangon, Burma")
      ("Asia/Dhaka" "Dhaka, Bangladesh")
      ("Asia/Kathmandu" "Kathmandu, Nepal")
      ("Asia/Calcutta" "New Delhi, India")
      ("Asia/Karachi" "Islamabad, Pakistan")
      ("Asia/Kabul" "Kabul, Afghanistan")
      ("Asia/Dubai" "Dubai, UAE")
      ("Asia/Tehran" "Tehran, Iran")
      ("Europe/Moscow" "Moscow, Russia")
      ("Europe/Athens" "Helsinki, Finland")
      ("Europe/Paris" "Paris, France")
      ("Europe/London" "London, UK")))
</code>

For each time zone in the world, I picked one city or island. Adapt the list to your liking. On my machine, I found the time zone names in <code>/usr/share/zoneinfo</code>. I used https://en.wikipedia.org/wiki/List_of_UTC_time_offsets for a list of locations in each of the time zones.


## Spelling

You can see what spell checking program your Emacs is using by typing <code>C-h v ispell-program-name &lt;RET&gt;</code>. For me, it's Aspell (other likely values would be Ispell or Hunspell).

You can see what dictionaries are available by typing <code>M-x ispell-change-dictionary &lt;RET&gt; &lt;SPC&gt;</code>.

I know there are Canadian dictionaries, but I don't like them; I prefer British dictionaries (I think that British English is proper English). To set the default dictionary, add the following to your init file: <code>(setq ispell-dictionary "en_GB-ise")</code>.


## Modes

Display the current function name (based on where point is in a buffer) in the mode line: <code>(which-function-mode t)</code>.

Automatically indent after typing <code>&lt;RET&gt;</code> when the previous line is indented: <code>(electric-indent-mode t)</code>.

Make it easier to switch buffers: <code>(iswitchb-mode t)</code>.

ido mode is a mode that basically extends the iswitchb behaviour to more than just buffers: <code>(ido-mode t)</code>. When ido mode is enabled and you want to enter something literally, type <code>C-j</code> instead of <code>&lt;RET&gt;</code>. ido shows completion suggestions all in one line; I think that this is unreadable. Luckily, there's another mode that displays the results vertically (one suggestion per line): <code>M-x package-install &lt;RET&gt; ido-vertical-mode</code>. Add the following to your init file: <code>(ido-vertical-mode t)</code>.

icomplete-mode basically extends the iswitchb behaviour to the M-x prompt: <code>(icomplete-mode t)</code>.

Font-Lock mode is enabled globally by default, but you can disable it in individual buffers.

Auto Fill mode inserts newlines as you type to prevent lines from becoming too long: <code>(auto-fill-mode t)</code>. This might be useful for editing plaintext.

Linum mode displays each line's line number in the window's left margin: <code>(global-linum-mode t)</code>. This looks ugly in terminal Emacs (there's no space between the line numbers and the lines).

Visual Line mode performs word wrapping, causing long lines to be wrapped at word boundaries: <code>(global-visual-line-mode t)</code>.

Delete Selection mode causes text insertion to first delete the text in the region, if the region is active: <code>(delete-selection-mode t)</code>.

Show Paren mode highlights both delimiters when point is before an opening delimiter or after a closing delimiter: <code>(show-paren-mode t)</code>.

Glasses mode is a buffer-local minor mode that makes it easier to read mixed-case (CamelCase) symbols like unReadableSymbol by altering how they are displayed. By default, it displays extra underscores between each lowercase letter and the following capital letter: <code>(glasses-mode t)</code>. This does alter the buffer text, only how it is displayed. If you try to enter a camel case name when glasses-mode is enabled, the name will automatically be converted to an underscore delimited name; when you disable glasses-mode, the name is converted to camel case. If you enter a name that contains underscores when glasses-mode is enabled, the name will be left alone when you disable glasses-mode.

Electric Layout mode is a global minor mode that automatically inserts newlines when you type certain characters, such as <code>{</code>, <code>}</code>, or <code>;</code>: <code>(electric-layout-mode t)</code>.

Subword mode allows Emac's commands to recognise uppercase letters in StudlyCapsIdentifiers as word boundaries: <code>(global-subword-mode t)</code>.

Display a list of available completions when you are in the minibuffer and completion is active: <code>(icomplete-mode t)</code>.

To display a list of completions in a pop-up when you're typing, install company-mode: <code>M-x package-install &lt;RET&gt; company</code>. To enable company-mode for programming modes, add the following to your init file: <code>(add-hook 'prog-mode-hook 'company-mode)</code>.

Disable the tool bar: <code>(tool-bar-mode -1)</code>.


## Mode Line

In your ~/.emacs/init.el:

* Show the size of the buffer: <code>(size-indication-mode t)</code>.
* Show the column number of point: <code>(column-number-mode t)</code>.
* Show the current time: <code>(display-time-mode t)</code>.
* Show your computer's battery charge: <code>(display-battery-mode t)</code>.

If you're using display-time-mode, then you can have the word "Mail" appear when you have unread email. Set <code>display-time-mail-directory</code> to the directory to check for unread email (any nonempty regular file in the directory is considered as unread email); for example, I use [mutt](http://www.mutt.org) and would add the following to my ~/.emacs.d/init.el: <code>(setq display-time-mail-directory "~/.mutt/mail/INBOX/new")</code>.

You should use 24-hour time format (don't you dare call this military time; 24-hour time is the most commonly used time format in the world and it makes a lot of sense and is heavily used outside the military and didn't even originate with the military). Add the following to your ~/.emacs.d/init.el: <code>(setq display-time-24hr-format t)</code>.

You can customise the format of the mode line by modifying the <code>mode-line-format</code> variable. Read its documentation (<code>C-h v mode-line-format</code>) for help on modifying it.


## Minibuffer

Delete duplicates from the minibuffer history list: <code>(setq history-delete-duplicates t)</code>.


## Backups and Auto Saves

Disable backups and autosaves:
<code>
(setq auto-save-default nil)
(setq backup-inhibited t)
(setq make-backup-files nil)
</code>


## Splash Screen (Welcome Screen)

Disable the the splash/welcome screen: <code>(setq inhibit-splash-screen t)</code>.


## Sentences

There should only be one space between sentences: <code>(setq sentence-end-double-space nil)</code>.


## Frames

Start Emacs with full width: <code>(add-to-list 'initial-frame-alist '(fullscreen . fullwidth))</code>.

Start Emacs with full height: <code>(add-to-list 'initial-frame-alist '(fullscreen . fullheight))</code>.

Start Emacs with full width and height: <code>(add-to-list 'initial-frame-alist '(fullscreen . fullboth))</code>.

Start Emacs maximised: <code>(add-to-list 'initial-frame-alist '(fullscreen . maximized))</code>.

Start Emacs with custom width and height:
<code>
(add-to-list 'initial-frame-alist '(height . N))
(add-to-list 'initial-frame-alist '(width . M))
</code>

I wish I could use fullheight, fullboth, or maximized, but this poses a problem for me with dwm because the frame covers my dmenu bar.


## Completion

Use ido-vertical-mode and icomplete-mode, or use helm.

Install helm: <code>M-x package-install &lt;RET&gt; helm</code>. Add the following to your init file: <code>(helm-mode t)</code>.


## Directories

To set the default directory, add the following to your init file: <code>(setq default-directory "~/PATH/")</code> (the final slash is necessary). Think of it as the initial default directory; any time you do something file or directory related, such as visiting a file, the default directory changes.

If you still have the splash screen enabled, then when you start Emacs, the default directory will be overridden immediately. In other words, your setting for default-directory won't take effect until you disable the splash screen.


# Calculator

Emacs comes with a powerful calculator called Calc.

By default, Calc uses Reverse Polish Notation (RPN) (also known as postfix notation), where you enter operands first, and then the operator (1 2 +). The central component of an RPN calculator is the stack. Each time you enter a number, it gets pushed onto the top of the stack. When you enter an operator, the appropriate number of operands are popped from the top of the stack, the operator is applied to them, and finally the result of the operation is pushed onto the top of the stack.

Infix notation (also known as algebraic notation) is probably the notation you're most used to. It's where an operator is surrounded by its operands (1 + 2). Calc lets you use infix notation if you're not comfortable using RPN. To enter a formula using infix notation, press <code>'</code> (apostrophe) followed by the formula. You can also enter Algebraic mode by typing <code>m a</code>, so that you don't have to keep prefixing all your formulas with an apostrophe; however, if your formula begins with a function name, then you still need to prefix the formula with an apostrophe, even when you're in Algebraic mode.

Polish notation (also known as prefix notation) may be familiar to you if you've programmed in a language such as Lisp. It's where an operator comes before its operands (+ 1 2).

Calc's standard interface shows two windows side-by-side. The one on the left is the stack window; the one on the right is the trail window. The stack window shows you the contents of the calculator's stack. The stack is actually shown with the top of the stack at the bottom of the window and the bottom of the stack at the top of the window. Each line is preceded by a number (a stack level number), which indicates that line's position in the stack (1: is the top, 2: is the second from the top, and so on). Some commands can be told what stack levels to work with. The trail window shows you the history of all the operands and operators you've entered. A number that isn't preceded by anything indicates an operand. A number that is preceded by an operator indicates the result of applying that operator to the previous operands. When the operator is followed by <code>&gt;</code> (the trail pointer), it indicates the most recent result. Since the stack and trail are Emacs buffers, you can scroll them and such like you normally would an ordinary buffer.

Calc has a few different modes. You can run it in standard mode (<code>M-x calc</code>), which shows two side-by-side windows; <code>M-x full-calc</code> shows standard mode in a full screen; <code>M-x calc-keypad</code> provides a keypad for mouse input (like a typical GUI calculator); <code>M-x full-calc-keypad</code> shows the keypad in a full screen; and <code>M-x quick-calc</code> uses the minibuffer to prompt for a formula, which should be entered in algebraic notation, and displays the result in the echo area; <code>M-x calc-embedded</code> enables Calc to be used directly inside a typical Emacs buffer; <code>M-x calc-grab-rectangle</code> can be used for grabbing a rectangle from a buffer and pushing it onto Calc's stack; <code>M-x calc-grab-region</code> can be used for grabbing a region from a buffer and pushing it onto Calc's stack.

If you just want to use Calc, but not Emacs, then you could do something like <code>emacs -f full-calc</code> or <code>emacs -f full-calc-keypad</code> to launch Emacs.

All Calc commands begin with the word "calc-". Since it's tedious to have to type "M-x calc-" for every command, Calc provides an 'x' key, which is shorthand for "M-x calc-"; for example, instead of typing <code>M-x calc-hypot</code>, you can simply type <code>x hypot</code>.

As in normal mathematical notation, the <code>*</code> symbol can often be omitted: <code>2a</code> and <code>2 a</code> are the same thing as <code>2 * a</code>.

To enter negative numbers into Calc, use an underscore as the negative sign, or enter the number as a positive, and then press <code>n</code> to negate the number.

To enter fractions into Calc, use a colon (<code>:</code>), since the forward slash and backslash are both reserved for division; for example, to enter two thirds (2/3), write <code>2:3</code>.

To enter a percentage into Calc, type <code>M-%</code> after the number; for example, to enter 50%, write <code>50 M-%</code>.

To enter a vector (a list of numbers) into Calc, press <code>[</code>, and then for each number you want to include in the vector, type the number followed by either <code>&lt;RET&gt;</code> or <code>,</code> (a comma). When you're done, press <code>]</code> to complete the vector. If you used <code>&lt;RET&gt;</code> instead of a comma, then the commas will be added for you when you press <code>]</code>. You can also enter vectors in algebraic mode using the same square bracket notation with comma delimited items.

To enter units into Calc, you need to use algebraic mode. To see a list of units, type <code>u v</code>. To enter composite units (a value that consists of more than one unit, such as 1 hr 30 min), use algebraic mode and use a plus between sets of units; for example, to enter 1 hr 30 min, you would type <code>' 1 hr + 30 min</code>. If you want to enter one unit per another unit, use the division (<code>/</code>) operator; for example to enter 20 metres per second, type <code>' 20 m / s</code>. If you want to also use composite units in that case, either use parentheses (<code>' (3 km + 200 m) / hr</code>) or enter each part separately with a plus (<code>+</code>) in between: <code>' 3 km / hr + 200 m / hr</code>.

To enter times into Calc, type <code>@</code> or <code>h</code> after the hours; type <code>'</code> or <code>m</code> after the minutes; and type <code>"</code> or <code>s</code> after the seconds.

To enter dates and times into Calc, you need to use algebraic mode and enter the date and/or time surrounded by <code>&lt;</code> and <code>&gt;</code>. To enter a date: <code>&lt;YYYY-MM-DD&gt;</code> (for example, <code>&lt;1932-09-25</code> for 25 September 1932). To enter a time: <code>HH:mm:SS</code> (for example, <code>&lt;17:30:05&gt;</code>). To change the date format to something sensible: <code>d d YYYY-MM-DD HH:mm:SS</code>; for a list of date formatting codes, go to the "Date Formatting Codes" section in the Calc manual.

You can use the <code>+</code> and <code>-</code> operators with dates and times. For dates, if you push a simple number onto the stack and then invoke <code>+</code> or <code>-</code>, then that many days will be added or subtracted from the date. For times, if you push a simple number onto the stack and then invoke <code>+</code> or <code>-</code>, then that many hours will be added or subtracted. In both cases, you can also use floats; for example, 1.5 means one and a half days (36 hours) or one and a half hours (90 minutes). You can also enter another date or time and then do arithmetic based on the two dates on the top of the stack. To add a month to a date, you can use <code>t I</code> and to subtract a month use <code>M-- t I</code> or <code>C-u - t I</code>. To add a second, use <code>f ]</code>. To subtract a second, use <code>f [</code>. Note that Emacs's calendar (<code>M-x calendar</code>) is also capable of doing date arithmetic; it can tell you how many days there are between two dates (move to a date, set mark, move to another date, type <code>M-=</code>); you can move forward or backward from a selected date (and you can use prefix arguments to move in larger jumps); etc. In other words, you don't need to rely on Calc in order to do some basic date arithmetic.

A variable name should consist of one or more letters or digits, beginning with a letter. Any variables in an algebraic formula for which you have not stored values are left alone, even when you evaluate the formula.

<dl>
  <dt><dfn>
  C-x * i<br>
  x info<br>
  M-x calc-info</dfn></dt>
  <dd>Go to the Calc manual.</dd>

  <dt><dfn>
  C-x * t<br>
  x tutorial<br>
  M-x calc-tutorial</dfn></dt>
  <dd>Go to the Calc tutorial.</dd>

  <dt><dfn>
  C-x * s<br>
  x info-summary<br>
  M-x calc-info-summary</dfn></dt>
  <dd>Go to the Calc summary, which lists all the Calc commands that are bound to keys.</dd>

  <dt><dfn>
  C-x * c<br>
  C-x * *<br>
  M-x calc<br>
  M-x full-calc</dfn></dt>
  <dd>Toggle Calc. When closing, the Calc windows will simply be hidden, not destroyed. This way, you don't lose your calculations (you'll get them back when you toggle Calc back on).</dd>

  <dt><dfn>
  C-x * x<br>
  q<br>
  x quit<br>
  M-x calc-quit</dfn></dt>
  <dd>Exit Calc. If you want to close Calc without losing your calculations, then you should toggle Calc with <code>C-x * c</code> or <code>C-x * *</code> instead of exiting.</dd>

  <dt><dfn>
  C-x * b</dfn></dt>
  <dd>Toggle between full screen Calc and standard size Calc.</dd>

  <dt><dfn>
  C-x * k<br>
  M-x calc-keypad<br>
  M-x full-calc-keypad</dfn></dt>
  <dd>Toggle Calc's keypad mode.</dd>

  <dt><dfn>
  C-x * q<br>
  M-x quick-calc</dfn></dt>
  <dd>Start Calc in quick mode, which uses the minibuffer to prompt for a formula, which should be entered using infix notation. The result will appear in the echo area.</dd>

  <dt><dfn>
  C-x * e<br>
  M-x calc-embedded</dfn></dt>
  <dd>Toggle Calc's embedded mode; this lets you use Calc in a normal Emacs buffer by making Calc's commands available in the buffer.</dd>

  <dt><dfn>
  '</dfn></dt>
  <dd>Use the minibuffer to prompt for a formula, which should be entered using infix notation.</dd>

  <dt><dfn>
  m a<br>
  x algebraic-mode<br>
  M-x calc-algebraic-mode</dfn></dt>
  <dd>Toggle Algebraic mode.</dd>

  <dt><dfn>
  M-x another-calc</dfn></dt>
  <dd>Open a new, independent Calc window, so that you can have multiple calculators.</dd>

  <dt><dfn>
  m O<br>
  x no-simplify-mode<br>
  M-x calc-no-simplify-mode</dfn></dt>
  <dd>Turn simplification mode off; this is useful to do when you want to pull something from or push something onto the stack as is.</dd>

  <dt><dfn>
  C-x * g<br>
  M-x calc-grab-region</dfn></dt>
  <dd>Place the contents of the region into a vector (list) of numbers on top of the stack. The order of the numbers is based on their left-to-right, top-to-bottom order in the region. To unpack the vector, so that each number is a separate operand on the stack, type <code>v u</code>. If you want to grab a region that contains units, then you need to use parentheses to surround each set of numbers with their units; otherwise, the whole region is treated as one element in the vector. Also, if you're grabbing units, you should probably disable simplification mode, so that they're copied over as is: <code>m O</code>.</dd>

  <dt><dfn>
  C-x * r<br>
  M-x calc-grab-rectangle</dfn></dt>
  <dd>Place the contents of the rectangle into a matrix (list of lists) of numbers on top of the stack. The matrix consists of a vector for each row in the rectangle.</dd>

  <dt><dfn>
  C-x * :</dfn></dt>
  <dd>Grab the rectangular region and compute the sums of its columns.</dd>

  <dt><dfn>
  C-x * _</dfn></dt>
  <dd>Grab the rectangular region and compute the sums of its rows.</dd>

  <dt><dfn>
  &lt;RET&gt;<br>
  &lt;SPC&gt;</dfn></dt>
  <dd>
<p>If you press &lt;RET&gt; or &lt;SPC&gt; after entering a number, then the number will be pushed onto the top of the stack. Note that you can enter an operator instead of &lt;RET&gt; or &lt;SPC&gt; after a number; in that case, the operand will be pushed and the operator will be applied immediately, saving you a keystroke.</p>

<p>If you press &lt;RET&gt; or &lt;SPC&gt; when you're not entering a number, then the top of the stack will be duplicated.</p>
  </dd>

  <dt><dfn>
  &lt;DEL&gt;</dfn></dt>
  <dd>Delete the top element from the stack.</dd>

  <dt><dfn>
  M-0 &lt;DEL&gt;<br>
  C-u 0 &lt;DEL&gt;</dfn></dt>
  <dd>Empty the entire stack.</dd>

  <dt><dfn>
  C-x * 0</dfn></dt>
  <dd>Empty Calc's stack and reset Calc's initial mode settings.</dd>

  <dt><dfn>
  &lt;TAB&gt;</dfn></dt>
  <dd>Swap the top two elements on the stack.</dd>

  <dt><dfn>
  M-&lt;TAB&gt;</dfn></dt>
  <dd>Cycle the top three elements on the stack upward (the top becomes the second element, the second element becomes the third element, and the third element becomes the new top).</dd>

  <dt><dfn>
  U<br>
  C-/<br>
  C-_<br>
  x undo<br>
  M-x calc-undo</dfn></dt>
  <dd>Undo.</dd>

  <dt><dfn>
  D<br>
  x redo<br>
  M-x calc-redo</dfn></dt>
  <dd>Redo.</dd>

  <dt><dfn>
  M-&lt;RET&gt;<br>
  x last-args<br>
  M-x calc-last-args</dfn></dt>
  <dd>Push the arguments of the most recent command back onto the stack (without removing the result of the previous command), so that you can perform another operation with the same arguments.</dd>

  <dt><dfn>
  `</dfn></dt>
  <dd>Edit the top of the stack. With a positive prefix argument, edit the past N stack entries. With 0 as the prefix argument, edit the entire stack. With a negative prefix argument, edit a specific stack entry.</dd>

  <dt><dfn>
  C-x * y</dfn></dt>
  <dd>Yank the top of the stack into a buffer.</dd>

  <dt><dfn>
  p PRECISION<br>
  x precision<br>
  M-x calc-precision</dfn></dt>
  <dd>Set the precision of the calculator to the specified number.</dd>

  <dt><dfn>
  d g<br>
  x group-digits<br>
  M-x calc-group-digits</dfn></dt>
  <dd>Group digits together in the integer part of a number. With a prefix argument, you can specify how many digits should belong to each group (with no prefix argument, the default is 3 or 4, depending on the radix).</dd>

  <dt><dfn>
  M-- d g<br>
  M-- x group-digits<br>
  M-- M-x calc-group-digits<br>
  C-u - d g<br>
  C-u - x group-digits<br>
  C-u - M-x calc-group-digits</dfn></dt>
  <dd>Group digits together in the fractional part of a number. With a prefix argument, you can specify how many digits should belong to each group (with no prefix argument, the default is 3 or 4, depending on the radix).</dd>

  <dt><dfn>
  d , GROUP_SEPARATOR<br>
  x group-char<br>
  M-x calc-group-char</dfn></dt>
  <dd>Change the group separator (a comma by default) to the specified character.</dd>

  <dt><dfn>
  d . DECIMAL_CHARACTER<br>
  x point-char<br>
  M-x calc-point-char</dfn></dt>
  <dd>Change the decimal separator (a period by default) to the specified character.</dd>

  <dt><dfn>
  d d<br>
  x date-notation<br>
  M-x calc-date-notation</dfn></dt>
  <dd>Change the display format of dates.</dd>

  <dt><dfn>
  d n<br>
  x normal-notation<br>
  M-x calc-normal-notation</dfn></dt>
  <dd>Display all floating point numbers on the stack in normal format. With a prefix argument, you can specify how many digits should be displayed.</dd>

  <dt><dfn>
  d f<br>
  x fix-notation<br>
  M-x calc-fix-notation</dfn></dt>
  <dd>Display all floating point numbers on the stack in fixed-point format. With a prefix argument, you can specify how many digits should be displayed.</dd>

  <dt><dfn>
  d s<br>
  x sci-notation<br>
  M-x calc-sci-notation</dfn></dt>
  <dd>Display all floating point numbers on the stack in scientific notation. With a prefix argument, you can specify how many digits should be displayed.</dd>

  <dt><dfn>
  d e<br>
  x eng-notation<br>
  M-x calc-eng-notation</dfn></dt>
  <dd>Display all floating point numbers on the stack in engineering notation. With a prefix argument, you can specify how many digits should be displayed.</dd>

  <dt><dfn>
  d r RADIX<br>
  x radix<br>
  M-x calc-radix</dfn></dt>
  <dd>Display the numbers on the stack in the specified radix (2 for binary, 8 for octal, 10 for decimal, 16 for hexadecimal, etc.).</dd>

  <dt><dfn>
  m r<br>
  x radians-mode<br>
  M-x calc-radians-mode</dfn></dt>
  <dd>Use radians for angles.</dd>

  <dt><dfn>
  m d<br>
  x degrees-mode<br>
  M-x calc-degrees-mode</dfn></dt>
  <dd>Use degrees for angles.</dd>

  <dt><dfn>
  m f<br>
  x frac-mode<br>
  M-x calc-frac-mode</dfn></dt>
  <dd>Display the results of integer division as fractions instead of decimals.</dd>

  <dt><dfn>
  d t<br>
  x truncate-stack<br>
  M-x calc-truncate-stack</dfn></dt>
  <dd>Move the stack pointer (the '.') to the current line.</dd>

  <dt><dfn>
  d [<br>
  x truncate-up<br>
  M-x calc-truncate-up</dfn></dt>
  <dd>Move the stack pointer one line up.</dd>

  <dt><dfn>
  d ]<br>
  x truncate-down<br>
  M-x calc-truncate-down</dfn></dt>
  <dd>Move the stack pointer one line down.</dd>

  <dt><dfn>
  t h<br>
  x trail-here<br>
  M-x calc-trail-here</dfn></dt>
  <dd>Move the trail pointer to the current line.</dd>

  <dt><dfn>
  t n<br>
  x trail-next<br>
  M-x calc-trail-next</dfn></dt>
  <dd>Move the trail pointer one line down.</dd>

  <dt><dfn>
  t p<br>
  x trail-previous<br>
  M-x calc-trail-previous</dfn></dt>
  <dd>Move the trail pointer one line up.</dd>

  <dt><dfn>
  t ]<br>
  x trail-last<br>
  M-x calc-trail-last</dfn></dt>
  <dd>Reset the trail pointer (move the trail pointer to the last line in the trail window).</dd>

  <dt><dfn>
  t [<br>
  x trail-first<br>
  M-x calc-trail-first</dfn></dt>
  <dd>Move the trail pointer to the first line in the trail window.</dd>

  <dt><dfn>
  t y<br>
  x trail-yank<br>
  M-x calc-trail-yank</dfn></dt>
  <dd>Yank the trail pointer's value onto the top of the stack.</dd>

  <dt><dfn>
  t r<br>
  x search-reverse<br>
  M-x trail-search-reverse</dfn></dt>
  <dd>Search the trail window. You can use <code>C-s</code> or <code>C-r</code> to continue the search forwards or backwards, just like you would in an ordinary Emacs buffer.</dd>

  <dt><dfn>
  t d<br>
  x trail-display<br>
  M-x calc-trail-display</dfn></dt>
  <dd>Toggle the display of the trail window.</dd>

  <dt><dfn>
  t i<br>
  x trail-in<br>
  M-x calc-trail-in</dfn></dt>
  <dd>Move the cursor into the trail window.</dd>

  <dt><dfn>
  t o<br>
  x trail-out<br>
  M-x calc-trail-out</dfn></dt>
  <dd>Move the cursor out of the trail window.</dd>

  <dt><dfn>
  n<br>
  x change-sign<br>
  M-x calc-change-sign<br>
  'neg(NUMBER)<br>
  '-NUMBER</dfn></dt>
  <dd>Negate a number (change negative to positive; change positive to negative). You can also input negative numbers directly using an underscore ('_') as the negative sign.</dd>

  <dt><dfn>
  P</dfn></dt>
  <dd>Insert Pi.</dd>

  <dt><dfn>
  H P</dfn></dt>
  <dd>Insert e.</dd>

  <dt><dfn>
  I H P</dfn></dt>
  <dd>Insert Phi.</dd>

  <dt><dfn>
  RADIX#NUMBER</dfn></dt>
  <dd>Enter a number in the specified radix.</dd>

  <dt><dfn>
  +<br>
  x plus<br>
  M-x calc-plus<br>
  'add(NUMBER1, NUMBER2)<br>
  'NUMBER1 + NUMBER2</dfn></dt>
  <dd>Add two numbers.</dd>

  <dt><dfn>
  -<br>
  x minus<br>
  M-x calc-minus<br>
  'sub(NUMBER1, NUMBER2)<br>
  'NUMBER1 - NUMBER2</dfn></dt>
  <dd>Subtract two numbers.</dd>

  <dt><dfn>
  *<br>
  x times<br>
  M-x calc-times<br>
  'mul(NUMBER1, NUMBER2)<br>
  'NUMBER1 * NUMBER2<br>
  'NUMBER1 NUMBER2</dfn></dt>
  <dd>Multiply two numbers.</dd>

  <dt><dfn>
  /<br>
  x divide<br>
  M-x calc-divide<br>
  'div(NUMBER1, NUMBER2)<br>
  'NUMBER1 / NUMBER2</dfn></dt>
  <dd>Divide two numbers.</dd>

  <dt><dfn>
  \<br>
  x idiv<br>
  M-x calc-idiv<br>
  'idiv(NUMBER1, NUMBER2)<br>
  'NUMBER1 \ NUMBER2</dfn></dt>
  <dd>Divide two numbers and then floor the result.</dd>

  <dt><dfn>
  %<br>
  x mod<br>
  M-x calc-mod<br>
  'mod(NUMBER1, NUMBER2)<br>
  'NUMBER1 % NUMBER2</dfn></dt>
  <dd>Divide two numbers, floor the result, and then return the remainder (in other words, perform a modulo operation).</dd>

  <dt><dfn>
  NUMBER M MODULUS</dfn></dt>
  <dd>Compute the value of NUMBER mod MODULUS; for example, <code>33 M 24</code> results in 9 mod 24.</dd>

  <dt><dfn>
  :<br>
  x fdiv<br>
  M-x calc-fdiv<br>
  'fdiv(NUMBER1, NUMBER2)</dfn></dt>
  <dd>Divide two numbers and display the result as a fraction.</dd>

  <dt><dfn>
  ^<br>
  x power<br>
  M-x calc-power<br>
  'pow(NUMBER1, NUMBER2)<br>
  'NUMBER1^NUMBER2</dfn></dt>
  <dd>Raise a number to the power of another number.</dd>

  <dt><dfn>
  I ^<br>
  'nroot(NUMBER1, NUMBER2)<br>
  'NUMBER1^(1/NUMBER2)</dfn></dt>
  <dd>Compute the nth root of a number.</dd>

  <dt><dfn>
  Q<br>
  x sqrt<br>
  M-x calc-sqrt<br>
  'sqrt(NUMBER)</dfn></dt>
  <dd>Take the square root of a number.</dd>

  <dt><dfn>
  I Q<br>
  'sqr(NUMBER)<br>
  'NUMBER^2</dfn></dt>
  <dd>Compute the square of a number.</dd>

  <dt><dfn>
  A<br>
  x abs<br>
  M-x calc-abs<br>
  'abs(NUMBER)</dfn></dt>
  <dd>Compute the absolute value of a number.</dd>

  <dt><dfn>
  &<br>
  x inv<br>
  M-x calc-inv<br>
  'inv(NUMBER)<br>
  '1 / NUMBER</dfn></dt>
  <dd>Compute the reciprocal of a number.</dd>

  <dt><dfn>
  !<br>
  x factorial<br>
  M-x calc-factorial<br>
  'fact(NUMBER)<br>
  'NUMBER!</dfn></dt>
  <dd>Compute the factorial of a number.</dd>

  <dt><dfn>
  f [<br>
  x decrement<br>
  M-x calc-decrement<br>
  'decr(NUMBER)<br>
  'decr(NUMBER, AMOUNT)</dfn></dt>
  <dd>Decrement the given number by the optionally specified amount (1 by default).</dd>

  <dt><dfn>
  f ]<br>
  x increment<br>
  M-x calc-increment<br>
  'incr(NUMBER)<br>
  'incr(NUMBER, AMOUNT)</dfn></dt>
  <dd>Increment the given number by the optionally specified amount (1 by default).</dd>

  <dt><dfn>
  L<br>
  x ln<br>
  M-x calc-ln<br>
  'ln(NUMBER)</dfn></dt>
  <dd>Compute the natural logarithm of a number.</dd>

  <dt><dfn>
  E<br>
  x exp<br>
  M-x calc-exp<br>
  'exp(NUMBER)</dfn></dt>
  <dd>Compute e to the specified power.</dd>

  <dt><dfn>
  H E<br>
  'exp10(NUMBER)<br>
  '10^NUMBER</dfn></dt>
  <dd>Compute 10 to the specified power.</dd>

  <dt><dfn>
  H L<br>
  x log10<br>
  M-x calc-log10<br>
  'log10(NUMBER)</dfn></dt>
  <dd>Compute the common (base-10) logarithm of a number.</dd>

  <dt><dfn>
  B<br>
  x log<br>
  M-x calc-log<br>
  'log(NUMBER, BASE)</dfn></dt>
  <dd>Compute the logarithm of a number using the specified base.</dd>

  <dt><dfn>
  I B<br>
  'alog(LOG, BASE)<br>
  'BASE^LOG</dfn></dt>
  <dd>Compute the anti-logarithm of a number using the specified base.</dd>

  <dt><dfn>
  k g<br>
  x gcd<br>
  M-x calc-gcd<br>
  'gcd(NUMBER1, NUMBER2)</dfn></dt>
  <dd>Compute the GCD of two numbers.</dd>

  <dt><dfn>
  k l<br>
  x lcm<br>
  M-x calc-lcm<br>
  'lcm(NUMBER1, NUMBER2)</dfn></dt>
  <dd>Compute the LCM of two numbers.</dd>

  <dt><dfn>
  k c<br>
  x choose<br>
  M-x calc-choose<br>
  'choose(NUMBER1, NUMBER2)</dfn></dt>
  <dd>Compute a binomial coefficient given two numbers.</dd>

  <dt><dfn>
  H k c<br>
  x perm<br>
  M-x calc-perm<br>
  'perm(NUMBER1, NUMBER2)</dfn></dt>
  <dd>Compute the number of permutations given two numbers.</dd>

  <dt><dfn>
  k p<br>
  x prime-test<br>
  M-x calc-prime-test</dfn></dt>
  <dd>Check if a number is prime.</dd>

  <dt><dfn>
  k f<br>
  x prime-factors<br>
  M-x calc-prime-factors<br>
  'prfac(NUMBER)</dfn></dt>
  <dd>Decompose an integer into its prime factors.</dd>

  <dt><dfn>
  a +<br>
  x summation<br>
  M-x calc-summation<br>
  'sum(FORMULA, SUMMATION_VARIABLE, FROM, TO)</dfn></dt>
  <dd>Sum the values from FROM to TO using the specified formula and increment the specified variable; for example, to sum the numbers from 1 to 4: <code>'x &lt;RET&gt; a + x &lt;RET&gt; 1 &lt;RET&gt; 4 &lt;RET&gt;</code>.</dd>

  <dt><dfn>
  a *<br>
  x product<br>
  M-x calc-product<br>
  'prod(FORMULA, PRODUCT_VARIABLE, FROM, TO)</dfn></dt>
  <dd>Multiply the values from FROM to TO using the specified formula and increment the specified variable; for example, to multiply the numbers from 1 to 4: <code>'x &lt;RET&gt; a * x &lt;RET&gt; 1 &lt;RET&gt; 4 &lt;RET&gt;</code>.</dd>

  <dt><dfn>
  S<br>
  x sin<br>
  M-x calc-sin<br>
  'sin(NUMBER)</dfn></dt>
  <dd>Sine.</dd>

  <dt><dfn>
  I S<br>
  x arcsin<br>
  M-x calc-arcsin<br>
  'arcsin(NUMBER)</dfn></dt>
  <dd>Arcsine.</dd>

  <dt><dfn>
  C<br>
  x cos<br>
  M-x calc-cos<br>
  'cos(NUMBER)</dfn></dt>
  <dd>Cosine.</dd>

  <dt><dfn>
  I C<br>
  x arccos<br>
  M-x calc-arccos<br>
  'arccos(NUMBER)</dfn></dt>
  <dd>Arccosine.</dd>

  <dt><dfn>
  T<br>
  x tan<br>
  M-x calc-tan<br>
  'tan(NUMBER)</dfn></dt>
  <dd>Tangent.</dd>

  <dt><dfn>
  I T<br>
  x arctan<br>
  M-x calc-arctan<br>
  'arctan(NUMBER)</dfn></dt>
  <dd>Arctangent.</dd>

  <dt><dfn>
  I F<br>
  x ceiling<br>
  M-x calc-ceiling<br>
  'ceil(NUMBER)</dfn></dt>
  <dd>Take the ceiling of a number.</dd>

  <dt><dfn>
  R<br>
  x round<br>
  M-x calc-round<br>
  'round(NUMBER)</dfn></dt>
  <dd>Round a number to the nearest integer.</dd>

  <dt><dfn>
  c f<br>
  x float<br>
  M-x calc-float<br>
  'pfloat(NUMBER)</dfn></dt>
  <dd>Convert a number from an integer to a float.</dd>

  <dt><dfn>
  F<br>
  x floor<br>
  M-x calc-floor<br>
  'floor(NUMBER)</dfn></dt>
  <dd>Convert a number from a float to an integer (take the floor of it).</dd>

  <dt><dfn>
  c r<br>
  x to-radians<br>
  M-x calc-to-radians<br>
  'rad(DEGREES)</dfn></dt>
  <dd>Convert a number from degrees to radians.</dd>

  <dt><dfn>
  c d<br>
  x to-degrees<br>
  M-x calc-to-degrees<br>
  'deg(RADIANS)</dfn></dt>
  <dd>Convert a number from radians to degrees.</dd>

  <dt><dfn>
  u b<br>
  x base-units<br>
  M-x calc-base-units</dfn></dt>
  <dd>Convert a number into its base units.</dd>

  <dt><dfn>
  u c<br>
  x convert-units<br>
  M-x calc-convert-units</dfn></dt>
  <dd>Convert a number into different units. If the number isn't associated with any units, you'll be prompted for its units. Then, you'll be prompted for the units to convert to. You can use composite units for the conversion; for example, subtract two dates (the result will be in days), and then type <code>u c day &lt;RET&gt; day + hr + min + sec &lt;RET&gt;</dd>.

  <dt><dfn>
  u e<br>
  x explain-units<br>
  M-x calc-explain-units</dfn></dt>
  <dd>Display the full name of the units for a number.</dd>

  <dt><dfn>
  u r<br>
  x remove-units<br>
  M-x calc-remove-units</dfn></dt>
  <dd>Remove the units from a number.</dd>

  <dt><dfn>
  t C<br>
  x convert-time-zones<br>
  M-x convert-time-zones<br>
  'tzconv(TIME, OLD_TIME_ZONE, NEW_TIME_ZONE)</dfn></dt>
  <dd>Convert from one time zone into another.</dd>

  <dt><dfn>
  v x SIZE<br>
  x index<br>
  M-x calc-index<br>
  'index(SIZE)</dfn></dt>
  <dd>Create a vector of the specified size using consecutive integers from 1 to SIZE; for example, to create a vector of size 6, type <code>v x 6</code>, which results in the vector [1, 2, 3, 4, 5, 6].</dd>

  <dt><dfn>
  v l<br>
  x vlength<br>
  M-x calc-vlength<br>
  'vlen(VECTOR)</dfn></dt>
  <dd>Compute the length of a vector.</dd>

  <dt><dfn>
  | =<br>
  x concat =<br>
  M-x calc-concat =</dfn></dt>
  <dd>Merge two vectors together.</dd>

  <dt><dfn>
  V S<br>
  x sort<br>
  M-x calc-sort<br>
  'sort(VECTOR)</dfn></dt>
  <dd>Sort the elements of a vector into increasing order.</dd>

  <dt><dfn>
  I V S<br>
  'rsort(VECTOR)</dfn></dt>
  <dd>Reverse sort a vector (sort the elements of a vector into decreasing order).</dd>

  <dt><dfn>
  V M OPERATOR<br>
  x map<br>
  M-x calc-map<br>
  'map(OPERATOR, VECTOR)</dfn></dt>
  <dd>Apply the specified operator to every element of a vector. For operators that take more than one argument, you need to have enough operands on the stack; for example, if you wanted to double all the elements in a vector, you would push a vector onto the stack, push a 2 onto the stack, and then type <code>V M *</code>.</dd>

  <dt><dfn>
  V R OPERATOR<br>
  x reduce<br>
  M-x calc-reduce<br>
  'reduce(OPERATOR, VECTOR)</dfn></dt>
  <dd>Apply the specified operator across a vector, reducing it to a single value; for example, if you wanted to sum the elements of [1, 2, 3, 4], you would push that vector onto the stack, and then type <code>V R +</code>, which would result in 10 (because 1 + 2 + 3 + 4 = 10).</dd>

  <dt><dfn>
  u +<br>
  x vector-sum<br>
  M-x calc-vector-sum<br>
  'vsum(VECTOR)</dfn></dt>
  <dd>Compute the sum of the values in a vector (similar to <code>V R +</code>).</dd>

  <dt><dfn>
  u *<br>
  x vector-prod<br>
  M-x calc-vector-prod<br>
  'vprod(VECTOR)</dfn></dt>
  <dd>Compute the product of the values in a vector (similar to <code>V R *</code>).</dd>

  <dt><dfn>
  u X<br>
  x vector-max<br>
  M-x calc-vector-max<br>
  'vmax(VECTOR)</dfn></dt>
  <dd>Find the maximum value in a vector.</dd>

  <dt><dfn>
  u N<br>
  x vector-min<br>
  M-x calc-vector-min<br>
  'vmin(VECTOR)</dfn></dt>
  <dd>Find the minimum value in a vector.</dd>

  <dt><dfn>
  u M<br>
  x vector-mean<br>
  M-x calc-vector-mean<br>
  'vmean(VECTOR)</dfn></dt>
  <dd>Compute the arithmetic mean of a vector.</dd>

  <dt><dfn>
  H u M<br>
  x vector-median<br>
  M-x calc-vector-median<br>
  'vmedian(VECTOR)</dfn></dt>
  <dd>Compute the median of a vector.</dd>

  <dt><dfn>
  u S<br>
  x vector-sdev<br>
  M-x calc-vector-sdev<br>
  'vsdev(VECTOR)</dfn></dt>
  <dd>Compute the sample standard deviation of a vector.</dd>

  <dt><dfn>
  I u S<br>
  x vector-pop-sdev<br>
  M-x calc-vector-pop-sdev<br>
  'vpsdev(VECTOR)</dfn></dt>
  <dd>Compute the population standard deviation of a vector.</dd>

  <dt><dfn>
  H u S<br>
  x vector-variance<br>
  M-x calc-vector-variance<br>
  'vvar(VECTOR)</dfn></dt>
  <dd>Compute the sample variance of a vector.</dd>

  <dt><dfn>
  I H u S<br>
  x vector-pop-variance<br>
  M-x calc-vector-pop-variance<br>
  'vpvar(VECTOR)</dfn></dt>
  <dd>Compute the population variance of a vector.</dd>

  <dt><dfn>
  t N<br>
  x now<br>
  M-x calc-now<br>
  'now()</dfn></dt>
  <dd>Push the current date and time onto the top of the stack.</dd>

  <dt><dfn>
  x time<br>
  M-x calc-time</dfn></dt>
  <dd>Push the current time onto the top of the stack.</dd>

  <dt><dfn>
  t I<br>
  x inc-month<br>
  M-x calc-inc-month<br>
  'incmonth(DATE)<br>
  'incmonth(DATE, AMOUNT)</dfn></dt>
  <dd>Increment a date by the optionally specified number of months (1 by default).</dd>

  <dt><dfn>
  M-%<br>
  x percent<br>
  M-x calc-percent<br>
  'percent(NUMBER)<br>
  'NUMBER%</dfn></dt>
  <dd>Input a percentage.</dd>

  <dt><dfn>
  c %<br>
  x convert-percent<br>
  M-x calc-convert-percent<br>
  'percent(NUMBER * 100)</dfn></dt>
  <dd>Convert a number to a percentage. To convert back to decimal, press <code>=</code>.</dd>

  <dt><dfn>
  M-% *</dfn></dt>
  <dd>Compute the number that is the percent of another number; for example, <code>68 &lt;RET&gt; 25 M-% *</code> computes 17 because 17 is 25% of 68.</dd>

  <dt><dfn>
  / c %</dfn></dt>
  <dd>Compute the percentage one number is of another number; for example, <code>17 &lt;RET&gt; 68 / c %</code> computes 25% because 17 is 25% of 68.</dd>

  <dt><dfn>
  b %<br>
  x percent-change<br>
  M-x calc-percent-change<br>
  'relch(NUMBER1, NUMBER2) &lt;RET&gt; c %</dfn></dt>
  <dd>Compute the percentage change from one number to another; for example, <code>17 &lt;RET&gt; 68 b %</code> computes 300% because in order to get from 17% to 68%, you need to add 300% of 17 to 17. Percentage change is calculated as (NUMBER2 - NUMBER1) / NUMBER2.</dd>

  <dt><dfn>
  b a<br>
  x and<br>
  M-x calc-and</dfn></dt>
  <dd>Compute the bitwise AND of two numbers.</dd>

  <dt><dfn>
  b o<br>
  x or<br>
  M-x calc-or</dfn></dt>
  <dd>Compute the bitwise OR of two numbers.</dd>

  <dt><dfn>
  b x<br>
  x xor<br>
  M-x calc-xor</dfn></dt>
  <dd>Compute the bitwise XOR of two numbers.</dd>

  <dt><dfn>
  b n<br>
  x not<br>
  M-x calc-not</dfn></dt>
  <dd>Compute the bitwise NOT of two numbers.</dd>

  <dt><dfn>
  b d<br>
  x diff<br>
  M-x calc-diff</dfn></dt>
  <dd>Compute the bitwise difference of two numbers.</dd>

  <dt><dfn>
  b l<br>
  x lshift-binary<br>
  M-x calc-lshift-binary</dfn></dt>
  <dd>Shift a number left by one bit.</dd>

  <dt><dfn>
  b r<br>
  x rshift-binary<br>
  M-x calc-rshift-binary</dfn></dt>
  <dd>Shift a number right by one bit.</dd>

  <dt><dfn>
  b t<br>
  x rotate-binary<br>
  M-x calc-rotate-binary</dfn></dt>
  <dd>Rotate a number one bit to the left. The leftmost bit is dropped off the left and shifted in on the right.</dd>
</dl>
