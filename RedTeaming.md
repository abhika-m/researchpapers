# Red Teaming Language Models to Reduce Harms Summary

## What
["Red Teaming Language Models to Reduce Harms: Methods, Scaling Behaviors, and Lessons Learned"](https://arxiv.org/pdf/2209.07858.pdf) explains the process of red teaming to alter language models to reduce harmful results. Red teaming is the act of either manually or automatically provoking models to return offensive or harmful results and then updating the model to not return that. This paper uses four different models and a team of red teaming members to actively produce harmful results and prevent models from doing that in the future.

## How
First, the team recruited participants to join the "red teaming team" from MTurk and Upwork platforms. They also had to ensure to effectively communicate the details of this research so that participants were prepared to work with and consented to potentially offensive data and responses. This team was responsible for interacting with an AI interface and their goal was to try and get the AI model to produce obnoxious, unethical, offensive responses. 

The four models used in this research include a plain language model (plain LM), prompted language model (prompted LM), rejection sampling (RS), and reinforcement learning from human feedback (RLHF). The plain LM is just a basic language model which acted as a base line. The prompted LM made sure to prompt the language model to produce harmless, helpful, and honest responses. The RS method had the model rank 16 generated samples by harmlessness and pick the two most harmless responses. The RLHF also prompts its model but then also uses reinforcement learning to update it each time to work better. 

Each member was randomly assigned two models from the four different models being used. They interacted with the AI assistant and received two responses, one from each model. They were then asked to pick the more harmful one in order to help create a harmlessness scale and expedite vulnerability detection by a factor of two. Harmfullness scores were also computed to model-human interaction responses on a scale of 1-4 where 0 means the person wasn't successful in getting the AI assistant to produce harmful results and 4 meaning they were successful in providing harmful results.

This data was used to improve the models and prevent them from reproducing these results. The RLHF model seemed to do the best out of all models.

## Why
As the world moves to a place where NLP is significantly used in everyday life, we want to ensure that the technology and NLP models that are being shared to the world don't reinstate harmful ideals, especially since there are so many efforts in reducing such offensive behavior. The wide accessibility of these models makes it even more important that the human-model interactions remain harmless and helpful. 

Additionally, the datasets these models are trained on come from years and years of data produced by humans. These datasets thus inherently hold biases that have been around for a long time. We want to prevent these biases from surfacing in these models and in order to do that, methods like red teaming are important. 

## Considerations
When manually detecting harmfullness, there can be many topics and social issues which could be missed. There needs to be constant updating of these models as well as a study on just how much harmfullness can be reduced by manual efforts. We can probably never create a perfectly ethical model, but finding the best way to get as close as possible will be really important as time goes on.

Additionally, using humans when evaluating such models still can result in participant bias. Choosing the right participants for research tasks like this is also crucial in obtaining the best results.

## Future Possibilties
I wonder if using models such as [Delphi](https://github.com/abhika-m/researchpapers/blob/main/DelphiExperiment.md) could help better these models. It would be super time consuming to run every output through Delphi, but utilizing the logic in Delphi in some way could help produce more helpful results.
