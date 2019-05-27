---
layout: post
title: "Building design libraries with React"
description: A few weeks ago I started a personal project involving creating a website – more like a landing page – with React.
separator: ✏️
---

A few weeks ago I started a personal project involving creating a website – more like a landing page – with React. I'm not a designer who codes, but I *am* a designer who enjoys learning about coding now and again, so this was a fun and small project to get my teeth into! There are two learnings from this project I'd like to cover in this post.

By the way, I followed [Design+Code's](https://designcode.io/){:target="_blank"} guide to designing and building a website with React.

## Building design components with React

My very simple landing page had a couple of buttons, a navigation bar, some animations and a few cards that functioned like a button and displayed several layers of information: image, title and description. These cards were organised in a grid, meaning that they would be re-utilised as many times as needed.

![](images/blog/react-libraries/cards-grid.png)

Just like in Sketch, Adobe XD or Figma, React introduces the concept of *nested components* or *nested symbols*, whereby a component includes other smaller components with their own styling and behaviours. In Sketch, this translates into a symbol that can be re-utilised but for which you can modify content and even switch elements within it, such as the icons from an icon set. In React, this means that you can build the card component within a `card.js` file, create a styling for it within your `card.css` file and re-use as many times as needed in your main `.js` file – in this case, `index.js`.

### `card.css`

In this example, the card component includes some animation upon hovering, which is defined with the different **transitions**. We're also defining how the different cards will stack up in a grid, and how they will slightly move sideways upon being hovered over.

In `.CardGroup` (at the bottom), we define how the grid is going to look and behave.

```css
.Card {
  width: 300px;
  height: 300px;
  position: relative;
  overflow: hidden;
  border-radius: 20px;
  box-shadow: 0 15px 30px rgba(0,0,0, 0.2);
  display: grid;
  grid-template-rows: 1fr 1fr;
  transition: 0.4s cubic-bezier(0.2, 0.8, 0.2, 1);
  cursor: pointer;
  background-color: rgba(255, 255, 255, 0.8);
}

.Card:hover {
  transform: scale(1.05, 1.05);
  box-shadow: 0 30px 60px rgba(0,0,0, 0.2);
}

.Card:hover img {
  transform: translateY(0px);
  height: 100%;
  width: 100%;
  opacity: 0;
  transition: 0.4s cubic-bezier(0.2, 0.8, 0.2, 1)
}

.Card img {
  height: 100%;
  position: absolute;
  top: 0;
  z-index: 1;
  transition: 0.4s cubic-bezier(0.2, 0.8, 0.2, 1);
}

.Card h3 {
  color: black;
  font-size: 30px;
  margin: 20px 0 0 20px;
  width: 190px;
}

.Card p {
  color: black;
  text-transform: uppercase;
  font-weight: 600;
  font-size: 20px;
  align-self: end;
  margin: 0 0 20px 20px;
}

.Cards h2 {
  color: black;
  margin: 50px 20px 50px 20px;
  font-size: 60px;
  text-align: center;
  font-weight: 700;
  margin-bottom: 100px;
}

.CardGroup{
  margin: 50px 100px 100px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 60px;
  justify-items: center;
}
```

### `card.js`

A much smaller bit of code, in `card.js` we just define what the card includes. We include an image, a title and a bit of text, the styling of which we have already defined in our `card.css` file.

```html
import React from 'react'
import './Card.css'

const Card = props => (
  <div className="Card">
    <img src={props.image} />
    <h3>{props.title}</h3>
    <p>{props.text}</p>
  </div>
)

export default Card
```

### `index.js`

It's in the `index` file where things start to get exciting! Ok, maybe that was a little bit of an overstatement, but I do think it's pretty cool that you can *pass* a line of content – be it some text or an image url – and, *voilá*, it just appears on your screen! And you can keep piling up them cards like it's nobody's business, they will all stack up neatly and nicely without you having to dive in into crazy CSS and HTML code.

```html
<div className="Cards">
  <h2>Case studies</h2>
  <div className="CardGroup">
    <Card
      title="Unmortgage"
      text="Work project"
      image={require('../images/unmortgage-pre-filtering-thumbnail.png')} />
    <Card
      title="Carwow Dealer Dashboard"
      text="Work project"
      image={require('../images/carwow_thumbnail.png')} />
    <Card
      title="Chippin"
      text="Client project"
      image={require('../images/chippin_thumbnail.png')} />
    <Card
      title="Nuffield Health"
      text="Concept project"
      image={require('../images/nuffield_thumbnail.png')} />
    <Card
      title="The Nanny App"
      text="Coming soon"
      image={require('../images/nanny_thumbnail.png')} />
    <Card
      title="My own portfolio"
      text="Personal project"
      image={require('../images/portfolio_thumbnail.png')} />
  </div>
</div>
```

## Building animations with Figma vectors

I also built in some fancy animations, like waves that move up and down and navigation bars with transitional backgrounds, but I can't quite explain this just yet as I was just following along a tutorial and didn't fully grasp what I was doing.

It's worth knowing though that you can use Figma vectors to create animations, and that JavaScript supports it.

<iframe width="800" height="450" src="https://www.youtube.com/embed/VBTgrcs_g0A" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
