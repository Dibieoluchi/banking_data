# Project Title: Analyzing Banking Trends: Customer Transactions and Regional Impact

![image](https://github.com/Dibieoluchi/banking_data/assets/88893142/06434477-6fd1-476f-978e-f48231921e13)

# Introduction


In the ever-evolving world of banking and finance, understanding customer behavior and the regional impact of transactions plays a crucial role in decision-making and strategic planning. This project, titled "Analyzing Banking Trends: Customer Transactions and Regional Impact," explores and analyzes vast troves of transaction data to gain valuable insights into customer behavior patterns and their implications on different world regions.


In this data work, we will delve into the findings of the analysis, showcasing the skills employed in SQL and Python for data manipulation, visualization, and the subsequent impact on banking trends for a specific bank. The report will be structured into several sections:

1.  Skills Demonstrated: This section will highlight the SQL and Python skills used in the analysis, including joins, subqueries, CTEs, conditional statements, Python functions, and data visualization.

2. Database ERD: We will provide an overview of the database schema and the relationship between the key tables used in the analysis.

3. Analysis and Insights Generated: This section will delve into the results of the analysis, summarizing the key findings related to customer behavior and regional impact. We will break down the findings based on the tasks mentioned in the project description.

4. Conclusion and Recommendations: We will conclude the data work by summarizing the implications of the analysis and providing recommendations for the bank based on the insights gained.

5. Data Limitations: It's important to acknowledge the limitations of the data, including the restricted time frame (data for only two years) and other potential constraints.



 # Skills Demonstrated

 
In this project, we leveraged several data analysis skills to uncover insights. The following skills were demonstrated:


# SQL Skills:


1.  Joins: We used SQL joins to combine data from multiple tables, such as joining customer data with transaction data based on customer IDs and regions.
2.  Subqueries: Subqueries were utilized to retrieve specific data subsets within larger queries, enabling us to answer complex questions efficiently.
3. Common Table Expressions (CTEs): CTEs were employed to create temporary result sets that could be used in subsequent queries, simplifying complex queries.
4. Conditional Statements in SQL: Conditional statements like CASE were used to categorize data and make comparisons, such as identifying churned customers based on their last transaction date.
# Python Skills:
5. Data Manipulation in Python: Python was used for calculating summary statistics.
6. Defining Functions in Python: Python functions were defined to encapsulate specific data processing tasks, making the code more modular and readable.
7. Data Visualization: Python libraries (e.g., Matplotlib or Seaborn) were used for data visualization, enabling the creation of informative charts to convey insights.

# Database ERD
The database schema for this analysis consists of three key tables:

![image](https://github.com/Dibieoluchi/banking_data/assets/88893142/08d4535a-7047-41f4-ad6d-b51351766cff)


1. world_regions: Contains data on various world regions and their corresponding codes and names.
2. user_nodes: Holds details about consumers' banking nodes, including their unique consumer IDs, associated region IDs, node IDs, start dates, and end dates.
3. user_transaction: A comprehensive repository of customer transactions, including data such as consumer IDs, transaction dates, types of transactions, and transaction amounts.


The relationship between these tables is established through foreign key relationships, which allow for the creation of meaningful queries that draw connections between customer behavior and regional impact.

# Analysis and Insights Generated

The analysis yielded several key insights:

# Customer Distribution and Region Impact:


Explanation: The analysis revealed significant disparities in customer distribution across different regions. The United States had the highest number of customers, whereas Russia and China had the lowest. Additionally, the number of banking nodes (physical locations) in each region varied, with the United States, Europe, and Australia having the most nodes.

Problem: The discrepancy in customer distribution can pose challenges for the bank. Regions with a lower number of customers may have untapped market potential, while regions with a high number of customers may face increased competition and resource allocation challenges. Furthermore, the number of banking nodes reflects the bank's physical presence, and imbalances in node distribution could impact customer convenience and accessibility.
![image](https://github.com/Dibieoluchi/banking_data/assets/88893142/59022715-dbd2-4980-b59b-a45ca5076578)


# Transaction Types

Explanation: The primary transaction types observed were withdrawals, purchases, and deposits. Deposits were common and significant, with customers making around 5 deposits on average, totaling approximately $2,718 each.

Problem: While the analysis provides valuable information about customer transaction behavior, it raises questions about the reasons behind high deposit activity. Are customers using the bank primarily as a savings institution? Are there enough investment and lending opportunities to make use of these deposits? It's essential for the bank to ensure that customers' financial needs and expectations are being met effectively.



![image](https://github.com/Dibieoluchi/banking_data/assets/88893142/c798831a-63fb-4742-b6ac-c8460578e070)



# Customer Churn Analysis

Explanation: The analysis indicated that approximately 14.28% of customers had churned by the end of 2020, while 85.72% were retained. Furthermore, churned customers had varying transaction amounts, with some making high-value transactions.

![image](https://github.com/Dibieoluchi/banking_data/assets/88893142/c8011033-9f5a-4808-a29e-4326034b0ca7)

# churned_summary
1. count    5864.000000
2. mean      504.228513
3. std       288.189135
4. min         0.000000
5. 25%       256.000000
6. 50%       503.000000
7. 75%       753.000000
8. max      1000.000000


Mean: On average, these customers had a typical transaction of around $504.23.

Standard Deviation (std): The transaction amounts vary, and on average, they differ by about $288.19 from the typical amount.

Minimum (min): The minimum transaction amount observed for churned customers is $0. This indicates that there are customers who churned without making any transactions.

25th Percentile (25%): 25% of these customers had transactions of $256 or less.

50th Percentile (Median, 50%): Half of these customers had transactions of $503 or less.

75th Percentile (75%): 75% of these customers had transactions of $753 or less.

Maximum (max): The highest transaction among these customers was $1000.

In summary, these statistics provide insights into the transaction amounts of customers who have churned.

The average transaction amount is approximately $504.23, with a moderate level of variability.

some customers have churned without making any transaction at all ,while others had a transaction amount ranging from 0 to a maximum of $1000


Problem: Customer churn can be a significant issue for the bank. High churn rates indicate a potential loss of revenue, and understanding the reasons behind churn is critical. The observation that customers with 'deposit' transaction behavior exhibit a higher likelihood of churning could suggest that the bank needs to provide more diverse and tailored financial products to retain these customers. Additionally, identifying and retaining high-value churned customers should be a priority.

![image](https://github.com/Dibieoluchi/banking_data/assets/88893142/e08bfa51-1db2-4366-8f14-ce9ee1d4875a)



# Regional Impact: Customer Presence and Customer Churn

Explanation:


The analysis revealed that the United States and Europe had a strong customer presence and high retention rates. In contrast, regions like Africa displayed comparatively lower customer retention and impact. The data provides a clear picture of customer distribution across various regions, offering vital insights for the bank's understanding of its customer base. When we connect this information with our earlier examination of banking nodes (locations), a compelling pattern emerges. It becomes evident that regions with a higher count of consumers often coincide with regions hosting a more extensive network of banking nodes.

For example, the United States, with the highest count of consumers at 770, aligns with our previous findings of an extensive banking node network, highlighting a robust presence and high customer activity in this region. Similarly, Europe's 735 consumers correspond to the significant number of banking nodes, signifying a flourishing financial environment with diverse services. The number of consumers in Australia, Asia, and Africa also corresponds with the banking activity observed in those regions.

The analysis extends to a KDE plot, offering further insights. It becomes apparent that each region managed to retain more customers than they lost, indicating a successful overall customer retention strategy. However, the data also reveals that Region 5, corresponding to Africa, had the lowest number of retained customers, while Region 1, representing the United States, had the highest retention rate.

This finding carries significance for the bank as it suggests that while the overall customer retention strategy is effective, specific challenges or factors may be affecting customer retention in the African region. This could imply that the bank needs to pay closer attention to this region and consider tailoring retention strategies to address region-specific issues.

Problem:
The regional disparities in customer retention and impact underscore potential challenges for the bank. Lower retention rates in certain regions may result from various factors, including inadequate services, the absence of tailored products, or external economic challenges. To address these disparities and avoid missed business opportunities, the bank must investigate the specific reasons behind these differences and develop strategies to rectify them. Neglecting regions with lower impact could lead to missed growth potential and a less effective market presence.


![image](https://github.com/Dibieoluchi/banking_data/assets/88893142/91406a92-d7d5-465f-80d5-d5100cb4056c)


![image](https://github.com/Dibieoluchi/banking_data/assets/88893142/3ff2bd0a-6d12-4b2b-b945-1bd3b180f16c)







# Conclusion and Recommendations

Conclusion and Recommendations:

In conclusion, our analysis has revealed important opportunities for the bank to improve its services and customer retention. Here are some straightforward recommendations:

1. Regional Focus:

Actionable Recommendation: Identify regions with fewer customers and lower retention rates, such as Africa. To address this, the bank can set up local branches and improve customer support in these areas. This will make banking more accessible and build trust in underserved regions.
2. Customer Engagement:

Actionable Recommendation: Customers who primarily save should be educated about investment opportunities. The bank can create simple brochures or online tutorials explaining the benefits of investments like mutual funds or certificates of deposit. Make sure this information is readily available on the bank's website.
3. Product Development:

Actionable Recommendation: Design region-specific savings accounts or loans that cater to the unique needs of customers in different areas. Create marketing materials that clearly explain these products, their advantages, and how to open or apply for them.
4. Data-Driven Marketing:

Actionable Recommendation: Use data to personalize marketing efforts. Send tailored messages to customers based on their transaction history. For example, if a customer mainly deposits money, send them information about the bank's high-yield savings account with a clear explanation of how it works and the benefits.
   

# Data Limitations

It's essential to acknowledge the limitations of the data, including the restricted time frame with data available for only two years. This limitation may affect the depth of insights related to long-term trends and changes in customer behavior. Additionally, external factors and macroeconomic conditions may influence regional impacts beyond what is captured in the dataset.

In conclusion, the combination of SQL and Python skills, coupled with data visualization, has allowed for a comprehensive analysis of customer transactions and their regional impact, offering actionable insights for the bank's strategic planning and decision-making. This approach can be a valuable asset for any financial institution seeking to optimize its services and improve customer retention.
