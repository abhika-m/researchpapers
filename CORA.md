# COORA H2Labs Paper Summary

## What
["One Question Answering Model for Many Languages
with Cross-lingual Dense Passage Retrieval"](https://arxiv.org/pdf/2107.11976.pdf) aims to improve question answer (QA) models by utilizing sources from multiple languages to provide an accurate answer. A QA model is pretty much exactly what it sounds like, it's a model to answer questions asked by the user. Technologies like Alexa may utilize QA models for their question answering features as well. In order to appeal to diverse crowds and ensure inclusivety, these QA models need to be able to cater to multiple different languages. Additionally, the accuracy of the answers returned by this model can be improved by opening up the search for answers to documents/files written in all languages. This is where Cross-lingual Open-Retrieval Answer (CORA) Generation comes in.

## How
At the very basic level, CORA works similar to any other QA model where it takes in a question in some language and outputs an answer in that same language. However, CORA utilizes texts and data from multiple different languages when generating the response instead of only using English texts or texts in the original input language. 

CORA breaks QA into two parts, passage retrieval and then answer generation in the original language. It retrieves passages using the computed relevance score for the question asked by using a multilingual dense passage retriever (mDPR). Then it uses a multilingual answer generator (mGEN) to generate an answer using the passages retrieved with the highest relevance scores. The generator can adapt to languages with relatively less data as well hence the generation approach was chosen.

## Why
Most QA models generally either translate questions for retrieving information then translate back to the original language or they only parse through passages in the original language to retrieve an answer. In the first method, meaning is usually lost during the translations, especially when translating a language with little to no data. This results in incorrect or unelpful answers, sometimes even results in no answer being provided. The second method limits the answer retrieval to passages in the original language which narrows the scope of the answer. So, by utilizing a language model, like CORA, which limits translation while searching through multiple languages, NLP tools can cater to multiple languages as accurately as possible regardless of how much data is available for a language. 

## Considerations
When finding relevance scores for passages, it can be difficult to accurately produce a score for a passage which is in an entirely different language without translation or some form of context analysis. Although I am not entirely familiar with the algorithm used for the relevance score, improving the algorithm will be very important to ensure accuracy and prevent false positives.

## Future Possibilties
CORA can be applied to many existing QA platforms. Alexa, ChatGPT, Siri, Google Home, etc. are all examples of areas where CORA can be used. 
