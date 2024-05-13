### Created and Analyzed by: Saddam Ansari @Aspiring Data Analyst [LinkedIn](https://www.linkedin.com/in/saddam-ansari-dataanalyst/)
### Live Dashboard At Novypro [Link](https://project.novypro.com/ZMInAW)

✨➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖✨

## Project Objective:
The objective of this project is to provide the higher management of the American hospital with comprehensive insights into patient visits over the past two years. 

By analyzing this dataset, the management aims to gain valuable insights into overall service performance, identify areas for improvement, and make strategic decisions for the future. This includes assessing trends, patterns, and factors influencing patient visits to inform strategic planning and optimize service delivery for enhanced patient care and satisfaction.

## About Datset:
Before Moving Forward I want to share with you about data set,

The dataset comprises visit data from an **American hospital**, encompassing detailed records of visits from **9216 individual customers**. Each entry in the dataset stores unique information regarding the visits, enabling a granular understanding of the patient interaction with the hospital services.

## Detailed Data Description:
The dataset includes several columns with the following descriptions:

 * **date**: The date and time of the patient visit.
 * **patient_id**: Unique identifier for each patient.
 * **patient_gender**: Gender of the patient (M for Male, F for Female).
 * **patient_age**: Age of the patient at the time of visit.
 * **patient_sat_score**: Patient satisfaction score, indicating the level of satisfaction with the service received.
 * **patient_first_inital**: First initial of the patient's first name.
 * **patient_last_name**: Last name of the patient.
 * **patient_race**: Race of the patient (e.g., White, African American, Asian, Native American/Alaska Native, Pacific Islander, Declined to Identify, Two or More Races).
 * **patient_admin_flag**: A boolean value indicating whether the patient is an administrator (TRUE or FALSE).
 * **patient_waittime**: Wait time in minutes before the patient was attended to.
 * **department_referral**: Department to which the patient was referred for further treatment or consultation.

These columns provide detailed information about each visit, including demographics, visit characteristics, and medical department visited within the hospital.

✨➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖✨

## Dashborad Overview:

