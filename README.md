# Employee Engagement Analysis Assignment

## **Overview**

In this assignment, you will leverage Spark Structured APIs to analyze a dataset containing employee information from various departments within an organization. Your goal is to extract meaningful insights related to employee satisfaction, engagement, concerns, and job titles. This exercise is designed to enhance your data manipulation and analytical skills using Spark's powerful APIs.

## **Objectives**

By the end of this assignment, you should be able to:

1. **Data Loading and Preparation**: Import and preprocess data using Spark Structured APIs.
2. **Data Analysis**: Perform complex queries and transformations to address specific business questions.
3. **Insight Generation**: Derive actionable insights from the analyzed data.

## **Dataset**

### **Employee Data (`employee_data.csv`)**

You will work with a dataset containing information about 100 employees across various departments. The dataset includes the following columns:

| Column Name          | Data Type | Description                                           |
|----------------------|-----------|-------------------------------------------------------|
| **EmployeeID**       | Integer   | Unique identifier for each employee                   |
| **Department**       | String    | Department where the employee works (e.g., Sales, IT) |
| **JobTitle**         | String    | Employee's job title (e.g., Manager, Executive)      |
| **SatisfactionRating** | Integer | Employee's satisfaction rating (1 to 5)               |
| **EngagementLevel**  | String    | Employee's engagement level (Low, Medium, High)       |
| **ReportsConcerns**  | Boolean   | Indicates if the employee has reported concerns       |
| **ProvidedSuggestions** | Boolean | Indicates if the employee has provided suggestions    |

### **Sample Data**

Below is a snippet of the `employee_data.csv` to illustrate the data structure. Ensure your dataset contains at least 100 records for meaningful analysis.

```
EmployeeID,Department,JobTitle,SatisfactionRating,EngagementLevel,ReportsConcerns,ProvidedSuggestions
1,Sales,Manager,5,High,False,True
2,IT,Developer,3,Low,True,False
3,HR,Executive,4,High,False,True
4,Sales,Executive,2,Low,True,False
5,IT,Manager,5,High,False,True
...
```

## **Assignment Tasks**

You are required to complete the following three analysis tasks using Spark Structured APIs. Ensure that your analysis is well-documented, with clear explanations and any relevant visualizations or summaries.

### **1. Identify Departments with High Satisfaction and Engagement**

**Objective:**

Determine which departments have more than 50% of their employees with a Satisfaction Rating greater than 4 and an Engagement Level of 'High'.

**Tasks:**

- **Filter Employees**: Select employees who have a Satisfaction Rating greater than 4 and an Engagement Level of 'High'.
- **Analyze Percentages**: Calculate the percentage of such employees within each department.
- **Identify Departments**: List departments where this percentage exceeds 50%.

**Expected Outcome:**

A list of departments meeting the specified criteria, along with the corresponding percentages.

**Example Output:**

| Department | Percentage |
|------------|------------|
| Finance    | 60%        |
| Marketing  | 55%        |

---

### **2. Who Feels Valued but Didn’t Suggest Improvements?**

**Objective:**

Identify employees who feel valued (defined as having a Satisfaction Rating of 4 or higher) but have not provided suggestions. Assess the significance of this group within the organization and explore potential reasons for their behavior.

**Tasks:**

- **Identify Valued Employees**: Select employees with a Satisfaction Rating of 4 or higher.
- **Filter Non-Contributors**: Among these, identify those who have `ProvidedSuggestions` marked as `False`.
- **Calculate Proportion**: Determine the number and proportion of these employees relative to the entire workforce.

**Expected Outcome:**

Insights into the number and proportion of employees who feel valued but aren’t providing suggestions.

**Example Output:**

```
Number of Employees Feeling Valued without Suggestions: 25
Proportion: 25%
```

---

### **3. Compare Engagement Levels Across Job Titles**

**Objective:**

Examine how Engagement Levels vary across different Job Titles and identify which Job Title has the highest average Engagement Level.

**Tasks:**

- **Map Engagement Levels**: Convert categorical Engagement Levels ('Low', 'Medium', 'High') to numerical values to facilitate calculation.
- **Group and Calculate Averages**: Group employees by Job Title and compute the average Engagement Level for each group.
- **Identify Top Performer**: Determine which Job Title has the highest average Engagement Level.

**Expected Outcome:**

A comparative analysis showing average Engagement Levels across Job Titles, highlighting the top-performing Job Title.

**Example Output:**

| JobTitle   | AvgEngagementLevel |
|------------|--------------------|
| Manager    | 4.5                |
| Executive  | 4.2                |
| Developer  | 3.8                |
| Analyst    | 3.5                |
| Coordinator | 3.0                |
| Support    | 2.8                |

---

## **Grading Criteria**

Your assignment will be evaluated based on the following criteria:

- **Question 1**: Correct identification of departments with over 50% high satisfaction and engagement (1 mark).
- **Question 2**: Accurate analysis of employees who feel valued but didn’t suggest improvements, including proportion (1 mark).
- **Question 3**: Proper comparison of engagement levels across job titles and correct identification of the top-performing job title (1 mark).

**Total Marks: 3**

---


Good luck, and happy analyzing!