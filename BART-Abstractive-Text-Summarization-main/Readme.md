# BART Summarization POC

This proof of concept (POC) demonstrates how to use the BART model for text summarization using the Hugging Face Transformers library and Google Text-to-Speech (gTTS) for audio generation.

## Text Extraction
Read the text from the file and perform filtering

###  1. Document Preprocessing:

        A. Text Extraction: In the step, extraction of text content from different document formats like pdf and docx is initiated as input for further processing.

        B. Tokenization: Tokenization involves breaking down the text into individual words or phrases, known as tokens. This step is essential for subsequent NLP tasks, enabling the analysis of the document at a more granular level. Used using BART Tokenizer.

###  2. Data Cleaning:

        A. Removing Formatting and Special Characters: Stripping away unnecessary formatting, such as font styles, sizes, and special characters, ensures a clean and uniform text representation.
        B. Handling Line Breaks and Whitespace:     Addressing line breaks and excessive whitespace helps in maintaining consistent spacing and structure within the text, making it easier for subsequent processing steps.

## BART Summarizer
Summarize the text using the BART model:

    BART is a transformer encoder-decoder (seq2seq) model with a bidirectional (BERT-like) encoder and an autoregressive (GPT-like) decoder. BART is pre-trained by (1) corrupting text with an arbitrary noising function, and (2) learning a model to reconstruct the original text.

    BART is particularly effective when fine-tuned for text generation (e.g. summarization, translation) but also works well for comprehension tasks (e.g. text classification, question answering).
    
    In my task, I have used BART as an Abstractive text summarizer. Compareed to the other models, the BART model is providing a pretty good summarized text of the Context.

## Text-to-Speech (TTS)
Convert the summary to speech and save it to an audio file:

    gTTS (Google Text-to-Speech), a Python library and CLI tool to interface with Google Translate’s text-to-speech API. Writes spoken mp3 data to a file, a file-like object (bytestring) for further audio manipulation, or stdout. It features flexible pre-processing and tokenizing.

    After summarizing the text, the gTTS library helps to generate the audio file of the summary generated using BART model.

## Reults
    ROUGE-1 on cnn_dailymail: 42.949 %
    ROUGE-2 on cnn_dailymail: 20.815 %
    ROUGE-L on cnn_dailymail: 30.619 %

This README provides the Proof of Concept of Facebook's BART Summarizer and step-by-step guide for text extraction, BART summarization, and text-to-speech conversion.