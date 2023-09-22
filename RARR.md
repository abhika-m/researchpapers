# LoRA Paper Summary

## What
["RARR: Researching and Revising What Language Models Say,
Using Language Models"](https://arxiv.org/pdf/2210.08726.pdf) is a paper with a focus on improving trushtworthiness of large language models through the process of revision. It looks at identifying hallucinations and revising the output if needed.

This paper has two parts to their approach in hallucination detection and editing: research and revision. When given an output, this two step approach will first research the output by query generation. During query generation, an LM is prompted to generate a comprehensive list of questions covering all aspects of a given passage. Next, a retrieval system is used to produce attributions for the generated questions. 

This brings us to the next step, revision. An agreement model is used to determine how well the passage aligns with the attributions. Depending on the results, the passage is then edited (or revised) to improve agreement with the retrieved documents and fix factuality errors present in the original passage.

## Why
Language Models are being increasingly utilized by the general public for everyday and specialized tasks. An everyday user of language models such as ChatGPT, are likely placing more trust in these language models than they should. Additionally, as language models progress, they will get better and better at sounding correct even when they're outputs are packed with factuality errors. Improving the detection of hallucinations and bringing this issue to light is critical to ensure our language models don't bring harm to the world.

## Considerations
The approach to correcting factuality errors in this paper has multiple parts to it. Each of these parts need to be strong in order to ensure that the entire pipeline is working at its best. If the retrieval system doesn't work as intended for certain examples or the agreement model is faulty in some instances, the entire approach can fall apart. Ensuring each aspect of the process is strong or finding ways to shorten this pipeline can help guarantee more consistency in hallucination detection and revision.

## Future Possibilties
Focusing on passages with rarer entities or topics where retrieval may not be possible can be an interesting direction. Right now the researching part of hallucination detection in this paper is heavily reliant on how good the retrieval passages are, so including examples where there may not be evidence easily accessible can be something to consider.