![final dashboard](https://github.com/user-saddam123/Patients-Emergency-Room-Visit-Report/assets/123800896/4b7476b3-f971-4df9-9038-a2bc2ebabfb7)

✨➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖✨

## Detailed Insights Explanation:

### Some Important KPIs:

![Screenshot 2024-05-13 081705](https://github.com/user-saddam123/Patients-Emergency-Room-Visit-Report/assets/123800896/a33c1fd1-dbfe-4396-959e-3717a65477db)

 * **Total Patients Visited:** This KPI represents the total number of patients who visited the hospital over the past two years. In the provided dataset, a total of 9216 patients visited.

 * **Patients Visited by Administrative Appointment**: This KPI indicates the number of patients who visited the hospital through administrative appointments, such as scheduled consultations, procedures, or administrative tasks.

 * **Patients Visited by Non-Administrative Appointment:** This KPI represents the number of patients who visited the hospital without administrative appointments, including emergency visits, walk-ins, and unscheduled consultations.

Based on the provided dataset, it is observed that out of the total 9216 patients visited in the past two years:

 * 50.04% of the visits were through administrative appointments.
 * 49.96% of the visits were without administrative appointments.

These KPIs provide insights into the distribution of patient visits based on appointment types, enabling the hospital management to assess appointment scheduling efficiency and resource allocation strategies.

#
### Breakdown of Customers by Gender:
Within the given time frame, the analysis reveals that out of the total patients who visited the hospital:
![Screenshot 2024-05-13 082401](https://github.com/user-saddam123/Patients-Emergency-Room-Visit-Report/assets/123800896/f5e2949c-890f-42c3-8f12-8e76215136f3)

 * 51.05% were male patients,
 * 48.69% were female patients, and
 * 0.26% were categorized as unknown gender.

#

![Screenshot 2024-05-13 083734](https://github.com/user-saddam123/Patients-Emergency-Room-Visit-Report/assets/123800896/27f8a938-9c9e-4a5c-bd0c-9c85c785fea4)

### Show Patients' Average Satisfaction Score:

The average customer satisfaction score is observed to be **5.47** out of 10. Notably, the satisfaction score **peaked in March at 5.93**, marking the highest rating during the observed period, whereas it reached its **lowest point in September at 5.30**.

### Percentage of Patients Not Rated:

Interestingly, **75.10%** of patients did not provide a satisfaction rating, indicating that they did not fill out the survey form or provide feedback on the service.

### Average Waiting Time of Customers:

The average waiting time for customers is calculated to be **35.26 minutes**. This metric offers insights into the efficiency of service delivery and can aid in identifying areas for improvement to minimize waiting times and enhance the overall patient experience.

#

### Show Patients Referred or Not:
![Screenshot 2024-05-13 084039](https://github.com/user-saddam123/Patients-Emergency-Room-Visit-Report/assets/123800896/5930e3cd-9c30-4158-8e88-a1245b9fd196)

The analysis indicates that **41.41%** of patients were **referred** to the hospital, while **58.59%** were **walk-in patients**. 

This breakdown highlights the proportion of patients who arrived at the hospital through referrals compared to those who visited without prior referral, providing insights into the sources of patient traffic and referral patterns.

#

### Show Patients Visits by Weektype:

Based on the analysis, it is observed that **6.6K patients visited on weekdays**, whereas **2.6K patients visited on weekends**.

![Screenshot 2024-05-13 084653](https://github.com/user-saddam123/Patients-Emergency-Room-Visit-Report/assets/123800896/94559931-0818-43ff-9f33-e2cf38b61774)

### Create Age Groups for Patients:

Age Groups have been created using the following DAX expression:

Age Groups = 

VAR _PatientAge = 'Patients Dataset'[patient_age]

RETURN

IF(
    _PatientAge <= 2, "Infancy",
    IF(
        _PatientAge < 6, "Early Childhood",
        IF(
            _PatientAge <= 12, "Middle Childhood",
            IF(
                _PatientAge <= 18, "Teenager",
                "Adult"
            )
        )
    )
)

#

 * Subsequently, the bar chart illustrates that the highest number of patients, 7106, falls within the adult age group. 
 * Followed by middle childhood with 839 patients, teenagers with 677 patients, early childhood with 368 patients, and infancy with 266 patients. 

This breakdown provides insights into the distribution of patient visits across different age groups, aiding in targeted healthcare planning and resource allocation.

#
### Patients Visit by Year
![Screenshot 2024-05-13 091619](https://github.com/user-saddam123/Patients-Emergency-Room-Visit-Report/assets/123800896/a447fe32-54b3-4474-8065-2089410224b1)

To display the trend line of patient visits by year, a line chart was utilized. It is evident from the chart that there were 4338 patient visits in 2019, whereas in 2020, there were 4878 visits.

#

### Total Patients by Department_Referral
![Screenshot 2024-05-13 091630](https://github.com/user-saddam123/Patients-Emergency-Room-Visit-Report/assets/123800896/97e8c5c6-e85b-446b-8057-4fbd1be197c7)

For illustrating the number of patients visiting each department, a bar chart was employed, allowing for clear visualization. 

 * Among the referred patients, the "None" department, which indicates general visits, has the highest frequency with 5400 visits. 

 * Following that, the General Practice department has the highest visit count of 1840, followed by Orthopedics with 995 visits. Conversely, the Renal department has the lowest visit count of 86.

#

### Total Patients Visits by Month
![Screenshot 2024-05-13 091643](https://github.com/user-saddam123/Patients-Emergency-Room-Visit-Report/assets/123800896/a60f0a17-0969-484f-a099-908c2367eaeb)

For displaying patient visits by month, a line chart was utilized to provide easy visualization of the number of customers visiting each month. The analysis reveals that the highest number of patients visited in August, totaling 1024. Conversely, February had the lowest visit count, with only 431 patients.

#
### Avg wait time by Patients_race and their age group:
![Screenshot 2024-05-13 092503](https://github.com/user-saddam123/Patients-Emergency-Room-Visit-Report/assets/123800896/00d8c003-54ba-4063-a06a-6b49520affea)

 * To display wait time by patient race and age group, a heatmap was employed, enabling easy visualization of the average wait time for each demographic segment.
 * The analysis indicates that the highest average wait time is observed among Native American or Alaska Native patients aged 70 and above, reaching 40.07.
 * Conversely, the lowest average wait time is seen among Pacific Islander patients aged between 21 and 30, with a wait time of 32.53.

This heatmap provides valuable insights into the distribution of average wait times across different demographic groups, aiding in understanding disparities and optimizing service delivery.

#

## Top Recomendation:
Based on the insights from the dashboard and the objective of optimizing patient visits and enhancing revenue growth, here are some top recommendations:

 * **Special Treatment Packages for Walk-in Patients:** Implement special treatment packages with affordable prices for patients who visit without referrals. By offering exclusive services or discounts tailored to walk-in patients, the hospital can attract more individuals seeking medical care without prior referrals. This strategy can help increase patient volume and revenue.

 * **Priority Services for Older Patients:** Prioritize services and reduce wait times for older patients, particularly those aged 70 and above. Implement dedicated fast-track services or appointment slots for elderly patients to ensure prompt medical attention and enhance their overall experience. By addressing the needs of this demographic group, the hospital can improve patient satisfaction and loyalty.

 * **Telemedicine Services for Remote Consultations:** Introduce telemedicine services to provide remote consultations for patients who may not be able to visit the hospital in person. This initiative can cater to patients with mobility issues, those residing in remote areas, or individuals seeking non-urgent medical advice. By expanding access to healthcare services through telemedicine, the hospital can broaden its patient base and generate additional revenue streams.

 * **Targeted Marketing Campaigns**: Launch targeted marketing campaigns to promote specialized departments or services with high demand, such as General Practice or Orthopedics. Utilize digital marketing channels, social media platforms, and email newsletters to reach potential patients and highlight the unique offerings of the hospital. By raising awareness and showcasing the hospital's expertise in specific medical areas, these campaigns can attract more patients and drive revenue growth.

 * **Enhanced Patient Engagement**: Implement initiatives to enhance patient engagement and foster long-term relationships. Develop personalized communication channels, such as patient portals or mobile apps, to provide health tips, appointment reminders, and follow-up care instructions. By staying connected with patients beyond their initial visit, the hospital can build trust, encourage loyalty, and increase repeat visits, ultimately contributing to revenue growth.

By implementing these strategic recommendations, the hospital can effectively attract new patients, improve patient satisfaction, and drive revenue growth while aligning with its overarching objective of providing comprehensive healthcare services and optimizing operational performance.

#

✨✨➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖✨✨

**Don't forget to give a start to this project because its motivate me and also please follow me on [Linkeldin](https://www.linkedin.com/in/saddam-ansari-dataanalyst/). and Please consider me for any internship or entry level data analyst role. I need a job or internship even thought its a free or paid. Thanks in Advance.**

#

## How Can You Help Me
 * First and foremost, your appreciation and endorsement of this project mean the world to me. If you have any recommendations or suggestions, please feel free to share them with me. Your input can immensely assist me in refining and improving this project further.

 * Additionally, I have worked on over 40 projects, which you can explore on my [portfolio at Novypro](https://www.novypro.com/profile_projects/saddamansari). If you believe that my skills align with your requirements, I would be grateful if you could recommend me on [LinkedIn]((https://www.linkedin.com/in/saddam-ansari-dataanalyst/)).

 * As I am currently seeking internship or entry-level positions, your support and assistance would be invaluable to me. I assure you of my gratitude for any help extended.

#

I hope you found this project enjoyable and insightful.😊😊


✨✨➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖➖✨✨

Created & Presented by -Saddam Ansari @ Aspiring Data Analyst

Date- 13/05/2024

Place- Bihar, India



