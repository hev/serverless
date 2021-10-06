<!--
title: Serverless Dashboard - FAQ
menuText: FAQ
layout: Doc
-->

# FAQ

## Is there a free tier?
Yes. The first 100,000 monitoring transactions are free.

## How much does it cost for more transactions?
After the first 100,000 monitoring transactions each million monitoring transactions 
per month costs $70.  

## What counts as a monitoring transaction? 
A monitoring transaction refers to the set of data points collected when a serverless 
compute invocation occurs. These data points are collected together meaning an API-Gateway 
request that triggers a Lamda invocation will only count as 1 metric. This open definition 
of monitoring transactions will allow us to expand to future compute platforms and is 
the data that powers our alerts, charts and explorer. 


## How can I check my monitoring transactions costs?
As we roll out transaction based pricing, the total monitoring transactions for your 
org will be listed in your billing page, along with the expected cost and invoice date 
for your next bill. 

## Are there usage limits for the team tier? Why?
Yes, the team tier is limited to 15 million monitoring transactions per month. 
This is to prevent your monthly costs from getting out of control. With this restriction 
the maximum monitoring bill of $1050 per month. 

## How can I ensure I have unlimited monitoring transactions?
To get unlimited marketing transactions please contact sales@serverless.com to sign up 
for the enterprise tier. 

## Can I disable monitoring on my service?
Yes. You can disable monitoring on your service by including the following in your 
`serverless.yaml` file and redeploying.

```
custom:
 enterprise:
   collectLambdaLogs: false
```
