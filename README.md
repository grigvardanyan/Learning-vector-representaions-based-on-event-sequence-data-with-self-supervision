# Master-s-project
<br>

## Structure of repo
- Task folder
- - data folder
- - notebooks<br>
### Gender classification
The **gender_classification folder**,  contains notebooks for data preprocessing, sparse matrix creation, training and necessary datasets.<br> 
Reason of different notebooks for data preprocessing and sparse matrix creation, is data preprocessing requires a lot of memory. After saving all necessary data you have to stop it and then run sparse matrix creation notebook.<br><br> 
**Note:** It is possible you will need to run for training and test data creation seperatly(shut down notebook after preprocessing of training or test data).

### CoLES: Contrastive Learning for Event Sequences with Self-Supervision 
The **CoLES** folder contains implementation of paper https://openreview.net/forum?id=tADlrawCrVU. <br/>

You can use **CoLES** to learn meneingfull data representation for each dataset( from other folders in repository).<br/> After learning meaningfull representation you can use learned embeddings for downstrim tasks.

Notebook contains as Neural Network as DataGenerator for it.<br/>

#### DataGenerator
**Input**
- **df**: Pandas Dataframe
- **group_column**: column based on which need to group data. E.g Client id
- **output_column**: output column for downstrim task.
- **column_order**: Dictinary which has categoricals and numericalsfileds, where each of one contains list of column names.
- **batch_size**
- **k**: count of sub-sequances
- **subseq_generator_type**: In future there will be many types of subsequance and pair genreators

#### CoLES NN
**Input**
- **categorical_embeddings_info**: categorcial feature name and embedding size. Tou can get it with DataGenerator.vocab_map
- **numerical_variables_info**: list of names numerical variables
- **input_length**: length of sub sequances. You can get if with DataGenerator.k
- **rnn_type**: 'simple','lstm','gru'
- **rnn_units**: number of neurons



