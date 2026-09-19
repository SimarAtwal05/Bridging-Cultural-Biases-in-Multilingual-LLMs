We compared multilingual model responses using similarity scores to measure how consistent their meaning is across different languages.

1️⃣ We asked the SAME question in many languages

Example:

English
Hindi
Tamil
Telugu
etc.
2️⃣ We gave these questions to 3 different models
mT5
BLOOM
IndicBART

👉 Each model gave answers in different languages

3️⃣ Now we checked:

👉 “Are the answers saying the SAME thing or not?”

4️⃣ How we checked this?

We used:

A tool (SBERT) that converts sentences into numbers
Then compared them using similarity
5️⃣ What we calculated

For each model:

Compare English answer with Hindi, Tamil, etc.
Get a similarity score (how close meanings are)
6️⃣ Then we averaged it

👉 For each model we got ONE number:

High number → Same meaning across languages ✅
Low number → Different meaning (cultural bias) ❌