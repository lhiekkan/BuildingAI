# Scheduling of combined heat and power production using AI methods

Intraday scheduling of combined heat and power production using AI methods
Final project for the Building AI course

## Summary

Optimizing daily operations in district heating utility is a tough task. I would like to find good toolkit how to optimize short term operations for heat production and distribution and intraday electricity markets.


## Background

How to utilize intraday electricity markets when making short term heat and power generation decisions? This kind of decision making is continous 24/7/365 and succesful decisions will contribute to local heat production costs and in large scale electricity grid stability. My personal motivation is professional and personal interest to methods that could be utilized to enhance district heating utilities efficiency. In the end this can have a positive effect on district heating end customers and climate goals.

## How is it used?

This kind of solution should be run automatically in short frequency as new data is coming in constantly. This kind of solution could help district heating operators or even automate short term decision making.

Sample data and process could be:
* Data from production measurements coming almost real time
* Data from district heating network available almost at same frequency
* Intraday electricity market trades and offers are also constantly living
* Weather and thus heat consumption forecast for different network areas is changing roughly every hour
* We have our current production plan and market commitments
* Model should run as frequently as possible like every minute
* Model should result how utility should fill it's heat delivery obligations with minimal cost considering production, electricity markets and available heat storages and consumption flexibilities.
* Execution of such plans would go to SCADA-systems and separate trading systems

## Data sources and AI methods
There is loads of data from heat and power production and distribution related to this and most of it belongs to utilities. Market data of the intraday markets are available from Nordpool and Fingrid in Finland. To get reasonable results solution should use logistic regression and/or neural networks to find out correlations combined with some physical modelling and constraints. So not exactly an easy task.

## Challenges

Ingesting all mentioned data and it's quality can be a problem as there is always some malfunctioning measurements etc. Also finding model that could holistically consider markets, production and heat distribution well enough can be challenging. Longer term planning has been usually done with MILP models and limits set by longer optimization need to be also taken into account.

This would not solve trade execution to electricity markets nor controlling any physical systems, but those should be integrated to this kind of holistic model.
When runnign this kind of scheduling and trading loop what should be role of 24/7 operators? Where is the responsibility if something potentially expensive happens?

## What next?

It could be interesting to build demonstration model around this idea to see whether it is possible and what are the real methods that might work. To build something concrete would need collaboration with some district heating utility and help from real modelling specialist(s) who could know what methods to use for each subproblems and how to combine those. My knowledge is limited to modelling basics and utility processes.

## Acknowledgments

I would start with Python AI and analytics libraries. My inspiration here is experience in energy business and emerging ideas of end-to-end optimization of district heating process to make a step change in district heating efficiency and enable unconventional heat sources.
