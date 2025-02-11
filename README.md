# **PrescRiptionsData**
Data used in the [***PrescRiptions***](https://github.com/muschitiello/PrescRiptions) RPackage

## **Repository Content**

The Repo includes [***Practice Level Prescribing***](https://digital.nhs.uk/data-and-information/areas-of-interest/prescribing/practice-level-prescribing-in-england-a-summary) data for years 2018 and 2019. Data files are renamed, checked for homogeneity and made available for the purposes of the R-Package PrescRiptions.

Data are organized in the following Sections and Subsections

### ***01_plpd***

Practice level prescribing data is a list of all medicines, dressings and appliances that are prescribed by all practices in England and dispensed in the community each month.

A zip file is available which users are able to download and extract all 3 files locally:

Practice Prescribing Data (pdpi) (monthly data from Jan 2019 to Dec 2019):
GP prescribing practice address (monthly data):
GP prescribing chemical substance (monthly data):
Because data are too large to be stored in a GitHub Repository,the section includes links to files.

### ***02_bnf***

The British National Formulary (BNF) is a reference book containing the standard list of medicines used in UK prescribing. It gives information on the indications, dosages and side effects for over 70,000 medicines. The BNF used to show medicines in a hierarchy, and the NHS Business Services Authority use a legacy version of the BNF hierarchy to assign codes to drugs and chemicals. You can find out more about how they assign codes here. UPDATED December 2018: You can find a download of the latest codes from the BSA here.

The BNF codes from this pseudo-classification are used in the prescribing dataset as a unique identifier to show what was prescribed. These BNF codes can tell you a lot about a drug or appliance. The codes are in a hierarchy:

  + The first characters tell you which part of the BNF a drug is from. For example, drugs in BNF Chapter 4 (Central Nervous System) will always begin with ’04’. The BNF is then further subdivided into sections. For example, Antidepressant Drugs, which are contained within Chapter 4 Section 3 of the BNF, all begin with ‘0403’
  + The last few characters of the BNF code give more detailed information about a drug. It tells you what the drug is, it tells you whether the product is generic or branded, and it tells you more about the presentation of the drug (e.g. whether it is a capsule or tablet, and what the strength of the drug is)

More information can be found @ https://ebmdatalab.net/prescribing-data-bnf-codes/

For the purpose of the usage in the *PrescRiprions* RPackage, the first 6 digits of the reported items in the monthly prescription data are used. 
BNF codes information were downloaded from the [NHS website](https://apps.nhsbsa.nhs.uk/infosystems/data/showDataSelector.do?reportId=126)

Bnf data are released once a year in *.zip* format.

Three years of data are present in this Repo, in the original .zip format but alcs, conversions in RData, feather and csv format: 

#### *02_bnf/zip*:
This are the original files downloaded from NHS website.

  * bnf 2018 01: 20200205_1580915838473_BNF_Code_Information.zip
  * bnf 2019 01: 20200205_1580915847332_BNF_Code_Information.zip
  * bnf 2020 01: 20200201_1580570906919_BNF_Code_Information.zip
  
#### *02_bnf/RData*:

  * bnf 2018 01: bnf201801.RData
  * bnf 2019 01: bnf201801.RData
  * bnf 2020 01: bnf201801.RData

#### *02_bnf/feather*:

For informnation on feather format: https://blog.rstudio.com/2016/03/29/feather/

  * bnf 2018 01: bnf201801.feather
  * bnf 2019 01: bnf201801.feather
  * bnf 2020 01: bnf201801.feather
  
#### *02_bnf/csv*:

  * bnf 2018 01: bnf201801.csv
  * bnf 2019 01: bnf201801.csv
  * bnf 2020 01: bnf201801.csv


### ***03_demog***

Practice size for some demographic groups, as measured by the number of registered patients. 
The number of registered patients was downloaded from NHS Digital General Practice Data Hub (https://digital.nhs.uk/data-and-information/data-tools-and-services/data-services/general-practice-data-hub). 

Data are available on: 

  * age
  * sex
  
for each GP in two different format: 

  * csv
  * feather

Data are organized in monthly files from january 2018 to december 2019 containing 2 files: 

  1. demographic data
  2. data map, with GP details
 
Data example for jannuary 2018 in csv format: 
 
#### *03_demog/csv/demog_201801*:

  * 201801_demog.csv
  * 201801_demogMap.csv

### ***04_qof***

Quality outcome framework indicators for individual conditions. 
Data on specific conditions were obtained from [NHS General Practice Data Hub](https://digital.nhs.uk/data-and-information/publications/statistical/quality-and-outcomes-framework-achievement-prevalence-and-exceptions-data/2018-19-pas ).
Considered conditions were: 
  
  1. cardiovascular group
  2. respiratory group
  3. lifestyle group
  4. long-term conditions group
  5. mental health group
  6. muscoloskeletal group

Details on the data content at the following link: 
https://digital.nhs.uk/data-and-information/publications/statistical/quality-and-outcomes-framework-achievement-prevalence-and-exceptions-data/2018-19-pas/technical-annex#definitions


#### *04_qof/xlsx*

Original data are in xlsx format and contain indicators at 2-years level. 

  * qof-1819-prev-ach-exc-cv-prac.xlsx
  * qof-1819-prev-ach-exc-hd-prac.xlsx
  * qof-1819-prev-ach-exc-ls-prac.xlsx
  * qof-1819-prev-ach-exc-ms-prac.xlsx
  * qof-1819-prev-ach-exc-neu-prac.xlsx
  * qof-1819-prev-ach-exc-resp-prac.xlsx

Because the *PrescRisptions* RPackage considers 2 years of data, only one set of data is considered in this Repository, the one containing data for 2018 and 2019.
Data structure of downloaded file was in a format not suitable for immediate usage. Therefore data were reorganized in separated files and in two formats: 

  * csv
  * feather 

#### *04_qof/csv*:

  * qofGP_CardioVascular.csv
  * qofGP_dependency.csv
  * qofGP_lifestyle.csv
  * qofGP_mental.csv
  * qofGP_muscul.csv
  * qofGP_respiratory.csv

#### *04_qof/feather*:

  * qofGP_CardioVascular.feather
  * qofGP_dependency.feather
  * qofGP_lifestyle.feather
  * qofGP_mental.feather
  * qofGP_muscul.feather
  * qofGP_respiratory.feather
 
