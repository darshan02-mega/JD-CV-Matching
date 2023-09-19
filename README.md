# Objective:

Build a PDF extractor to pull relevant details from CVs in PDF format, and match them against the job descriptions from the Hugging Face dataset.

# Datasets Used:

We leveraged the Kaggle Resume Dataset, which comprises a vast collection of CVs in PDF format. Additionally, we tapped into the rich Hugging Face dataset, containing diverse job descriptions.

# PDF Extractor:

To kickstart the CV matching magic, we needed to extract valuable details from those pesky PDFs. We harnessed the power of the pdfplumber library to gracefully extract text from PDFs. Then, we embarked on a journey of taming the chaos within those CVs. We wrangled the relevant skills and education sections using Python regex, laying the groundwork for our matching wizardry. The extracted treasure trove of information was neatly organized into a CSV file, aptly named 'pdf1.csv.'

# Challenges Faced:

They always keep things exciting. While we conquered skills and education sections with regex, taming the wild beast of experience proved to be a formidable task. Extracting company names, start dates, and end dates from multiple headers within CVs was a puzzle that required more than just regex. 

# Proposed Solution:

Our future plans involve creating custom NER models for skills, education, and experience, but this requires curated datasets. This endeavor will provide a more robust solution to the extraction challenge we faced.

## CV-JD Matching:

Now, let's talk about the matchmaking! We sourced 15 job descriptions from the Hugging Face dataset to test our CV-JD compatibility algorithm. To ensure a level playing field, we cleaned the text, converting it to lowercase and removing pesky punctuations, emails, and phone numbers. For our secret sauce, we turned to DistilBertTokenizer and DistilBertModel from the mighty Transformers library to tokenize and embed JDs and CVs. Cosine similarity, a trusty tool from sklearn, was our weapon of choice for matching.

# Challenges Faced:

Venturing into PyTorch and the Transformers library for the first time was akin to diving into uncharted waters. But, the real adventure was in extracting the necessary data from the CVs, a puzzle more complex than the matching itself.

# Conclusion:

In the ever-evolving world of AI and NLP, our JD-CV Matching System is a beacon of hope for job seekers and hiring managers alike. As we continue to refine our algorithms, tackle the extraction enigma, and delve deeper into the world of machine learning, we inch closer to a future where job hunting and recruitment become a breeze.
