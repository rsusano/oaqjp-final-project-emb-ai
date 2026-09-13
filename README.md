# Emotion Detector

**by Rafael Susano**

AI-powered Flask web app that analyzes text and reports emotion scores (anger, disgust, fear, joy, sadness) plus the dominant emotion.

Built as the final project for IBM’s **Developing AI Applications with Python and Flask** (Coursera / IBM Full Stack path).

**GitHub:** [https://github.com/rsusano/oaqjp-final-project-emb-ai](https://github.com/rsusano/oaqjp-final-project-emb-ai)

---

## What it does

1. Open the web UI and enter customer-feedback style text  
2. The app calls an IBM Watson NLP Emotion Predict endpoint  
3. You get confidence scores for five emotions and the **dominant** one  
4. Empty / invalid input returns a clear error message  

Useful as a small demo of wrapping an NLP API in a Python web service.

---

## Features

- Flask server with `/` (UI) and `/emotionDetector` (API)
- Watson NLP emotion prediction (Skills Network lab endpoint)
- Error handling for blank / invalid text (`400` → friendly message)
- Unit tests for joy, anger, disgust, sadness, and fear
- Packaged `EmotionDetection` module for reuse

---

## Stack

- **Python**
- **Flask**
- **IBM Watson NLP** (embeddable Emotion Predict API)
- **Requests**
- **unittest** + **pylint**

---

## Run locally

```bash
pip install -r requirements.txt
python test_emotion_detection.py
python server.py
```

Open [http://localhost:5000](http://localhost:5000).

> The Watson lab endpoint is provided by IBM Skills Network. It may require network access consistent with the course environment.

---

## API

| Method | Path | Purpose |
|--------|------|---------|
| GET | `/` | Web UI |
| GET | `/emotionDetector?textToAnalyze=...` | Emotion analysis |

Example:

```text
/emotionDetector?textToAnalyze=I%20am%20glad%20this%20happened
```

---

## Project structure

```text
├── EmotionDetection/          # emotion_detector package
├── templates/                 # Flask HTML
├── static/                    # frontend script
├── server.py                  # Flask app
├── test_emotion_detection.py  # unit tests
└── requirements.txt
```

---

## Course context

Final project for **Developing AI Applications with Python and Flask** in the IBM professional certificate path. Companion portfolio piece to [CodeCraftHub](https://github.com/rsusano/codecrafthub) (Next.js + Gemini).

---

## License

See [LICENSE](./LICENSE) (project template license from the IBM Skills Network starter).
