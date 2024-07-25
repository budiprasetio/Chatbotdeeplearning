Deploying a Chatbot with Flask and JavaScript

Deployment Options:

    1. Embed within a Flask App using Jinja2 Templates: You can integrate predictions directly into a Flask app that utilizes Jinja2 templates.
    2. Serve as a Standalone Flask Prediction API: You can run the prediction API separately. The HTML and JavaScript files can be included in any frontend application with minor modifications and will run completely independently from the Flask app.

## Initial Setup:
This repository currently contains the starter files

Clone repo and create a virtual environment
```
$ git clone https://github.com/budiprasetio/Chatbotdeeplearning
$ cd chatbot-deployment
$ python3 -m venv venv
$ . venv/bin/activate
```
Install dependencies
```
$ (venv) pip install Flask torch torchvision nltk
```
Install nltk package
```
$ (venv) python
>>> import nltk
>>> nltk.download('punkt')
```
Modify `intents.json` with different intents and responses for your Chatbot

Run
```
$ (venv) python train.py
```
This will dump data.pth file. And then run
the following command to test it in the console.
```
$ (venv) python chat.py
```

Now for deployment follow my tutorial to implement `app.py` and `app.js`.
