 README File for Indian Language Translation Project

---

 **Project Title:**  
**Evaluating Indian Language Translation Models: A Case Study with LLaMA 3.2 and IndicTrans2**

---

 **Project Description:**  
This project aims to evaluate the translation capabilities of large language models (LLMs) like LLaMA 3.2 and compare their performance with state-of-the-art models such as IndicTrans2. The evaluation focuses on Indian languages, leveraging the IN22-Conv dataset to compute BLEU scores for 22 Indic languages. The findings highlight the strengths and limitations of general-purpose models like LLaMA and specialized models like IndicTrans2 for Indian language translation tasks.

---

 **Key Features:**
- Evaluates the **translation performance** of LLaMA 3.2 405B and IndicTrans2 using BLEU scores.
- Focuses on **22 Indian languages**, including low-resource languages such as Santali, Bodo, and Dogri.
- Uses the **IN22-Conv dataset** for English-to-Indic translation benchmarks.
- Handles missing translations and aligns predictions with references dynamically.
- Provides insights into challenges with low-resource languages and future improvements for translation models.

---

 **Directory Structure:**

```
project_root/
├── data/                 Contains the IN22-Conv dataset files
├── translations/         JSONL files with machine-generated translations
├── results/              Stores BLEU scores and performance metrics
├── scripts/              Python scripts for data processing and evaluation
│   ├── compute_bleu.py   Main script for BLEU score computation
│   ├── preprocess.py     Script for preprocessing translations
│   └── utils.py          Helper functions
├── README.md             Project description and usage guide
└── requirements.txt      Dependencies
```

---

 **Dataset:**
- **Dataset Name:** IN22-Conv  
- **Description:** An n-way parallel corpus for evaluating conversational translation in 22 Indian languages.  
- **Source:** [ai4bharat/IN22-Conv](https://huggingface.co/datasets/ai4bharat/IN22-Conv)  

---

 **Dependencies:**
To run the project, install the required libraries using `pip`:
```bash
pip install -r requirements.txt
```

**Key Libraries:**
- `datasets`: For loading and processing the IN22-Conv dataset.
- `evaluate`: For BLEU score computation.
- `pandas`: For data manipulation.
- `tqdm`: For progress bars.

---

 **Usage:**

1. **Prepare the Dataset:**
   - Download the IN22-Conv dataset using the `datasets` library.
   - Ensure translations are stored as JSONL files in the `translations/` directory.

2. **Run BLEU Score Computation:**
   Execute the main script to compute BLEU scores for each language:
   ```bash
   python scripts/compute_bleu.py
   ```

3. **Analyze Results:**
   - The script outputs BLEU scores for each language.
   - Results are stored in the `results/` directory.

---

 **Example Command:**
To compute BLEU scores for all languages:
```bash
python scripts/compute_bleu.py --translations_dir translations/ --output_dir results/
```

---

 **Results Overview:**
BLEU scores for 22 Indian languages are provided in tabular format, with comparative performance across IndicTrans2, LLaMA 405B, and commercial systems like Google Translate and Azure Translator.

---

 **Future Directions:**
- **Improve Tokenization:** Develop tokenizers tailored for Indian scripts.  
- **Expand Datasets:** Incorporate more high-quality data for low-resource languages.  
- **Fine-Tuning:** Apply fine-tuning strategies for LLaMA models to enhance translation accuracy.

---

 **Contributors:**
- **Rasheena Arimbrathodi** (da23c015@smail.iitm.ac.in)  
  Indian Institute of Technology Madras, Wadhwani School of Data Science and AI  

---

 **License:**
This project is released under the MIT License.

---

 **Acknowledgments:**
- **AI4Bharat** for providing the IN22-Conv dataset.
- **Hugging Face** for hosting and supporting NLP datasets and evaluation tools.
```
