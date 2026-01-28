# Text Tutor: Getting Texts to Make Sense

This application provides a simple and intuitive user interface that helps understand a text by providing additional cues. Word-level cues like Part-of-Speech (ADJ, NOUN, VERB, etc.) or grammatical function (subj, obj, indirect obj, etc.) are invoked by default, while additional functionalities like translation (using GoogleTranslate) and rephrasing (using OLLaMa's mistral model) can be leveraged on demand.

## Overview
This is a **local-first application** designed to run on the user's machine.
It uses:
- Flask (backend)
- React (frontend)
- SQLite (local DB)
- Ollama (local LLM)

No cloud services required.

## Quick Start (Local)

1. Clone:
   git clone https://github.com/dominic-fischer/Text-Tutor.git
2. Install Dependencies + Run:
   python main.py

Optional:
1. Install Ollama: 
   https://ollama.com/download
2. Pull a model:
   ollama pull llama3


## Demo

![Login Demo](./screenshots/Login.gif)


## Usage Instructions

Once the application is open in your browser, you can log in on the "Sign In" page or input a text on the "Home" page. If you are signed in, your past requests will be saved in the database and can be retrieved quickly. 
After copying or writing text into the input box, you can click the "Submit" button. This will process the text, which might take a few dozens of seconds.

A new box will then appear with the processed text. Upon hovering over individual words, additional information such as Part-of-Speech tags and grammatical function will be displayed.

For additional information - such as translation or rephrasing of (parts of) sentences, as well as getting definitions and synonyms for individual words - the text on which the action should be performed needs to be selected in the **input window**. Upon doing that, a context menu will appear (in case it does not, you can open it by right-clicking), where the desired action can be performed by hovering over it. In order to close the context menu, hover over "Hide".

The results of context-menu actions will appear in the corresponding boxes further below.
