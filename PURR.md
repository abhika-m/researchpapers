# PURR Google Paper Summary

## What
["PURR: Efficiently Editing Language Model Hallucinations
by Denoising Language Model Corruptions"](https://arxiv.org/pdf/2305.14908.pdf) explores hallucinations in the generative AI, specifically large language models. Large language models often generate misleading and factually incorrect claims which sound convincing, which is what makes these hallucinations so dangerous. Developing a way to mitigate these hallucinations will help boost the credibility of all large language models.

## How
In this paper, a model was fine tuned on synthetically created data. This data was creating a base paragraph about an entity or subject, grounded on some sort of evidence to ensure it is fully factually correct. Then, with the help of a large language model, the "clean" or factually correct passage was corrupted by asking the LLM to make the passage erroneous. 

This data was then used to fine tune an editing model.

## Why
Large language models are increasing in popularity and becoming more and more easy accessible to the general public. People often put more faith than they should in technology, and this remains the case with LLMs like ChatGPT. If these large language models are generating false statements but presenting them convincingly, it is likely the user won't question it. This isn't a big deal when the user is asking an LLM to generate a poem about something but it can be very problematic if the user is asking about a medical diagnosis, for example. 

## Considerations
This paper focuses largely on entity level errors even though there is a wide variety of errors which are present in large language model outputs. Taking other errors into account can strengthen the model and boost its usefulness. 

## Future Possibilties
This model can be somehow integrated to already existing generative ai models to provide the editing before outputting the generation. In order for this to be possible, the model will likely need to be smaller and easier to integrate.
