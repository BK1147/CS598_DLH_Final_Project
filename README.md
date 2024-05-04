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
- [`secret.key`] (https://drive.google.com/drive/folders/1SOuU9TfnHdI9R6mxhpTNvlaZ61zbgn5p)
```
4. You can simply RUN ALL `DL4H_Team_74_Final_Report.ipynb`

## Data Preprocessing 

1. A
2. B
3. C


## Training 

1. A
2. B
3. C


## Evaluation & Result

| Model        | Precision  | Recall     | F1-score   | ROC AUC    |
| ------------ | ---------- | ---------- | ---------- | ---------- |
| RF           | 0.2667     | 0.1905     | 0.2222     | 0.7849     |
| LR           | 0.4000     | 0.0952     | 0.1538     | 0.8500     |
| SVM          | 0.2500     | 0.0476     | 0.0800     | 0.7765     |
| ------------ | ---------- | ---------- | ---------- | ---------- |
| GRU          | 0.9100     | 0.9220     | 0.9160     | 0.9650     |
| LSTM         | 0.8870     | 0.9220     | 0.9040     | 0.9600     |
| RETAIN       | 0.9580     | 0.8960     | 0.9260     | 0.9660     |
| ------------ | ---------- | ---------- | ---------- | ---------- |
| RNN          | 0.9474     | 0.9351     | 0.9412     | 0.9692     |
| RNN+rev      | 0.9494     | 0.9740     | 0.9615     | 0.9860     |
| RNN+max_pool | 0.9375     | 0.9740     | 0.9554     | 0.9758     |
| RNN+rev      | 0.9351     | 0.9351     | 0.9351     | 0.9844     |
|  + max_pool  |            |            |            |            |

