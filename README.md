This exercise focused on creating a **Bag of Words (BoW) model** from **web-scraped text**. 

Here's a summary of the steps we took:

**Web Scraping and Initial Setup:** We started by importing necessary libraries (nltk, numpy, BeautifulSoup, urllib.request, re). We then scraped an article from IBM's website on Data Science, extracted its text content, and performed initial cleaning by converting it to lowercase and removing punctuation.

**Text Tokenization and Preprocessing:** The cleaned text was then tokenized into individual sentences using nltk.sent_tokenize.

**Word Frequency Analysis:** We manually calculated the frequency of each word in the corpus and identified the 200 most frequent words using Python's heapq library. This set of words formed our vocabulary for the Bag of Words model.

**Bag of Words Model Creation:** We constructed a Bag of Words representation where each sentence was converted into a binary vector. Each position in the vector corresponded to one of the top 200 words, with a 1 indicating the presence of the word in the sentence and 0 indicating its absence.

**Bag of Words Model Creation (Scikit-learn):** To demonstrate a more efficient approach, we then used sklearn's CountVectorizer. This tool automatically handles tokenization, counting, and vocabulary creation, generating a matrix where each row is a sentence and each column is a word from the vocabulary, with values representing the count of that word in the sentence.

**Data Visualization:** Finally, we converted the CountVectorizer output into a pandas DataFrame (bow_df) for better readability and inspection, with sentences as indices and words as columns.
