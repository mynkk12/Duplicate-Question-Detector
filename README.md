Duplicate Question Detector

<img width="1039" height="527" alt="image" src="https://github.com/user-attachments/assets/67db81f1-3c6d-4b33-b440-eec80c612c86" />


An NLP-powered web app that detects whether two questions are semantically identical, built on the Quora Question Pairs dataset.


Overview
QuoraMirror uses machine learning and natural language processing to determine if two questions carry the same intent — a problem at the heart of large Q&A platforms like Quora, Stack Overflow, and community forums. Duplicate questions fragment knowledge and waste readers' time; this model helps surface them automatically.
The app is live as a Streamlit web interface: paste two questions, hit Find, and instantly get a Duplicate or Not Duplicate verdict.

Features

Text preprocessing — contraction expansion, HTML stripping, special character normalization
Hand-crafted NLP features:

Token overlap ratios (stopwords vs. non-stopwords)
Length-based features (absolute diff, average length, longest common substring)
Fuzzy string matching (QRatio, partial ratio, token sort & set ratio via fuzzywuzzy)


Bag-of-Words (BoW) representation using a pre-fitted CountVectorizer
Final feature vector of 22 engineered features + BoW for q1 + BoW for q2
Clean Streamlit UI — no setup required for end users


Tech Stack
LayerToolsLanguagePython 3Web AppStreamlitMLscikit-learnNLPNLTK, fuzzywuzzy, distance, BeautifulSoup
