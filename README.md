# Reproducibility Study for : Integrating ChatGPT into Secure Hospital Networks: A Case Study on Improving Radiology Report Analysis 
Paper Link : [link](https://arxiv.org/pdf/2402.09358)
Presentation Link: [Youtube](https://youtu.be/U5M4hE0m1sM)
## Dependencies:
- Python 3.10
- requests
- beautifulsoup4
- getpass
- tqdm
- pandas
- torch
- torch.nn
- torch.utils.data
- transformers
- scikit-learn (sklearn)	


And all the dependencies mentioned in repositories used to sections below.

## Data Download & Processing

1. Request access to 'MIMIC-CXR Database' Data Set from Physionet website.
2. With your approved Physionet access, run [data_extract.ipynb](data_extract.ipynb) file to all the data and turn it into a csv file used for this reproducing exercise. This is extracting all p10 data.
3. This should create a file called 'mimic-cxr-p10' that you will then upload to ChatGPT and use the following prompt:
      'I have this spreadsheet where the text column are radiology reports. Can you create a new column in the csv file called 'Results' and determine from the radiology reports whether the patient's photo is normal, abnormal, or if the results are uncertain?'
4. Rename the file downloaded from ChatGPT to 'mimic_reports_with_results.csv' and upload it into the /content folder.

## Modeling
Once you have 'mimic_reports_with_results.csv' file in the /content folder, run [modeling.ipynb](modeling.ipynb) file to best reproduce the results.

## Results
This paper was not reproducible due to lack of computing power and resources. The model is only using the first 100 radiology reports, if you would like to use more feel free to change cell 1 of [modeling.ipynb](modeling.ipynb) and change the number '100' in code df = pd.read_csv(csv_path).head(100) to the number of rows you'd like. If all of p10 files were downloaded, there should be a total of 22,197 radiology reports available.
