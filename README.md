# NLP-NER

Analyze the organization name recognition system and dataset annotations.

Tools used:
Python 3.7.3 = used a programing language 
spaCy 2..2.4 = used to evaluate the NER models 
en_core_web_sm model to rn analysis on given datasets 
Jupyterlab 2.1.2 = used to test and run scripts in Notebooks 


Results:
I was able to read and run analysis on the Ontonotes.json dataset, using spaCy’s en_core_web_sm model
I was not able to evaluate the Enron sentences,json dataset. I was able to read and print the file I have tried all spaCy’s models I could find. The script was breaking when trying to iterate through the Json objects using :
f = open ('/Users/l_parau/Enronsentences.json', "r")
TEST_DATA = json.loads(f.read())
test_sentences = [x[0] for x in TEST_DATA[0:5]]
I was getting this error:
----> 9 test_sentences = [x[0] for x in TEST_DATA[0:5]]

One thing I noticed is that the Enronsentences.json objects are formatted differently, having an extra { “text”: in the beginning. 
After some research I found out that it is consistent with the spaCy’s other annotation tool, Prodigy, which does not have a free version. I have tried finding ways to either read the json differently or top converted into spaCy’s format, butI did not succeed. 
I was unable to analyse more datasets from either of the two generic target domains, OntoNotes 5.0 dataset or https://www.cs.cmu.edu/~enron. The OntoNotes5.0.zip was not extracting (I don’t know if it was the size of the zip, ~1.5gb) whie for  https://www.cs.cmu.edu/~enron, my account either did not have sufficient credentials or I was doing something wrong, because I was not able to download additional datasets. 
For the NER annotation analysis on the Ontonotes.json dataset:
OntoNotesMetrics.ypinb runs a script to calculate the Precision, Recall and F1-score for the model 
OntoNotesScorer.ypinb uses spaCy’s scorer method to display the scores for entities in Ontonotes.json    
For the ORG entity analysis I was unsuccessful in getting conclusive results, even after trying to adapt scripts found on various platforms, like Git repositories, Stackoverflow, etc.


 
