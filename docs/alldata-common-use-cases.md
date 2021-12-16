![](RackMultipart20211216-4-qi02uc_html_53682ed0403f8dd3.png) ![](RackMultipart20211216-4-qi02uc_html_d0e7ab49cd1625bc.jpg)

AllData®

Common Data Aggregation Use Cases and AllData API Solutions

August, 2020

#####


© 2020 Fiserv, Inc. or its affiliates. All rights reserved. This work is confidential, and its use is strictly limited. Use is permitted only in accordance with the terms of the agreement under which it was furnished. Any other use, duplication, or dissemination without the prior written consent of Fiserv, Inc. or its affiliates is strictly prohibited. The information contained herein is subject to change without notice. Except as specified by the agreement under which the materials are furnished, Fiserv, Inc. and its affiliates do not accept any liabilities with respect to the information contained herein and are not responsible for any direct, indirect, special, consequential or exemplary damages resulting from the use of this information. No warranties, either express or implied, are granted or extended by this document.

[http://www.fiserv.com](http://www.fiserv.com/)

Fiserv is a registered trademark of Fiserv, Inc.

Other brands and their products are trademarks or registered trademarks of their respective holders and should be noted as such.

# Contents

**[Introduction 4](#_Toc47364352)**

[Overview 4](#_Toc47364353)

**[Use Cases 5](#_Toc47364354)**

[Bank account ownership verification 5](#_Toc47364355)

[Balance verification 5](#_Toc47364356)

[Add payment account 5](#_Toc47364357)

[Transaction history 6](#_Toc47364358)

[Asset verification 6](#_Toc47364359)

[Liability verification 7](#_Toc47364360)

[Personal Financial Management (PFM) 7](#_Toc47364361)

# Introduction

The purpose of this document is to provide guidance to Fiserv partners on the order in which they should call the AllData APIs as well as the APIs to call for specific use cases and solutions. This document is meant for API partners that do not use Fiserv widgets.

## Overview

In all instances noted below, the partner must first be created in the AllData system. Fiserv&#39;s professional services team creates the partner&#39;s administrative account and whitelists the partner&#39;s IP address.

Each partner will have a partner ID and at least one home ID created in the AllData system. Some partners may choose to use multiple home IDs depending on different use cases. A partner can provision multiple customers (users) under its home ID. A user may have more than one financial institution account under his or her profile.

For all use cases outlined below, the partner must create a user profile using the [CreateUser API](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/User%20Management%20Service/createUser). The user profile consists of the user ID, password, and several optional fields including name, address, etc.

Partners must follow the bootstrapping process to synchronize the Fiserv AllData connections directory on their end. This one-time process uses the [GetFinancialInstInfo API](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Seeded%20Data%20Inquiry%20Service/getFinancialInstInfo). Partners can also periodically refresh to get the latest changes made by financial institutions. See the _AllData Web Services API Specifications_ document for additional details.

# Use Cases

This chapter describes several use cases or solutions and lists the APIs they require.

### Bank account ownership verification

A wide variety of organizations can benefit from bank account ownership verification, such as lenders (including mortgage lenders), ACH payment processors, e-commerce platforms, and wealth management organizations.

This use case is necessary for a partner to verify the bank account ownership of its end users. This can be accomplished through AllData by exposing the following APIs that allow end users to connect to their FI accounts using their login credentials.

**APIs required:**

- [initiateAddAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/initiateAddAccounts)
- [getAddAccountStatus](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/getAddAccountStatus) (1..n)
- [getNewAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/getNewAccounts)

**Note:** This series of APIs only validates that the user can log in and has ownership of the account. If the partner requires routing and account numbers, see &quot;Add payment account&quot; below.

### Balance verification

Balance verification is useful for lenders, ACH payment processors, e-commerce platforms, and others.

This use case is necessary for a partner to verify the balance(s) of the account(s) linked to the consumer.

**APIs required:**

- [initiateAddAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/initiateAddAccounts)
- [getAddAccountStatus](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/getAddAccountStatus) (1..n)
- [getNewAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/getNewAccounts)

### Add payment account

Adding a payment account is useful for organizations specializing in ACH money movement, which can include lenders (including mortgage lenders), e-commerce platforms, and bill payment providers.

AllData can be used to add an ACH payment account of an end user after that account has been verified. The full account number and routing number must be collected for the account to add it as a payment account.

**APIs required:**

- [initiateAddAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/initiateAddAccounts)
- [getAddAccountStatus](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/getAddAccountStatus) (1..n)
- [getNewAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/getNewAccounts)
- [createAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/createAccounts)
- [updateAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Harvest%20Account%20Data%20Management%20Service/updateAccounts)
- [getHarvestStatus](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Harvest%20Account%20Data%20Management%20Service/getHarvestStatus) (1..n)
- [getAccountDetails](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getAccountDetails)

### Transaction history

Transaction history is useful for any organization requiring insight into consumer account activity.

AllData can be used to obtain the transaction history for a number of accounts including savings, checking, credit card, money market, and investments.

**APIs required:**

- [initiateAddAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/initiateAddAccounts)
- [getAddAccountStatus](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/getAddAccountStatus) (1..n)
- [getNewAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/getNewAccounts)
- [createAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/createAccounts)
- [updateAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Harvest%20Account%20Data%20Management%20Service/updateAccounts)
- [getHarvestStatus](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Harvest%20Account%20Data%20Management%20Service/getHarvestStatus) (1..n)
- [getAccountDetails](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getAccountDetails)
- For banking account transactions, use [getBankingTrans](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getBankingTrans)
- For biller account transactions, use [getOtherAccountTrans](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getOtherAccountTrans)
- For credit card account transactions, use [getCreditCardTrans](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getCreditCardTrans)
- For investment account transactions, use [getInvestmentTrans](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getInvestmentTrans)

### Asset verification

Asset verification is useful for lenders, who often need to know the net worth of their borrowers.

AllData can be used to verify the assets held by an end user. These assets are grouped into categories including bank accounts, investment accounts, retirement accounts, home values, and insurance policies.

**APIs required:**

- [initiateAddAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/initiateAddAccounts)
- [getAddAccountStatus](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/getAddAccountStatus) (1..n)
- [getNewAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/getNewAccounts)
- [createAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/createAccounts)
- [updateAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Harvest%20Account%20Data%20Management%20Service/updateAccounts)
- [getHarvestStatus](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Harvest%20Account%20Data%20Management%20Service/getHarvestStatus) (1..n)
- [getAccountDetails](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getAccountDetails)
- [getOtherAccountTrans](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getOtherAccountTrans)
- [getEmployerStockOptions](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getEmployerStockOptions)
- [getInvestmentPos](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getInvestmentPos)
- [getInvestmentTrans](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getInvestmentTrans)

### Liability verification

Liability verification is useful for lenders because they often need to know the outstanding financial commitments of their borrowers.

AllData can be used to verify the liabilities of an end user. Liabilities are grouped into categories including credit cards, mortgages, loans, and bills.

**APIs required:**

- [initiateAddAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/initiateAddAccounts)
- [getAddAccountStatus](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/getAddAccountStatus) (1..n)
- [getNewAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/getNewAccounts)
- [createAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Management%20Service/createAccounts)
- [updateAccounts](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Harvest%20Account%20Data%20Management%20Service/updateAccounts)
- [getHarvestStatus](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Harvest%20Account%20Data%20Management%20Service/getHarvestStatus) (1..n)
- [getAccountDetails](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getAccountDetails)
- [getOtherAccountTrans](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getOtherAccountTrans)
- [getCreditCardTrans](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Account%20Data%20Inquiry%20Service/getCreditCardTrans)

### Personal Financial Management (PFM)

PFM is used for partners who want to provide end users with budgeting tools, savings goals, statements (including bank statements and tax documents), forecasting, home values, and cash flow analysis.

AllData can be configured to categorize transactions.

All the APIs noted in the above use cases are applicable to PFM since PFM tools are typically used to provide a complete picture of an end user&#39;s financial position. In addition to the APIs noted above, the following can also be applied to the PFM use case:

- [categorizeTransaction](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Update%20Transaction%20Category%20Service%20PFM/categorizeTransaction)
- [deleteSubCategory](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Update%20Transaction%20Category%20Service%20PFM/deleteSubcategory)
- [createBudget](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Budget%20Management%20Service%20PFM/createBudget)
- [editBudget](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Budget%20Management%20Service%20PFM/editBudget)
- [deleteBudget](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Budget%20Management%20Service%20PFM/deleteBudget)
- [findBudget](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Budget%20Management%20Service%20PFM/findBudget)
- [editGoal](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Goal%20Management%20Service%20PFM/editGoal)
- [deleteGoal](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Goal%20Management%20Service%20PFM/deleteGoal)
- [findGoal](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Goal%20Management%20Service%20PFM/findGoal)
- [createGoal](https://agg-uat.api.fiservapps.com/WealthManagementWeb/api/index.jsp#/Goal%20Management%20Service%20PFM/createGoal)