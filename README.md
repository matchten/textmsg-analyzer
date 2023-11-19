# Text Message Sentiment Analyzer
Uses sentiment analysis to predict whether the other user finds the conversation positive, neutral, or negative. Classifier consists of a finetuned RoBERTa model originally trained on twitter sentiment analysis data. To view the model card, see https://huggingface.co/matchten/text-message-analyzer-finetuned. To deploy the model directly, use either of the following methods:
```python
# Use a pipeline as a high-level helper
from transformers import pipeline

pipe = pipeline("text-classification", model="matchten/text-message-analyzer-finetuned")
```
```python
# Load model directly
from transformers import AutoTokenizer, AutoModelForSequenceClassification

tokenizer = AutoTokenizer.from_pretrained("matchten/text-message-analyzer-finetuned")
model = AutoModelForSequenceClassification.from_pretrained("matchten/text-message-analyzer-finetuned")
```
