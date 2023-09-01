# LoRA Paper Summary

## What
["LORA: LOW-RANK ADAPTATION OF LARGE LANGUAGE MODELS"](https://arxiv.org/pdf/2106.09685.pdf) is a method proposed to make training more efficient in terms of cost, time, and memory. It is essentially tackling an optimization task on finetuning.
## How
At the most basic level, the process of training is simply a method of updating weights or parameters of a base model until it does well on a desired task. So there are some initial weights W<sub>0</sub> which are used to predict model outputs. When you train a model, these weights are updated by some &Delta;W: W<sub>0</sub> += W. Usually, &Delta;W is the same dimension as W<sub>0</sub> and so calculating &Delta;W can be very time and memory consuming.

LoRA describes a method where &Delta;W is broken into the product of two matrices A and B, each with a lower rank than W<sub>0</sub>. So now, during training, A and B are updated in order to update &Delta;W. Since A and B are of lower ranks, they will be faster to update and take up less memory. Additionally, inference time won't be majorly impacted unlike other adapter methods because merging lora weights with the base model weights is simple.

## Why
As NLP and Gen AI are progressing, more and more complex models are being produced. Training these large models, like LLAMA 70B, not only take a long time but also require lots of resources. Using methods like LoRA can make training these models faster and more accessible to those who may not have all the resources, such as number of gpus, to train a large model.

## Considerations
Determining the ranks of the lower ranks matrices and also determining the optimal scaling factor adds a little more complexity to training using LoRA. Having an easy way to find out the best rank to scale down to and the best scaling factor to use can make it easier to determine what configuration will bring in the highest performance.

## Future Possibilties
LoRA currently reduces the updating matrix to two lower rank matrices. What would happen if &Delta;W is reduced to three lower rank matrices?
