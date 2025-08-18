**Project Structure**

In order to run this project note:

1. *This GIT repository*
   Contains all code, the main notebook, and documentation required to run the pipeline.

2. *External Drive folder (not included in Git)*
   This includes:

   * check_points/ and compression_check_points/ folders — model files too large to store in Git.
   * Project reports, hyperparameter tuning logs, evaluation figures, and related artifacts.

Within this repository, the directory structure is organized as follows:


Desktop/DL/
│
├── data/
│   ├── Corona_NLP_train.xlsx
│   └── Corona_NLP_test.xlsx
│
├── lexicons/
│   ├── AFINN-11.txt
│   ├── MPQA.txt
│   └── NRC.txt
│
├── check_points/
│   ├── roberta_state_dict.pt
│   ├── roberta_full_model.pt
│   ├── distilbert_state_dict.pt
│   ├── distilbert_full_model.pt
│   ├── roberta_hf_best/                 # HuggingFace Trainer outputs (RoBERTa)
│   └── distilbert_hf_best/              # HuggingFace Trainer outputs (DistilBERT)
│
├── compression_check_points/            # Note there are no folders inside here. just all the checkpoint files
│                                          (the additional hirarchy is for clariffication)
│   ├── Quantized models/
│   │   ├── distilbert_quantized_full.pt
│   │   ├── distilbert_hf_quantized_full.pt
│   │   ├── roberta_quantized_full.pt
│   │   └── roberta_hf_quantized_full.pt
│
│   ├── Pruned models/
│   │   ├── distilbert_pruned_full.pt
│   │   ├── distilbert_pruned_state_dict.pt
│   │   ├── distilbert_hf_pruned_state_dict.pt
│   │   ├── roberta_pruned_only.pt
│   │   └── roberta_hf_pruned_state_dict.pt
│
│   └── TinyBERT distilled students/
│       ├── tinybert_student_full.pt
│       ├── tinybert_student_state_dict.pt
│       ├── tinybert_student_from_distilbert_full.pt
│       ├── tinybert_student_from_distilbert_state_dict.pt
│       ├── tinybert_student_full_from_distilbert_hf.pt
│       └── tinybert_student_full_from_roberta_hf.pt
│
└── Adv_DL - Final [IPYNB].ipynb


**Instructions for Model Files**

Due to their size, the following folders are *excluded from version control* and are *not included in the GitHub repository*:

* check_points/
* compression_check_points/

These directories contain full model checkpoints, HuggingFace Trainer outputs, and compressed models (quantized, pruned, and distilled variants).

To evaluate or continue working with the trained models, you must *manually copy these folders* from the shared Google Drive directory provided with the project. Place them inside the Project_Files/ directory exactly as shown above.

If necessary, update the file paths in Adv_DL - Final [IPYNB].ipynb to match your local directory structure.


**Alternative Setup**

Alternatively, the entire Desktop/DL folder — including model files, data, and notebook — can be downloaded directly from a mail we swnt, as well as the drive. 
As long as the original folder hierarchy is preserved, the notebook can be run locally without modification.

No installation or manual folder placement is required beyond ensuring dependencies are installed and paths remain consistent.


**Additional Files (For Completeness)**

The repository also includes the following files, which are *not required to run the pipeline*, but are provided for documentation, reproducibility, and grading purposes:
│
├── Adv_DL - Final [PDF].pdf            # Final notebook (PDF version)
├── Adv_DL - Final [Py].py              # Exported notebook as .py script
├── Optuna_Trials.zip                   # Logged results from hyperparameter optimization
├── Report [PDF].pdf                    # Final written report (PDF)
├── Report [Word].docx                  # Final written report (editable Word version)
