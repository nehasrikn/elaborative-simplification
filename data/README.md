### Data

Since we are unable to release the Newsela data publicly due to their copyright terms, we release the starting and bigram ending of each identified elaboration in our corpus. For a given elaboration, we identify the start and end bigram, as well as the sentence and document number in the Newsela corpus. Please contact us if you have any questions. 

Each of the split folders contains a `json` file with the following fields:

+ `elaboration_identifier`: This is in the form `<newsela_doc_number>.<sentence_number_in_doc>`. <br>
+ `newsela_document_number`: Document number within the Newsela corpus. <br>
+ `sentence_number`: Sentence number within the document.
+ `start_bigram`: Starting bigram of our identified elaboration for identification within the document. <br>
+ `end_bigram`: Ending bigram of our identified elaboration for identification within the document. <br>
+ `split`: Specific data split (train, val, test). <br>
+ `contextual_specificity_label`: Aggregated (or in the case of val/test, expert) label. <br>
+ `crowd_annotations`: List of dictionaries of the annotations we elicited from crowdworkers on the Amazon Mechanical Turk platform. For the val/test splits, this field will be empty, since those annotations were elicited from expert annotators. Each dictionary corresponds to an annotation and has the following fields: 
  	+ `worker_id_anon`: An anonymized worker ID for the particular annotator. <br>
  	+ `is_addition`: The annotation for whether or not the worker identified this particular elaboration as a true elaboration or not. <br>
  	+ `explanation`: The explanation for the annotator's contextual specificity rating. <br>
  	+ `contextual_specificity_level`: The contextual specificity rating given by the annotator. A value of -1 means that the crowdworker did not provide a rating. <br>
