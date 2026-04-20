# Child Malnutrition Health Survey  

## Overview
This repository contains an XLSForm structure for the health survey, following DHS Model Questionnaires for household members, household data, child and mothers questionnaire tocpics.
It includes conditional loop structure to generate survey block according to household members characteristics such age, sex and other filters. 

This Health Surveys example qutomatically genrates structure data collection by organizing questionnaires based on the characteristics of household members. The Demographic and Health Surveys (DHS) begin with a Household Questionnaire that records key details—such as age, sex, education, and relationship to the head of household—for all usual residents and visitors.
From this roster, specific survey modules are assigned to eligible individuals:
- Women’s Questionnaire: Administered to women aged 15–49, it gathers detailed information on reproductive history, contraceptive use, antenatal and postnatal care, breastfeeding, and women's empowerment.
- Child’s Questionnaire: Administered to children under 2 yo: growth and development monitoring of children under 2 years of age: immunizations, childhood diseases, child development centers and daycare, motor development, language milestones (>1 yo)
- Biomarker Questionnaire: Conducted for children and women it collects physical measurements like height, weight, and hemoglobin levels to assess nutritional status and anemia.
This health survey organize data collection by grouping questionnaire modules according to the demographic and health characteristics of specific household members. 

**Total Questions:** 403
**Choice Lists:** 152

## Survey description

The variables of interest collected in the survey focused on measurements of the nutritional status of the described population—primarily chronic malnutrition and iron-deficiency anemia, in addition to others linked to social determinants and demographic information. Likewise, information was gathered on child development and its determinants, such as household conditions and maternal healthcare during pregnancy, as well as relevant indicators regarding healthcare for children from birth and for mothers during pregnancy. Aside from these research variables, indicators for breastfeeding and motor development in children were also measured.
Roster are generated when entering hh members data for specific groups (adults, child, mothers, under 2 yo child).
Conditional questionnaire begin with the selection of a member and ends blocks with a choice to include data from another member of the list. 

### Survey structure:
!!!
Survey logic in KoBoToolbox can become unstable or fail to update correctly when users navigate backward to edit previous answers, particularly when using complex loops. 
This often results in questions not appearing, options remaining empty, or validation errors triggering only at the end of the survey rather than in real-time.
For this survey interviewee must be trained to follow exact flow of the survey entering household member information as this section generates conditional lists.
Loop sections begin with the selection of a list-member and ends with the option to add another questionnaire.   !!!

The survey is organized into the following main sections:

Main questionnaires:
- GENERAL INFORMATION
- RESPONDENT DATA

Lists generation: 
- SECTION A. HOUSEHOLD MEMBERS 
  - SECTION A.1. ADULTS MEMBERS (generate specific lists)
  - SECTION A.2. CHILD UNDER 5 YO (generate specific lists)

Child questionnaires (cond. loop):
- SECTION B. EDUCATION

Adults questionnaires  (cond. loop):
- SECTION C. EMPLOYMENT

Main questionnaires:
- SECTION D. HOUSING AND HOUSEHOLD DATA
  - SECTION D.1. FOOD SECURITY

Child questionnaires (cond. loop):
- SECTION E. GROWTH AND DEVELOPMENT MONITORING OF CHILDREN UNDER 2 YEARS OF AGE  (cond. loop)
- SECTION F. IMMUNIZATIONS FOR CHILDREN UNDER 2 YEARS OF AGE 

Mother questionnaires (cond. loop):
- SECTION G. PRENATAL CARE
- SECTION H. SEXUAL AND REPRODUCTIVE HEALTH
- SECTION I. DEPRESSION
- SECTION J. BREASTFEEDING AND COMPLEMENTARY FEEDING

Child questionnaires (cond. loop):
- SECTION K. PREVALENT CHILDHOOD DISEASES
- SECTION L. CHILD DEVELOPMENT CENTERS AND DAYCARE
- SECTION M. MOTOR DEVELOPMENT
- SECTION N. LANGUAGE MILESTONES FOR CHILDREN AGED 12 TO 59 MONTHS

Mother questionnaires (cond. loop):
- SECTION O.1. MOTHER ANTHROPOMETRY 

Child questionnaires (cond. loop):
- SECTION O.2. CHILD ANTHROPOMETRY 
- SECTION P. CHILD BLOOD SAMPLES 

## Technical Details
- **Form ID:** dci_eipost_2025
- **Tools Used:** KoboToolbox / XLSForm
- **Data Types:** Includes Text, Select One, Select Multiple, Geopoint, Date, and Decimal types.

## Deployment Instructions
1. Upload the `xxx.xlsx` file to [KoboToolbox](https://kf.kobotoolbox.org/).
2. Preview the form to ensure all skip logic and constraints work as expected.
3. Deploy the form to start data collection.
4. KoboCollect app was used for mobile collection,

