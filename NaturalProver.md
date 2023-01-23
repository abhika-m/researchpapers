# Natural Prover Allen Institute Paper Summary

## What
["NATURALPROVER: Grounded Mathematical Proof Generation with Language Models"](https://arxiv.org/pdf/2205.12910.pdf) explores the use of generative language models in mathematical proofs. It focuses on improving both full proof creation as well as next step generation using background theorems and definitions calling from the NaturalProofs-Gen dataset. The NaturalProofs-Gen dataset was created using NaturalProofs which is sourced from ProofWiki. 

## How
From my understanding, given a theorem or problem, this neural model reconstructs and generates references (terms such as "even", "odd", "integer", etc.) which are then fed into the GPT-3 language model to output a proof. Using the example problem "let x be an even integer, then show that x + 5 is an odd integer", the reconstructed references would include "even integer", "odd integer", etc. pulled from the dataset to find relevant axioms and theorems to produce a proof step. A more complicated problem, such as "prove that the square root of a prime number is irrational" may have references such as "square root", "prime", "irrational".

## Why
Mathematical proofs are commonly taught to develop reasoning and practice applying rationalization to solve problems. A tool such as Natural Prover can be used to support students struggling with mathematical proofs. It can also be used by teachers and professors to make grading proofs simpler (use the model to generate correct answers and compare student answers). It can also be used by math support websites such as Symbolab to improve their answers to mathematical questions. 

## Considerations
Such tools can often be used to cheat. Although ideally this would be used as an assistance tool, it's hard to enforce correct use of this tool. Partnerships with schools and university can help lessen the negative use of this however it is hard to rid of completely.

With about 40% correct and useful responses, this tool isn't accurate most of the time. Improving its accuracy over time will be important to ensure usefuleness of Natural Prover. This can be done by continuously training and improving the model with more data and conditional probability checks as well as constantly tracking and evaluating the model which is currently done using a joint loss function. 

In this paper, the idea of user choice in next step generation is brought up. This would mean, when suggesting a next step, the user would be given a number of next step options and they can choose which one is most useful/correct. It is discussed that the chosen response can be used as a data point to improve Natural Prover. I think this would even aid in lessening cheating as forcing the user to choose a next step will not just provide the user with an answer, but force the user to consider what the best next step in a proof would be. 

For next step generation on human provided steps, if this tool is able to identify incorrect reasoning in provided proof and correct that mistake, it would boost the usefulness of this tool. I believe currently the assumption is that human provided steps are correct thus far, but that may not always be the case.

## Future Possibilties
While currently this is being used for Mathematical Proof generation, proofs are seen in many fields and this model can be used as a base for proofs in different fields as well. Computer Science theory proofs (proving a code solves given problem) also tend to be complicated and I'm not sure if they are accounted for in this model. Briefly mentioned before, identifying mistakes in given proofs can also be a future addition to this tool to improve usefulness. 
