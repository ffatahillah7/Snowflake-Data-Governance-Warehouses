# Snowflake-Data-Governance-Snowflake-Warehouses

## Overview
Welcome to the Powered by Tasty Bytes - Zero to Snowflake Quickstart focused on Data Governance!

Within this Quickstart we will learn about Snowflake Roles, Role Based Access Control and deploy both Column and Row Level Security that can scale with your business.

quickstart link : https://quickstarts.snowflake.com/guide/tasty_bytes_zero_to_snowflake_governance_with_horizon/index.html?index=..%2F..index#0

## Prerequisites
Before beginning, please make sure you have completed the Introduction to Tasty Bytes Quickstart which provides a walkthrough on setting up a trial account and deploying the Tasty Bytes Foundation required to complete this Quickstart.
Please note that features leveraged within this Quickstart will require an Enterprise or Business Critical Snowflake account. Please see our documentation an Overview of Snowflake Editions.

## What You Will Learn
1.  What System Defined Roles Exist in Snowflake Accounts
2.  How to Create a Role
3.  How to Grant Privileges to a Role
4.  How to Create a Tag
5.  How to Create a Masking Policy
6.  How to Deploy a Tag Based Masking Policy
7.  How to Create a Row Access Policy using a Mapping Table
8.  How to Create an Aggregation Policy
9.  How to Create a Project Policy
10.  How to Leverage Automatic and Custom Data Classification
11.  How to use Universal Search
    
## What You Will Build
1.  Complete Role Based Access Control for a Test Role
2.  A Robust Data Governance Foundation for your Account

## Lesson Result
1.  Create roles structure such as account admin, system admin, custom role and public.
2.  Grant access to each role.
3.  Column-Level Security and Tagging = Tag-Based Masking. This tag is set to masking specific columns such as email, phone number and any other restricted data. Change the value with masking (***---**). So, it can't read by the users.
4.  Row-Access Policies. In this scenario, we create roles and policies for specific value in the table. For example, for roles IT department, it's just retrieved all data in IT Department. Another examples is roles or policies for just specific country for certain users based on the country.
5.  Aggregation Policies. In this secnario, we create roles and policies for just aggregate the query. If we query all using select *, it show warning Aggregation policy violation. We just have access for aggregating based on specific columns.
6.  Projection Policies. In this steps, we will prevent queries from using a SELECT statement to project values from a column. Except we use exclude function to exclude specific columns from the table. If we query by normal it will show warning : The following columns are restricted by a Projection Policy. Please remove them from the list of projected columns.
7.  Sensitive Data Classification. Using this query CALL SYSTEM$CLASSIFY('raw_customer.customer_loyalty', {'auto_tag': true});  , we can scanning the columns with possible sensitive data and give us recommendation to masking or taging the columns.
8.  Access History (Read and Writes). Last step is to discover query , counting the query for each table. For Examples, we have 30 query on employee table.
