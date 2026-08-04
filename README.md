### EX4 Implementation of Cluster and Visitor Segmentation for Navigation patterns
### DATE:04/08/2026
### NAME:SHRAVANI M
### REGISTER NUMBER:212224230263
### AIM: 
To implement Cluster and Visitor Segmentation for Navigation patterns in Python.
### Description:
<div align= "justify">Cluster visitor segmentation refers to the process of grouping or categorizing visitors to a website, 
  application, or physical location into distinct clusters or segments based on various characteristics or behaviors they exhibit. 
  This segmentation allows businesses or organizations to better understand their audience and tailor their strategies, marketing efforts, 
  or services to meet the specific needs and preferences of each cluster.</div>
  
### Procedure:
1) Read the CSV file: Use pd.read_csv to load the CSV file into a pandas DataFrame.
2) Define Age Groups by creating a dictionary containing age group conditions using Boolean conditions.
3) Segment Visitors by iterating through the dictionary and filter the visitors into respective age groups.
4) Visualize the result using matplotlib.

### Program:
```python
import pandas as pd
import matplotlib.pyplot as plt

# Read CSV file
df = pd.read_csv(r"C:\Users\admin\Downloads\clustervisitor (1).csv")

# Assign clusters manually based on Age
def assign_cluster(age):
    if age <= 31:
        return 2
    elif age <= 41:
        return 0
    else:
        return 1

df["Cluster"] = df["Age"].apply(assign_cluster)

# ----------------------------
# Display Complete Dataset
# ----------------------------
print("\n========== COMPLETE DATASET ==========\n")
print(df)

# ----------------------------
# Display Each Cluster
# ----------------------------
for i in [0, 1, 2]:
    print(f"\n========== CLUSTER {i} ==========\n")
    print(df[df["Cluster"] == i])



```
### Output:

<img width="892" height="457" alt="Screenshot 2026-08-03 162242" src="https://github.com/user-attachments/assets/fd57f8e2-f433-4a51-91ff-b16254cf0a5d" />


<img width="948" height="271" alt="Screenshot 2026-08-03 162220" src="https://github.com/user-attachments/assets/265e0a26-035e-45b6-9268-dfcf72bc7c69" />


<img width="952" height="311" alt="Screenshot 2026-08-03 162206" src="https://github.com/user-attachments/assets/d25cd37f-c064-459f-a47c-1cf9fbdbdc2f" />

<img width="930" height="263" alt="Screenshot 2026-08-03 162147" src="https://github.com/user-attachments/assets/5be88a74-a2ef-4b25-bdb5-6ef36160ff4b" />


### Visualization:
```python
# Create a list to store counts of visitors in each age group
visitor_counts = []

# Count visitors in each age group
for group, condition in age_groups.item():
visitors_in_group = visitor_df[condition]
visitor_counts.append(len(visitors_in_group))
    
# Define age group labels and plot a bar chart
age_group+labels = list(Age_groups.keys())

plt.figure(figsize=(8, 6))
plt.bar(age_group_labels, visitor_counts, color='skyblue')
plt.xlabel('Age Groups')
plt.ylabel('Number of Visitors')
plt.title('Visitor Distribution Across Age Groups')
plt.show()
```
### Output:

<img width="807" height="472" alt="Screenshot 2026-08-03 162044" src="https://github.com/user-attachments/assets/fc426d19-d3a9-47e7-926f-9318ddc1406b" />


### Result:
Thus  Cluster and Visitor Segmentation for Navigation patterns are exicuted successfully

