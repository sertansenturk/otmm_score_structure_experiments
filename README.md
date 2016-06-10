# otmm-score-structure-experiments
Structure Analysis Experiments on Ottoman-Turkish Makam Music Scores

This repository contains the experiments to find the optimal melodic and lyrics similarity threshold, conducted in the paper:

Şentürk, S., & Serra X. (2016). A method for structural analysis of Ottoman-Turkish makam music scores. In Proceedings of 6th International Workshop on Folk Music Analysis, (pp. XX–XX)., Dublin, Ireland.

For the details of the experiments, please refer to the paper.

The submodule [turkish_makam_section_dataset](https://github.com/MTG/turkish_makam_section_dataset/tree/score_section) stores the test scores in the SymbTr-txt format. The experiments folder have the experimental results and evaluation. Each folder in this folder stores the sections extracted from each score for the given threshold, e.g. folder "0_6" has the results obtained using a similarity threshold of 0.6 for both melodic and lyrical relationship computation. The extracted sections for each score are stored in a csv file, which has the same name as the SymbTr-name (makam--form--usul--name--composer) of the analyzed score. The fields are:

```
  start_note:         The starting note index in the SymbTr-txt score
  end_note:           The ending note index in the SymbTr-txt score
  name:               The basic semantic name of the section. Right now, it is the name 
                      (TESLİM, ARANAĞME...) annotated in the score for instumental sections or 
                      "VOCAL_SECTION" for vocal sections.	
  melodic_structure:  Melodic semiotic label
  lyric_structure:    Lyrical semiotic label	
  lyrics:             Lyrics of the section
  slug:               The processed version of "name" field with the Turkish characters and 
                      special characters handled.
```

results.json stores the evaluation and the statistics of the experiments.

To run the experiments you have to install Jupyter notebook and the [requirements](https://github.com/sertansenturk/otmm-score-structure-experiments/blob/master/requirements).

For additional information please contact the authors.
