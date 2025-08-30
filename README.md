# Game libraries review

My thoughts on different Javascript game libraries.

## Background

Probably around June 2025, don't have the exact date, I started a conversation with ChatGPT to learn about possible libraries to use to build a web game in Javascript, specifically in Typescript. This was the prompt:

> Make a list of 6 game libraries for 2d web games for a project that will be made in Typescript.
> As project goals, this will be the first game made by a couple of 50 years
> old guys, who entered the field of computer programming with the idea of
> making games, and never made one. So the first and only requirement would be
> "feasibility". We want to lower all barriers that would increase cognitive
> load, in order to give us the maximum probabilities of success. 
> We don't have any requirements regarding performance or visual fidelity.
> Would like to target the web, but if the chosen framework or library ease the
> transition to a mobile game, it would be s nice feature.

The suggested libraries were:

- [Pixijs](https://pixijs.com)
- [Phaser](https://phaser.io)
- [Kaboomjs](https://kaboomjs.com) which is dead, but a fork remains called [Kaplayjs](https://kaplayjs.com/)
- [Melonjs](https://melonjs.org)
- [Excaliburjs](https://excaliburjs.com)
- [PlayCanvas](https://playcanvas.com)

## Libraries

### Phaser ❌

I started testing out Phaser, as I've been subscribed to its "Phaser World" newsletter for some time now and although I never used the library, I was fond of the things his creator does.

However after doing a tiny demo project I realized I don't like its `class` approach which leads to use stuff like `something.bind(this)`. That's a feature of Javascript that I've been avoiding for almost all my programming years with Javascript. I think there are better ways to write code, avoiding that `bind/call` non-sense, which only makes code obscure.

So sadly Phaser won't be for me.

### Excalibur ❌

Has the same issue as Phaser, checked some demo code and saw things like: `this.state.bind(this)`. FUCK OFF!

### PlayCanvas ❌

Discarded without testing it as it's not what I'm looking for. Also it's closed source and while there's a free tier, it comes at a price. Discarded.

### Pixijs ❓

Saw some professional games on their showcase.

I tried the scaffolder and the code generated looked free of this, but they have several, when I tried the "Creation Template", it came with a very different scaffold that contained some modules with classes and, of course, the dreaded `this`.

This requires further inspection, as maybe there is more than one way to program using Pixijs.

**Update:** ok, the "Creation Template" is more suited to the kind of games I'd like to make, and it's true that there's a classic OOP approach for some parts of the library. But one could use factory functions and other mechanisms to hide those implementation details and have a very narrow surface dealing with binding `this`.

So maybe it's usable for me after all, but I will try KaPlay first.

### Kaplayjs ✅

At first sight it looks like a nice library to start learning how to make games. Has some assets incorporated, so you can start right away without needed to hunt for graphics for your first game.

Maybe it's not for an experienced programmer, however I like it so far.

It has pretty good documentation and a list of project examples explaining each concept, which is pretty cool.

Has a playground where you can follow the examples.

Not `.bind or .call(this)` so far, so great! :)

### Melonjs ❌

Saw that some games from their showcase gallery are on Google Playstore, so that means it's a good library to write professional games.

Sadly it also uses classes, so `.bind/.call(this)` all over the place.
