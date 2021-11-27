# FloDial: Flowchart Grounded Task Oriented Dialogs 


<table bgcolor=#0f62fe>
  <tr>
    <td width="22%" align="left">
      <img src="https://dair-iitd.github.io/FloDial/logo-iit.png" alt="IIT-D" style="max-width: 60%;">
    </td>
    <td>
      <div class="row" align="center">
        <div class="col-md-12">
          <!--<h1 id="appTitle">FloDial</h1>-->
          <img src="https://dair-iitd.github.io/FloDial/flodial.png" alt="FloDial" style="max-width: 100%;">
        </div>
      </div>
    </td>
    <td width="25%" align="right">
        &nbsp;&nbsp;&nbsp;&nbsp;<img src="https://dair-iitd.github.io/FloDial/core_gray10_on_blue60.svg" alt="IBM" style="max-width: 75%;">
    </td>
  </tr>
</table>

Flowchart Grounded Dialog Dataset (FloDial) is a corpus of troubleshooting dialogs between a user and an agent collected using Amazon Mechanical Turk. The dataset is accompanied with two knowledge sources over which the dialogs are grounded: (1) a set of troubleshooting flowcharts and (2) a set of FAQs which contains supplementary information about the domain not present in the flowchart. FloDial consists of 2,738 dialogs grounded on 12 different troubleshooting flowcharts.

## Data Splits

We create two different splits of the dialogs in FloDial. In the Seen Flowcharts (*S-Flo*) split, the test dialogs are grounded on flowcharts seen at train time. This split can be used to study the ability of a dialog system to generate responses by following flowchart and FAQs. In the Unseen Flowcharts *U-Flo* split, the test dialogs are grounded on new flowcharts that were unseen during train. This split is used to study the ability of dialog system to generalize to flowcharts unseen during train in a zero-shot flowchart grounded response generation setting.

This reposirtory only contains the dialogs in the train and the validation sets. The test sets are hidden. To measure the accuracy of your model on the test set, we are in the process of seting up an evaluation page where you can submit your model to compute test metrics (such as BLEU, Recall@1 and Success Rate).

If you wish to measure any other metric, please contact us and we will be happy to add that as a part of the evaluation.

## Data Structure

The collected dialogs are present in the `dialogs` folder and the associated knowledge sources (flowcharts and FAQs) are present in the `knowledge-sources` folder.

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
