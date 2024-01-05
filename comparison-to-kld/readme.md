comparison-to-kld
=================

I don't want to exaggerate the difference between earlier lexical methods and the predictive, LLM-based methods I'm exploring here. Most of the information in text is registered on a lexical level, so lexical methods are often a good approximation of anything one can do with deep learning.

In a couple of initial tests, for instance, I've found that measuring KL divergence between word distributions of samples (using the method in [Piper et al 2023](https://ceur-ws.org/Vol-3558/paper6166.pdf)) is a reasonable approximation of the "prediction-summary divergence" I measure using GPT-3.5. "Reasonable approximation" meaning, *r* is often .4 to .6 if one compares the two sets of measurements.

On the other hand, there are dramatic patterns that appear only using one method, or only using the other.

In particular, previous work on "novelty" and "revelation" in narrative has tended to find that it decreases across narrative time.

McGrath et al. find this using a Bloom filter.

![Fig. 1 from 'Measuring Modernist Novelty'](https://github.com/tedunderwood/next-twist/blob/main/comparison-to-kld/MeasuringModernistNoveltyFig1.png)

Piper et al also find this using KL divergence.

![Fig 2 from 'Modeling Narrative Revelation'](https://github.com/tedunderwood/next-twist/blob/main/comparison-to-kld/ModelingNarrativeRevelationFig2.png)

But no such trend is visible when we plot the divergence of prediction from summary across narrative time.

![image produced by AnalyzeFirstRunOfAll.ipynb](https://github.com/tedunderwood/next-twist/blob/main/comparison-to-kld/trend-over-narrative-time.jpg)

If there's a trend there, it's almost invisible to the naked eye.

This could be evidence that the LLM-based method is noisier or less sensitive; or it could be interpreted as evidence that surprise is relatively constant across a narrative, even if lexical novelty is not. Further work is needed to decide. All I'm suggesting right now is that the methods don't always produce the same result.