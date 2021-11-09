# Chatbot Deployment with Flask and JavaScript

This repo currently contains a custom chatbot I created  with Flask and JavaScript.

This gives 2 deployment options:
- Deploy within Flask app with jinja2 template
- Serve only the Flask prediction API. The used html and javascript files can be included in any Frontend application (with only a slight modification) and can run completely separate from the Flask App then.

## Initial Setup:


Clone repo and create a virtual environment
```
$ download the repository
$ cd chatbot-deployment
$ cond create -n env_name
$ conda activate env_name
```
Install dependencies
```
$ (env_name) pip install Flask torch torchvision nltk
```
Install nltk package
```
$ (env_name) python
>>> import nltk
>>> nltk.download('punkt')
```
Modify `intents.json` with different intents and responses for your Chatbot

Run
```
$ (env_name) python train.py
```
This will dump data.pth file. And then run
the following command to test it in the console.
```
$ (env_name) python chat.py
```

Now for deployment follow my tutorial to implement `app.py` and `app.js`.

## Credits:
This repo was used for the frontend code:
https://github.com/hitchcliff/front-end-chatjs
