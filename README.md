# Insurance-Analytics-Project
You are working for an insurance company that has a network of agents across different cities and countries. The company has a database of agents, customers, and orders. The goal is to effectively manage the relationships between agents, customers, and the orders placed by the customers. Additionally, the company aims to assess risks associated with customer accounts and detect potential fraud in the orders placed.

### ERD
![image](https://github.com/user-attachments/assets/d6808a37-a924-46b6-865a-1516f283a07a)

### Problem 1
*Business Scenario*: The company wants to optimize its operations by identifying agents who are underperforming in terms of the total order amounts they are handling. Specifically, they need to find the 5 agents with the lowest total order amounts. These agents might be subject to review or potential termination based on their performance.

*Task*: Write a SQL query that retrieves the names of the 5 agents with the least total order amounts. The output should include the following columns:
* agent_name: The name of the agent.
* total_ord_amount: The total amount of orders handled by the agent.
* ranking: The rank of the agent based on the total order amount, where 1 indicates the agent with the lowest total order amount.

### Problem 2
*Business Scenario*: The company aims to identify the most financially stable customers by finding those with the lowest outstanding amounts in each country. This analysis will help the company understand which customers are least likely to default on payments. However, it has been noted that data provided by the agent named "Mukesh" is not reliable, so any data associated with this agent should be excluded from the analysis.

*Task*: Write a SQL query that retrieves the name of the customer with the minimum outstanding amount from each country. The output should include the following columns:
* cust_country: The country of the customer.
* cust_name: The name of the customer with the minimum outstanding amount in that country.

### Problem 3
*Business Scenario*: The company wants to analyze the payment behavior of customers in different cities. Specifically, they are interested in understanding how payments accumulate over time for customers within the same city. Additionally, the company is interested in seeing how payments trend when considering not just the current payment but also the payments from the next two rows.

*Task*: Write a SQL query that calculates the running total of the payment_amt for each cust_city, ordered by the grade in ascending order. The running total should include the payment_amt of the current row plus the payment_amt from the next two rows.The output should include the following columns:
* cust_city: The city of the customer.
* payment_amt: The payment amount from the current row.
* running_tot: The running total of payment_amt calculated by summing the current row's payment_amt and the payment_amt of the next two rows.

### Problem 4
*Business Scenario*: The company wants to adjust the commission rates for its agents based on their performance in collecting advance payments. The adjustment is to be made according to the average amount of advance payments each agent has collected. The goal is to incentivize agents who collect higher advance payments by increasing their commission, while reducing the commission for those who collect lower advance payments.

*Task*: Write a SQL query that calculates a new commission rate for each agent based on the following rules:
1. If the average advance amount collected by an agent is less than 750: The new commission will be 0.75 times the current commission.
2. If the average advance amount collected by an agent is between 750 and 1000 (inclusive): The new commission will be 0.9 times the current commission.
3. If the average advance amount collected by an agent is more than 1000: The new commission will be 1.2 times the current commission.

The output should include the following columns(The newly calculated commission based on the rules above):
* agent_code: The code of the agent.
* updated_commission:
