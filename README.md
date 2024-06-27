# Speech-to-Speech Model
Function that takes in an audio file and outputs a summarized audio file using various models from HuggingFace


This is a short, entry-level function that takes in an audio file, transcribes it, summarizes the text, then outputs a TTS representation of the summary. All models and datasets used come from the HuggingFace library, and most implementations follow the examples given in the NLP and Audio courses on HF.

Necessary packages:
transformers
datasets
IPython.display
torch
gradio
soundfile
ffmpeg

# Step 1: Automatic Speech Recognition (ASR)
Model used: openai/whisper-large-v3<br/>
Check file for implementation

# Step 2: Text Summarization (TSum)
Model used: google/flan-t5-xl<br/>
Prompt used: "summarize : " + text from step 1<br/>
Check file for implementation

# Step 3: Text-to-Speech (TTS)
Checkpoint used: microsoft/speecht5_tts<br/>
Dataset used: Matthijs/cmu-arctic-xvectors<br/>
Vocoder used: microsoft/speecht5_hifigan<br/>
Check file for implementation

Expected input is an audio file, and an audio playback will be outputted, which can be modified to be outputted to a file if desired.

Links to the HF NLP and Audio courses for more information:<br/>
https://huggingface.co/learn/nlp-course/chapter0/1<br/>
https://huggingface.co/learn/audio-course/en/chapter0/introduction
