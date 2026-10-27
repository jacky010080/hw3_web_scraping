# nanoGPT Training Observations

## Overview

I trained nanoGPT using the Shakespeare dataset and experimented with four hyperparameters to observe their effects on training and validation loss.

## Results

| Parameter Changed | Train Loss | Val Loss |
|---|---|---|
| Baseline | 1.7648 | 1.8857 |
| max_iters: 2000 → 3000 | 1.7016 | 1.8612 |
| n_layer: 4 → 6 | 1.8024 | 1.9197 |
| n_embd: 128 → 256 | 1.5554 | 1.7516 |
| eval_iters: 20 → 100 | 1.7904 | 1.9062 |

## Observations

**1. Increasing Training Iterations**

Increasing `max_iters` from 2000 to 3000 reduced both training loss and validation loss.

**2. Increasing Transformer Layers**

Increasing `n_layer` from 4 to 6 resulted in slightly higher training loss and validation loss. 

**3. Increasing Embedding Dimension**

Increasing `n_embd` from 128 to 256 significantly reduced both training loss and validation loss.

**4. Increasing Evaluation Iterations**

Increasing `eval_iters` from 20 to 100 resulted in slightly higher training loss and validation loss.

## Conclusion

Among the tested configurations, increasing the embedding dimension produced the lowest training and validation losses. Increasing training iterations also improved performance, while adding more layers and increasing evaluation iterations didn't help in this experiment.