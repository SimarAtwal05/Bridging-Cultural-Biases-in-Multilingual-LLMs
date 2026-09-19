In Stage 3, we generate multilingual responses using multiple baseline models to analyze cross-lingual consistency and potential cultural variation.


1. Input

We already had:

English question
Hindi version
Tamil version
Telugu, Malayalam, Punjabi, Nepali

👉 All are the same meaning, just different languages

2. We used 3 AI models
mT5
BLOOM
IndicBART

👉 Think of them as 3 different students answering the same question

3. We asked each model:

👉 “Give answer in this language”

Example:

Hindi prompt → answer in Hindi
Tamil prompt → answer in Tamil
4. Models generated answers

So for one question, we now have:

English answer
Hindi answer
Tamil answer
… (for all languages)
AND from 3 different models
5. We saved everything

👉 All outputs stored in one CSV file