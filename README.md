# CS598 Deep Learning for Healthcare Spring 2024
Team ID: 74
Paper ID: 69 

Byunggeun Park (bpark14@illinois.edu)
Spencer Arbour (sarbour2@illinois.edu)
Yun Gao (yungao3@illinois.edu)


# Domain Knowledge Guided Deep Learning with Electronic Health Records 

C. Yin, R. Zhao, B. Qian, X. Lv and P. Zhang, "Domain Knowledge Guided Deep Learning with Electronic Health Records," 2019 IEEE International Conference on Data Mining (ICDM), Beijing, China, 2019, pp. 738-747, doi: 10.1109/ICDM.2019.00084.
>📋 In the realm of healthcare, the utilization of Electronic Health Records (EHRs) for predictive analytics stands as a beacon of opportunity for enhancing patient care and resource allocation. However, the complexity inherent in EHR data, characterized by its high dimensionality, sparsity, and irregularity, poses formidable challenges to accurate prediction of clinical outcomes. Addressing these challenges is paramount for unlocking the full potential of EHRs in revolutionizing healthcare practices. This paper presents a pioneering solution to the intricate problem of clinical risk prediction using EHRs: the Domain Knowledge Guided Recurrent Neural Networks (DG-RNN). By seamlessly integrating rich medical knowledge into the predictive modeling process, DG-RNN transcends the limitations of conventional approaches, offering unprecedented accuracy, interpretability, and adaptability in clinical risk assessment.


## File Structure

    .
    ├── Data_Preprocess_Increase_HF_Ratio.ipynb
    ├── data                    
    │   ├── vids.pickle          
    │   ├── types.pickle         
    │   ├── seqs.pickle  
    │   ├── rtypes.pickle  
    │   ├── pids.pickle
    │   ├── hfs.pickle  
    │   ├── d_icd_diagnoses.csv
    │   └── diagnoses_icd.csv
    │
    └── DL4H_Team_74_Final_Report.ipynb
    └── requirements.txt
    └── enc_d_icd_diagnoses
    └── enc_diagnoses
    └── enc_hfs_dataset_pkl
    └── README.md
    └── secret.key
    └── ...

## Set-up


1. Clone the repository.
```bash
git clone https://github.com/BK1147/CS598_DLH_Final_Project.git
```
2. Install python package requirements using requirements.txt (Optional: use python virtual environments).
```bash
python3 -m venv env
source env/bin/activate
pip install -r requirements.txt
```
3. A secret key will be included as a separate download/note in our submission. Save this file to the root directory for this project as `secret.key`.
```bash
You can download `secret.key`
- [`secret.key`] (https://drive.google.com/drive/folders/1GuJjVOCeXADcaQ6eqSlMZsx9IGR8UFxn)
```
4. You can simply RUN ALL `DL4H_Team_74_Final_Report.ipynb`

## Data Preprocessing 

MIMIC IV data tables (version 2.2) are used as a basis for patient data analysis. The data was collected from PhysioNet. Our dataset was pulled from 'hosp' patient EHRs, and were filtered to only contain ICD-9 codes.

The pre-processing of the MIMIC IV dataset has been relocated to Data_Preprocess.ipynb. Please refer to that notebook for inquiries regarding the filtering of the original dataset. After the pre-processing of the MIMIC IV dataset, we simply create the pickle file and utilize it directly from DL4H_Team_74_Final_Report.ipynb. The total pre-processing time ranges from 20 to 30 minutes depending on the computational background.



## Evaluation & Result

| Model        | Precision  | Recall     | F1-score   | ROC AUC    |
| ------------ | ---------- | ---------- | ---------- | ---------- |
| RF           | 0.2667     | 0.1905     | 0.2222     | 0.7849     |
| LR           | 0.4000     | 0.0952     | 0.1538     | 0.8500     |
| SVM          | 0.2500     | 0.0476     | 0.0800     | 0.7765     |
| ------------ | ---------- | ---------- | ---------- | ---------- |
| GRU          | 0.8290     | 0.8830     | 0.8550     | 0.9590     |
| LSTM         | 0.9180     | 0.8700     | 0.8930     | 0.9310     |
| RETAIN       | 0.9470     | 0.9350     | 0.9410     | 0.9790     |
| ------------ | ---------- | ---------- | ---------- | ---------- |
| RNN          | 0.9474     | 0.9351     | 0.9412     | 0.9692     |
| RNN+rev      | 0.9494     | 0.9740     | 0.9615     | 0.9860     |
| RNN+max_pool | 0.9054     | 0.8701     | 0.8874     | 0.9639     |
| RNN+rev      | 0.9012     | 0.9481     | 0.9241     | 0.9837     |
|  + max_pool  |            |            |            |            |

