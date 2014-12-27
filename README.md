TODO: add a table of contents (it would be nice if GitHub's markdown auto-generated this...)

# Legal Stuff

You do **not** have permission to make any money off of this document or any version of it (either in its entirety or in parts), claim any credit for this document or any version of it (either in its entirety or in parts), or modify this document or any version of it.

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


# Starting Emacs

If you installed Emacs with X support, then invoking Emacs with <code>emacs &</code> will launch graphical Emacs and invoking Emacs with <code>emacs -nw</code> will launch terminal Emacs. If you installed Emacs without X support, then invoking Emacs with either <code>emacs</code> or <code>emacs -nw</code> will launch terminal Emacs.

The recommended way to use Emacs is to start it just once and do all your editing in the same Emacs session rather than starting a new instance each time you want to edit a file.

Additionally, you can tell Emacs to load one or more specified files after launching:

<dl>
  <dt><dfn>emacs FILENAME</dfn></dt>
  <dd>Launch Emacs and then load the specified file.</dd>

  <dt><dfn>emacs +LINE_NUMBER FILENAME</dfn></dt>
  <dd>Launch Emacs, load the specified file, and then move point to the specified line number in that file.</dd>

  <dt><dfn>emacs +LINE_NUMBER:COLUMN_NUMBER FILENAME</dfn></dt>
  <dd>Launch Emacs, load the specified file, and then move the cursor to the specified column number on the specified line number in that file.</dd>
</dl>

You'll only see the last file that you specified; however, the other files will also have been loaded and are available in the buffer list.

The optional <code>+LINE_NUMBER:COLUMN_NUMBER</code> applies only to the next file specified.


# Most Important Things to Know First

The most important things to know first are knowing how to quit, cancel, undo, close, switch and close buffers, and get help, and before you can know that, you need to know how to invoke commands in Emacs.

To invoke a command in Emacs:

1. You can use a key sequence (aka keyboard shortcut, key binding, or key for short).
2. Or you can call the command by name.

Some commands are (or can be) disabled, which means that you'll be asked for confirmation when you try to invoke them. The usual reason for disabling a command is that some commands are potentially confusing for beginning users.

You'll notice that some commands are grouped by similar prefix keys or prefix or suffix names; for example, a lot of window-based key sequences start with <code>C-x 4</code> and a lot of frame-based commands start with <code>C-x 5</code>.


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
* <code>C-M-v</code> is supposed to invoke <code>scroll-other-window</code>, but instead it pastes text. This was only a problem for me in my terminal. This is because I'm using the rxvt-unicode clipboard extension from [urxvt-perls](https://github.com/muennich/urxvt-perls), which binds <code>C-M-v</code> to paste_escaped by default. To resolve the conflict, you can define a different key binding for paste_escaped in your ~/.Xresources file: <code>URxvt.keysym.CHANGEME:perl:clipboard:paste_escaped</code>. Don't bind to <code>C-M-S-v</code> because that will conflict with <code>scroll-other-window-down</code>. Another solution you could do is remove the <code>paste_escaped</code> elsif in the on_user_command subroutine in /usr/lib\*/urxvt/perl/clipboard, if paste_escaped is something that you don't use; it's not something that I use, so it's the solution that I went with.
* <code>C-M-s</code> is supposed to invoke <code>isearch-forward-regexp</code>, but instead it invokes a urxvtperl scrollback search. This was only a problem for me in my terminal. I never use it, so I simply removed "searchable-scrollback" from the URxvt.perl-ext-common line in my ~/.Xresources.
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

<dl>
  <dt><dfn>C-q C-S-2</dfn></dt>
  <dd>Null (caret notation: ^@; C escape code: \0).</dd>

  <dt><dfn>C-q C-g</dfn></dt>
  <dd>Bell (caret notation: ^G; C escape code: \a).</dd>

  <dt><dfn>C-q C-h</dfn></dt>
  <dd>Backspace (caret notation: ^H; C escape code: \b).</dd>

  <dt><dfn>C-q C-i</dfn></dt>
  <dd>Horizontal tab (caret notation: ^I; C escape code: \t).</dd>

  <dt><dfn>C-q C-j</dfn></dt>
  <dd>Line feed (caret notation: ^J; C escape code: \n).</dd>

  <dt><dfn>C-q C-k</dfn></dt>
  <dd>Vertical tab (caret notation: ^K; C escape code: \v).</dd>

  <dt><dfn>C-q C-l</dfn></dt>
  <dd>Form feed (caret notation: ^L; C escape code: \f).</dd>

  <dt><dfn>C-q C-m</dfn></dt>
  <dd>Carriage return (caret notation: ^M; C escape code: \r).</dd>

  <dt><dfn>C-q C-[</dfn></dt>
  <dd>Escape (caret notation: ^[; C escape code: \e).</dd>
</dl>

If you want to insert ASCII control characters literally, then look up their value in caret notation (the caret stands for the Ctrl key); for example, end of file is ^D, which means C-d, so to insert that control character literally, type <code>C-q</code> to quote the following character, and then type <code>C-d</code> as the character you want to quote and insert literally. To find the caret notation for ASCII control characters, search for something like "C0 control codes."

Caret notation is used for the 33 ASCII control characters. The notation consists of a caret (^) followed by a character in the ASCII range from ? to \_ (look at an ASCII table); this digraph stands for the ASCII control character that has the numerical equivalent to the characters's position in the range from ? to \_: ? is -1 (for ASCII control character 127), @ is 0 (for ASCII control character 0), A is 1, Z is 26, \[ is 27, and \_ is 31. For the letters, it's easy, because it's the position in the alphabet (A is the first, M is the 13th letter, Z is the 26th letter). ASCII control character 10 is the line feed (\\n) character. The 10th letter of the alphabet is J, so the caret notation for \\n is ^J. ASCII control character 27 is the escape (\\e) character. The first character after Z ("letter 27") in the ASCII table is \[, so the caret notation for escape is ^\[.


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

  <dt><dfn>M-x kill-emacs</dfn></dt>
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

The minibuffer is where Emacs commands read complicated arguments, such as file names, buffer names, command names, or Lisp expressions. When the minibuffer is in use, it appears in the echo area with a cursor. The minibuffer starts with a prompt string, which states what kind of input is expected. The prompt string usually ends with a colon and stands out from the input text. Sometimes, the prompt shows a default argument, inside parentheses before the colon. This default will be used as the argument if you just type <code>&lt;RET&gt;</code> without entering anything else (in other words, when you submit an empty string). The minibuffer doesn't have a mode line.

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
  <dt><dfn>C-x &lt;ESC&gt; &lt;ESC&gt;</dfn></dt>
  <dd>
<p>Turn the previous command into a Lisp expression and then enter a minibuffer initialised with the text for that expression. If you type just &lt;RET&gt;, that repeats the command unchanged. You can also change the command by editing the Lisp expression before you execute it.</p>

<p>A numeric argument to <code>C-x &lt;ESC&gt; &lt;ESC&gt;</code> specifies which command to repeat; 1 means the last one, 2 the previous, and so on.</p>

<p>Once inside the minibuffer for <code>C-x &lt;ESC&gt; &lt;ESC&gt;</code>, you can use the usual minibuffer history commands to move through the history list.</p>
  </dd>

  <dt><dfn>M-x list-command-history</dfn></dt>
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
  
  <dt><dfn>M-x set-frame-name &lt;RET&gt; FRAME_NAME</dfn></dt>
  <dd>Rename the selected frame.</dd>

  <dt><dfn>M-x select-frame-by-name &lt;RET&gt; FRAME_NAME</dfn></dt>
  <dd>Select the specified frame by its name.</dd>

  <dt><dfn>M-x fit-frame-to-buffer</dfn></dt>
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

<p>You cannot use the command while in the minibuffer.</p>
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

  <dt><dfn>M-x maximize-window</dfn></dt>
  <dd>Make the selected window as tall and wide as possible.</dd>

  <dt><dfn>M-x minimize-window</dfn></dt>
  <dd>Make the selected window as short and narrow as possible.</dd>

  <dt><dfn>
  C-x +<br>
  M-x balance-windows</dfn></dt>
  <dd>Even out the heights of all the windows in the selected frame, making their sizes as similar as possible.</dd>

  <dt><dfn>M-x balance-windows-area</dfn></dt>
  <dd>Adjust the area of all the windows in the selected frame, making their sizes as similar as possible.</dd>

  <dt><dfn>M-x fit-window-to-buffer</dfn></dt>
  <dd>Adjust the selected window's height to display its buffer's contents exactly (if it can fit in the height of the frame); otherwise, adjust the selected window's height to the height of the frame.</dd>

  <dt><dfn>M-x delete-windows-on &lt;RET&gt; BUFFER_NAME</dfn></dt>
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

  <dt><dfn>C-u C-x C-b</dfn></dt>
  <dd>Display only a list of the existing buffers that are visiting files.</dd>

  <dt><dfn>
  C-x C-q<br>
  M-x read-only-mode</dfn></dt>
  <dd>Toggle the read-only status of a buffer.</dd>

  <dt><dfn>M-x rename-buffer &lt;RET&gt; BUFFER_NAME</dfn></dt>
  <dd>Rename the current buffer to BUFFER_NAME.</dd>

  <dt><dfn>M-x rename-uniquely</dfn></dt>
  <dd>Rename the current buffer by appending a unique number to its current name.</dd>

  <dt><dfn>
  C-x k BUFFER_NAME<br>
  M-x kill-buffer &lt;RET&gt; BUFFER_NAME</dfn></dt>
  <dd>Kill buffer BUFFER_NAME. If you don't specify a name and just immediately press <code>&lt;RET&gt;</code>, then the current buffer will be killed by default.</dd>

  <dt><dfn>M-x kill-some-buffers</dfn></dt>
  <dd>Offer to kill each buffer, one by one.</dd>

  <dt><dfn>M-x kill-matching-buffers</dfn></dt>
  <dd>Offer to kill all buffers matching a regular expression.</dd>

  <dt><dfn>M-x clean-buffer-list</dfn></dt>
  <dd>
<p>By default, kill any unmodified buffers that haven't been displayed in the past three days.</p>

<p>If you enable Midnight mode (<code>M-x midnight-mode</code>), then <code>clean-buffer-list</code> will be run automatically for you every midnight.</p>
  </dd>
</dl>

Enabling Iswitchb mode (<code>M-x iswitchb-mode</code>) makes it much easier to switch buffers. It redefines what <code>C-x b</code>, <code>C-x 4 b</code>, and <code>C-x 5 b</code> do. When you enter one of those commands, they will prompt you with a list of possible buffer names. You can do one of two things: you can either start typing the name of the buffer you want to switch to it, until it appears first in the list, or you can press <code>C-s</code> (rotate left) or <code>C-r</code> (rotate right) until the buffer you want to switch to appears first in the list. Once the buffer you want to switch to appears first in the list (or is the only buffer listed), then press <code>&lt;RET&gt;</code>.

Narrowing means focusing in on some portion of the buffer, making the rest temporarily inaccessible. When you have narrowed down to a part of the buffer, that part appears to be all there is. You can't see the rest, you can't move into it (motion commands won't go outside the accessible part), you can't change it in any way; however, it is not gone, and if you save the file, all the inaccessible text will be saved. The word "Narrow" appears in the mode line whenever narrowing is in effect.

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
  <dd>Narrow buffer down to the current defun.</dd>

  <dt><dfn>
  C-x n w<br>
  M-x widen</dfn></dt>
  <dd>Widen the current buffer (make the entire buffer accessible again).</dd>

  <dt><dfn>
  C-x =<br>
  M-x what-cursor-position</dfn></dt>
  <dd>Display information about where point is relative to the entire buffer (not just the narrowed region). The numbers in angle brackets are the first line number in the narrowed region (relative to the entire buffer) and the last line number in the narrowed region (also relative to the entire buffer).</dd>
</dl>


# Modes

Modes alter the functionality of buffers; for example, by introducing new commands and variables, altering key sequences, or altering various variables. Major modes tailor a buffer for a specific type of task.

Major modes are mutually exclusive; each buffer has one and only one major mode at any time. Minor modes are optional features which you can turn on or off, not necessarily specific to a type of file or buffer. Minor modes are independent of one another, and of the selected major mode.

The least specialised major mode is called "Fundamental mode". This mode has no mode-specific redefinitions or variable settings, so that each Emacs commands behaves in its most general manner, and each user option variable is in its default state.

Modes are either major or minor. Minor modes are either buffer-local (can be selectively enabled on a per-buffer basis) or global (always applies to all buffers).

Each mode is associated with a mode command, whose name consists of the mode name followed by "-mode". To toggle a minor mode (if it's enabled, then disable it; if it's disabled, then enable it) or switch to a major mode, you simply invoke its mode command: <code>M-x MODENAME-mode</code>. Since a buffer must have a major mode and can't have more than one major mode, you can't toggle a major mode on and off. Enabling a major mode disables the previous major mode. If you don't want to use the current major mode, then switch to a different one.


# Files

When editing a file in Emacs, you're actually working with a copy of the file: Emacs inserts the contents of the file into a buffer, which is called "visiting the file." Your changes last only as long as the Emacs session. To keep your changes permanently, you must save the buffer back into the file.

Each buffer is associated with a different default directory (typically the directory of the file that's being visited in the buffer). Entering a file name without a directory specifies a file in the default directory. Entering a file name with a relative path specifies a file relative to the default directory. When you create a new buffer that is not visiting a file, its default directory is usually copied from the buffer that was current at the time. To see the default directory, type <code>M-x pwd</code>. To set the default directory explicitly, type <code>M-x cd</code>.

Saving a buffer in Emacs means writing its contents back into the file that the buffer is visiting.

A backup file records the contents that a file had before the current editing session. The first time you save a file from a buffer, a backup file will automatically be created for you consisting of the contents of the file before your changes. The backup will be overwritten next time you visit the file and then save. A backup filename will appear as <code>FILENAME~</code>, <code>%FILENAME%~</code>, or <code>FILENAME.~NUMBER~</code>. To prevent excessive consumption of disk space, Emacs will automatically keep the first few backups and the latest few backups, and delete any in between, each time a new backup is made.

Auto saving is the practice of periodically saving the contents of an Emacs buffer in a separate file, so that the information will be preserved if the buffer is lost due to a system error or user error. By default, when visiting a file, Emacs will auto-save the buffer into a separate file after 300 or more characters have been typed in the buffer or after Emacs has been idle for 30 seconds. Emacs will also automatically auto save whenever it gets a fatal error. To explicitly auto save a buffer, type <code>M-x do-auto-save</code>. The auto-save file name is of the form <code>#FILENAME#</code> or <code>#FILENAME#UNIQUESTRING</code>. When you delete a substantial part of the text in a large buffer, auto save turns off temporarily in that buffer. To reenable auto-saving after this happens, save the buffer with <code>C-x C-s</code>, or use <code>C-u 1 M-x auto-save-mode</code>. A buffer's auto-save file is deleted when you save the buffer of the visited file. Changing the visited file name with <code>C-x C-w</code> or <code>set-visited-file-name</code> renames any auto-save file to go with the new visited name. If you want to recover a file from an auto save file, then do <code>M-x recover-file &lt;RET&gt; FILENAME &lt;RET&gt;</code>, where FILENAME is the official file's name, not the auto save file's name; note that this alone doesn't recover the file on disk. To recover the file on disk, you should save the buffer (after you invoke <code>M-x recover-file</code>). If Emacs or the computer crashes, you can recover all the files you were editing from their auto save files with the command <code>M-x recover-session</code>.

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

<p>The TRAMP package (comes with Emacs and works right out of the box) provides a way to edit remote files (files that are stored on a system other than your own) or edit files as another user (the package also allows you to do other things, but the gist of the package is that it allows you to do things remotely). All you have to do is prepend some stuff to the file name you want to visit: <code>/METHODNAME:USERNAME@HOST.DOMAINNAME#PORTNUMBER:/PATH/TO/FILE</code>. Only the initial forward slash ('/'), host, colon (':'), and filename are required. Note that the host can be specified by name, IPv4 address, or IPv6 address. If you use IPv6, then you must surround the IPv6 address with square brackets. There are many possibilities for method name: rsh, ssh, telnet, su, sudo, sshx, krlogin, ksu, plink, plinkx, rcp, scp, sftp, rsync, scpx, scpc, rsyncc, pscp, psftp, fcp, ftp, and smb. TRAMP is supposed to make editing a remote file seem just like editing a local file, so all the commands you normally you use for local files can also be used with remote files.</p>

<p>In graphical Emacs, if you visit an image, the image will be displayed in Emacs. You can type <code>C-c C-c</code> to toggle between viewing the image and viewing the image's file contents. If the image is animated, then <code>&lt;RET&gt;</code> can toggle animation on and off.</p>

<p>In graphical Emacs, if you visit a PDF, the PDF will be displayed in Emacs. You can type <code>C-c C-c</code> to toggle between viewing the PDF and viewing the PDF's file contents.</p>
  </dd>

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

  <dt><dfn>M-x set-visited-file-name &lt;RET&gt; FILENAME</dfn></dt>
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

  <dt><dfn>M-x make-directory &lt;RET&gt; DIRNAME</dfn></dt>
  <dd>Create a new directory using the specified name.</dd>

  <dt><dfn>M-x delete-file &lt;RET&gt; FILENAME</dfn></dt>
  <dd>Delete the specified file.</dd>

  <dt><dfn>M-x delete-directory &lt;RET&gt; DIRNAME</dfn></dt>
  <dd>Delete the specified directory.</dd>

  <dt><dfn>M-x copy-file &lt;RET&gt; OLD &lt;RET&gt; NEW</dfn></dt>
  <dd>Copy the specified file into a file named NEW.</dd>

  <dt><dfn>M-x copy-directory &lt;RET&gt; OLD &lt;RET&gt; NEW</dfn></dt>
  <dd>Copy the specified directory into a directory named NEW.</dd>

  <dt><dfn>M-x rename-file &lt;RET&gt; OLD &lt;RET&gt; NEW</dfn></dt>
  <dd>Rename the specified file from OLD to NEW. If NEW is a directory name, then use that directory, and move OLD into it.</dd>

  <dt><dfn>M-x make-symbolic-link &lt;RET&gt; TARGET &lt;RET&gt; LINKNAME</dfn></dt>
  <dd>Create a symbolic link named LINKNAME, which points to TARGET.</dd>

  <dt><dfn>
  C-x i<br>
  M-x insert-file</dfn></dt>
  <dd>Insert a copy of the contents of the specified file into the current buffer at point, leaving point unchanged, but moving mark to the end of the inserted contents.</dd>

  <dt><dfn>M-x write-region</dfn></dt>
  <dd>Copy the contents of region into the specified file.</dd>

  <dt><dfn>M-x append-to-file</dfn></dt>
  <dd>Append the contents of region to the end of the specified file.</dd>

  <dt><dfn>
  M-x set-file-modes<br>
  M-x chmod</dfn></dt>
  <dd>Change the file modes (file permissions) of the specified file. Specify the arguments in the same format that chmod would expect.</dd>

  <dt><dfn>
  </dfn></dt>
  <dd></dd>

  <dt><dfn>
  </dfn></dt>
  <dd></dd>

  <dt><dfn>
  </dfn></dt>
  <dd></dd>

  <dt><dfn>
  </dfn></dt>
  <dd></dd>
</dl>



# Completion

TODO


## Minibuffer

TODO


# Customisation


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
