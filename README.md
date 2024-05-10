# Let's build our first LLM agent


## Table of Contents
- [What is this repo about?](#)
- [How to run the code](#features)
- [Wanna get more hands-on content like this?](#)

## What is this repo about?
In this repository you will find a Python implementation of an LLM agent.

> What is an LLM agent?

In this example we will use LangChain to implement a multi-hop


## Why agents?



## How to run the code?

## Wanna get more hands-on content like this?



```
$ poetry run python src/main.py --input "Create a plot of the number of full time employees at the 3 tech companies with the highest market cap in the United States in 2024."
```

No plot was saved to disk. Let's adjust the prompt.

```
$ poetry run python src/main.py --input "Create a plot of the number of full time employees at the 3 tech companies with the highest market cap in the United States in 2024. Save the plot as a png file under plots/"
```

These work
```
$ poetry run python src/main.py --input "Create a plot of the ETH/EUR price in January 1st 2024. Save the plot as a png file under plots/"
$ poetry run python src/main.py --input "Create a plot of the ETH/EUR price for today. Save the plot as a png file under plots/"
```

So, so
```
$ poetry run python src/main.py --input "Create a plot of the ETH/EUR daily price for the last 3 days. Save the plot as a png file under plots/"
```

This one does not work
```
$ poetry run python src/main.py --input "Create a line chart with the daily ETH/EUR price from January 1st 2024 until January 10th 2024. Save the plot as a png file under plots/"
```

The reason is `I could not find the daily ETH/EUR price from January 1st 2024 until January 10th 2024.`

Let's fix this by adding a new tool.
