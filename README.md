* Dataset Source – OpenDataSus  - Registros de Vacinação Covid19 - Dados SC – Santa Catarina – Brasil (1)
* Dataset downloaded on 30 May 2021 as 05:00 am.
* Inicial master File named – sc3005_05am.csv
* Original total file size – 1.11 GB = 34 columns and 2,017,225 rows (or registers) (2)

# Problem: Combinations_of_Concern

Inconsistencies between 3 columns in a covid- 19 registration (for Dose 1 and/or Dose2) related to identification of covid_19 vaccine applied to an individual.

Such inconsistencies do not allow to confirm which is the manufacturer of the vaccine received by the subject. 

The 3 columns (or features or variables depending on how you want to call it) are:

* coluna 26 - vacina_fabricante_nome
* coluna 30 - vacina_codigo
* coluna 31 - vacina_nome

# Objectif of this proof of concept project: 

This personal project was developped for the completion of the Module 1 of the Alura Bootcamp Applied Data Sciences II (ABADSII). 

Due to my yet limit knowledge of the python language and Google Colab interface, I explored a combination of tools for parsing UDVE data and develop a proof of concept analysis to be used as Risk Based Monitoring (RBM) tool in the management of covid vaccination plan in Brazilian State of Santa Catarina. 

In the development of this proof of concept I am using ICH&GCP (3) RBM procedures I am used to follow on my operational clinical research activities.


# Interim results: 

Up to 30 May 2021, for 12% of vaccination registrations in the Brazilian state of Santa Catarina (249,437 registrations out of 2 Million), it is not possible to be 100% sure which covid-19 vaccine the individual received. 

About 100% of the combinations of concern involves the Oxford-Astra Zeneca/ F. Oswaldo Cruz e SINOVAC/BUTANTAN.

We should remember that the intervals between the doses 1 and 2 between these two manufactureres are 3 months and 1 month respectively. 

We also must remember that the intervals between the two doses changed, for both manufacturers, sometime between January and May 2021.

Amongst the most serious problems such combinations of concern between those three columns can create:

* Pharmacovigilance analysis: as per example, the evaluation of frequency of Serious Adverse Events as Atypical Strokes already identified and documented in the European territory (4)

* Compliance: ensure local health centers across the UDVEs are able to identify and follow up when their members should return for dose 2.

* Logistic and management of different vaccines stock at federal, state and county level at appropriate intervals.


# Method used for this proof of concept project:

As explained above, to compensate for my yet limit knowledge of Python and the Google Colab interface I organised this project in 3 phases:

* Phase 1: Using Terminal Command Line: as I had trouble using Google Colab to import large files, I used the terminal command line from my computer to parse and create 17 separated files, each corresponding to one of  UDVE ( "Unidades De Vigilancia Epidemiologica (UDVE)" regionais do estado de SC Catarina.)

* Phase 2: Using Google Drive & Colab and Python - I then uploaded all the 17 csv files to Google Drive and created a notebook for each of the UDVES. For each notebook I isolated the 3 above columns and counted the nr of registers for each unique combinations between the 3 columns.

* Phase 3: Using Excel - As my knowledge of Colab&Python is still limited and to respect the Bootcamp deadline to deliver the project I used Excel to group the different results per UDVE region obtained in phase 2, and count the total nr of registers per UDVE and the proportion of each of the differentes combinations of concern.

## As the structure of the 17 notebooks created in the phase II are identical, for convenience and because we are still on the early phases of this work, I only downloaded to this github repository the notebook for UDVE13.

## Further information about Phases 1 to 3 can be found in the Excel file “sc3005_05am - Documentação Github Phases 1 e 3 - amf60 vac-covid_19_3005_SC_c26_c30_c31”


* (1) https://opendatasus.saude.gov.br/dataset/covid-19-vacinacao/resource/ef3bd0b8-b605-474b-9ae5-c97390c197a8?view_id=6bf433e7-16ec-4dfa-a725-08db02322bd6

* (2) O numero de linhas esta relativamente proximo do ultimo DIVE boletim disponivel do dia 26 de Maio que contabilizava 2,263,441 ( http://www.dive.sc.gov.br/index.php/arquivo-noticias/1635-vacinacao-em-sc-2-263-441-doses-da-vacina-contra-a-covid-19-foram-aplicadas-em-sc). E possivel tambem que parte desta diferenca se deva a problemas tecnicos nos ultimos dias (http://www.dive.sc.gov.br/index.php/arquivo-noticias/1639-nota-sobre-dados-do-balanco-parcial-de-vacinacao-contra-a-covid-19-em-santa-catarina)

* (3) https://www.ich.org

* (4) https://www.bbc.com/news/health-56674796)

* (5) https://www.nap.edu/catalog/25303/reproducibility-and-replicability-in-science

