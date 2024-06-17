# Annotations for MultiplEYE in DE

## Introduction

For the EU-funded "MultiplEYE" project, I annotated German text data. "MultiplEYE" focuses on analyzing eye movement data during reading in different languages to understand reading habits and cognitive processing of texts. My work contributes to this project by preparing and analyzing German texts.

## Data

The data consists of short, translated texts from various genres provided in TXT format. The texts were preprocessed to ensure uniform formats.

## Tokenization

I tokenized texts in German, Ukrainian, and Russian using NLTK and SpaCy:

German and Russian: Both NLTK and SpaCy performed well.
Ukrainian: Only SpaCy was used as NLTK doesn't support Ukrainian.
Both libraries delivered similar quality results.

## Part of Speech Tagging

For POS tagging:

German: Both NLTK and SpaCy delivered precise results.
Russian: SpaCy was accurate, while NLTK overused the "NNP" tag.
Ukrainian: Only SpaCy was used and performed well.
SpaCy provided consistent and accurate results across all languages.

## Sentence Alignment

I aligned annotated German sentences to raw English sentences using [BertAlign](https://github.com/bfsujason/bertalign), which uses sentence transformers and the Google Translate API. The alignment process involved dynamic programming for accurate sentence matching.

The process involved:

Using TSV format for annotated data.
Aligning using BertAlign and extracting results into a second TSV file.
Adding sentence IDs manually to ensure accuracy.
Evaluation

Lemmas: Over 92% accuracy.
POS Tags: Over 93% accuracy.

## Surprisal

The surprisal was calculated with BERT. The offset might be slightly off.
Sentence Alignment: Perfect accuracy.
Conclusion

The annotation process was successful, especially the sentence alignment. If redoing the project, I would align sentences before annotating to save time and focus only on German data.
