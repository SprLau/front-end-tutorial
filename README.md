# Front End Tutorial

## Chapter 1 HTML

### Verse 1 - Environment Preparation

> MacOS

Make sure `vim` is available, typically MacOS is equipped with this code editor before hitting the store, so you don’t have to manuelly install it.

Run this to check availability:

```bash
vim
```

You should be able to see a welcome interface.

To edit in **Vim**, input `i` to invoke insert mode, in which you can finally edit the code. Notice this, in **Vim**, originally the mouse is nullified, if you try to activate mouse functions(this is optional), create a file named `~/.vimrc` to permanently modify settings for **Vim**. Step by step goes like this:

> First we create `~/.vimrc` via **Vim**
>
> ```bash
> vim ~/.vimrc
> ```

> Then we insert some lines, besides activating mouse functions, we can also do more to make the interface more friendly.
>
> ```bash
> set nu			# This is to show line numbers
> set mouse=a		# This is to activate mouse functions
> set sw=4		# The following lines are to set tab length 4
> set ts=4
> set sts=4
> ```

> Done! Let’s save our changes and quit. Notice, this command receiver is invoked by `:`, only when we input `:`, such commands can be responded.
>
> So actaully you cannot simply copy and paste the following line, you are supposed to first input `:`, then input `w` and `q` in order, where `w` means “save” and `q` means “quit”.
>
> ```
> :wq
> ```

After this, let’s modify our `~/.bash_profile`, which could permanently store some frequently-used tools. Run this to edit the file:

```bash
vim ~/.bash_profile
```

After entering into the file, use what we have learnt, insert the following lines:

```bash
alias chrome="/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome"
alias vscode="/Applications/Visual\ Studio\ Code.app/Contents/MacOS/Electron"
```

Make sure you have already installed **Chrome browser** and **VSCode code editor** in advance. Besides, pathes of the two may vary on different computers, if they are different with mine, change what after `=` accordingly.

Try to verify correctness by running these in `Terminal`:

```bash
chrome
vscode
```

Expectedly, **Chrome browser** and **VSCode code editor** will open immediately.

------

NOW, all the work pertaining environment preparation have been done.



