OUTPUT:   <img width="1919" height="992" alt="image" src="https://github.com/user-attachments/assets/0b15dce2-9508-4a0b-a571-efbaa888e900" />


This project is an AI-powered email analysis and response assistant built using Python. It allows users to upload a CSV file containing emails and automatically:

Classifies the sentiment of each email (Positive, Neutral, Negative).

Detects priority/urgency based on keywords (Urgent vs Not Urgent).

Generates professional draft replies using a Large Language Model (LLM).

It provides a Streamlit-based interactive interface, making it easy to process emails and visualize results in a table.

Features

Sentiment Analysis: Uses a pre-trained transformer model (cardiffnlp/twitter-roberta-base-sentiment-latest) to classify email body sentiment.

Urgency Detection: Detects critical or urgent emails using a keyword-based approach.

Automated Reply Generation: Uses google/flan-t5-small (T5-based LLM) to generate professional email responses.

Interactive UI: Streamlit interface allows users to upload CSV files and view processed email data.

Data Handling: Efficiently processes CSV files using pandas.

Tech Stack & Libraries

Python 3.10+

Streamlit: For building the web-based interactive UI.

Transformers (Hugging Face): For sentiment analysis and text generation.

cardiffnlp/twitter-roberta-base-sentiment-latest → sentiment classification

google/flan-t5-small → draft email generation

Pandas: For CSV reading and data manipulation.

Dataclasses: For structured email representation (EmailItem).

Other libraries: datetime, typing, os, re

Note: The project does not require NumPy explicitly, but transformers/pandas internally may use it.

How It Works

User uploads a CSV file with emails containing at least sender, subject, body, and sent_date columns.

The app iterates through each email:

Classifies the sentiment of the email body.

Detects if the email is urgent using predefined keywords.

Generates a professional draft reply using LLM.

Displays the processed results in a table, including:

Sender

Subject

Sentiment

Priority

Draft reply
