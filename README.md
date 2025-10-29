# Verbclasses in German Prose
This is a German annotated dataset of the Levin verbclasses as understood by Wordnet/Germanet. We annotated five different German prose texts. Below we list the number of annotations for each text.

|                       |   Annotator 1 |   Annotator 2 |   Annotator 3 | Fleiss' Kappa |
|:----------------------|--------------:|--------------:|--------------:|--------------:|
| Das Erdbeben in Chili |           666 |           725 |           677 |          0.64 |
| Der blonde Eckbert    |           898 |           930 |            54 |          0.85 |
| Die Judenbuche        |            52 |             0 |          2269 |          0.73 |
| Die Verwandlung       |          2296 |          2283 |            53 |          0.69 |
| Krambambuli           |           135 |             0 |           507 |          0.76 |


In the json file `annotation_data.json` contains all annotations in our dataset. The format of the file is as follows, where spans hold indices into the full text.

```json
{
  "Text Name": {
    "full_text": "The full text of the document", 
    "annotations" {"tag": ..., "author": ..., "spans": [(10, 15)]}
  }
}
```

In `splits` we give the data corresponding to the datasplits we used in our paper.
This data is intended for comparing against our experimental results.
```
splits
├── verb_classes_dev.jsonl       # Contains the development data, a stratified sample of all classes only taken from two texts ('Das Erdbeben in Chili' and ''Die Judenbuche'') 
├── verb_classes_dev_more.jsonl  # The rest of the data from ('Das Erdbeben in Chili' and ''Die Judenbuche'')
└── verb_classes_test.jsonl      # The test split, i.e. the texts that were not used in the development phase. ('Krambambuli', and 'Die Verwandlung', 'Der blonde Eckbert')
```


## License
This dataset is licensed under the **Creative Commons Attribution 4.0 International License (CC-BY 4.0)**.

To view a copy of this license, visit:
[http://creativecommons.org/licenses/by/4.0/](http://creativecommons.org/licenses/by/4.0/)

## Citation
Under this license, you are required to give appropriate credit. If you use this dataset in your research, please cite it as follows:

**Plain Text:**
Hatzel, Hans Ole, Haimo Stiemer, Evelyn Gius, and Chris Biemann. (2025). Scalable Verb-Based Literary Semantics. In *Proceedings of the Sixth Conference on Computational Humanities Research (CHR 2025)*. Luxembourg.

**BibTeX:**
```bibtex
@inproceedings{hatzel_scalable_2025,
  author    = {Hatzel, Hans Ole and Stiemer, Haimo and Gius, Evelyn and Biemann, Chris},
  title     = {Scalable Verb-Based Literary Semantics},
  booktitle = {Proceedings of the Sixth Conference on Computational Humanities Research (CHR 2025)},
  year      = {2025},
  address   = {Belval, Luxembourg}
}
```
