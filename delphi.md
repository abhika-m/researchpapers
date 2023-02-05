# Delphi Experiment Summary

## What
["Can Machines Learn Morality? The Delphi Experiment"](https://arxiv.org/pdf/2110.07574.pdf) explores a model which classifies morality using natural language processing. Succeeding in making machines learn morality can lead to better language models in all domains within NLP as it can help reduce immoral responses and promote equality.

[The Delphi platform](https://delphi.allenai.org/) is open for the public to demo with their yes/no questions or general statements to determine morality. A sample question/statement that can be passed to the model is "holding the door open for my friend", which will result in a positive response, or "can i stomp in my apartment when someone lives below me?", which will result in a negative response.

## How
The Delphi Experiment uses a bottom up, descriptive, and example based approach. Essentially, instead of passing the model certain morality rules for it to remember and use when classifying a statement, Delphi provides the model with multiple examples from which the model can self-classify the examples and learn what is right/wrong. 

It uses different datasets to learn certain morality judgements by assigning a positive value to certain rule of thumbs and then negating those and assigning a negative value to the negated rule of thumbs. There also syntactic noise added to the model to ensure accuracy when the same question or statement may be posited in a slightly different way.

## Why
Teaching models what is moral and what is not can help the state of many other language models. If a model is able to determine right vs wrong on its own, reducing bias in these models will be much simpler. The models can use such morality models to determine whether the data they are training on or the output they are producing are morally right or not. This can help reduce bias and automate the preprocessing of data. 

## Considerations
As explained in the paper, Delphi is also biased on the data it learns on. Reducing the bias of Delphi in and of itself will be an important task. Additionally, Delphi is mostly trained on American senses of morality. Certain gestures or actions can be ok in America but not in other countries. For exaple, flicking your chin is considered rude in certain countries, but if you were to pass to Delphi the statement "Flicking my chin", Delphi would respond saying that's ok, when it actually depends on where you are. Accounting for these differences will be especially important considering Delphi will be used by people from all around the world.

## Future Possibilties
As mentioned before, Delphi can be used by other language models to self-determine whether certain data holds bias or if a model is outputting an immoral response. It can help create ethical AI models.
