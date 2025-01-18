# Insurance-Analytics-Project
You are working for an insurance company that has a network of agents across different cities and countries. The company has a database of agents, customers, and orders. The goal is to effectively manage the relationships between agents, customers, and the orders placed by the customers. Additionally, the company aims to assess risks associated with customer accounts and detect potential fraud in the orders placed.

### ERD
![image](https://github.com/user-attachments/assets/d6808a37-a924-46b6-865a-1516f283a07a)

### Problem 1
*Business Scenario*: The company wants to optimize its operations by identifying
agents who are underperforming in terms of the total order amounts they are
handling. Specifically, they need to find the 5 agents with the lowest total order
amounts. These agents might be subject to review or potential termination based
on their performance.

*Task*: Write a SQL query that retrieves the names of the 5 agents with the least
total order amounts. The output should include the following columns:
1. agent_name: The name of the agent.
2. total_ord_amount: The total amount of orders handled by the agent.
3. ranking: The rank of the agent based on the total order amount, where 1 indicates the agent with the lowest total order amount.

### Problem 2
*Business Scenario*: The company aims to identify the most financially stable
customers by finding those with the lowest outstanding amounts in each country.
This analysis will help the company understand which customers are least likely
to default on payments. However, it has been noted that data provided by the
agent named "Mukesh" is not reliable, so any data associated with this agent
should be excluded from the analysis.

*Task*: Write a SQL query that retrieves the name of the customer with the
minimum outstanding amount from each country. The output should include the
following columns:
1. cust_country: The country of the customer.
2. cust_name: The name of the customer with the minimum outstanding amount in that country.

