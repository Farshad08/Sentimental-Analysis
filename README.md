# Sentimental-Analysis
from textblob import TextBlob

# Ask user to input a review
text = input("Please enter your review: ")

# Create a TextBlob object
blob = TextBlob(text)

# Get the sentiment
sentiment = blob.sentiment

print(f"\nSentiment Analysis Results:")
print(f"Polarity: {sentiment.polarity}")
print(f"Subjectivity: {sentiment.subjectivity}")

# Interpretation
if sentiment.polarity > 0:
    print("The sentiment is positive.")
elif sentiment.polarity < 0:
    print("The sentiment is negative.")
else:
    print("The sentiment is neutral.")
