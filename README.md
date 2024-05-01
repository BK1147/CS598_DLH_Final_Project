# CS598 Deep Learning for Healthcare Spring 2024
Team ID: 74
Paper ID: 69 

Byunggeun Park (bpark14@illinois.edu)
Spencer Arbour (sarbour2@illinois.edu)
Yun Gao (yungao3@illinois.edu)


# Domain Knowledge Guided Deep Learning with Electronic Health Records 

C. Yin, R. Zhao, B. Qian, X. Lv and P. Zhang, "Domain Knowledge Guided Deep Learning with Electronic Health Records," 2019 IEEE International Conference on Data Mining (ICDM), Beijing, China, 2019, pp. 738-747, doi: 10.1109/ICDM.2019.00084.
>📋 In the realm of healthcare, the utilization of Electronic Health Records (EHRs) for predictive analytics stands as a beacon of opportunity for enhancing patient care and resource allocation. However, the complexity inherent in EHR data, characterized by its high dimensionality, sparsity, and irregularity, poses formidable challenges to accurate prediction of clinical outcomes. Addressing these challenges is paramount for unlocking the full potential of EHRs in revolutionizing healthcare practices. This paper presents a pioneering solution to the intricate problem of clinical risk prediction using EHRs: the Domain Knowledge Guided Recurrent Neural Networks (DG-RNN). By seamlessly integrating rich medical knowledge into the predictive modeling process, DG-RNN transcends the limitations of conventional approaches, offering unprecedented accuracy, interpretability, and adaptability in clinical risk assessment.


## Requirements 

```bash
pip install -r requirements.txt
```

## File Structure

    .
    ├── Data_Preprocess_Increase_HF_Ratio.ipynb
    ├── data                    
    │   ├── vid.pickle          
    │   ├── types.pickle         
    │   ├──  sdqs.pickle  
    │   ├──  rtypes.pickle  
    │   ├── pids.pickle
    │   ├──  hfs.pickle  
    │   ├──  d_icd_diagnoses.csv
    │   ├──  diagnoses_icd.csv
    └── DL4H_Team_74_Final_Report.ipynb
    └── requirements.txt
    └── ...
    └── ...

## Set-up

1. A
2. B
3. C
4. D

## Data Preprocessing 

1. A
2. B
3. C
4. D

## Training 

1. A
2. B
3. C
4. D

## Evaluation & Result

| Model        | Precision  | Recall     | F1-score   | ROC AUC    |
| ------------ | ---------- | ---------- | ---------- | ---------- |
| LR           | **0.0000** | 0.0000     | 0.0000     | 0.0000     |
| RF           | 0.0000     | 0.0000     | 0.0000     | 0.0000     |
| SVM          | 0.0000     | 0.0000     | 0.0000     | 0.0000     |
| ------------ | ---------- | ---------- | ---------- | ---------- |
| GRU          | 0.0000     | 0.0000     | 0.0000     | 0.0000     |
| LSTM         | 0.0000     | 0.0000     | 0.0000     | 0.0000     |
| RETAIN       | 0.0000     | 0.0000     | 0.0000     | 0.0000     |
| GRAM         | 0.0000     | 0.0000     | 0.0000     | 0.0000     |
| KAME         | 0.0000     | 0.0000     | 0.0000     | 0.0000     |
| ------------ | ---------- | ---------- | ---------- | ---------- |
| RNN          | 0.0000     | 0.0000     | 0.0000     | 0.0000     |
| RNN+Maxpool  | 0.0000     | 0.0000     | 0.0000     | 0.0000     |
| RNN+rev      | 0.0000     | 0.0000     | 0.0000     | 0.0000     |

