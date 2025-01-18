# Challenge: Colorectal Cancer Analysis

## Overview
This is a coding challenge designed to test your ability to analyze data from a real-world colorectal cancer dataset based on the real-world domain we deal with at Radical Health. The dataset contains longitudinal clinical, genomic, and treatment data for all cancer patients. 

You may do this at your own pace at home. The time you should spend on this task is 3 hours. The scope of the challenge is designed to take much more than 3 hours and it is normal to not have finished your task by the end of the time limit. We recommend breaking down the task and prioritize what you can do within the time. We will schedule a call with Bryan where we explore up to where you stopped and your thought processes!

# Your task
Colorectal cancer remains a leading cause of cancer-related morbidity and mortality worldwide, making optimal treatment decisions crucial for improving patient outcomes. In this coding task, we focus on three major clinical questions related to colorectal cancer management:

**Question 1: Is the sequence of FOLFOX followed by FOLFIRI better than alternating FOLFOX and FOLFIRI? for Stage 4 Colorectal Cancer Patients?**
There are two first-line chemotherapy treatment options for Stage IV colorectal cancer (FOLFOX and FOLFIRI). Clinicians believe their efficacy is equivalent and take a shot in the dark, but we believe there is an optimal treatment choice for patients based on their features (note: this particular dataset size might not be sufficient to show this). Develop model(s) to investigate the differential effectiveness of the two main chemotherapy treatments on stage IV colorectal cancer patients based on their features.

**Question 2:Is Surgery always the right choice? Or might a less invasive therapy suffice?**
In colorectal cancer, clinicians often default to surgical resection, yet some patients could be spared surgery if a less invasive therapy can achieve comparable outcomes. Develop predictive models to help identify which patients truly need surgery versus those who might benefit from more conservative interventions, minimizing overtreatment and improving overall patient outcomes.

**Question 3: Which Stage I-III Colorectal Cancer Patients are at High Risk of Recurrence After Surgery or Radiation Therapy and Require Adjuvant Chemotherapy?**
There are standard curative treatments for early-stage (I-III) colorectal cancer, including surgery and radiation therapy. However, identifying which patients might experience disease recurrence and would most benefit from subsequent adjuvant chemotherapy is challenging. Identify biomarkers (e.g., MMR status is known) to enable clinicians to make personalized decisions about recommending adjuvant chemotherapy, minimizing unnecessary treatment for low-risk patients while improving outcomes for those at high risk of relapse.

## Instructions and Tips
Your specific instructions are as follows:
1. Download the dataset from [here](https://cbioportal-datahub.s3.amazonaws.com/msk_chord_2024.tar.gz). This dataset is ~360Mb was published alongside this [paper](https://www.nature.com/articles/s41586-024-08167-5) from MSK. We do not recommend you spend time looking at the paper itself as it will not be of much help for the task.
2. This dataset contains 24,950 cancer patients, of which only 5,543 are colorectal cancer patients.
Hints:
> Each patient is identified with an ID in the *PATIENT_ID* col.
> You can filter for Colorectal Patients using `data_clinical_sample.txt` to get 5,543 patients.
> You can quickly filter for Stage 1-3 vs Stage 4 patients using `data_clinical_patient.txt`.
> There is rich longitudinal data in files with the format `data_timeline_*.txt`. E.g., `data_timeline_treatment.csv` lists all cancer treatments given to patients and `data_timeline_diagnosis` lists their longitudinal diagnoses.
> The *Overall Survival (Months)* col in `data_clinical_patient.txt` can be used to derive when a patient died.
3. Write scripts to achieve your overarching task. (You may use ANY tooling, programming language & any open source libraries you want to maximize your efficiency.)
4. Document all of your work, including exploratory data analyses and thought processes.
5. Delete any unneeded data files to avoid storage issues on your local machine.
6. When you're finished, send your code to Simone (simone@radicalhealth.ai) and Bryan (bryan@radicalhealth.ai) and schedule a call!

Beyond anything specifically mentioned, feel free to make any assumptions and justify your assumptions to achieve your tasks. 
Note that while we expect submitted code to run, we don't expect it to be ready to deploy! Leaving comments about things you would like to do given more time is totally fine.
