# Speech-to-speech translation for a real-world unwritten language

Full Paper: http://arxiv.org/abs/2211.06474

# Problems presented
- 40% of the languages in the world do not have text written forms [https://www.ethnologue.com](https://www.ethnologue.com)
- S2ST for unwritten languages still remains a research area with little exploration mainly due **to lack of training data.**
- Majority of previous work on S2ST conducts experiments on datasets built from **applying TTS on S2T corpora to generate synthetic target speech for model training** [(Tjandra et al., 2019; ](https://ieeexplore.ieee.org/document/9003853)[Zhang et al., 2020).](https://arxiv.org/abs/2006.07926)
- [Lee et al. (2022b)](https://arxiv.org/abs/2112.08352) presents the first textless S2ST system trained on real S2ST data, while it **only investigates translation between high-resource and similar language pairs** (English<->Spanish, English<->French). The feasibility of **S2ST for unwritten languages under a low-resource setup, which is a more realistic scenario, remains unknown.**
- **Hokkien lacks a unitary writing system that is widely adopted** by its native speakers, though a few possible writing systems exists, e.g. Chinese characters (Hanji), or romanizasion systems such as Peh-oe-ji (POJ) and Tai-lo, etc.
- **Hokkien is a tonal language that has complex tone sandhi rules**

# Approach presented
- Take advantage of the discrete unit-based S2ST approach [(Lee et al., 2022a)](https://arxiv.org/abs/2107.05604), which applies a self-supervised speech encoder to convert the target speech into a sequence of integers and translates source speech into target discrete units
- Extends HuBERT-based discrete unit extraction [(Hsu et al., 2021)](https://arxiv.org/abs/2106.07447) and examine the feasibility of unit-to-waveform generation [(Polyak et al., 2021)](https://arxiv.org/abs/2104.00355) for tonal languages.
- Leverage the unit-based speech normalization technique proposed in [Lee et al. (2022b)](https://arxiv.org/abs/2112.08352) to remove the non-linguistic variations in speech from multiple speakers. Original study takes advantage of synthetic speech generated from TTS as reference target for normalization, but this study uses real Hokkien speech data.
- Study two S2ST model training strategies, speech-to-unit translation (S2UT) with a single decoder [(Lee et al., 2022a)](https://arxiv.org/abs/2107.05604) or a two-pass decoding process [(Inaguma et al., 2022)](https://arxiv.org/abs/2212.08055) that leverages Mandarin as a written language similar to Hokkien to provide extra text supervision.
- Leverage Mandarin to assist the parallel S2ST data creation process and create a 60-hr human annotated training set and an open benchmark set as no En<->Hokkien dataset available.
- Applies En<->Zh MT to create weakly supervised data [(Popuri et al., 2022; ](https://arxiv.org/abs/2204.02967) [Dong et al., 2022](https://arxiv.org/abs/2205.08993) to tackle data scarcity issue
- Learn a joint embedding space for English and Hokkien through Mandarin to support automatic data mining from unlabeled English and Hokkien data [(Duquenne et al., 2021)](https://papers.nips.cc/paper/2021/hash/8466f9ace6a9acbe71f75762ffc890f1-Abstract.html)