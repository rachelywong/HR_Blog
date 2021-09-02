---
title: Processed Makes a Come Back
subtitle: NLP to The Rescue
alt: 

caption:
  title: Processed Makes a Come Back
  subtitle: NLP to The Rescue
  thumbnail: https://github.com/rachelywong/HR_Blog/raw/master/assets/img/portfolio/project6/nlp.png
---
Processed Makes a Come Back

What is NLP?

NLP is natural language processing. It’s a way for machines to understand and make sense of human language - in this case, English. NLP is extremely powerful because the technology around us is driven by our interactions. Our interactions take form in Tweets, Instagram posts, ecommerce reviews and more. You’ll notice that all these interactions are done over text. NLP allows machines to parse these bits of text and draw out information like topics, sentiment and anomalies in ways that humans cannot easily replicate. 

The Basic Mechanics of Preprocessing

Typically, the first step in NLP is cleaning the data. There’s a few common approaches listed below but the overarching principle is that we want to make different variations of text that mean the same thing, as similar as we can. 

Basic preprocessing: Removing punctuation, lower casing everything, removing digits, expanding contractions (i.e. don’t → do not) 

Stemming: This is the process of cutting off suffixes and prefixes of words to that words with roughly the same meaning are representing the same. 

	Ex// Walking → Walk 
	Ex// Walked → Walk

Lemmatization: This is a smarter version of stemming. Instead of just blindly chopping off the beginning and the end, we take into account the morphological meaning.

	Ex// Studies → Study
	Ex// Studying → Study

	If we had used stemming instead of lemmatization, we would have:

	Ex// Studies → Studi
	Ex// Studying → Study 
Stop words: This is the process of removing very common words that don’t necessarily have value. For example, “the” is bound to come up endlessly in most English texts. Removing this word, likely has no impact on our interpretation of the topic.

After preprocessing, a piece of text can transform from:

```Wow! This laptop is incredible. I can’t believe it was on sale. I’m buying another one.” ```

To

```wow laptop incredible. i cannot believe on sale. i am buy another one.```

You can see that the text is much shorter but the general semantic meaning is still preserved. There’s a number of common packages such as `spaCy` and `gensim` that can handle all of this preprocessing.


Creating the Dictionary

The next step is typically taking the transformed text and building a dictionary. All this means is that we’re taking all the words we’re left with post processing and using it to define the entire universe of all the words we know. So the example above, `incredible` was mentioned once, `I` was mentioned twice and so forth. The dictionary helps us understand the frequency of all the words used.

Modeling the Data

Once we have the dictionary, there’s a number of different models we can feed this data into. We can learn things about our text such as:
Sentiment For example, are my customer reviews typically negative or positive? Which words contribute to that?
Topics: What are my customers typically talking about? Perhaps shipping issues or stock outs are a common issue.
Anomalies: Are there events that are outliers? For example, maybe the latest customer reviews are excessively long - perhaps a product malfunction?

At the end of the day, machines are not that smart, but they are great at doing computations of scale. We preprocess text to help machines consolidate the amount of information they need to take in. We create dictionaries to define the universe of words that are applicable to us. And finally, we use the relevant model to help us find the insights we need about text data. There’s much more to NLP but the TDLR is: We help machines understand text in the way humans interpret it so they can help us extract large scale insights. 


{:.list-inline}
- Date: July 2021
- Category: NLP

