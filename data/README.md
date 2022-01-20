### Data

Since we are unable to release the Newsela data publicly due to their copyright terms, we release the starting and bigram ending of each identified elaboration in our corpus. For a given elaboration, we identify the start and end bigram, as well as the sentence and document number in the Newsela corpus. Please contact us if you have any questions. 

Each of the split folders contains a `json` file with the following fields:

<ul>
  <li> `elaboration_identifier`: This is in the form `<newsela_doc_number>.<sentence_number_in_doc>`. </li>
  <li> `newsela_document_number`: Document number within the Newsela corpus.</li>
  <li> `sentence_number`: Sentence number within the document. </li>
  <li> `start_bigram`: Starting bigram of our identified elaboration for identification within the document. </li>
  <li> 'end_bigram`: Ending bigram of our identified elaboration for identification within the document. </li>
  <li> `crowd_annotations`: List of dictionaries of the annotations we elicited from crowdworkers on the Amazon Mechanical Turk platform. For the val/test splits, this field will be empty, since those annotations were elicited from expert annotators. Each dictionary corresponds to an annotation and has the following fields: 
  	<li> `worker_id_anon`: An anonymized worker ID for the particular annotator. </li>
  	<li> `is_addition`: The annotation for whether or not the worker identified this particular elaboration as a true elaboration or not. </li>
  	<li> `explanation`: The explanation for the annotator's contextual specificity rating. </li>
  	<li> `contextual_specificity_level`: The contextual specificity rating given by the annotator. A value of -1 means that the crowdworker did not provide a rating. </li>
  </li>
  <li> `split`: Specific data split (train, val, test). </li>
  <li> `contextual_specificity_label`: Aggregated (or in the case of val/test, expert) label. </li>
</ul> 
