Analyze data of Stroke Prediction Dataset from Kaggle(https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)

The dataset contains 5110 observations with 12 attributes. 

The attributes are id, gender, age, hypertension, heart_disease, ever_married, work_type, residence_type, avg_glucose_level, bmi,somking_status, stroke.
Most of attributes have unique numbers, and letters, but some rows have blank data or unknown options in bmi and smoking_status. Therefore, I deleted the blank rows to clean up the dataset.
 <img width="975" height="1043" alt="image" src="https://github.com/user-attachments/assets/4402125d-50da-4f65-adbb-2624b8cd4350" />

It is the heatmap of dataset. The heatmap correlation index is from -1 to 1 
According to the heatmap, stroke has correlation with age, hypertension, heart disease, average of glucose level. the inverse correlations are single status, working in children, and unknown smoking status. However, the correlations are very weak with each attribute. However, it does not mean that, the attributes do not have any relationship with stroke. 
<img width="975" height="446" alt="image" src="https://github.com/user-attachments/assets/bb6ee11a-5436-4641-95fa-2b983e6f2d01" />

 
Based on a linear regression model, age, bmi, and stroke has specific relationship as you can see the graph. Most of stroke experienced people commonly have from 20 to 60 bmi, more than 40 years old. 
 <img width="975" height="422" alt="image" src="https://github.com/user-attachments/assets/132380d8-fb53-45b1-8b9c-a14892eb32dc" />

However, there is not clear relationship with average glucose levels of each participants. The graph still shows that, stroke as strong relationship with ages. 
 
<img width="975" height="634" alt="image" src="https://github.com/user-attachments/assets/93a17a74-7c3b-433a-8f28-f12f26aebfd6" />

As you can see the graph, the heart disease is not related to stroke. Age has much more impact to stroke than heart disease. 
 <img width="975" height="609" alt="image" src="https://github.com/user-attachments/assets/862ea491-dfb8-4da0-8a1d-6002887068dc" />
<img width="976" height="598" alt="image" src="https://github.com/user-attachments/assets/103d4677-0d09-4861-af1b-201b90b56391" />

According to gender-based graph, Female has less chance to have stroke from 40 and 60 years old range, but female has larger age range than male. However, the two different gender has common part, they both have high potential around 80 years old area. 
 
<img width="843" height="650" alt="image" src="https://github.com/user-attachments/assets/ff5c19f7-ddbd-4eaa-9d05-fc0211d09e6d" />
<img width="843" height="650" alt="image" src="https://github.com/user-attachments/assets/f2147935-1b6a-4473-893b-8c2cce0f30cd" />
<img width="843" height="650" alt="image" src="https://github.com/user-attachments/assets/fb17a85f-946e-4607-bdc5-98e087220eff" />
<img width="843" height="650" alt="image" src="https://github.com/user-attachments/assets/2c737b22-becf-4e36-ab7c-45c40aaac998" />
<img width="843" height="650" alt="image" src="https://github.com/user-attachments/assets/57458714-6ef3-476a-89be-31ecfbdd8e4f" />

 
 
Based on job graph, most of job field has different tendency of possibility of stroke. Especially, government job and children job sectors. Especially, children work type is outlier characteristic. They mostly have stroke from 0 to 40 years old. Besides, governments workers have slightly different patterns of stroke history. They mostly had stroke from 50 to 80 years old. 
 <img width="843" height="650" alt="image" src="https://github.com/user-attachments/assets/cc2f24f8-402a-4024-9713-96dbb0125a59" />
<img width="843" height="650" alt="image" src="https://github.com/user-attachments/assets/0bf1e7bc-3901-47d5-b957-ce1b40cd99f4" />

 
The residence type does not have any impact on the stroke. Urban, and rural area people have same tendencies of stroke data, thus we do not consider the residence type for machine learning dataset. 
 
 <img width="856" height="650" alt="image" src="https://github.com/user-attachments/assets/597be82d-3875-4261-a413-efe5dd31f7a5" />
<img width="843" height="650" alt="image" src="https://github.com/user-attachments/assets/97e8666b-d471-497f-87a3-eda912dbeaeb" />
<img width="843" height="650" alt="image" src="https://github.com/user-attachments/assets/eedc344e-6cc4-4c26-82e8-8626c7efa1fa" />
<img width="843" height="650" alt="image" src="https://github.com/user-attachments/assets/b4362c28-42fb-4110-8fc5-2e8dbd71306f" />

 
 
 For smoking status, smokers and former smokers have the similar tendency of stroke. The current smoker’s exposure higher risk of stroke, especially they faced stroke younger than non-smokers, but they have less stroke history than older than 80 years old. 

Therefore, every attributes impact on the stroke history, but the strongest reason is age, bmi, average of glucose level, and smoking status. 

Using Random Forest to predict stroke patient
For training set, to address data imbalance, the training set was balanced with a 1:1 ratio between stroke and non-stroke cases, allowing the Random Forest model to learn stroke patterns effectively.
The model was evaluated on an unseen test set with a 1:2 ratio, simulating a more realistic environment where non-stroke cases are more frequent.

<img width="488" height="661" alt="image" src="https://github.com/user-attachments/assets/cc6043e7-63c4-4222-94c3-174a057d0ba6" />

This is the result of the ML model.
While maintaining an overall accuracy of 70%, the model achieved a high Recall of 82%. This prioritizes minimizing "False Negatives," ensuring that potential stroke patients are not overlooked.


