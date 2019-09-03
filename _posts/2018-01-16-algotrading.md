---
title: ML experiments manager
layout: post
category: data
tags:  python keras rl baselines
---

For a few months I've been trying to train an agent able to invest on stock market without loosing money (let's be realistic).

In previous learning project I'd choose a specific technology I was interested on and tried to apply it to something. In this case I selected a specific problem and tried to solve in the best possible way.

This creates the necessity of doing lots of tests with small variations. Over the time that translated on a modular platform:

Each experiment is fully described in a YAML file. When the platform is in demon mode, it's continually looking for a new job by looking at a specific directory. This approach works but is not very handy, so a frontend in a form of Telegram Bot have been implemented. It not only works as a job submitter, but also enables stats query and error reporting.

![bot](/assets/img/bot.png)

A job is then selected by priority and submission time.

At a high level there are four different stages:


- Dataset fetch
- Dataset preprocessing and feature generation
- Model training. In the specific case of RL this has more modular stages:
  - Environment definition
  - Data preprocessing and feature generation at iteration window.
  - Agent training
- Results generation and reporting


![bot](/assets/img/algotrading.png)

As an example here is a YAML configuration:
[YAML Gist](https://gist.github.com/fevsea/4755c117025a2b8610bd5b0384d21f19)
