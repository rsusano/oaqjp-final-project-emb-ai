# Emotion Detector — Submission Guide

**Repo:** https://github.com/rsusano/oaqjp-final-project-emb-ai  
**Passing score:** 12/16 (75%)

> **Important:** Watson NLP API only works in **IBM Skills Network Cloud IDE**.  
> Run tests and take screenshots there after pushing code.

---

## Q1 — GitHub README URL

```
https://github.com/rsusano/oaqjp-final-project-emb-ai/blob/main/README.md
```

---

## Cloud IDE commands (run in terminal)

### Task 2 — Import and test emotion_detector

```bash
python3
```

```python
from EmotionDetection.emotion_detection import emotion_detector
emotion_detector("I love this new technology.")
exit()
```

### Task 3 — Test formatted output

```python
from EmotionDetection.emotion_detection import emotion_detector
print(emotion_detector("I am so happy today!"))
exit()
```

### Task 4 — Validate package

```bash
python3 -c "import EmotionDetection; print('EmotionDetection is a valid package')"
```

**Q4 URL:**
```
https://github.com/rsusano/oaqjp-final-project-emb-ai/blob/main/EmotionDetection/__init__.py
```

### Task 5 — Run unit tests

```bash
python3 test_emotion_detection.py
```

### Task 6 — Deploy Flask app

```bash
python3 server.py
```

Open `http://localhost:5000`, enter text, click **Run Sentiment Analysis**.  
Take screenshot → save as **`6b_deployment_test.png`**

### Task 7 — Error handling test

With server running, submit **blank text** in the web form.  
Should show: `Invalid text! Please try again.`  
Take screenshot → save as **`7c_error_handling_interface.png`**

### Task 8 — Pylint (aim for 10/10)

```bash
python3 -m pylint server.py
```

---

## GitHub file URLs for code questions

| File | URL |
|------|-----|
| emotion_detection.py | https://github.com/rsusano/oaqjp-final-project-emb-ai/blob/main/EmotionDetection/emotion_detection.py |
| __init__.py | https://github.com/rsusano/oaqjp-final-project-emb-ai/blob/main/EmotionDetection/__init__.py |
| test_emotion_detection.py | https://github.com/rsusano/oaqjp-final-project-emb-ai/blob/main/test_emotion_detection.py |
| server.py | https://github.com/rsusano/oaqjp-final-project-emb-ai/blob/main/server.py |

---

## Submission order

1. Push code to GitHub (done)
2. Open **Skills Network Cloud IDE** lab
3. Clone your fork: `git clone https://github.com/rsusano/oaqjp-final-project-emb-ai.git`
4. Run commands above, capture terminal outputs + 2 screenshots
5. **Launch App** on Coursera → paste answers into Mark grader
