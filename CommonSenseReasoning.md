# Commonsense Reasoning

## What
["Generated Knowledge Prompting for Commonsense Reasoning"](https://arxiv.org/pdf/2110.08387.pdf) examines improving Question Answering (QA) models using generated knowledge statements. So, essentially providing the model with an extra layer of a generated knowledge statement to help it improve its answer. It looks at numerical commonsense (NumerSense), general commonsense (CommonsenseQA 2.0), and scientific commonsense (QASC). 

## How
The method used in this paper includes two basic parts: knowledge generation and knowledge integration. The first task is to generate the knowledge statement which will be provided to the model when answering a question. There are multiple different datasets used to help generate knowledge statements. Numerical commonsense prompts, for example, will utilize the NumerSense dataset which holds numerical statements. These datasets are used to generate a finite set of knowledge statements conditioned on the question. 

Now, with a set of knowledge statements, the second task requires integrating the knowledge to produce the answer. An inference model is used to predict an answer with each knowledge statement presented. The knowledge statement with the highest-confidence prediction is then used as the knowledge statement to produce the answer.

## Why
Looking at the results of this new method of question answering, there is significant improvement in answer predictions made by these QA models. For example, when asked if part of golf is trying to get a higher point total than others, without knowledge generation incorporated, the model predicted yes. With the knowledge statement, "the player with the lowest score wins", the model returned no. So, knowledge generation helped the model provide the correct answer in this case. Very simply put: the more accurate QA models are, the more useful or helpful they'll be. 

QA models have multiple uses too. They can be used to ask Siri simple general knowledge questions for fun. They could also potentially be used by doctors to recieve quick answers to questions about medications or illnesses. There is a variety of use cases for QA models and we see them everywhere, so the more accurate they are, the more they can help us in our everyday lives. 

Additionally, knowledge generation helps when there is no information retrievable by the datasets. When datasets don't have an answer to a question, knowledge generation can help generate a knowledge statement which can aid in providing an answer to an otherwise unanswerable question.

## Considerations
Knowledge generation, while helpful when it comes to accuracy, will add some time to the prediction process. If it is able to be optimized efficiently, then it won't necessarily be a problem, but ensuring this optimization will become more and more important as data grows.

## Future Possibilties
This method can be used to all existing QA models to further improve them. In some cases, accuracy becomes very important. Consider a situation where you need to call emergency services in a foreign country and you don't know the number to dial. You can use a QA system like Siri to quickly ask what the emergency services number is and in this case you would want accurate results the first time around.

All in all, continuously finding ways to better QA models is very important especially with the increasing popularity of question answering (take ChatGPT for exaple).
