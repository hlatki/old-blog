---
layout: post
title: "A note about Nodewar"
date: 2013-04-13 14:55
comments: true
categories: 
- CoffeeScript 
- Nodewar
- fun
---

A few days ago there was a [post on Hacker News](https://news.ycombinator.com/item?id=5532360) about a new site called [Nodewar](http://nodewar.com) where you program little fleets of JavaScript powered space bots and battle other programmers for a 10 bitcoin prize.  The battles take place in an arena containing three unstable moons that will devour unwary ships, not to mention the opposition fleet laying in wait behind them.  Each fleet consists of a queen ship and several drones.  Combat happens by slamming your ships into the opposition -- if they impact properly, the enemy ship will split into two pieces, the smaller of which becomes one of your ships.

One of the owners of the site wrote one of the initially successfully teams, [The Spinara](http://nodewar.com/the/spinara). They try to fly away from all threats (some categories like the dread moons are given a larger weight, and thus more leeway).  This rudimentary navigation system seems to be the basis for many of top teams.  I based my first attempt, [The FlailBeans](http://nodewar.com/the/flailbeans), on a descendent of The Spinara called [The Ripoffs](http://nodewar.com/the/ripoffs) whose primary innovations were to change the weighting such that the enemy queen is targeted and to introduce an aggressiveness factor.  My chief "improvement" was reading the docs and noticing that smaller ships are faster, so I thought I would try to make these speedy little splinters into divebombers.  To do this, I multiplied the aggressiveness constant by the inverse of a ship's weight.  This seems to be working reasonably well, although I doubt that the FlailBeans will continue to be ranked so highly since they still use the standard simple targeting method and so have a tendency to miss the queen and careen off the map.  Ideally, I would like my ships to curve around the edge of the map and dive down onto the enemy queen and force it off the map via an improved targeting mechanism, but I think I'll have to leave that endeavor to those who have a firmer grasp of physics.

One of the most interesting things about Nodewar is that you can code your ships in either CoffeeScript or JavaScript.  Since the basis for the FlailBeans was written in CoffeeScript, I ended up learning a bit about it, and despite some initial doubts (what do you mean I have to indent that!), I think that I really like CoffeeScript. Although I really do like JavaScript, I do feel that sometimes the language can get in the way of immediate comprehension.  However, I think I'm much more excited about the possible addition of ClojureScript to the menu.

One more thing I wanted to discuss is the fact that you can make your code public.  Despite the obvious incentive not to do this (I imagine it would be a bit annoying to have your team in the top spot and then be usurped by your own code + some minor optimizations), I would love to see how the teams evolve over time and which strategy is ultimately the most successful.
