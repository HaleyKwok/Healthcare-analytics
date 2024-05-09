# Healthcare_analytics

# 🔆 Introduction

The healthcare services at UC Berkeley is undergoing a significant transformation with the integration of data analytics and technology. This project aims to leverage data analytics and optimization techniques to improve the efficiency and effectiveness of healthcare systems, specifically focusing on appointment scheduling and queue management within a healthcare facility.

```mermaid
flowchart LR
    A[Login to eTang Portal] --> B[Select Appointment Type]
    B --> C[View Roster of Doctors]
    C --> D[Select Doctor and Available Time]
    D --> E[Confirm Appointment]
    E --> F{Appointment Day}
    F --> G[Student Arrives On Time]
    F --> H[Student Arrives Late]
    F --> I[Student Does Not Show]
    G --> J[Appointment Proceeds]
    H --> K[Reschedule or Cancel]
    I --> L[Time Slot Wasted]
```


# 🥳 Features

## Analysis and Methodology

1. Data Preparation: University Health Services (UHS) statistics originated from [fenghaolin/HanguData (github.com)](https://github.com/fenghaolin/HanguData)
2. Exploratory Data Analysis (EDA)
3. Feature Importance Analysis
4. Model Building
5. Queuing Simulation and Algorithms
6. System Architecture Design

This table summarizes the average waiting time and average system time for each scheduling algorithm.

| Scheduling Algorithm | Average Waiting Time | Average System Time |
|----------------------|----------------------|---------------------|
| FCFS                 | 7.53                 | 12.41               |
| SPT                  | 487.53               | 492.41              |
| EDD                  | 25.12                | 30.00               |
| Slack Time Remaining | 26.78                | 31.67               |
| Critical Ratio       | 67.36                | 72.24               |


## System Design

```mermaid
graph LR;
    frontend[Frontend] --> ui[User Interface]
    frontend --> appointment[Appointment Booking]
    frontend --> feedback[Feedback Submission]
    
    appointment --> online[Online Appointment Scheduler]
    appointment --> inperson[In-person FCFS Queue Management]
    
    backend[Backend] --> ams[Appointment Management System AMS]
    backend --> analysis[Data Analysis Module]
    backend --> qms[Queue Management System QMS]
    backend --> staffing[Staffing Optimization]
    
    ui -.-> online
    ui -.-> inperson
    appointment -.-> online
    appointment -.-> inperson
    feedback --> online
    
    online -.-> ams
    inperson -.-> ams
    analysis --> ams
    analysis -.-> qms
    qms --> ams
    staffing --> ams
    
    ams --> db[Database]
    ams --> web[Web Server]
    ams --> analytics[Analytics Platform]
    qms --> notification[Notification System]
    qms --> screens[Display Screens]
    
    db -.-> analysis
    analytics --> analysis
```






---


# 📝 Changelog
- [2024.04.15] Added initial project proposal
- [2024.04.20] Completed data collection and cleaning
- [2024.04.21] Conducted exploratory data analysis (EDA) and identified key insights
- [2024.04.26] Designed the online appointment scheduler system architecture
- [2024.04.28] Finalized the project details


---

# 📢 Disclaimer
This repository is for personal/research/non-commercial use only.

---
Copyright © University of California, Berkeley, Faculty of Engineering, Department of Industrial Engineering and Operation Research, [Hin Chi Kwok](https://github.com/HaleyKwok). All rights reserved.