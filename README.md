# FloDial: Flowchart Grounded Task Oriented Dialogs 

<p align="center">
  <img align="centre" height="150" src="https://dair-iitd.github.io/FloDial/flodial.png">
</p>

Flowchart Grounded Dialog Dataset (FloDial) is a corpus of troubleshooting dialogs between a user and an agent collected using Amazon Mechanical Turk. The dataset is accompanied with two knowledge sources over which the dialogs are grounded: (1) a set of troubleshooting flowcharts and (2) a set of FAQs which contains supplementary information about the domain not present in the flowchart.

## Data Splits

We create two different splits of the dialogs in FloDial. In the Seen Flowcharts (*S-Flo*) split, the test dialogs are grounded on flowcharts seen at train time. In the Unseen Flowcharts *U-Flo* split, the test dialogs are grounded on new flowcharts that were unseen during train.

This reposirtory only contains the dialogs in the train and the validation sets. The test sets are hidden. We are in the process of seting up an evaluation page where you can submit your model and get the performance on the hidden test set (such as BLEU, Recall@1 and Success Rate).

## Data Structure

The collected dialogs are present in the `dialogs` folder and the associated knowledge sources (flowcharts and FAQs) are present in the `knowledge-sources` folder.

### Dialogs
All the dialogs are present in `dialogs.json`. The *S-Flo* and the *U-Flo* split are mentioned in the `s-flo.json` and `u-flo.json` respectively.

Each dialog is a key-value pair, where the key represents the `dialog-id` and the value contains the actual dialog. The value has the following structure:
- **utterences**: a list of utterances in the dialog. Each utterance has the following structure
  - **speaker**: speaker of the utterance (user/agent)
  - **utterance**: the utterance text
  - **turn_id**: indicate the turn in the dialog
  - **grounded_doc_id**: points to the node in the flowchart or FQA on which the utterance is grounded on 
- **flowchart**: contains the name of the flowchart on which the dialog is grounded on. This should match the `name` attribute of the flowchart present in the `knowledge-sources` folder. 

## Citation
Please cite the following paper if you use this dataset in your work 

```
@inproceedings{raghu-etal-2021-end,
    title = "End-to-End Learning of Flowchart Grounded Task-Oriented Dialogs",
    author = "Raghu, Dinesh  and
      Agarwal, Shantanu  and
      Joshi, Sachindra  and
      {Mausam}",
    booktitle = "Proceedings of the 2021 Conference on Empirical Methods in Natural Language Processing",
    month = nov,
    year = "2021",
    address = "Online and Punta Cana, Dominican Republic",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2021.emnlp-main.357",
    pages = "4348--4366",
}
```

## Contact Us

If you have any questions please raise a [GitHub issues](https://github.com/dair-iitd/FloDial/issues) or contact the authors.
