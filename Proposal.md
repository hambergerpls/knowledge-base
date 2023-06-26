
# Research Title
Speech-to-speech translation for Kadazandusun

# Problems
 - Kadazandusun is considered stable based on EGIDS measurement tool, however the language still has the possibility of declining if the children in the community did not learn the language.
 - There exists Kadazandusun digital media, however, there is no Bahasa Melayu <-> Kadazandusun and English <-> Kadazandusun speech dataset available currently
 - [Chen et al., (2022)](http://arxiv.org/abs/2211.06474) presented a speech-to-speech translation (S2ST) end-to-end solution for low-resource unwritten languages, using Hokkien as a case study for English<->Hokkien S2ST, by leveraging Mandarin as a written language similar to Hokkien to provide extra text supervision and to assist the parallel S2ST data creation process. English<->Mandarin machine translation also applied to create weakly supervised data to tackle data scarcity. However, the study did not present any data of the same language family, e.g. Mandarin<->Hokkien S2ST.

# Research Objectives
- To create initial S2ST dataset for Bahasa Melayu <-> Kadazandusun for future applications.
- To create initial TAT-S2ST evaluation dataset for Bahasa Melayu <-> Kadazandusun for future research
- To apply a similar approach by [Chen et al., (2022)](http://arxiv.org/abs/2211.06474) for Bahasa Melayu <-> Kadazandusun S2ST and evaluate the translation quality by computing the ASR-BLEU on the TAT-S2ST evaluation dataset

# Abstract Draft v1

We study speech-to-speech translation (S2ST) that translates speech from one language under the same family into its sibling. We use Bahasa Melayu-Kadazandusun as a case study, and used existing methods to train collected data and to benchmark the dataset.

## Introduction

### Draft v1

Speech-to-speech translation (S2ST) heavily relies on intermediate text for translation by first transcribing the source language into text using automated speech recognition (ASR), translate the text into target language using machine learning (MT), then synthesize the target speech with the translated text using text-to-speech synthesis (TTS). Direct S2ST is currently in attention of researchers and industries. Direct S2ST aims to integrate the above three tasks into an end-to-end model which translate the audio speech directly to the audio speech of another language.

The current challenges in achieving direct speech translation tasks is data scarcity. At the moment, there is no S2ST data for Bahasa Melayu <-> Kadazandusun. [Chen et al., (2022)](http://arxiv.org/abs/2211.06474) presented a speech-to-speech translation (S2ST) end-to-end solution for low-resource unwritten languages, using Hokkien as a case study for English<->Hokkien S2ST, by leveraging Mandarin as a written language similar to Hokkien to provide extra text supervision and to assist the parallel S2ST data creation process. English<->Mandarin machine translation also applied to create weakly supervised data to tackle data scarcity. However, the study did not present any benchmark of the same language family, e.g. Mandarin<->Hokkien S2ST.

The objectives of this study are as follows:
- To create initial S2ST dataset for Bahasa Melayu <-> Kadazandusun for future applications.
- To create initial TAT-S2ST evaluation dataset for Bahasa Melayu <-> Kadazandusun for future research
- To apply a similar approach by [Chen et al., (2022)](http://arxiv.org/abs/2211.06474) for Bahasa Melayu <-> Kadazandusun S2ST and evaluate the translation quality by computing the ASR-BLEU on the TAT-S2ST evaluation dataset

## Related work/literature review

[1] C. Wang et al., ‘VoxPopuli: A Large-Scale Multilingual Speech Corpus for Representation Learning, Semi-Supervised Learning and Interpretation’. arXiv, Jul. 27, 2021. doi: 10.48550/arXiv.2101.00390.

[2] C. Zhang, X. Tan, Y. Ren, T. Qin, K. Zhang, and T.-Y. Liu, ‘UWSpeech: Speech to Speech Translation for Unwritten Languages’. arXiv, Dec. 17, 2020. doi: 10.48550/arXiv.2006.07926.

[3] H. Inaguma et al., ‘UnitY: Two-pass Direct Speech-to-speech Translation with Discrete Units’. arXiv, May 26, 2023. doi: 10.48550/arXiv.2212.08055.

[4] A. Lee et al., ‘Textless Speech-to-Speech Translation on Real Data’. arXiv, May 04, 2022. doi: 10.48550/arXiv.2112.08352.

[5] P.-J. Chen et al., ‘Speech-to-Speech Translation For A Real-world Unwritten Language’. arXiv, Nov. 11, 2022. doi: 10.48550/arXiv.2211.06474.

[6] A. Tjandra, S. Sakti, and S. Nakamura, ‘Speech-to-Speech Translation Between Untranscribed Unknown Languages’, in 2019 IEEE Automatic Speech Recognition and Understanding Workshop (ASRU), Dec. 2019, pp. 593–600. doi: 10.1109/ASRU46091.2019.9003853.

[7] A. Polyak et al., ‘Speech Resynthesis from Discrete Disentangled Self-Supervised Representations’. arXiv, Jul. 27, 2021. doi: 10.48550/arXiv.2104.00355.

[8] C. Wang et al., ‘Simple and Effective Unsupervised Speech Translation’. arXiv, Oct. 18, 2022. doi: 10.48550/arXiv.2210.10191.

[9] P.-A. Duquenne, H. Gong, and H. Schwenk, ‘Multimodal and Multilingual Embeddings for Large-Scale Speech Mining’, in Advances in Neural Information Processing Systems, Curran Associates, Inc., 2021, pp. 15748–15761. Accessed: Jun. 22, 2023. [Online]. Available: https://papers.nips.cc/paper/2021/hash/8466f9ace6a9acbe71f75762ffc890f1-Abstract.html

[10] Q. Dong, F. Yue, T. Ko, M. Wang, Q. Bai, and Y. Zhang, ‘Leveraging Pseudo-labeled Data to Improve Direct Speech-to-Speech Translation’. arXiv, May 18, 2022. doi: 10.48550/arXiv.2205.08993.

[11] M. S. Sainin and M. H. Haris, ‘Kadazandusun Speech Recognition: A Case Study’, 2020.

[12] W.-N. Hsu, B. Bolte, Y.-H. H. Tsai, K. Lakhotia, R. Salakhutdinov, and A. Mohamed, ‘HuBERT: Self-Supervised Speech Representation Learning by Masked Prediction of Hidden Units’. arXiv, Jun. 14, 2021. doi: 10.48550/arXiv.2106.07447.

[13] S. Popuri et al., ‘Enhanced Direct Speech-to-Speech Translation Using Self-supervised Pre-training and Data Augmentation’. arXiv, Sep. 13, 2022. doi: 10.48550/arXiv.2204.02967.

[14] A. Lee et al., ‘Direct speech-to-speech translation with discrete units’. arXiv, Mar. 21, 2022. doi: 10.48550/arXiv.2107.05604.

[15] Y. Jia et al., ‘Direct speech-to-speech translation with a sequence-to-sequence model’. arXiv, Jun. 25, 2019. doi: 10.48550/arXiv.1904.06037.

[16] J. Betker, ‘Better speech synthesis through scaling’. arXiv, May 23, 2023. doi: 10.48550/arXiv.2305.07243.

[17] Y. Zhang et al., ‘Google USM: Scaling Automatic Speech Recognition Beyond 100 Languages’. arXiv, Mar. 02, 2023. doi: 10.48550/arXiv.2303.01037.

[18] K. Wei et al., ‘Joint Pre-Training with Speech and Bilingual Text for Direct Speech to Speech Translation’, arXiv.org, Oct. 31, 2022. https://arxiv.org/abs/2210.17027v1 (accessed Jun. 07, 2023).

[19] A. Anastasopoulos and D. Chiang, ‘A case study on using speech-to-translation alignments for language documentation’, in Proceedings of the 2nd Workshop on the Use of Computational Methods in the Study of Endangered Languages, Honolulu: Association for Computational Linguistics, Mar. 2017, pp. 170–178. doi: 10.18653/v1/W17-0123.
