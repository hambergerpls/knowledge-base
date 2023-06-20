# Proposal

# Title
Direct speech-to-speech translation using generative pre-trained transformer. ???

Suitable direct speech-to-speech approach for Kadazandusun language



# Gap
 - No raw data
 - We have audio but is not paired (Raw data)

# Abstract

Existing speech-to-speech translation (S2ST) heavily relies on the text of the target language. They usually transcribe the source language audio into text first, translate the text to the target language, then synthesize the translated text. However, this method cannot be applied to languages that do not have a writing system or phoneme.  

# Introduction

Speech-to-speech translation (S2ST) has been used in scenarios such as international conference, travelling and tourism Cascading S2ST heavily relies on intermediate text for translation by first transcribing the source language into text using automated speech recognition (ASR), translate the text into target language using machine learning (MT), then synthesize the target speech with the translated text using text-to-speech synthesis (TTS). Direct S2ST is currently in attention of researchers and industries. Direct S2ST aims to integrate the above three tasks into an end-to-end model which translate the audio speech directly to the audio speech of another language. In comparison to cascaded S2ST, Kun et al., 2022, states that direct S2ST (1) is able to alleviate the error propagation problem of pipeline systems; (2) can retain the emotion, pitch, and prosody information of the speaker to the greatest extent; (3) has faster reasoning speed and takes up fewer storage resources.

However, the current challenges in achieving direct speech translation tasks is data scarcity. At the moment, there is very little S2ST data To alleviate this problem, a line of work tries to leverage pseudo data to improve direct S2ST. They usually convert the ASR data into speech to text translation data using an MT system, and then generate the target audio from the target text with a TTS system. Unfortunately, these methods do not guarantee the accuracy of the generated pseudo S2ST data. 

 # Method

 - Text-to-speech (for unwritten languages?)
 - 

 ???