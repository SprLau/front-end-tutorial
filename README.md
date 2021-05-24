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

### Verse 2 - What is Git, Seriously?

Git’s slogan is:

**"Everything is local."**

And it is not bluffing.

You can regard it as if there is a remote servant who is handling your codes, and you can always tell the guy to store or fetch your codes. So can your friends, unless they are not permitted by you. Sounds like a bank or something, huh? This is good, because you can collaborate while don’t have to worry about losing your codes somehow.

There are several frequently used **Git** commands:

```bash
git add .
git commit -a -m "some information to mark this commit"

git push -u origin master#branch

git pull
```

First two always work together, they are to commit local changes but without pushing them. The third is to push your local changes to the remote server, where you can store your code and fetch from. The fourth is to pull from the remote server, which you can update your local codes to the remote server.

Though all of these we’ve discussed, there is definitely still a lot that we cannot quite understand, like `-a`, or `origin`, `master`. But don’t worry, we’ll get into them later on in our practices.
