---
title: Beam Search for Reasoning

description: |
  A framework of stepwise LLM reasoning.

layout: project
last-updated: 2023-05-01
---

We introduce a stepwise self-evaluation mechanism to enhance the reasoning capabilities of Large Language Models (LLMs). Our approach integrates self-evaluation guidance via stochastic beam search, serving as a calibrated criterion that facilitates efficient reasoning and superior prediction quality. By balancing exploitation and exploration with temperature-controlled randomness, our method excels in producing high-quality single-chain generations and adapts well to multiple-chain scenarios with high diversity. Our approach surpasses Codex-backboned baselines in few-shot accuracy by 6.34%, 9.56%, and 5.46% on the GSM8K, AQuA, and StrategyQA benchmarks, respectively. Further analysis in multi-step reasoning indicates that our self-evaluation guidance effectively identifies logical failures, leading to higher consistency and robustness.

**Paper**: [arXiv:2305.00633](https://arxiv.org/abs/2305.00633)  
**Code**: [GitHub Repository](https://github.com/guideddecoding)

## Generated Examples

We compare the predictions of baseline methods and our approach on specific instances. Scores from low to high are visualized from orange, yellow, to green. Here, *C*, *P*, and *E* represent the evaluation confidence, generation confidence (probability), and their combination as the final self-evaluation score, respectively.

In general, the evaluation confidence *C* is more effective at identifying logical errors, considering accumulated mistakes from prior steps, while the generation probability *P* focuses more on text perplexity as the confidence of the LLM generator.

{:center: style="text-align: center"}
![image](/img/beamsearchreasoning/beamsearchreasoning.jpg){: width="80%"}
{:center}

## Citation

```bibtex
@misc{xie2023decomposition,
      title={Decomposition Enhances Reasoning via Self-Evaluation Guided Decoding}, 
      author={Yuxi Xie and Kenji Kawaguchi and Yiran Zhao and Xu Zhao and Min-Yen Kan and Junxian He and Qizhe Xie},
      year={2023},
      eprint={2305.00633},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```
