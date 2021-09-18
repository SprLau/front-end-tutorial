# Front End Tutorial

[toc]

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

### Verse 3 - Write your first `.html`

HTML is kind of a programming language, but it is plain-speaking.

Let’s look at this example code:

```html
<!DOCTYPE html>

<html>
    <head>
        <title>SprLau's Web Design Learning</title>
    </head>

    <body>
        <h1>About Me</h1>
        <p>I am a junior year student majoring in computer science.</p>
        <p>To know more about me, please search on <a href="http://www.baidu.com">Baidu</a>.</p>
    </body>
</html>
```

Now let’s dissect it…

#### `<!DOCTYPE html>`

The `<!DOCTYPE>` declaration represents the document type, and helps browsers to display web pages correctly.

It must only appear once, at the top of the page (before any HTML tags).

The `<!DOCTYPE>` declaration is not case sensitive.

The `<!DOCTYPE>` declaration for HTML5 is

```html
<!DOCTYPE html>
```

#### `<html></html>`

The HTML document itself begins with `<html>` and ends with `</html>`.

#### `<head></head>`

This shows the title in the bar.

#### `<body></body>`

The visible part of the HTML document is between `<body>` and `</body>`.

#### `<h1></h1>`

This declares a Size 1 header, quite bold.

#### `<p></p>`

This declares a paragraph, a plain text.

#### `<a href></a>`

This declares a link, any link, on which click to visit.

> The real output should be like this:
>
> ![1](img/1.png)
>
> Try to match every element on this page to the code.

***Try yourself!!!***

### Verse 4 - What if I want to add some pics?

```html
<img src="ROUTE/FILE_NAME" alt="TEXT_SHOWN_WHEN_IMG_BROKEN" width="WIDTH" height="HEIGHT">
```

This code above declares an image added to your website. Based on the previous code, let’s implement by adding an image:

```html
<!DOCTYPE html>

<html>
    <head>
        <title>SprLau's Web Design Learning</title>
    </head>

    <body>
        <h1>About Me</h1>
        <p>I am a junior year student majoring in computer science.</p>
        <p>To know more about me, please search on <a href="http://www.baidu.com">Baidu</a>.</p>
        <p>This is my favorite cat:</p>
        <img src="./../img/cat.jpg", alt="Punggaw Cat!!!", width="300", height="100">
    </body>
</html>
```

> The page should be look like this:
>
> ![2](img/2.png)

Quite weird, right? Why Punggaw Cat is so flat??? So, if you want to keep the **actual size** of a pic, don’t manually set `width` and `height`:

```html
<!DOCTYPE html>

<html>
    <head>
        <title>SprLau's Web Design Learning</title>
    </head>

    <body>
        <h1>About Me</h1>
        <p>I am a junior year student majoring in computer science.</p>
        <p>To know more about me, please search on <a href="http://www.baidu.com">Baidu</a>.</p>
        <p>This is my favorite cat:</p>
        <img src="./../img/cat.jpg", alt="Punggaw Cat!!!">
    </body>
</html>
```

> ![3](img/3.png)
>
> The size is normal. So big… I can’t even cut the whole page.

### Verse 5 - What is an *Attribute*?

Consider this:

**“Anything behand the first word after < is an attribute.”**

For instance, recall this: `<img src="...", alt="...", width="...", height="...">`

Here `img` is the first word after <, so `src, alt, width, height` are all attributes.

`<p></p>` has attribute options as well, the most frequent one among them is **the style attribute**:

```html
<p style="color:blue;">My favorite color is blue.</p>
```

Without the style attribute, it is just a plain text; with the style attribute, the text is blue in color.

> ![4](img/4.png)

You can also declare a color with its hex code, like `#FFFFFF`, where `#` identifies a hex code.

In this way, you can declare colors in a more accurate way, which is also strongly recommeded.

```html
<p style="color:#B4C5D8;">My favorite color is iceberg blue.</p>
```

> ![5](img/5.png)

You can also add a *title* attribute to a `<p></p>`:

```html
<p title="My Favorite Color" style="color:#B4C5D8;">My favorite color is iceberg blue.</p>
```

After you add this, the effect is not so visible as the precious ones. If you want to see the title of an element, move your mouse to the element and hold there for seconds, then the title reveals:

![6](img/6.png)

#### Summary

All HTML elements can have **attributes**:

- The `href` attribute of `<a>` specifies the URL of the page the link goes to
- The `src` attribute of `<img>` specifies the path to the image to be displayed
- The `width` and `height` attributes of `<img>` provide size information for images
- The `alt` attribute of `<img>` provides an alternate text for an image
- The `style` attribute is used to add styles to an element, such as color, font, size, and more
- The `lang` attribute of the `<html>` tag declares the language of the Web page
- The `title` attribute defines some extra information about an element
