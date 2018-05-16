---
title: Motivation for OPQ
sidebar_label: Motivation for OPQ
---

## The problem with power

Power quality is not currently a concern for most people in the United States.  Just like most people assume that their tap water is of adequate quality to drink, most also assume that their electricity is of adequate quality to power their homes and appliances without causing harm. And, in both cases, most people assume that public utilities will monitor and correct any quality problems if they occur.

Successfully maintaining adequate power quality and providing sufficient amounts of it to meet the rising needs of consumers has been a triumph of electrical utilities for over 100 years.  In recent times, however, there have been changes to the nature of electrical generation and consumption that make power quality of increasing public concern and interest.  

The Open Power Quality project began in 2012 with the goal of developing and evaluating technology to support three important improvements to electrical infrastructure: 

  1. Increase the capacity of small and large electrical grids to employ distributed, intermittent forms of renewable energy.
  2. Gain insight into lifespan and failure rate problems in consumer electronics due to poor power quality.
  3. Provide an independent, low cost source of useful power quality data to consumers, researchers, and public policy makers.  

Let's look at each part of this vision in a bit more detail.

### We need more renewable energy

There is now a global movement away from centralized, fossil-fuel based forms of electrical energy generation and toward distributed, renewable alternatives such as wind and solar. This movement is particularly relevant to Hawaii, where over 80% of its electrical energy comes from oil, and where the average cost per kilowatt-hour of electricity is triple that of the mainland United States.  But the economic, environmental, and political advantages of renewable energy comes with significant new technical challenges.  Wind and solar are intermittent (for example, solar energy cannot be harvested at night) and unpredictable (for example, wind and solar energy fluctuate based upon cloud cover and wind speed).  In addition, renewable energy generation can be distributed throughout the grid (such as in the case of residential rooftop photovoltaic (PV) systems).  

One impact of adding renewable energy generation to an electrical grid is that maintaining adequate power quality is much more challenging.  This manifests itself in Hawaii in a very visible and negative way: the public demand for rooftop solar far exceeds Hawaiian Electric Company's ability to utilize it and maintain adequate power quality. As a result, in many neighborhoods, new rooftop solar installation is prohibited because Hawaiian Electric fears its impact on not only local power quality but global grid stability.  

OPQ intends to provide power quality data that can be used by utilities and renewable energy researchers to create technology that will enable grids like Hawaii's to increase their use of renewable energy.  

### Consumer electronics require higher quality power 

The rise of consumer electronics has raised the bar for what constitutes "adequate" power quality. Only a few decades ago, computers were a rare presence outside of labs and large institutions.  Today, computers are everywhere: embedded in phones, washers, refrigerators, thermostats, and so forth. These electronic devices not only have higher power quality requirements, but some of them actually introduce power quality problems in the form of harmonic distortion.  Poor power quality can result in electronic devices failing unpredictably, and/or decreasing their lifespan.

OPQ intends to provide power quality data that can be used to determine if potentially harmful fluctuations in power are being supplied to appliances. 

### Power quality data should be publicly available

Electrical utilities are not required to be totally transparent about the quality of power they provide to consumers.  For example, in Hawaii, utilities are required to make a "best effort" to provide non-harmful voltage and frequency values, but are only required to publicly report on power outages of more than 3 minutes. There is no requirement for utilities to report potentially harmful forms of voltage, frequency, THD, or transients.  Indeed, in Hawaii, there is not yet infrastructure in place that would enable utilities to collect that information, even if they were asked to report on it. For more details, see [Hawaiian Electric Tariff Rule No. 2 Character of Service](https://www.hawaiianelectric.com/Documents/my_account/rates/hawaiian_electric_rules/2.pdf) and [Hawaiian Electric Tariff Rule No. 16 Interruption of Service](https://www.hawaiianelectric.com/Documents/my_account/rates/hawaiian_electric_rules/16.pdf).

OPQ intends is to provide an unbiased, independent, third party source of accurate power quality data. This can be used by consumers to better understand the performance of their public utilities, by researchers to devise improvements to grid control, and by public policy makers responsible for designing and implementing regulatory frameworks for electrical utilities.

## What's new about OPQ?

Successfully achieving this vision requires innovative research in power quality hardware design, analytics design, and visualization design. To support the research process, the OPQ project has a unique combination of features.

First, our power quality monitoring hardware device, called "OPQ Box" can be produced for approximately \$75. This is from 10 to 100 times less expensive than commercial power quality monitors. We achieve these cost savings by customizing the capabilities of OPQ Boxes to our specific goals. 

Second, our architecture is "cloud native", which means that OPQ Boxes cannot be used in a "stand alone", autonomous fashion. Instead, our hardware boxes and cloud-based services perform real-time, two-way communication over the Internet to determine what power quality data must be gathered and analyzed. This creates the ability to make requests of individual OPQ Boxes based upon the global state of all OPQ Boxes. It also means our cloud services can obtain and analyze high fidelity wave form data only when desired, without the prohibitive network overhead of constantly communicating this data from boxes to the cloud. 

Third, all OPQ software subsystems are designed for extensibility and interoperation.  Our middleware components (Mauka and Makai) provide a plugin architecture.  Our visualization component (View) consists of modular UI elements using React. We also provide API endpoints for interoperation with other software systems.

Finally, our software and hardware designs and implementations are made available using open source licenses. Our goal is to facilitate the creation of a community of researchers and industry practitioners to replicate, extend, and apply the insights gained from the OPQ system.

## Short term goals for OPQ

To make progress toward our vision, our goals for 2018 are the following:

1. Assess the ability of our current hardware and software to support fast deployment of a distributed sensor network for collecting accurate and useful power quality data. 

2. Design and implement a suite of analyses and visualizations that provide useful and actionable feedback to users regarding the sensor network and any power quality problems it detects.

3. Perform a pilot deployment of OPQ to monitor the University of Hawaii at Manoa's microgrid as part of the [Agile Power Monitoring Project](agile-power-monitoring.md).