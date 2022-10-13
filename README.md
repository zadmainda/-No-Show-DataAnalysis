# No Show Appointments Data Exploration

## Dataset

This dataset contains details on medical appointments, characteristics of patients and whether they showed up for their appointments. It contains 110,527 rows of appointments and 14 columns explained below: 

The dataset can be found in the repository  [here](https://d17h27t6h515a5.cloudfront.net/topher/2017?October/59dd2e9a_noshowappointments-kagglev2-may-2016/noshowappointments-kagglev2-may-2016.csv),
with feature documentation available [here](https://www.kaggle.com/datasets/joniarroba/noshowappointments).

### Data Dictionary

***Column Name | Data Type | Brief Description of the data***
1. *PatientID (int)* - Unique identifier for each patient
2. *AppointmentID (int)* - Unique identifier for each appointment
3. *Gender (str)* - Gender of the patient
4. *ScheduledDay (date)*- The date a patient booked the appointment
5. *ScheduledDayTime (dtime)*- The time a patient booked the appointment
6. *AppointmentDay (date)* - The date a patient is supposed to see a doctor
7. *Age (int)*- The age of the patient
8. *Neighborhood (str)* - Location/area near the hospital
9. *Scholarship (boolean)* - indicates whether patient is enrolled in govt welfare social program
10. *Hypertension (boolean)* - indicates whther patient has high blood pressure
11. *Diabetes (boolean)* -indicates whether patient is diabetic or not
12. *Alcoholism (boolean)* - Indicates whether patient is alcoholic or not
13. *SMS_received (boolean)* - indicates whether patient was notified of upcoming appointment
14. *No_show (str)* - indicates whether patient showed up to appointment 

    >NB: The dataset uses 0 and 1 to represent False and True respectively

### Questions that were investigated in this project
The goal of this project is to determine how the various characteristics of a patient may help determine whether they will show up to their medical appointment by examining the following questions:
1. what is the gender distribution of the patients?
2. What is the gender distribution of patients who showed up to their appointments?
3. Do patients with pre-existing medical conditions (hypertension) adhere to their appointments?
4. What are the average ages for patients based on their gender for the no-show categories?
5. Do medical appointment attendance rates improve as patients grow older?

## Summary of Findings

> We found that Gender distribution of the appointments stood as follows; Female:64% , Male:35%. These percentages represent the percentage distribution of the genders indicated on the appointments. It is important to note that it doesnt take into account the fact that a single patient may have requested more than one appointment in the period covered by the dataset.  

> On examining the Gender of distinct patients who showed up to atleast once to their appointments the  figures indicated that figures mirrored the gender distribution percentages in the overall dataset. 64% of patients who turned up for their appointments were female while 35% of the Show-ups were male.

> Patients with Hypertension have a higher appointment attendance rate of 83% when compared to patients without hypertension whose appointment attendance rate stands at 79%

> The average age of Female patients who showed up is 36yrs and 39years for those who chose to ignore their checkup.On the other hand, the average age of men who showed up for appointment was 30years while the avergare was 34years for men who skipped their appoinments.
        
> Medical appointment attendance rates do not improve as patients grow older. The attendance rates peak at the second cohort of patients that lies between 18-38yrs and then proceeds to slump in the following cohorts.The cohort with the oldest patients of ages between 56-115yrs has the appointment attendance count. 

#### Limitations
1. The presence of outliers in the dataset for instance in the age column may distort some statistical methods such as mean or skew the distribution thereby causing bias. In the age column, we had a (-1)negative entry and several figures that are more than 100.  
2. The dataset contains a limited set of metrics that would not be sufficient to conclusively determine health-care utilization/medical appointment attendance. There are several economic, social and environmental factors that influence the consumption of healthcare such as quality of service delivery, availability of cheaper alternate sources of healthcare,prevalance of traditional myths, severity of the ailment, distance to healthcare centers, medical sensitization and disability among many others ("Factors that affect health-care utilization - health-care utilization as a proxy in disability determination - NCBI bookshelf," 2018 p.2). 
