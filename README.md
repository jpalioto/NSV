# NSV_Hackfest


Work done for the ML model during the Microsoft Hackfest 2018.


### File Descriptions
- **behavior.csv**: table with the behavior types the team manually extracted from the literature.
- **input_label.npy**: 2D numpy data object that houses the labels for the LSTM supervised learning experiment.
- **input_vol.npy**: 3D numpy data object that houses the behaviors after have been cleaned and word2vec'd. The dimensions are:
  - dim1 ("rows"): # of words in the behavior, max 6, padded with 0s if less than 6.
  - dim2 ("columns"): # of behaviors in behavior.csv
  - dim3 ("depth"): the word2vec encoding of each word using google's pretrained _GoogleNews-vectors-negative300.bin_, which is 300 units long.
- **InputLabel.ipynb**: notebook where the input_label.npy is prepared
- **lda**: notebook for exploratory LDA (Latent Drichilet Allocation) analysis for unsupervised learning of behavior semantics.
  - This did not work well, so we abandoned it for now
- **lemmatize.ipynb**: notebook where the lemmatization of the behaviors is prototyped.
- **lstm.ipynb**: notebook where an LSTM model is constructed and trained in Keras.
  - It uses the input_vol.npy and input_label.npy,
  - Performs a simple train/test split,
  - Ends with simple glance at the classification output.
- **model.h5**: a saved model created by the lstm.ipynb notebook.
- **NSV_Cleaning.ipynb**: a protoype for cleaning the training data
- **randomize_input.ipynb**: a prototype for randomizing input that is implemented in lstm.ipynb
- **w2v.ipynb**: notebook that transforms behavior.csv into input_vol.npy

### Data Folder
- **NoSchoolViolenceLabels.csv**: the file containing the behaviors and their labels, which were done by the team by hand.
