
# Coding Challenge

## Overview

This coding challenge is directly based on the kind of economic questions you will be trying to answer with your research. As with all data challenges, there is no one way or correct way of doing this. This coding challenge is a two-way test. It not only shows us how you can creatively solve issues by playing with economic intuition, definitions, data, and coding, but it also shows you what kind of issues you will be faced with daily.

The question of nowcasting is straightforward: if you had all the data, you would just need to do a simple sum to get the right numbers. However, reality is that you will never have all the data nor anywhere near perfect data for the economic activity in the whole country. You will need to do smart aggregation, balancing, labeling, etc. Figuring out novel and inventive ways of getting as much information as possible out of the data you do have and still getting a good picture of what the economy is doing will be the majority of the work. By the end of your Ph.D., you will have spent so much time tackling such issues that you will be a wizard with financial data in Python at scale.

This test is as much for us to get to know if you are a good fit for us as it is for you to see if this project is a good fit for you. You should not spend more than an afternoon or evening on this project (+- 3 hours max). Submit your solution to your own branch on the [Prometis Lab GitHub project](https://github.com/PrometisLab/Coding-interview-nowcastingv2).

## Instructions

1. **Document your thinking**.
2. **Provide a basic solution** to the challenge in Python and push it to your own branch on the [GitHub repo](https://github.com/PrometisLab/Coding-interview-nowcastingv2).
3. **Visualization** is optional but will help us better understand what you are trying to do. 
4. You can also write part of your solution in **pseudo-code or text**. If you do, explain what you would do, the breakdown of how you would do it logic- and code-wise, and the output you intend to generate.
5. **Provide a report** communicating your approach and results to the selection committee. Be concise but clear. The committee is made up of economists, finance professionals, and data scientists. Communicate accordingly.

## Datasets Provided

You are provided with two datasets:
- **Company Information Dataset (`company_info.csv`)**
- **Transactions Dataset (`transactions.csv`)**

While this is completely fake data, treat it as if it represents all financial transactions for all clients of one financial institution within a single country.

### Company Information Dataset (`company_info.csv`)

| Column       | Description                                                                            |
|--------------|----------------------------------------------------------------------------------------|
| company_id   | Unique ID for each company (e.g., A1, A2, ... A400)                                     |
| nace_code    | Industry classification code (A to U)                                                  |
| location     | Province in Belgium                                                                    |

### Transactions Dataset (`transactions.csv`)

| Column         | Description                                                                                          |
|----------------|------------------------------------------------------------------------------------------------------|
| party          | A client ID (0-1000) or company ID (A1-A400) and sender of the transaction                           |
| timestamp      | datetime between 2022-2024                                                                           |
| amount         | Transaction amount                                                                                   |
| counterparty   | The counterparty or receiver of the transaction                                                      |
| communication  | Text field filled in by the sender of the transaction                                                |

## Challenge Objective

Your challenge is to map the economic activity in Belgium from the data using Python. You are encouraged to take inspiration from the literature (especially the work by Killian Huber and Ludwig Straub on [disaggregated economic accounts](https://www.disaggregatedaccounts.com/research_paper) and Vasco Carvalho on [National Accounts](http://vasco-m-carvalho.github.io/pdfs/Buda_et_al_2022_Consumption_online.pdf)).

### Elements to Consider:

1. **Scales of Economic Activity**:
   - Economic activity has multiple scales from the country level (e.g., GDP) down to the individual level (personal finances).
   - Consider the following questions:
     - How can economic activity be defined? If there are multiple approaches, why choose one over the other? Or why mix multiple?
     - What information is available to give economic meaning to the transactions and how would you utilize it in a scalable way?

2. **Output and Standards**:
   - Your output should be usable by financial institutions, governments, and executives across the private sector to make decisions regarding policy, business investments, loans, etc.
   - What standards exist (or would you create) to define, categorize, and present “economic activity” such that all economic actors across the world can use this information?

3. **Visualization**:
   - What visualization(s) would help make the information digestible?

4. **Challenges**:
   - What challenges are there that you didn’t get to tackle and how would you approach them if you had more time?
   - Is there information available that you did not end up using but would if you had more time? For what would you use it and how?
