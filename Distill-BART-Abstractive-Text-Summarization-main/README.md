# Distil-BART Summarization POC

This proof of concept (POC) demonstrates how to use the Distil-BART model for text summarization using the Hugging Face Transformers library and Google Text-to-Speech (gTTS) for audio generation.

## Text Extraction
Read the text from the file and perform filtering

###  1. Document Preprocessing:

    A. Text Extraction: In the step, extraction of text content from different document formats like pdf and docx is initiated as input for further processing.

    B. Tokenization: Tokenization involves breaking down the text into individual words or phrases, known as tokens. This step is essential for subsequent NLP tasks, enabling the analysis of the document at a more granular level. Used using distil-BART Tokenizer.

###  2. Data Cleaning:

    A. Removing Formatting and Special Characters: Stripping away unnecessary formatting, such as font styles, sizes, and special characters, ensures a clean and uniform text representation.
    
    B. Handling Line Breaks and Whitespace:     Addressing line breaks and excessive whitespace helps in maintaining consistent spacing and structure within the text, making it easier for subsequent processing steps.

## Distill BART Summarizer
Summarize the text using the Distil-BART model:

"Distill" in the context of machine learning models often refers to a process of compressing or distilling a large, complex model into a smaller and more efficient version while preserving its essential capabilities. This is typically done to reduce the model's size, speed up inference, or make it more suitable for deployment in resource-constrained environments.
The distil-BART model is distilled or compressed version of the original BART model. In the context of NLP, a distilled model often aims to achieve similar performance to a larger model but with reduced computational resources and memory requirements.

## Text-to-Speech (TTS)
Convert the summary to speech and save it to an audio file:

    gTTS (Google Text-to-Speech), a Python library and CLI tool to interface with Google Translate’s text-to-speech API. Writes spoken mp3 data to a file, a file-like object (bytestring) for further audio manipulation, or stdout. It features flexible pre-processing and tokenizing.

    After summarizing the text, the gTTS library helps to generate the audio file of the summary generated using distil-BART model.

## Reults
    ROUGE-2: 22.12 %
    ROUGE-L: 36.99 %

This README provides the Proof of Concept of distil-BART Summarizer and step-by-step guide for text extraction, distil-BART summarization, and text-to-speech conversion.
