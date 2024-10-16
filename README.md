# adress_parsing

The task in this notebook is to train a model to correctly label the different parts of a mailing adress, in particular the street number, the street name, the postal code and the city name. The data used for training comes from Spain's statistics institute. I chose sequential algorithm to treat this problem, that is conditional random fields (CRF) and Spacy's NER component, which consists of a shift-reduce parsing algorithm. In order to add robustness to the models, I used data augmentation where I switch the position of the adress parts. The results obtained are very high, that is superior to 0.99 f-score. Further work could be to add variations in the test data to better verify the models robustness.  

### Dependencies

pandas, sklearn-crfsuite, spacy
