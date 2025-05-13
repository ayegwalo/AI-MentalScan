<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. -->

# Project Title

AI-Powered Early Detection of Mental Health Issues in Teens

## Summary

This project uses AI to analyze social media text and behavioral patterns to identify 
early signs of mental health challenges in teens. The goal is to provide early, 
non-invasive alerts to professionals or guardians to enable timely support.


## Background

Mental health issues in adolescents are increasing globally, 
yet early diagnosis is often missed due to privacy and stigma.
Social media often reflects emotional states and patterns that can act as signals if analyzed effectively.
* Difficulty in identifying early signs of depression and anxiety in teens.
* Stigma prevents open conversations or seeking help.
* Healthcare systems struggle to offer early intervention.
* Parents, teachers may not recognize signs until the problem escalates.

I have decided to take this topic because I have seen close friends and students struggle with undiagnosed mental health issues. 
Early detection can save lives and improve long-term outcomes, making this a socially impactful use of AI.


## How is it used?

This AI solution is used to monitor social media content (text posts, captions, and activity patterns) of consenting teenagers. 
It is very valuable in school settings, wellness programs, or home environments where early emotional support is vital.

The process works like this:
* Guardian gives consent to monitor online activity.
* An AI model analyzes natural language in posts using NLP and sentiment analysis (the process of analyzing digital text to determine if the emotional tone of the message is positive, negative, or neutral).
* If patterns of emotional distress or risk indicators are detected, a non-invasive alert is generated for a mental health professional or guardian.

The primary users are:
* Mental health professionals
* School counselors
* Parents/guardians
* Researchers

Important considerations:
* User privacy and data consent are critical(Users shoud be made to know this).
* Language and cultural context must be accounted for to avoid misinterpretation.
* Alerts must be respectful, non-alarming, and designed to encourage support.

[Cat] <img src="https://upload.wikimedia.org/wikipedia/commons/5/5e/Sleeping_cat_on_her_back.jpg" width="300">


Code sample:
```
from transformers import pipeline

# Load a sentiment analysis model
analyzer = pipeline("sentiment-analysis")

# Example text input from a teen's social media post
text = "I feel exhausted and nothing makes sense anymore..."

# Run analysis
result = analyzer(text)
print(result)
```


## Data sources and AI methods
Data sources and AI methods
The project uses publicly available or consented datasets such as:
* [CLPsych 2015 dataset](https://aclanthology.org/W15-1204/)
* [Twitter API](https://docs.x.com/home)
* Public datasets from Reddit mental health communities

AI Methods used:
* Natural Language Processing (NLP)
* Sentiment analysis and emotion detection (e.g., BERT, RoBERTa models)
* Time-series trend analysis to detect shifts in mood over time

| Method            | Description                                 |
| ------------------| ---------------------------------------     |
| NLP Model         | Understands language patterns and tone      |
| Sentiment Score   | Measures emotional intensity and polarity   |
| Alert Logic       | Flags risk based on thresholds and trends   |


## Challenges
This project does not:
* Diagnose any mental illness
* Replace professional psychological evaluation
* Monitor private or encrypted communications

Ethical and practical limitations:
*Risk of false positives/negatives
Cultural differences in emotional expression
Potential stigma if alerts are misused
High privacy and security requirements for sensitive data

## What next?
* Partner with schools or wellness programs for pilot studies
* Recruit data ethics and mental health professionals
* Language support to cover more regions/countries
* More social media platforms


## Acknowledgments
* Inspired by the growing mental health crisis among teens during the pandemic.
* Thanks to researchers behind the CLPsych shared tasks and sentiment analysis tools.
* Sentiment models adapted from Hugging Face open-source libraries.
* Image - [Sleeping Cat on Her Back by Umberto Salvagnin](https://commons.wikimedia.org/wiki/File:Sleeping_cat_on_her_back.jpg#filelinks) / [CC BY 2.0](https://creativecommons.org/licenses/by/2.0)
