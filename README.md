# PostEra's Relative Ranking Model
**Big Idea**: Predict if compound A will be more or less active than compound B based on the differences in their fingerprint representation.
- Input: 2 SMILE strings
- Output: Probability of compound A having a higher activity than compound B

**Notebooks**

As you can see there are 4 notebooks in this repo.
- 'Create_Chemical_Classes.ipynb': This is specific to the Moonshot data where we extract just a noncovalent, acrylamide or infact a PLPro series. This notebook is likely not applicable to your data unless it is taken from Moonshot.
- 'Preprocess_data.ipynb': This is where we taken absolute potency data and convert it into relative activity data (with the added advantage of creating perfectly balanced class dataset). Both features (fingerprints) and targets (IC50) are converted into relative metrics between 2 compounds.
- 'FASTAI_model.ipynb': Here we leverage the FASTAI tabular model to take the data generated in the prior notebook and train a classification model.
- 'Model_Inference.ipynb': Here we take a trained model and run inference over a screening library. We create fingerprints diffs between known top actives and screening compounds and use the model to select promising compounds predicted to be more active than a set of the top known actives.
