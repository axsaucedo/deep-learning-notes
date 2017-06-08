
# Reinforcement Learning

Computers that can play games are always a hot topic.

In December 2013, Deepmind released a groundbreaking paper called "Playing Atari with Deep Reinforcement Learning".

A little over a month later, Google announced they bought deep mind for a big sum of money.

Since then there has been a lot of talk about reinforcement learning in the field of AI.

In January 2016, alphago was able to beat the world champion.

## History

The history of RL goes all the way back to AI, animal psychology, and control theory. 

At the heart of it, it involves an autonomous agent like a person, learning to navigate an uncertain environment with the objective of maximizing a numerical reward.

Sports are a great example of this. 

In a tennis game, the player needs to review his actions available, and choose one as it will change the state of the game.

Every action is performed with a rewarding in mind: trying to get a point to win the set/game/match.

The agent needs to follow a set of rules and strategies in order to maximize the score.


## Model 

However if you're building an autonomous agent how woudl you model this?

We know that the agent's actions will change the state of the environment, so a model would need to take a state and an action as input, and generate the maximum expected reward as output.

However, because that would only take you to the next state, the model needs to take into consideration the total expected reward for every action from the current until the end state.

The way this works is different for each application.

Building a tennis agent is different than building an Atari agent.

## Deep Atari

The researchers at deep mind use a series of Atari screenshots to build a CNN with a couple of tweaks.

The output isn't a class  - but instead a target number for the maximum reward.

So it was actually dealing **with regression**, not classification.

They also **didn't use pooling layers**, since unlike image recognition, individual positions of game objects like the player are important and can't be reduced.

A recurrent network could be used too, as long as the output layer was tailored for regression, and the input at each timestep included the action and the environment state.

## Deep Q Network

There is also the Deep Q Network, or DQN.

It also uses the principles of predicting the maximum reward given a state and an action. 

It was **patented by google**, and it has seen a lot of improvements like the experience replay, and the dooling network architecture.

## Supervised learning

Reinforcement learning isn't just a fancy way to say "Supervised learning".

Supervised learning is all about making sense of the environment based on historical examples.

However, that is not always the best way of doing things.

Imagine if you're trying to drive a car in heavy traffic based on the road patterns you observed the week before where the roads where clear. Or like driving only looking at the rear-look mirror.

Reinforcement learning is all about reward. You get points for your actions, like staying in your lane, signalling when you need to.

You can also lose points for dangerous actions like tailgating and speeding.

The objective is to get the maximum number of points possible given the current state of the traffic on the road around you.

Reinforcement learning emphasises that an action results in a change in the state which supervised learning doesn't focus on.

## Exploration vs Exploitation

In April 2016 Jeff BEzoz said how amazon is great to fail and most companies cannot go through failed experiments.

Most organizations are used to operate in the realms of conventional wisdom, which is about exploiting what is known to achieve finite rewards with known odds.

Some groups venture into the unknown and explore new territory, looking for rewards. Many organizations fail, but some succeed and change the world.

With reinforcement learning, an agent can explore the tradeoff between exploration and exploitation, and choose the path to the maximum expected reward.

## Global Approach

Deep Reinforcement learning falls in the broader umbrella of AI, and between Deep Learning and Reinforcement learning.

It involves topics like goal setting, planning and perception.

And it can build a link between AI and engineering disciplines.

## Relevant URLs

* Richard Sutton book: https://webdocs.cs.ualberta.ca/~sutto...
* Tambet Matiisen post: https://www.nervanasys.com/demystifyi...
* Andrej Karpathy post: http://karpathy.github.io/2016/05/31/rl/
