---
title: "Gomoku Gongzhu"
permalink: /gomoku.html
layout: single
classes: wide
toc: false
sidebar:
    - nav: sitemap

---

We solved Gomoku (Five in a Row) using both alpha-beta pruning and AlphaZero's architecture.
For simplicity, this Gomoku applies no professional rules ([Renju's 33, 44 and overlines rules applied to black](https://en.wikipedia.org/wiki/Gomoku#Specific_variations)).
We show that a 16 layer convolutional network can reach a higher level than man-made evaluation only by self-learning.
We investigate some statistical properties of our AIs.
This project takes advantage of [Gongzhu-Society](https://github.com/Gongzhu-Society/MCTS)'s MCTS and alpha-beta pruning package.

### Features

* Generate MANY train data from one by rotation, flip, and translation.
* Beautiful terminal output.
* Visualization of convolutional layer and interesting (also unsolved) phenomena in visualization.

### Kernel Visualization

This gif shows how these kernels changed during the training.

<div align=center>
   <img width="40%" src="https://raw.githubusercontent.com/WhymustIhaveaname/FiveStone-Gongzhu/main/figures/17th-500ms-min.gif"/>
</div>

### Training and Abelation Experiments

The following figure is for the 17th try.
Its main parameters are `{"ACTION_NUM": 100, "POSSACT_RAD": 1, "FINAL_LEN": 4, "FINAL_BIAS": 0.5, "UID_ROT": 4, "SHIFT_MAX":3}`.
The dashed blue line indicates the number of steps taken to make five in a line (FIAL) with no opponent assigned, corresponding to the left vertical axis.
Its minimal possible value is 5, while a randomly initialized network's FIAL is around 30.
The solid lines with round data points are the win rate in percent of the raw network against man-craft AI with search deep 1, corresponding to the right vertical axis.
The win rate stables at half-half after 200 epochs (each epoch contains 30 games).
The most impressive point is, the FIAL drops to around 5 after only 5 epochs!

<div align=center>
   <img width="80%" src="https://raw.githubusercontent.com/WhymustIhaveaname/FiveStone-Gongzhu/main/figures/try17.png"/>
</div>
