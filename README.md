# CompoundEventsMigrationABM

Accompanying paper: Thalheimer, L.; Choquette-Levy, N.; and F. Garip (2022). "Compound Impacts from Droughts and Structural Vulnerability on Human Mobility", iScience (in preparation).

Hello! This repository contains the code used to develop the agent-based model used for the Nepal case study in the paper "Compound Impacts from Droughts and Structural Vulnerability on Human Mobility."

The main goal of this project was to better understand how compound risks, including droughts and social factors leading to vulnerability (e.g. limited social networks) affect human mobility outcomes, compared to single events. The paper assesses these intersections for three case studies - Madagascar, Mexico, and Nepal - using three methods - vulnerability pathway modelling, linear probability modelling, and agent-based modelling, respectively. This repository contains the code for the ABM, which simulates how farmers decide on livelihood strategies with different risk/reward profiles, as a function of information they receive from their social networks, changing climatic conditions, and policy interventions.

This ABM is an extension of the one developed for the paper 'Risk transfer policies and climate-induced immobility among smallholder farmers', whose code can be found here: https://github.com/nchoquettelevy/RiskTransferClimateImmobilityABM. There are two main additions to this extension. First it includes two distinct migraiton channels - a local and international channel - parameterized by costs, expected incomes, and standard deviations of remittances as reported in Shrestha, M. (2017). Push and Pull: A Study of International Migration from Nepal (SSRN Scholarly Paper No. 2913956). Social Science Research Network. https://papers.ssrn.com/abstract=2913956![image](https://user-images.githubusercontent.com/49871094/196009056-63d2165e-708e-487b-85da-ebf7a6f6a795.png).

Second, this extension also includes the ability to precisely turn on/off droughts in specific cropping cycles through the parameters experiment_start (which specifies the cycle at which stochastic droughts are turned "off") and drought_cycles (a list that includes the specific cycles in which a drought is to occur). To investigate the compounding effects of droughts and a spike in temperature, the parameters spike_start and spike_end specify the period over which a short-term temperature spike is simulated.


The model is parameterized with economic data from the Chitwan Valley Family Study (CVFS); specifically, the public-use version of the "Agriculture and Migration Survey Calendar Data", available here: https://cvfs.isr.umich.edu/data/data-documentation/household-level-data/.

The accompanying code is in Jupyter notebook format (.ipynb), and contains the function defintions, parameter initializations, and main code loops to execute the model. It also contains code used to produce the figures in the paper.

For questions/comments, please contact Nicolas Choquette-Levy at nc8@princeton.edu.
