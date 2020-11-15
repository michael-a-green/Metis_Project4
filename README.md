

# Automatically Understanding Customer Feedback

## Description

This project demonstrates [natural language processing](https://en.wikipedia.org/wiki/Natural_language_processing) can
be used to automatically identify specific messages customers send to product
developers about their products using unsolicted data.

Specifically, this project employs [topic modeling](https://en.wikipedia.org/wiki/Natural_language_processing) of a large set of prose text
product reviews.

## Data Used

The data set used in the project is the [Amazon Fine Foods Reviews](https://www.kaggle.com/snap/amazon-fine-food-reviews). This data
set is composed of 568,454 reviews from 256,059 reviewers on nearly 75,000
different products, primarily foods.

## Brief Overview of NLP Pipeline Used to Perform Topic Modeling

The project takes a large corpus of prose text reviews and performs
unsupervised learning analysis of the reviews. By doing so it creates a structural model
which serves as an abstraction of the latent properties of said corpus. This
structure is then used to identify specific subjects mentioned in the 
corpus. The topic modeling quantifies the prevalence of the concepts in the underlying corpus. So a user can
not only know what is being said in the corpus but also be able to numerically
understand the significance of the subject matter. It also enables relating one
subject matter to another such as knowing if two subjects are similar and to
what degree they are similar.

Also based on the methodology employed in this project, a user of the
information can, for a specific subject, compare and contrast both highly
positive and negative points of view by the same said subject. This enables a
person to quickly determine what users either like or dislike about any of the
products covered by the underlying corpus.

Below are diagrams of the NLP pipeline used to perform the topic modeling:


![Text Preprocessing](./Documents/Images/text_preprocessing.jpg "Text Preprocessing" )
<span class="caption">_Text Preprocessing_</span>


![TFIDF Vectorization](./Documents/Images/tfidf_vectorization.jpg "TFIDF Vectorization" )
_[TFIDF](https://en.wikipedia.org/wiki/Tf%E2%80%93idf) Vectorization_

![LDA and Final Analysis](./Documents/Images/lda_analysis.jpg "LDA and Final Analysis" )
_[LDA](https://en.wikipedia.org/wiki/Tf%E2%80%93idf) and [PCA](https://en.wikipedia.org/wiki/Tf%E2%80%93idf) to identify topics and visualize document relationships
overlaid with per document topic assignment.


## Tools Used

* Kaggle: Initial data set
* python `re`: Used regular expressions to clean HTML and other strings that
  would have hampered downstream analysis of the text corpus
* pandas: For cleaning and analysis of topic-modeling results
* numpy: Analysis of topic modeling results
* NLTK: Perform tokenization (splitting into words) and
  [lemmatization](https://en.wikipedia.org/wiki/Lemmatisation) of the original text corpus and cleaning (removal of non-English words).
* sklearn: To perform TFIDF vectorization of the documents, LDA of the
  vectorized documents, and PCA that enabled visualization of the documents,
  topics, and their relationships to the underlying text.
* matplotlib: Used to visualize the underlying text corpus, the calculated
  topics, and their relationships
* seaborn: Visualization
* pyLDAvis: To perform several visualizations of the resultant topic model in
  relationships to the text corpus.

## Description of Files

* `Source/Project4.ipynb`: The jupyter notebook for the project
* `Documents/Link_to_Presentation.md`: Markdown file that has a link to the
  presentation.
* `Doucments/Images`: Images used to in this file or other files for
  documentation purposes

## Steps To Reproduce This Project

1. Clone this repo
1. Run this command: `conda env create -f Source/project4_venv.yml`
1. Once that's done and you have activated your virtual environment you should
   be able to start jupyter lab with this command: `jupyter lab`
1. With Jupyter Lab, open the notebook `Source/Project4.ipynb`
1. You should be able to run the cells. Please note that the default settings
   of the notebook require pkl files of the cleaned data. Please contact me
   if you want that data. Depending on the option settings in the notebook,
   you can run the cells reproduce this information from scratch. Note you
   will have to download the CSV file associated with the data set.



