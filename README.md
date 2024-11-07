# adress_parsing

The task in this notebook is to train a model to correctly label the different parts of a mailing adress, in particular the street number, the street name, the postal code and the city name. The data used for training comes from Spain's statistics institute. I chose sequential algorithm to treat this problem, that is conditional random fields (CRF) and Spacy's NER component, which consists of a shift-reduce parsing algorithm. In order to add robustness to the models, I used data augmentation where I switch the position of the adress parts. The results obtained are very high, that is superior to 0.99 accuracy. Further work could be to add variations in the test data to better verify the models robustness.  

### Dependencies

pandas, sklearn-crfsuite, spacy

### Notes

The notebook ends with a download of spanish word embeddings to enhance features for the CRF. Considering the high results obtained, I didn't finish implementing it.  
I also added an implementation of Spacy NER module with a description of the algorithm and the performances over a few batches of training. A full epoch on the dataset took hours to complete and gave results above 0.99 f-score. Considering the CRF already has very high results, Spacy's NER full epoch is not displayed in the notebook.  
These two neural architectures would be worth implementing in a more complex task. Maybe adding extra variations on the test data, unseen by the model, would require these implementations to achieve high results. 
