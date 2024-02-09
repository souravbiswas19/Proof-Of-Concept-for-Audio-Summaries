# TF-IDF Extractive Summarization POC

This Proof of Concept (POC) on extractive text summarization using TF-IDF features and Google Text-to-Speech (gTTS) for audio generation.

## Data Preparation:

Collect a dataset for testing the extractive summarization model. Ensure the dataset includes text documents for summarization.

## TF-IDF Vectorization:

TF-IDF vectorization technique has been used to convert the preprocessed text into numerical features. This involves calculating the TF-IDF scores for each term in the document.

## Sentence Scoring:

Calculate the importance score for each sentence based on the TF-IDF features. This is done by summing the TF-IDF scores of the terms present in each sentence.

## Extract Top Sentences:

Identifying the top-ranked sentences based on their TF-IDF scores. These sentences are considered the most important and will be included in the final summary.

## Output Summary:

Compiling the top-ranked sentences to generate the final extractive summary.

## Text-to-Speech (TTS)
Convert the summary to speech and save it to an audio file:

gTTS (Google Text-to-Speech), a Python library and CLI tool to interface with Google Translate’s text-to-speech API. Writes spoken mp3 data to a file, a file-like object (bytestring) for further audio manipulation, or stdout. It features flexible pre-processing and tokenizing.

After summarizing the text, the gTTS library helps to generate the audio file of the summary generated using distil-BART model.

## Reults
As there is no reference summary available for comparing the results, no such results have been provided provided.
