# PrescRiptionsData
Data to be used in the PrescRiprions RPackage

# Repository Content

## 02_bnf

The British National Formulary (BNF) is a reference book containing the standard list of medicines used in UK prescribing. It gives information on the indications, dosages and side effects for over 70,000 medicines. The BNF used to show medicines in a hierarchy, and the NHS Business Services Authority use a legacy version of the BNF hierarchy to assign codes to drugs and chemicals. You can find out more about how they assign codes here. UPDATED December 2018: You can find a download of the latest codes from the BSA here.

The BNF codes from this pseudo-classification are used in the prescribing dataset as a unique identifier to show what was prescribed. These BNF codes can tell you a lot about a drug or appliance. The codes are in a hierarchy:

  + The first characters tell you which part of the BNF a drug is from. For example, drugs in BNF Chapter 4 (Central Nervous System) will always begin with ’04’. The BNF is then further subdivided into sections. For example, Antidepressant Drugs, which are contained within Chapter 4 Section 3 of the BNF, all begin with ‘0403’
  + The last few characters of the BNF code give more detailed information about a drug. It tells you what the drug is, it tells you whether the product is generic or branded, and it tells you more about the presentation of the drug (e.g. whether it is a capsule or tablet, and what the strength of the drug is)

More information can be found @ (https://ebmdatalab.net/prescribing-data-bnf-codes/)[https://ebmdatalab.net/prescribing-data-bnf-codes/]