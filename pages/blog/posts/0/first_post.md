# Well... I made a website
Hey! Welcome to the introductory post on my website. I wanna kinda give an overview of this site, mostly to talk about everything that went into making it. I made this all by hand, but I couldn't have done it without some already-existing and very awesome libraries, frameworks, and lots of other cool stuff that other people made and lets people use for free.

I made this site myself for a lot of reasons, but the chiefiest among them was that I wanted to get acquainted with web development. I've been working on some internal web apps while working at Qualcomm, and it kind of piqued my interest a bit. So with a little GitHub and a lotta JavaScript, I made the site you see before you.

## Audience
So before I get started, this post will probably have a good amount of technical jargon that won't make a lot of sense to people who don't write software. Since I know I might have people reading this that don't necessarily understand that technical stuff as well as others (Hey Mom!!), I'll break down each section into a Technical and Non-Technical portion, just to make it easier.

# So, how does this site work?
Here I'll list everything I used in making this site. 

## GitHub Pages
This site wouldn't be possible without the awesome people who make GitHub. Thanks to [GitHub Pages](https://pages.github.com/), I can host this static site for free! 

### If you don't speak computer
#### Servers 
So, on a very basic level, the internet and its websites are just a collection of interconnected computers that know each others name, called servers. When you go to [google.com](http://google.com), your internet browser knows which server google.com is, and it goes to that computer and says "Hey, someone wants to look at your site, can you show it to them?". Then Google's servers (they have literally millions) connect you to their fabulous search engine. 

Well, having a server connected to the internet and configured to generate websites all the time cost money. Some sites, like Google or Amazon or Facebook, need super fast ones that are prepared to do a lot of work to find your latest Google search or decide which stories to post on your News Feed. But a site like mine doesn't need anything too special. 

#### Where GitHub comes in
Luckily, there's this company called [GitHub](https://github.com/) that is centered around storing files online. All I have to do is store the files I use for this site on there, follow the steps on their [GitHub Pages](https://pages.github.com/) page, and voila! Now you're looking at my site.

### If you speak computer
#### It's just  GitHub repo!
GitHub Pages is great. They host static sites for free, all you need to do is store it in one of your GitHub repos. You can see the repo for my site [here](https://github.com/migreva/migreva.github.io). Because it's a static site, there's no code execution or anything, so it's all HTML, CSS, and JS. So if you want to still use PHP, you can just write scrips to generate all the HTML beforehand and then commit those changes to your branch. That's what I do (but I use Python cause its way better than PHP).

It also encouraged me to do a lot of stuff in JavaScript. Because everything on the site has to be static and un-changing, it caused me to have to write JavaScript that is flexible based on the input that it is given. As you see, there are no deeper URLs on this site, only hashes like [http://migreva.com/#blog](http://migreva.com/#blog). This is because all the site's navigation is in JavaScript, which I'll get to later. While this has it's limitations, it's been a good JS learning experience.


## JavaScript Navigation

### If you don't speak computer
####What is HTML?
HTML, which is the computer language behind how every website displays their content, is inherently static, meaning HTML itself does not have the power to change what it looks like. If a website shows up with a blue background, it will stay a blue backgound until it is changed by an outside source. On way to do this is a computer language called [JavaScript](http://en.wikipedia.org/wiki/JavaScript). JavaScript is in every major web browser and plays a huge role in almost everything you do online, you just didn't know it yet.

Many websites have a lot of HTML - represented by individual HTML files on a computer - that go into their sites. For example, the [Twitter homepage](https://twitter.com/) is a different HTML file than my [Twitter profile](https://twitter.com/migreva). When you click on a link, it usually goes and tells a computer to get a different HTML file. I designed my site a little differently.

#### How JavaScript helps
My site was designed to be one HTML file with all the navigation and different pages and animations to be done in JavaScript. I wanted to be able to learn JavaScript, which at the time was a language I didn't know, and I wanted to make the look and feel of the site as smooth as possible. It was a large undertaking, a lot of code was written, but it was quite enjoyable.

### If you speak computer
This entire site's navigation is run on JavaScript. The whole website is one page that changes based on input - intercepting click handlers and reading href attrbutes. I did this for a couple reasons, the main one being I didn't really know JavaScript that well and the only way to really learn a language is by working on a project that uses that language. The second reason is that I had some cool animations in mind (some that didn't make the cut) that wouldn't have been possible if the navigation worked off links.

## SASS
The hompage for [SASS](http://sass-lang.com/) markets it as "CSS with Superpowers", and that's exactly what it is.

### If you don't speak computer
In the last section, we talked about how JavaScript is what can change HTML to make them do cool stuff that websites wouldn't otherwise be able to do. There's another language that helps make modern webpages so beautiful and awesome, and that's called Cascading Style Sheets, or [CSS](http://en.wikipedia.org/wiki/Cascading_Style_Sheets). 

#### The languages of the internet
Let me first define the three major languages of web development - HTML, JavaScript, and CSS - and then I can talk about how CSS helps make awesome wesbites.

* HTML - How the websites is **laid out**. It says that the title goes at the top of the page, and the footer goes below it
* JavaScript - How to be able to **change** the HTML.
* CSS - How to define the **style** of the wesbite (CSS = Cascading **style** sheets)

#### CSS is the style
CSS is how the website is **styled**, but what does that mean? 

Well, let's say you're making a website for the Detroit Red Wings, and you know you're going to have a lot of red on the site, cause - uh - they're the Red Wings. Well, instead of going to each specific thing on the page that you want to be the color red, and explcitly saying "Hey, you, be the color red", CSS allows you to say: "Okay, anything I name 'Red Thing' should be called red". Then, when you make a new thing on your Detroit Red Wings wesbite that you want to be red, you call it a Red Thing and then it knows it has to be red.

I hope that made sense. Really, I said all of that to say this: CSS is awsome in a lot of ways, but sucks in a lot of other ways. So enough people got annoyed with stuff in CSS that they said "Okay, enough. I wanna do it my way", and they made their own way, and it's pretty awesome and easy and makes it easier to make websites. 

### If you speak computer
#### CSS - "Meh"
If you've ever worked on a website, you've worked with CSS. And if you've worked with CSS, you'll notice that it does a lot of great stuff that enables you to make a good looking website - if you know how to use it right. But if you've worked with CSS you'll also notice it has its limitations. You can't store variables; there's no inheritance built into the language, so you find yourself repeating a lot of code; in any event, anyone who uses CSS can admit that it sometimes makes you go "meh".

Oh yeah, and don't lie, everytime you write some code like this you die a little inside.

> -webkit-border-radius: 10px;

> -moz-border-radius: 10px;

> -ms-border-radius: 10px;

> border-radius: 10px;

#### SASS - "Yay"
Well, SASS does away with a lot of that. They have a [SASS Basics page](http://sass-lang.com/guide) that goes over just a couple of the basic things that, honestly, if you used it would cut your working css code base in half. So if CSS makes me "Meh" then SASS makes me "Yay".

In addition to having some cool code that you can write, the way the [import functionailty](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#import) works allows you to compile all you SASS into one base.css file that you can serve up all over your site. I learned very early on the need to have one master css file, and how the CSS import functionality can actually be [horrible for performance](http://stackoverflow.com/a/10037064/1337683). Luckily, because of the way sass converts to CSS (see next section), it allows you to develop in separate files to make it easier for development (what are we, animals?), while letting your site serve up just the one file to the user.

#### SASS Compiling and CodeKit
The one drawback of SASS is that even though it is a great language, browsers still only know how to read .css files. So when you write SASS, you have to convert it to CSS before it can actually be useful. They have a [command line tool](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#syntax) that provides for convenient ways to convert .scss to .css files. 

If you're not into that kind of things - command lines aren't for everyone. After all, it is 2014 - there's a great Mac App I use called [Code Kit](http://stackoverflow.com/a/10037064/1337683) that watches the files for you and auto-converts them every time you save a SASS file. It'll also minify your JavaScript for you, which is nice.

#### Bourbon - but not the drink
Yes, alcohol was used in the making of this website. However, another type of Bourbon was used, the [SASS mixin library](http://bourbon.io/) that does away with vendor prefixes! The days of typing `-webkit` a trillion times your files are over, my friend. Cause nothing's worse than having to adapt to web standards

## Require.js
Without the great folks behind [Require.js](http://requirejs.org/), this blog post would have shown up to you possibly hundreds of milliseconds later than it did.

### If you don't speak computer
Well, if you've gotten this far you have to know about JavaScript, right? Well, since my site is so chock-full of JavaScript files, that means when this site loads, each one of those JavaScript files is loaded one by one, which means that the website takes slightly longer to load for each additional file I have.

For the most part, this doesn't really matter; the time it takes to load this the JavaScript for this website is almost negligble to by human standards. When it really comes into play is for large companies, where studies have shows milliseconds in additional page loading times can result in sometimes rather astounding revenue loss. While I have no revenue to lose, it's good practice to do something like this. The more efficient the better!

### If you speak computer
If you have a personal website like mine, the latency involved in loading the JavaScript for this site *shouldn't* deter visitors. I'm not Google, where a millisecond-of-a-millisecond in page loading means a drop in half a billion dollars in revenue. I am, however, still an engineer and care very deeply about how fast my site loads, even if the human eye can't even detect it. That's why I'm so glad I found require.js.

#### Load all you JavaScript at once
Require.js's main selling point, I think, is how easy it is to load all your JavaScript files all at once. This is the only line needed to load all 5 of my JavaScriptFiles ([source](http://requirejs.org/docs/api.html#jsfiles)):

    <script data-main="scripts/main.js" src=./scripts/require.js ></script>

Within my `main.js` file I import all of the JavaScript files I've created, which is actually done by passing them as arguments to the `require()` function, and by what I assume is black magic that is done by require.js, my files are loaded all at once. 

#### OO Encouragement
If you've ever learned JavaScript, you know that it is not an Object Oriented language by design. Because of this, a lot of beginners (i.e. me) tend to write large JavaScript files that end up being just function after function, with a couple that run in a $(document).ready() function. However, as I began to learn the language more - most of that being in my work at Qualcomm - I learned about some tricks that people use to make the lanuage appear OO-based, my favorite of which is [closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Closures).

Another great thing that require.js does is almost strongarms you into using module-based programming. Each one of the JavaScript files that you want to be imported via require.js needs to be passed in as a parameter to the function in the aforementioned `main.js` script. Here is the entire contents of my version of `main.js`.


    require(["index", "nav", "helpers", "lwf", "fetch", "constants"], function(){

    	fetch = new Fetch();
    	fetch.init();
    
    	var nav = new Nav();
    	nav.init();
    
    	helpers = new Helpers();
	};

That loads the following JavaScript files: index.js, nav.js, helpers.js, lwf.js, fetch.js, and constants.js. I then initialize some of these files, because require.js considers them [modules](http://requirejs.org/docs/api.html#define).

You can check out their quickstart guide [here](http://requirejs.org/docs/start.html).


## Font Awesome
I came to terms very early on in life that I will never be good at art. Even simple doodles seem difficult to me. Luckily, for the artistically-challenged web developer in your life, there's [Font Awesome](http://fortawesome.github.io/Font-Awesome/)

Pretty much, I used Font Awesome whenever I needed a cool symbol that I knew I wasn't gonna be able to make myself. For example, all my search buttons are Font Awesome.

<div class="externals">
	<div class='external twitter'><a href="http://twitter.com/migreva" target="_blank"><i class="fa fa-twitter"></i></a></div>
	<div class='external github'><a href="http://github.com/migreva" target="_blank"><i class="fa fa-github-alt"></i></a></div>
	<div class='external stack-overflow'><a href="http://stackoverflow.com/users/1337683/migreva" target="_blank"><i class="fa fa-stack-overflow"></i></a></div> 
	<div class='external spotify'><a href="http://open.spotify.com/user/123789431" target="_blank"><i class="fa fa-spotify"></i> </a></div>
	<div class='external email'><a href="mailto:mikevee313@gmail.com" target="_blank"><i class="fa fa-envelope-o"></i></a></div>
</div>

# I think that's about it
Thanks for reading this far, I know it wasn't easy. I'll post things on here from time to time, on various things I find interesting and other work I'll be doing. I'll also post about updates to the site, if I find anything else interesting I wanna talk about.