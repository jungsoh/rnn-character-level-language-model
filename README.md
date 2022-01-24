# Recurrent neural network: Character-level language model

We build a recurrent neural network (RNN) that can generate text at the character level. We use it to generate new names for dinosaurs.

![dinosaur](images/dino.jpg)

## Dataset
We have a list of 1536 dinosaur names compiled into a dataset that looks like:
```
Aachenosaurus
Aardonyx
Abdallahsaurus
Abelisaurus
Abrictosaurus
...
Zunityrannus
Zuolong
Zuoyunlong
Zupaysaurus
Zuul
```
To create new dinosaur names, we build a character-level language model to generate new names. The learning algorithm will learn the different name patterns, and randomly generate new names.

## RNN architecture
The RNN model architecture is shown below. At each time-step, the RNN tries to predict what the next character is, given the previous characters.

![rnn architecture](images/rnn.png)

## Generated names
Given the dataset of dinosaur names, we use each line of the dataset (one name) as one training example. At every 2000 steps of stochastic gradient descent, we sample several randomly chosen names to see how the algorithm is doing. At 22000 iterations, the generated names are:
```
Iteration: 22000, Loss: 22.728886

Onustreofkelus
Llecagosaurus
Mystolojmiaterltasaurus
Ola
Yuskeolongus
Eiacosaurus
Trodonosaurus
```
