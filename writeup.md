{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# NLP & Classification of sentiment for Amazon luxury beauty product Reviews"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Introduction"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "In this project, we worked on a dataset which contains amazon luxury beauty product reviews. \n",
    "The aim of this project is to build an NLP model to find topics for each review. Along the way, we added the sentiment to build a classification model.\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Goals:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- Finding a topic for each review .\n",
    "- Building a classification model to determine the type of sentiment weather its positive or negative.\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Methodology:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "1- Loading the dataset.\n",
    "\n",
    "2- EDA (cleaning and visualizing the data).\n",
    "\n",
    "3- Building different topics Models.\n",
    "\n",
    "4- choosing the best topic model\n",
    "\n",
    "5- Building different classification Models.\n",
    "\n",
    "6- choosing the model based on given best f1 to prediction."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Dataset:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "We used the dataset from  https://nijianmo.github.io/amazon/index.html#\n",
    "The dataset contains  34278 reviews (rows) and 12 columns in total.\n",
    "\n",
    "### Cleaning Data and preprocessing  :\n",
    "- Removing Null \n",
    "- Strip columns name \n",
    "- Removing outliers \n",
    "- Removing unwanted columns \n",
    "- spellcheck for text review \n",
    "- Lemmatize for text review \n",
    "- Add new columns for date by induvial \n",
    "- Adding sentiment column \n",
    "- Adding new two columns for the review length and the words counts\n",
    "- Covert text to CountVectorizer\n",
    "- Covert text to TfidfVectorizer\n",
    "- Feature Extraction Using svd , variance=.86\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Topic modelling :"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- Frist, we used LSA model to try and find topics from the data, we tried with different numbers of topics from 2 to 10 but were not successful.\n",
    "- then, we used LDA model to try and find topics instead of LSA, we tried with different numbers of topics from 2 to 10 but were not successful.\n",
    "- Finally, we used Corex which gave us some sensible topics, but they were interlinked so much that we had to use anchors to try to force the model to focus on a sensible topics.\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Classification:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "On this dataset we used different methods of classification to determine the type of sentiment weather its positive or negative :\n",
    "\n",
    "    \n",
    "- Descion Tree model.\n",
    "- Logistic regression model.\n",
    "- Random forest model.\n",
    "- XGradient boosting model.\n",
    "    "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Conclusion :"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- Our best topic modeling is Corex\n",
    "- Using over sampling to solve in balance data reduced  our f1 score \n",
    "- Our best classifier is XGBClassifier"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Future work:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- collect more reviews for different products.\n",
    "- build a recommendation system for each user .\n",
    "- Try  more classifiers .\n",
    "- Build classification model to predict the topic of each review .\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Tools:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "\n",
    "\n",
    "- Matplotlib.\n",
    "- Seaborn.\n",
    "- SQLite.\n",
    "- Pandas.\n",
    "- sklearn.\n",
    "- json.\n",
    "- dateTime.\n",
    "- numpy.\n",
    "- re.\n",
    "- textBlob.\n",
    "- String.\n",
    "- nltk.\n",
    "- pickle.\n",
    "\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.7.4"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
