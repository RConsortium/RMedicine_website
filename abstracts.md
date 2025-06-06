<div id="what-to-do-when-shiny-packages"></div><br><br>

# What to Do When Shiny Packages Don't Fully Support Your Idea

Shiny is great, but what if you need more flexibility and performance? In this lightning talk, I'll show how the reactR package helped me extend Shiny’s capabilities to build ESQapp, a highly interactive and scalable application. By integrating React.js, I overcame Shiny’s UI limitations, improved performance, and created custom components that wouldn’t be possible with Shiny alone. If you’re looking to level up your Shiny apps with modern web technologies, this talk is for you!

<div id="intro-to-medical-harmonisation"></div><br><br>

# Introduction to medical data harmonisation reporting using R and Quarto

There has been an increase of projects that involved data pooling from multiple sources. This is because combining data is an economical way to increase the statistical power of an analysis of a rare outcome that could not be addressed using data from a single project. Prior to statistical or machine learning analysis, a data steward must be able to sort through these heterogeneous inputs and document this process in a coherent way for different stakeholders.
This session will show how I create data harmonisation reports using some R packages and Quarto book project. The report will consist of some description to show how a data field will be harmonised, the code that does the harmonisation and suggested outputs in the report to show higher management with limited programming experience that the code works. An R script will also be used to create a pipeline to create many harmonisation reports automatically. Code demonstrations also include how to create validation checks (using pointblank, testthat and collateral) should the dataset changes.

<div id="pretestcad-package"></div><br><br>

# pretestcad: An R package to calculate PreTest Probability (PTP) scores for obstructive Coronary Artery Disease (CAD)

Most clinicians in cardiology use an online portal such as HeartScore (https://www.escardio.org/Education/Practice-Tools/CVD-prevention-toolbox/HeartScore) to calculate a risk score for a patient. However, as risk scores continue to evolve and update themselves, it can be a tedious process to recalculate the risk score of many patients as these online portal could only do so one patient at a time. As such, there has been a rise of R package dedicated to calculating a patient's risk of having cardiovascular diseases such as CVrisk (https://cran.r-project.org/web/packages/CVrisk/index.html), RiskScorescvd (https://cran.r-project.org/web/packages/RiskScorescvd/index.html) and whoishRisk (https://github.com/DylanRJCollins/whoishRisk) in an automated way. 

Despite the progress made, pretest risk scores for obstructive CAD is lacking, an R package called pretestcad (https://github.com/JauntyJJS/pretestcad) was made to fill this gap, allowing users to calculate these scores automatically for many patients. Examples of such scores are the 2012 CAD Consortium 2 (CAD2) PTP scores, 2017 PROMISE Minimal-Risk Score and the 2020 Winther et. al. Risk-Factor-weighted Clinical Likelihood (RF-CL) and Coronary Artery Calcium Score-Weighted Clinical Likelihood (CACS-CL) PTP which was recommended to be used in the 2024 ESC Guidelines (https://academic.oup.com/eurheartj/article/45/36/3415/7743115). 

I hope that presenting this R package in this conference could not only raise awareness of the package in the medical field but also collaboration to make the R package more accessible and user friendly and to expand my knowledge of other pretest scores.

<div id="retrospective-clinical-date-harmonisation-reporting"></div><br><br>

# Retrospective clinical data harmonisation reporting using R and Quarto

There has been an increase of projects that involved data pooling from multiple sources. This is because combining data is an economical way to increase the statistical power of an analysis of a rare outcome that could not be addressed using data from a single project. Prior to statistical or machine learning analysis, a data steward must be able to sort through these heterogeneous inputs and document this process in a coherent way for different stakeholders. Despite its importance in the big data environment, there are limit resources on how to document this process in a structured, efficient and robust way. This presentation will provide an overview on how I create clinical data harmonisation reports using some R packages and a Quarto book project.

The audience in this talk will be able to know the basic framework of creating a Quarto Book or website to document data harmonisation processes, the basic workflow during the data harmonisation process, how to do data validation when writing code for data harmonisation to ensure code workflow is robust to changes in the input data, ways to show to higher management (with limited programming experience) in the harmonisation report that your code works (It is not enough to say that I use test units), able to write an R script to create many data harmonisation reports (One technical report for each cohort pooled and one report that summarised the data harmonisation process for all cohorts).

<div id="miipw-package"></div><br><br>

# MIIPW: An R package for Generalized Estimating Equations with missing data integration using a combination of mean score and inverse probability weighted approaches and multiple imputation

The presence of missing values in longitudinal cohort data can lead to inaccuracies in parameter estimation and decreased statistical power. To address this issue, we have developed the MIIPW R package, which incorporates the mean score and inverse probability weighted methods in generalized estimating equations to impute missing scores due to incomplete covariate data. Augmentation of incomplete data in the estimating equation is done through a multiple imputation model. The package employs various methods such as mean score, SIPW, AIPW, miSIPW, and miAIPW to estimate parameters while considering four different covariance structures (AR-1, Exchangeable, Unstructured, and Independent). Additionally, the package uses the QIC for model selection and pays special attention to the calculation of weights within the dataset. The performance of the above mentioned methods has been evaluated through simulation study as well as real data analysis. The MIIPW package is available for download from the comprehensive R archive network and this article provides a practical guide to solve missing data issues. https://CRAN.R-project.org/package=MIIPW

<div id="the-cohortconstructor-package"></div><br><br>

# A framework for cohort building in R: the CohortConstructor package for data mapped to the OMOP Common Data Model

Cohorts are a key concept in epidemiological research, used to identify groups of people who meet specific criteria over a set period based on their clinical records. However, building and managing cohorts in medical data analysis can be complex, often resulting in code that is difficult to review and reuse. 

When working with the OMOP Common Data Model (CDM), efforts have been made to define the `cohort_table` class along with methods and object attributes to facilitate its use. This class is implemented in the `omopgenerics` R package. The cohort table contains at least four mandatory columns: cohort ID (unique cohort identifier within a cohort table), subject id (unique person identifier), and the cohort start and end dates for each individual. 

Additionally, cohort objects have four key attributes: 1) Settings - links the cohort ID to its name, 2) Counts - provides the number of subjects and records in each cohort, 3) Attrition - flow chart of excluded records and individuals for each inclusion criteria, and 4) Code lists - stores clinical concept lists used to define cohort entry, exclusion, or exit. These attributes ensure transparency in cohort creation, facilitate validation, and enable easy dissemination of study results. 

To streamline cohort building in R using OMOP data, we developed the R package CohortConstructor. It provides tools for cohort manipulation, including filtering by demographics, calendar time, or presence/absence in other cohorts. Additionally, the package tracks clinical codes used and population attrition for each operation. 

CohortConstructor version 0.3.5 is available in CRAN at the time of abstract submission. The development version is publicly available in GitHub: https://github.com/OHDSI/CohortConstructor/. 

The pipeline to build cohorts begins by creating base cohorts. These can be defined using clinical concepts (e.g., asthma diagnoses) or demographics (e.g., females aged >18). Once base cohorts are established, curation steps are applied to meet study-specific inclusion criteria. 

The curation functions cover the most usual operations in cohort studies, as well as more complex cohort manipulations. These functions can be grouped into three categories: 1) Requirement and Filtering – demographic restrictions, event presence/absence conditions, or filtering specific records, 2) Time Manipulation – adjusting entry and exit dates to align with study periods, observation windows, or key events, and 3) Transformation and Combination – Merging, stratifying, collapsing, matching, or intersecting cohorts. 

CohortConstructor enables researchers to efficiently build and refine cohorts using validated, and reusable code lists. Its user-friendly interface allows both data scientists and epidemiologists to review and apply study-specific criteria with ease. Additionally, tracking attrition throughout the process enhances cohort validation and supports research dissemination. 

In our demo we will demonstrate the use of the package on synthetic data that the audience can also download and run locally. We will show how a variety of patient cohorts can be identified using the package, and how these can then be used as the foundation for subsequent data analyses. In addition, we will explain how the package works behind the scenes so that it works efficiently on big data and across different database management platforms.

<div id="riskcalc-org-repository"></div><br><br>

# riskcalc.org: A Repository of Risk Calculators for Medical Decision Making

riskcalc.org is a repository of clinical risk calculators for medical decision making. In this talk, we provide an overview of the platform, how it is used, and a look at how open-source tools such as Shiny and Shiny Server are used to facilitate its functionality. Finally, we discuss some areas potentially in store for future development.

<div id="nonprobsvy-package"></div><br><br>

# nonprobsvy -- An R package for modern methods for non-probability survey

I present nonprobsvy -- an \proglang{R} package for inference based on non-probability samples. The package implements various approaches that can be categorized into three groups: prediction-based approach, inverse probability weighting, and doubly robust approach. In the package, we assume the existence of either population-level data or probability-based population information and leverage the survey package for inference. The package implements both analytical and bootstrap variance estimation for all of the proposed estimators. In the paper, we present the theory behind the package, its functionalities, and a case study that showcases the usage of the package. The package is aimed at researchers who would like to use non-probability samples (e.g., big data, opt-in web panels, social media) to accurately estimate population characteristics. The package is available on CRAN (https://cran.r-project.org/package=nonprobsvy) and the development version is available at GitHub (http://github.com/ncn-foreigners/nonprobsvy).

<div id="rainbowr-community"></div><br><br>

# rainbowR: A community for LGBTQ+ folks who code in R

rainbowR is a community that connects, supports and promotes LGBTQ+ people who code in R and spreads awareness of LGBTQ+ issues through data-driven activism. We run monthly online meet-ups where participants chat and share their R work in a supportive environment. We also organise a buddies scheme, which randomly pairs members of the community, to encourage people to meet and connect. We have a book club, and maintain a repository of queer data sets. We have exciting plans for the future!

You'll learn about what rainbowR does and how you can get involved, whether as a member of the LGBTQ+ community or as an ally, and hopefully forge new connections at the conference and beyond. We believe the whole R community benefits when that community is diverse and inclusive.

<div id="controlled-vocabularies"></div><br><br>

# Improving Reproducibility of Medical Research with Controlled Vocabularies

The reproducibility of medical research has been a consistently growing topic of interest. Replicating medical research relies on a few key aspects of the original analysis and methodology such as code correctness, documentation, and effective communication of the methods used. A lot of the discussion about reproducibility tends to focus on project setup and configuration such as coding environment, package/library versioning, data access, and study design. However, even when all the above criteria are met, the objective of replicating an analysis still relies on the original work being implemented correctly, clearly documented, and effectively communicated, all of which can be difficult to achieve when restricted by time, budget, and general resource limitations.

In this presentation, we introduce a data analysis concept, controlled vocabularies for variable naming, and demonstrate how it can be integrated into medical research. Examples of how a controlled vocabulary can be leveraged to make code correctness, analysis documentation, and methods communication more feasible to achieve will be presented.

A controlled vocabulary for variable naming allows a user to encode metadata such as time period (e.g. baseline, follow-up), data source (e.g. laboratory results, procedures, diagnoses etc.), event type (e.g. eGFR lab test), data type (e.g. count, numeric, indicator, categorical, date, etc.), unit of measure, and any additional optional pieces of metadata that would be useful to include for a particular project. For example, to document patients in a population who have a record of an eGFR lab test during the baseline period of a study, a potential variable name from a controlled vocabulary for this eGFR indicator variable would be labs_eGFR_baseline_ind. This variable name encodes all relevant information about this variable in the variable name itself.

The benefits of encoding this information within the variable names of a project using a defined procedure to name the variables are significant. With a controlled vocabulary defined globally for a project, all variable names will be formatted consistently. This can be particularly helpful during the development process and when debugging code, as the variable names can help a user understand what information should be stored in the column (e.g. if a variable name contains the term num it should be a numeric column).
Beyond data wrangling and cleaning, the benefits of having an entire project defined using a controlled vocabulary is that it enables the use of regular expression commands to simplify data modelling, reporting, and communication pipelines. Regressions and sensitivity analyses can be done more succinctly, and constructing tables and figures requires less hardcoded variable definitions.

An additional advantage of using a controlled vocabulary is it can help automate the production of a project data dictionary. Using a defined procedure to name the variables in a project means that it is more straightforward to break apart these variable names and generate expanded explanations of each variable automatically to document and communicate the variables used in the analysis.

<div id="refactor-or-preserve"></div><br><br>

# Refactor or Preserve? Challenging the 'If It Ain’t Broken, Don’t Fix It' Mindset in Shiny App Lifecycle

As technology evolves, even well-crafted software eventually reaches obsolescence. This presentation explores the critical question: To refactor or not? Using the Pharmaverse/Teal framework as a case study, we examine the benefits and risks of transitioning a functional Shiny application to a modern framework.

Modern software frameworks often offer improved efficiency, enhanced stability, and expanded capabilities. However, they come with the tradeoff of upfront costs—such as learning new tools, adapting workflows, and ensuring long-term maintainability. The pragmatic adage, If it ain’t broken, don’t fix it, highlights the tension between maintaining stability and seizing opportunities for innovation.
We will delve into a pragmatic assessment of refactoring decisions, weighing the advantages of adopting contemporary solutions against the potential challenges of disruption and technical debt. Attendees will gain insights into evaluating trade-offs, identifying critical factors for modernization, and applying lessons from the R/Pharmaverse Teal framework to make informed strategic decisions.

<div id="bootstrap-inference-made-easy"></div><br><br>

# Bootstrap inference made easy: p-values and confidence intervals in one line of code

Bootstrap methods are a great way to get reliable p-values and confidence intervals, especially when classical model assumptions don’t quite hold or when analytical formulas aren’t available. Still, they’re not used as much as they could be—often because they seem complicated to implement.

In this talk, I’ll show how easy it can be. I’ll present the R package boot.pval, which lets you compute bootstrap p-values and confidence intervals for a wide range of models and parameters using just a single line of code. This includes tests of location, as well as regression coefficients in linear models, GLMs, survival models, and mixed models. I’ll also touch on how it works under the hood, how to extend it to custom test statistics, and how it can fit into your everyday analysis workflow.

<div id="advanced-distance-metrics"></div><br><br>

# Advanced Distance Metrics for High-Dimensional Clustering: introducing 'distanceHD' R-package

This presentation introduces the newly released R package, distanceHD, which provides distance metrics for high-dimensional clustering. We provide three distance metrics for measuring the separation between two clusters in high-dimensional spaces. The first metric is the centroid distance, which calculates the Euclidean distance between the centers of the two groups. The second is a ridge Mahalanobis distance, which incorporates a ridge correction constant, alpha, to ensure that the covariance matrix is invertible. The third metric is the maximal data piling distance, which computes the orthogonal distance between the affine spaces spanned by each class. These three distances are asymptotically interconnected and are applicable in tasks such as discrimination, clustering, and outlier detection in high-dimensional settings.

<div id="aousdohtools-package"></div><br><br>

# AOUSDOHtools: An R Package for Social Determinants of Health Survey data in the All of Us Research Program

AOUSDOHtools is an R package that was created to support standardized and reproducible scoring of the Social Determinants of Health (SDOH) constructs from survey data collected as part of the All of Us Research Program. Developed in conjunction with a user guide (Koleck et al., 2024, https://doi.org/10.1093/jamia/ocae214), the package provides functions to process raw SDOH Survey responses and compute 30 literature-informed construct-level scores across 14 SDOH constructs, such as Neighborhood Cohesion, Social Support, and Perceived Stress. 

The package is designed for use within the All of Us Researcher Workbench, a secure cloud-based platform where the de-identified data are accessed and analyzed. The package is compatible with both Jupyter and RStudio environments hosted on the platform. AOUSDOHtools automates the data cleaning, recoding, scoring, and variable construction, which enables researchers to generate interpretable SDOH scores for downstream analysis. 

The package is openly developed and maintained on GitHub and available through CRAN (https://cran.r-project.org/package=AOUSDOHtools) and GitHub (github.com/zhd52/AOUSDOHtools). It is intended to facilitate equitable and scalable research by making complex SDOH survey data accessible and analysis-ready for approved researchers working within the All of Us ecosystem.

<div id="r-you-compliant"></div><br><br>

# R You Compliant? Validating Packages for Regulatory Readiness

As R continues to gain momentum in clinical research, regulatory agencies are paying closer attention to how it’s used in regulated environments. Whether supporting statistical analysis, data visualization, or automation pipelines, R packages must meet stringent validation requirements to be considered fit for use in clinical trials and other regulated activities. But what does validation actually mean in this context—and how can researchers, data scientists, and system administrators ensure their R-based tools hold up under scrutiny?
This talk will walk through practical strategies for validating R packages in alignment with regulatory expectations, including those from FDA, EMA, and under ICH guidelines such as E6(R3), E9, and M10. We’ll explore the intersection of open-source software and GxP compliance, unpacking the nuances of how to assess, document, and justify the use of community-developed or custom-built R packages.
Attendees will learn:
• What regulators expect when R is used in a clinical or GxP-regulated environment.
• How to categorize R packages based on risk and intended use.
• Validation approaches for both CRAN packages and internally developed tools.
• How to document package selection, qualification, and performance testing.
• Best practices for ongoing change control, version tracking, and reproducibility.
• Real-world examples of validation frameworks and testing workflows using tools like {testthat}, {renv}, and {devtools}.
Whether you're part of a small academic research team or a large sponsor organization, this session offers practical guidance for creating defensible validation packages that support transparency, reproducibility, and regulatory compliance. We’ll also touch on tools and templates that can help streamline validation documentation and collaborate with Quality Assurance teams more effectively.
By the end of this talk, you'll walk away with a clearer understanding of what it takes to “make R compliant,” how to integrate validation into your development workflows, and how to future-proof your R environment in a regulated research setting.
Because in clinical research, compliance isn’t just a checkbox—it’s part of building trust in our data, our methods, and ultimately, the science we support.

<div id="first-steps-with-sql"></div><br><br>

# First Steps with SQL in R: Making Data Talk

Curious about SQL but not ready to dive into full-blown databases or external connections? This hands-on, beginner-friendly workshop is the perfect starting point. Using the lightweight and intuitive {sqldf} package in R, you’ll learn how to write SQL queries directly on your existing R data frames—no database setup required.

SQL (Structured Query Language) is a powerful tool for querying and transforming structured data, and it’s widely used in clinical research, data science, and industry analytics. In this 3-hour introductory session, we’ll bridge the gap between R and SQL in the most approachable way possible—by working with the data frames you already use in R.

We’ll cover:

What SQL is and why it’s useful alongside R

The basics of SQL syntax: SELECT, FROM, WHERE, ORDER BY, GROUP BY, and JOIN

How to use the {sqldf} package to run SQL queries on R data frames

Comparing SQL and dplyr for common data tasks

Writing readable, reusable SQL queries inside R scripts

This session is geared toward R users with little to no SQL experience. You’ll learn through guided examples and live coding, with time to practice writing your own queries. There’s no need for databases or complicated setup—just bring your laptop with R and {sqldf} installed, and we’ll take it from there.

By the end of the workshop, you’ll be able to:

Write SQL queries to filter, sort, group, and join data frames

Use {sqldf} to integrate SQL smoothly into your R scripts

Decide when SQL might be more effective than tidyverse functions (and vice versa)

Gain confidence in querying data more efficiently—even with large or complex datasets

This workshop is especially helpful for analysts, students, and researchers who want to become more versatile in handling data but prefer to stay within the comfort of the R environment. It’s also a great stepping stone for those who may later work with external databases (e.g., REDCap, EDC systems, or clinical trial platforms).

Come explore the power of SQL in a simple, approachable way—and learn to make your data talk.

<div id="unified-deep-learning-survival"></div><br><br>

# Unified Deep Learning Survival Analysis for Competing Risk Modeling with Functional Covariates and Missing Data Imputation

Discharging patients from the intensive care unit (ICU) marks an important moment in their recovery—it’s a transition from acute care to a lower level of dependency. However, even after leaving the ICU, many patients still face serious risks for adverse outcomes, such as ICU readmission due to complications or subsequent in-hospital death. Such events can slow recovery, increase healthcare costs, and substantially impact patients' quality of life. Accurate prediction of these outcomes could transform the way we care for ICU survivors. With improved predictive capabilities, clinicians can intervene sooner, personalize post-ICU support, and ultimately improve recovery while reducing the chances of returning to critical care.
That said, making these predictions is anything but simple. ICU data is challenging—there are multiple competing risks (such as septic shock, ICU readmission, or death during or after hospitalization), and the data is both complex and multidimensional, spanning demographic factors, clinical information, and continuous waveform covariates (e.g., blood pressure and respiratory rate). Additionally, some data may be frequently missing, and time-dependent treatments make it even more difficult. Traditional competing risk models, such as cause-specific hazard models and the Fine & Gray sub-distribution hazard models, often fall short in managing these complexities. 
To address these challenges, our research team has developed an innovative deep-learning model specifically designed for competing risk analysis in ICU settings. This framework integrates discrete-time competing risk analysis techniques, adaptive data-driven basis layers with micro neural network for functional variables, and advanced Imputation-Regularized Optimization (IRO) method to manage missing data effectively. Unlike traditional basis representation methods—such as those using Fourier or spline bases—which do not leverage outcome information during dimension reduction, our approach fully integrates this information. This comprehensive approach greatly enhances our ability to understand and predict complex patient outcomes based on vital signs and other critical data.
We validated our model through simulations and real-world ICU data from both a large public ICU database MIMIC-4 (over 12,000 patients) and the Cleveland Clinic's ICU records (over 25,000 patients). Across different clinical scenarios, our deep-learning framework outperformed traditional methods on most occasions, showing better predictive accuracy based on the metrics, integrated brier score and concordance index. Ultimately, this research represents an important step forward in improving ICU patient care, enabling more precise, timely, and effective clinical decisions.

<div id="redquack-package"></div><br><br>

# {redquack}: An R Package for Memory Efficient REDCap-to-DuckDB Workflows

Healthcare researchers working with REDCap often face challenges when using the API to read large clinical datasets. Random access memory (RAM) limitations of modern business and consumer hardware may not be capable of loading millions of records with hundreds of variables without pushing these systems to their limits. 

This challenge became particularly evident at the School of Pharmacy, University of Pittsburgh, where data scientists manage a REDCap database containing clinical data from over 200 outpatient treatment centers. With 5 distinct forms resulting in nearly 3 million rows across 400 columns, traditional export methods using {REDCapR} failed due to memory constraints, while most analyses only required subsets of this data. 

The {redquack} package was developed as a solution to this problem. It solves memory limitation through batch processing of REDCap data to DuckDB, an efficient columnar-storage database. This approach enables scientists and researchers to efficiently read large REDCap projects without memory constraints, process data in configurable batches of record IDs, optimize column types across batches, track extraction progress with detailed logging, and integrate with existing tidyverse workflows. 

Using {redquack} is straightforward and requires minimal code. Researchers simply provide their REDCap API credentials and configuration preferences to the redcap_to_duckdb() function, which handles the extraction process. The resulting DuckDB connection can be immediately used with familiar dplyr syntax for filtering, grouping, and summarizing clinical data. This approach allows analysts to work with data too large to fit in memory while maintaining the workflows they may be accustomed to. The package also includes quality-of-life features like sound notifications (quacks on success) for long-running operations. 

This presentation will showcase practical examples based on clinical research data from the School of Pharmacy at the University of Pittsburgh, demonstrating how {redquack} streamlines the data pipeline from REDCap to analysis. By eliminating memory constraints and simplifying the extraction process, {redquack} helps clinical researchers, data scientists and analysts, and research coordinators work more efficiently with large datasets while maintaining their existing workflows. The presentation will benefit anyone involved in clinical research who needs to process and analyze REDCap data in R, particularly those working with large multi-form projects or longitudinal studies where traditional extraction methods fail.

<div id="validating-shiny-apps"></div><br><br>

# Validating Shiny Apps in Regulated Environments

Shiny apps are increasingly used to deliver interactive tools in clinical and healthcare settings. But when these tools are used in regulated environments, validation becomes essential. How can we ensure that our Shiny apps are trustworthy, without stifling innovation?

In this talk we'll explore practical approaches to validating Shiny applications in regulated contexts, drawing on principles from software engineering, quality assurance, and risk based validation. We'll discuss key challenges like traceability, documentation, and versioning, as well as share techniques for building apps that are easier to validate from the start.

I'll highlight some of the tools and packages used in Jumping Rivers that can support validation workflows that satisfies both internal reviewers and external regulators, including the Litmusverse, a suite of R packages designed to assess code quality and generate validation evidence.

By the end of the session, you'll understand:
- Why validation is critical for Shiny apps in regulated contexts;
- What elements make a Shiny app more or less validatable;
- How to incorporate validation strategies into your development process.

This session is ideal for R users in pharma, clinical research, and healthcare who want to build confidence in their dashboards, while maintaining flexibility in how they work.

<div id="ethical-considerations"></div><br><br>

# Ethical Considerations of Contrasts in Statistical Modeling of Medical Equity

Given that English is the dominant language for healthcare delivery in most places in the US, it can be argued that English is an appropriate referent language group for research design and statistical analysis. However, the decision to use English as the referent language centers English-speaking populations and perpetuates the narrative that English is the standard to which all other languages should be compared. Implicitly or explicitly, this assigns value to those who prefer to speak English. Such centering is not a practice isolated to language. Normalizing a group as the referent is often performed across other demographic and geographic variables in statistical modeling, including race, ethnicity, socioeconomic indicators, insurance status, sexuality, and rurality to name a few. Here, we discuss the use of contrasts in statistical modeling as a way to surface the impact of value judgements and their effect on inferential results, using R with an example from our institution.

<div id="rhealth-toolkit"></div><br><br>

# RHealth – A Deep Learning Toolkit for Healthcare Predictive Modeling

Deep learning (DL) offers significant potential for advancing healthcare through improved analysis of electronic health records (EHRs), medical imaging, and physiological signals. However, the implementation of state-of-the-art DL models often requires advanced programming skills in Python, creating a barrier for clinical researchers and practitioners who primarily use R. Furthermore, applying complex DL methodologies is compounded by the inherent challenges in managing and processing the large-scale, complex, hierarchical, and multi-modal nature of healthcare data. While R is widely adopted in healthcare analytics, it currently lacks comprehensive, tailored toolkits designed for these specific data types and modeling complexities. This contrasts with the Python ecosystem, where toolkits like PyHealth have successfully standardized DL pipelines for healthcare, supporting diverse data, tasks, and models, and achieving widespread adoption (e.g., over 144k downloads and 11k stars). 

As the main developer for PyHealth, we introduce RHealth, an open-source R package specifically designed to bring similar capabilities to the R community for healthcare predictive modeling using deep learning. Funded by the ISC grant from the R Consortium, RHealth aims to provide an accessible, integrated environment for R users. The initial development stage focuses on two core modules: 

1. EHR Database Module: This module provides a standardized framework to ingest, process, and manage diverse EHR datasets, including public sources (like MIMIC-III, MIMIC-IV and eICU datasets) and user-specific data formats (OMOP-CDM), ensuring data consistency for downstream modeling.
2. EHR Code Mapping Module: This module facilitates the mapping between and within various medical coding systems (e.g., ICD, NDC, RxNorm), simplifying the integration of disparate clinical data sources.

Future funding will be sought to expand RHealth with additional modules, including a Healthcare DL Core module incorporating traditional machine learning and state-of-the-art healthcare-specific DL models (e.g., RETAIN, Transformers), and a Prediction module for various clinical prediction tasks (e.g., mortality prediction, readmission risk). Planned enhancements also include support for multi-modal data integration, clinical trial applications and large language model enhancement.

RHealth seeks to empower the R-focused healthcare community by providing user-friendly tools, validated models, and reproducible benchmarks for leveraging advanced deep learning techniques. By lowering the technical barrier and building on established success in the Python domain, we aim to facilitate innovative clinical research and ultimately contribute to improved healthcare outcomes.

<div id="optimizing-public-healthcare"></div><br><br>

# Optimizing Public Healthcare Cost Recovery with R: A Use Case from Argentina

This work aims to demonstrate how the implementation of an open-source tool like R can optimize key processes in cost recovery within the public healthcare system, with a direct impact on its efficiency and sustainability.

In Argentina, the healthcare system is organized into three subsystems: the public, social security, and private sectors. In order to reduce health disparities, programs such as SUMAR have been developed. SUMAR seeks to guarantee equitable and quality access to healthcare for the population with exclusive public coverage. Through external funding from non-governmental entities, healthcare providers within the network of the Government of the City of Buenos Aires (CABA) receive financial incentives each time a basic effective coverage (CEB) health service is provided.

In CABA, the widespread use of the Electronic Health Record system across all healthcare providers facilitates the identification and tracking of patients enrolled in the program, enabling longitudinal follow-up and documentation of CEB services delivered. For each individual and each healthcare encounter, the health center receives additional resources.
Within this framework, this public policy makes it possible to transform healthcare services into concrete financial resources. At the Operational Management of Health Information and Statistics, we have a technical team that leverages open-source tools—particularly R—to apply text mining techniques that help identify diagnoses, services, patients, and care pathways relevant to the preparation of the documentation required to access financial incentives.

Our presentation aims to share with the R Medicine community a real-world use case from Latin America that highlights the value of open and sustainable tools in subnational public settings, promoting their adoption where they are most needed. The decision to use free and open-source tools is a strategic one, based on their flexibility to adapt to different technical needs and their long-term sustainability within the public sector. This approach allows for the systematization and acceleration of documentation processes, with a tangible impact on increasing the efficiency and volume of cost recovery efforts under the SUMAR Program.
Throughout the presentation, we intend to show how applying data science tools in real public healthcare settings can lead to innovative solutions. In particular, we seek to highlight R’s potential to automate administrative workflows, improve process traceability, and transform data into concrete actions with measurable impact.

<div id="examining-factors-nhis"></div><br><br>

# Examining Factors Associated with Depressive Severity Among Cancer Survivors: An Analysis of the National Health Interview Survey

This study explores the factors linked to heightened severity of depressive symptoms in individuals who have self-reported a cancer diagnosis, utilizing data from the National Health Interview Survey (NHIS). A cancer diagnosis often brings significant psychological distress, making it essential to understand the correlates of depression within this group to guide targeted interventions and enhance patient well-being. This analysis focuses on a subgroup of NHIS participants who reported a cancer diagnosis, investigating the connection between depressive symptoms, as assessed by the Patient Health Questionnaire-8 (PHQ-8), and various demographic characteristics (e.g., age, sex, race/ethnicity, education, poverty), healthcare utilization patterns (e.g., delayed visits, emergency room visits, overnight hospitalization), and other factors (e.g., living alone, anxiety symptoms).

The study utilizes a data-driven approach to explore the predictors of depressive symptom severity. By leveraging a nationally representative sample, we investigate the associations between depressive severity and various demographic, health care utilization, and other factors. Using various R packages for data processing and analysis, descriptive statistics and survey-based regression are employed to identify significant correlates of heightened depression symptoms. Interaction terms will be considered to determine whether the relationship between certain factors and depression differs across various subgroups (e.g., by age, race/ethnicity, or gender, if data permits).

This study highlights the importance of large-scale public health datasets in elucidating the psychosocial challenges faced by patients who report having cancer. It underscores the need to integrate mental health considerations into cancer care. The findings aim to guide clinical decision-making and direct the development of precision mental health interventions within oncology settings.

<div id="kidney-epi-package"></div><br><br>

# kidney.epi R Package for Facilitating Research in Diabetes, Kidney, Heart, and Other Diseases

Chronic Kidney Disease (CKD) is a major global health challenge, affecting approximately 700 million people worldwide and contributing to 3.2 million deaths annually. Despite this substantial burden, CKD is often excluded from many health prevention programs, and not taken into account in many clinical trials and noncommunicable disease screening programs. This leads to a concerning disparity, with only 10-20% of individuals with CKD being aware of the existing disease. Early detection and management of CKD are critical to slowing its progression to end-stage renal disease, a costly and debilitating outcome, and to prevent other complications. Fortunately, CKD can be easily diagnosed through two inexpensive and widely available tests: urine analysis and serum creatinine (and/or cystatine C) measurement with subsequent calculation of estimated glomerular filtration rate (eGFR). These two simple tests should be regularly performed in high-risk patients including those with diabetes, hypertension, and other CKD risk factors.

Despite the simplicity and cost-effectiveness of these diagnostic measures, the integration of CKD testing into clinical practice and epidemiological studies remains limited. To bridge this gap, the kidney.epi R package has been developed by Scientific-Tools.Org. The package facilitates the exploration and analysis of CKD in diverse populations by providing a comprehensive set of functions tailored for kidney-related data analysis. The kidney.epi package enables researchers and data scientists to calculate eGFR using multiple validated equations, categorize results of urine analysis (albuminuria, proteinuria), and assign categories of complications risk based on the actual KDIGO classification. It allows to calculate eGFR based on the widely used CKD-EPI equation and more than 15 other equations based on both serum creatinine and/or cystatine C (both for children and adults). The package also has functions focused on kidney transplantation that allow calculating the Kidney Donor Profile Index (KDPI) and the Kidney Donor Risk Index (KDRI).

One of the key advantages of the kidney.epi package is the user-friendly design of functions that provide flexible label handling. Researchers do not need to modify datasets, recalculate different measurement units for laboratory values, or reformat existing labels for variables like sex or ethnicity. Instead, the functions accept user-defined labels and appropriate measurements units, thereby adapting seamlessly to various datasets.

The kidney.epi package allows automating kidney-related calculations in screening programs, clinical trials, and observational studies. It improves the accessibility and reproducibility of CKD-related research, and also contributes to the global effort to raise awareness, improve early detection, and ultimately reduce the CKD burden.

<div id="rum-cocktail"></div><br><br>

# Mix, Pour, Share: The rUM Cocktail for Biomedical Project Packaging

The reproducibility crisis in biomedical research demands systematic approaches to documentation, data sharing, and analysis transparency. While R Markdown and Quarto have revolutionized reproducible reporting, challenges remain in organizing complete research projects with associated datasets, documentation, and presentation materials. We present rUM (version 2.2 rUM runner), an R package developed at the University of Miami to streamline the creation of comprehensive, CRAN-ready research packages with minimal coding effort. rUM enables researchers to bundle entire biomedical research projects—including analyses, datasets, documentation, and presentations—into a single distributable package using one-line function calls.

Key features of rUM include:

1. Creation of CRAN-ready package structures with a single function call
2. Automated templates for R Markdown and Quarto manuscripts as package vignettes
3. Enhanced tools for documenting datasets with comprehensive metadata
4. Functions to create and integrate Quarto RevealJS presentations within packages
5. Tools to display and share slide decks stored within packages

Our presentation will demonstrate how rUM addresses reproducibility challenges through a complete workflow: analyzing a pharmacokinetic dataset (medicaldata::theophylline), documenting the dataset with enhanced metadata, creating presentation slides with analysis visualizations, and bundling everything into a distributable package. rUM significantly reduces the technical barriers to creating R packages, making reproducible research practices more accessible to biomedical researchers who have even minimal of programming experience. By transforming completed projects into packages, researchers can ensure their work is discoverable, reusable, and properly documented—addressing critical elements of the reproducibility crisis in medical research.

<div id="unlocking-statistical-consistency"></div><br><br>

# Unlocking Statistical Consistency Across Platforms: The CAMIS Project

As we transition to a world of multilingual programming, replication across software is critical. Comparing Analysis Method Implementations in Software (CAMIS) is an open-source repository dedicated to documenting the differences in statistical methodologies across a variety of software platforms such as SAS, R, Python, StatXact, and EAST. In the rigorously regulated medical research industry, ensuring the accuracy of results requires double or even triple programming, demanding matches in results from disparate systems.

We'll introduce the PHUSE CAMIS project, which delves into the nuances between different software implementations of methods. All relevant code, case studies, results, and findings are stored in our GitHub repository (https://psiaims.github.io/CAMIS/).

Through practical examples, we highlight observed discrepancies and pitfalls and how CAMIS helps to bridge a user’s understanding across software. Beyond asking whether results match, we'll emphasize the importance of assessing the robustness of the software packages and libraries generating these results.

Participants will gain valuable tools for efficiently investigating software discrepancies faced in daily tasks. We will address concerns and reassure current and future R users that, in most cases, results can be replicated across platforms. For those instances where replication fails, the CAMIS repository offers clear explanations to guide your understanding and resolution.

<div id="dengue-forecasting"></div><br><br>

# Dengue Forecasting Addressing the Interrupted Effect from COVID-19 Cases

Dengue is one of the deadliest vector-borne diseases in the world. Accurate time series forecasting of dengue cases is essential for preparedness—such as effective resource allocation for smoking to destroy breeding sites, distribution of medical supplies, and the development of early warning systems. In this study, we used weekly, district-wise dengue cases from 2007 to 2025 in Sri Lanka. Due to similar symptoms between dengue and COVID-19, case reporting from 2020 to 2022 may be unreliable, introducing an interrupted effect into the time series. This study investigates three modeling strategies to address this interruption. They are (i) excluding the interrupted period from model training, (ii) forecasting the interrupted period first and then using it for modeling, and (iii) down-weighting observations in the interrupted period. Data from 2007 to 2024 were used for model fitting, and data for 2025 were used for model testing. We evaluated the performance of these methods across 25 districts in Sri Lanka. There is no single method outperformed across all districts. The study further explores why certain approaches perform better in some districts than others, providing insights into tailoring forecasting methods to specific regional characteristics.

<div id="the-power-of-targets-package"></div><br><br>

# The power of {targets} package for reproducible data science 

Reproducibility is a cornerstone of credible and robust data science. This talk delves into the powerful targets package showcasing how it streamlines and enhances reproducibility in data science workflows. The targets package in R provides a comprehensive framework for pipeline management, enabling eﬃcient dependency tracking, automated pipeline execution, and clear documentation of the entire data analysis process. It ensures execution of complex pipelines in consistent and isolated environments.

Combined with tools like {renv} and docker, this approach eliminates the it works on my
machine problem. Through real-world examples, attendees will learn how to leverage these
tools to create reproducible, scalable, and maintainable data science projects, ensuring that
their analyses can be reliably replicated and shared across diverse computational
environments.

This workshop is designed for data scientists and analysts who are looking to enhance their ability to manage and scale up their analytical pipelines. By the end of the session, attendees will have a deeper understanding of the targets package, it’s capabilities and how to apply this package to their workflows, from exploration, to model building, to plotting and report generation.

<div id="no-more-copy-paste"></div><br><br>

# No More Copy-Paste: Automating Patient Inquiry Tracking in Pharma with Shiny

Managing patient support and prescription workflows often involves disparate tools, manual data wrangling, and time-consuming reporting. To streamline this process and provide real-time, actionable insights to field teams and DFAs (Dedicated Field Agents), we developed an R Shiny application that integrates prescription fulfillment data with Smartsheet-tracked patient inquiries.

This application serves as a dynamic operational hub, merging daily Excel-based prescription data with live Smartsheet API feeds to create a unified, interactive dashboard. Users can filter, sort, and export patient records while tracking key support metrics such as shipment history, days' supply remaining, and open ticket status.

This solution has replaced previously manual workflows with a self-serve analytics tool that is intuitive, lightweight, and built entirely in R. It demonstrates how combining existing tools like Smartsheet and Excel with R Shiny can unlock powerful efficiencies for medical field operations without requiring heavy infrastructure or vendor solutions.

<div id="cards-package"></div><br><br>

# Supercharging Statistical Analysis with ARDs and the {cards} R Package

The Analysis Results Data (ARD) Model is an approach that facilitates encoding statistical analysis summaries in a machine-readable format. This method seeks to streamline automation, improve reproducibility, encourage reusability, and enhance traceability in statistical practices. This talk will introduce the {cards} R package—a collaborative development by Roche, GSK, Novartis, Pfizer, and Eli Lilly within the Pharmaverse initiative. This powerful tool enables users to create ARDs, covering a range from straightforward statistical summaries like means and tabulations to complex analyses involving regression models and statistical tests.

Attendees will discover the extensive capabilities of {cards} and how it can be paired effectively with tabling packages such as {gtsummary} and {tfrmt} to create insightful displays. By the end of the session, participants will gain a practical understanding of these tools and acquire actionable strategies for integrating them into their workflows, thereby enhancing the efficiency and reliability of their statistical analyses.

<div id="accelerometry-biomarker-framework"></div><br><br>

# An Accelerometry Biomarker Framework with Application in Vigilance in UK Biobank Data

This talk introduces a framework for assessing vigilance using accelerometry data from the UK Biobank. We define vigilant and non-vigilant participant groups based on self-reported questionnaires, resulting in 95 matched pairs after propensity score matching on physical and behavioral characteristics. We present the sorted spectral image, a structured representation of daily accelerometry data derived from 5-minute bouts processed via Discrete Fourier Transform. A simplified convolutional neural network, inspired by AlexNet, is developed to classify participants based on these spectral images. Using 20-fold cross-validation, the model achieves an out-of-sample F1 score of 0.576 and an AUC of 0.539 at the sample level for participants aged 65 or younger. Subject-level analysis of this younger cohort yields an F1 score of 0.539 and an AUC of 0.564. These findings demonstrate the potential of accelerometry-derived biomarkers for non-invasively assessing vigilance, opening avenues for broader applications in monitoring cognitive states and movement-related disorders.

<div id="preprocessing-ehr-asthma"></div><br><br>

# Preprocessing Electronic Health Records for Analysis-Ready Data in an Asthma Cohort

Electronic health record (EHR) data has become an invaluable resource of extensive patient data for large-scale studies. However, EHR data is often accompanied by inconsistent data entries and formats which can involve a lengthy process of understanding the data and data preparation. Here, I will discuss several specific challenges observed when preparing EHR data for analysis using the tidyverse suite in R. Drawing on examples from an asthma cohort study, I will demonstrate how to clean and transform demographic characteristics, diagnostic codes, medications, and laboratory results data at both an encounter and patient level using packages such as dplyr, tidyr, stringr, and lubridate. This lightning talk will provide insight on common EHR data quality issues and provide strategies for resolving them to prepare users for their own research.

<div id="swimmer-plots"></div><br><br>

# Swimmer Plots with ggswim

Title: Simplifying Swimmer Plots in R using ggswim

Motivation

Swimmer plots are a valuable tool for visualizing treatment timelines, such as those in clinical trials. They provide a clear, interpretable way to track subjects over time, capturing various discrete events in a compact and accessible format offering a high-level comparative view of a population. Despite their usefulness, swimmer plots are not trivial to generate in R, limiting their use across research teams.

Creating swimmer plots using ggplot2 in R can be technically demanding. Proper scale alignment and legend composition requires deeper familiarity with ggplot2 internals than one might typically expect from a researcher. While some packages exist that support swimmer plot development, we were not able to find any that bridge the gap of easing plot generation while maintaining full compatibility with the grammar of graphics.

Approach

The ggswim package was developed as an extension to ggplot2 to address these challenges. It introduces a streamlined grammar specifically for swimmer plots, organizing visual elements into two conceptual categories: lanes and markers. Lanes represent continuous duration such as time on a given study while markers represent discrete points such as adverse events or outcomes. This framework integrates smoothly with existing tools that follow the grammar of graphics, allowing users to layer and label plot components using concise and intuitive syntax that maintains full compatibility with ggplot2.

Conclusion

ggswim fills a key gap in the R visualization toolkit by making swimmer plots accessible to a broader audience without sacrificing flexibility or aesthetics. By reducing the technical overhead typically required to produce swimmer plots, ggswim promotes reproducibility, transparency, and more effective collaboration in medical research settings. In this talk we’ll focus on not only the technical achievements of ggswim, but also the many changes it went through to get to its current state and what prompted its development in the first place.

<div id="visualising-data-for-patients"></div><br><br>

# Visualising data for patients: create accessible charts

Visualising data for patients or other stakeholders may be difficult. Most of the time, our audience does not have a scientific or medical background, so our duty is to present data in a way that is understandable for them. To create clear and accessible charts, there are several factors to consider, such as decluttering, accessibility of the colour palette, and fonts.

During this demo, we will see how to create accessible and clear charts in R.
Attendees will learn how to create a new palette in R that is colourblind-friendly, and also how to create an autism-friendly palette. 
We will check if the colours in the chart are colourblind friendly in R using colourblind, and we will see how a brand palette can be made accessible.
Starting with a brand palette that is not colourblind-friendly, we will create a new one that is colourblind-friendly.
Moreover, we will look for fonts that have high readability and see how to include them in our R code.

<div id="using-r-shiny-to-automate"></div><br><br>

# Using R shiny to perform and automate decision-analytic modeling for cost-effectiveness analysis

R is increasingly used for decision-analytic modeling such as Markov and microsimulation modeling in recent years for economic evaluation (cost-effectiveness, cost-utility, budget impact), thanks to the development of guidelines and packages. Base R, however, is still the most flexible way of constructing these models, which can then be rolled up into Shiny applications. In this presentation, I will demonstrate two cases of using base R and R Shiny for cost-effectiveness analyses: 1) a specific use case of Markov modeling for cost-effectiveness of remote patient monitoring, which was developed for better presentation of the results, and 2) a generic set-up which can be quickly adapted for several Markov model-based cost-effectiveness analyses. The generic set-up will include importing model input parameters from csv/excel files for various models with different model structure and number of parameters, which the script will automatically handle. I will show how we can either run the model inside the Shiny app itself or, in case of models that takes several hours to days to run, we can run and save the model results outside of Shiny and use Shiny to summarize the results in tables and figures.

<div id="in-the-nix-of-time"></div><br><br>

# In the Nix of Time: Creating a reproducible analytical environment with Nix and {rix}

The world of data science in medical research has seen tremendous growth in large part to the innovations powered by open-source software, especially in the ecosystem surrounding R. Even with the advanced tooling available to perform cutting-edge analytics and create novel software such as R packages, developers will encounter unique challenges to ensure reproducibility from both the analytical side as well as the development environments used to create software. A perfectly valid combination to address these challenges is using {renv} to manage R package dependencies and Docker/Podman to handle system-level dependencies. In recent years, the Nix package manager has emerged as an appealing framework to manage the full dependency stack of software projects, albeit with a rather steep learning curve. In this hands-on demonstration, I'll share how the new {rix} package (authored by Bruno Rodriguez and Philipp Baumann) has turbo-boosted my R package and reproducible analysis workflows, empowering me to rapidly iterate on new ideas while ensuring reproducibility across a wide variety of projects.

<div id="application-of-attention-mechanism"></div><br><br>

# Application of attention mechanism to improve performance of surveyed llm/mllm used across R/Medicine

Private-public partnerships have been engaged with regulatory agencies to foster adoption and conformance to mandated submission guidelines. The Linux Foundation / R Consortium Pilot Series with FDA have focused considerable efforts in collaboration with industry sponsors to provide proof of concept studies to accelerate conformance to technical guidelines required in modern technical submissions. The industry teams engaged in these pilot studies have recently directed focus into areas where use of llm/mllm might assist in areas ranging from use of Gen[Ai] to produce instructive vignettes to describe analytical datasets to auto-generation of the Analysis Data Reviewer's Guide (ADRG) to be included for Agency Reviewers as part of the eCTD (Electronic Common Technical Document) submission.

The hope for this demonstration is to allow the audience to engage with and understand the motivation of the model architectures including how the {attention} mechanism improves output performance, for example, with vignettes describing safety and efficacy data sets
used in the R Consortium Pilot Series with FDA. My hope is to further raise awareness and participation about the importance of these Pilot Series in R (and historically in context of the almost two decades efforts ongoing with the Standards and Regulatory Agencies) not
only to drive adoption but also push the industry forwards in alignment and implementation to meet the mandated changes. Excellent progress has been made and the hope is to continue the acceleration to include everyone who wishes to participate even if only
through organizational efforts at the local level using the public repository provided with the demonstration to raise the R/Medicine Ecosystem with a working examples of clinical importance for analytics and with regulatory submissions. 

The Demonstration Agenda (1 hour)
00:00-00:10 - Introduction: History and Technical Context - Motivation
00:10-00:25 - Background of Transformer Architecture with {attention} used in R/Medicine
00:25-00:50 - Demo of {attention} mechanism for vignette generation of Analysis Dataset Descriptions
00:50-00:59 - Q&A, Concluding Remarks

Most importantly, every effort is afforded to expand inclusion so every person feels welcome and encouraged to participate with the demonstration provided through the event.

<div id="redcapsync-and-rosyredcap"></div><br><br>

# REDCapSync and RosyREDCap: two development R packages using the REDCap API for standardized data pipelines and exploratory data analysis

R and REDCap are both widely utilized in medicine, including basic science, clinical research, and clinal trials. Both have independent strengths, but together they can create powerful data pipelines. Several R packages exist for using the REDCap Application Program Interface (API) such as, REDCapR, redcapAPI, and tidyREDCap. However, there are no standard R packages for maintaining synchronized data pipelines from REDCap or comprehensive shiny applications that are built to work for any possible REDCap project. 

REDCapSync streamlines comprehensive metadata and data extraction from one or multiple REDCap projects with a handful of functions like `setup_project` and `sync_project`. Using a cache of the last project save, a file directory, and the REDCap log, REDCapSync only updates the data that has been changed since the last API call. Each project is maintained as a standardized R list object that can be used downstream for the best that R has to offer in statistics, visualization, shiny apps, and more! Experimental functions exist for saving adding derived variables, merging REDCap forms, and generating data subsets that also refresh with `sync_project`. Furthermore, REDCapSync can be used to upload labelled data with the API, a feature not available on the REDCap website. 

RosyREDCap is an R shiny application that launches a local website for exploratory data analysis of REDCap projects. It is built to load all previous projects that were setup with the REDCapSync package. The user is able to toggle between projects, deidentify data, perform ad-hoc data visualizations, and more. 

Using tools like REDCapSync and RosyREDCap allow even new R users to harness the power of the REDCap API without the burden of having to learn the details. Simply get approved access to REDCap API token, choose a safe file directory, sync your project, and explore! At R medicine, I plan to demonstrate several examples and use cases for REDCapSync and RosyREDCap R packages to demonstrate how the combined strengths of R and REDCap are perfect for maintaining strong reproducible clinical data pipelines that improve research and patient care.

<div id="biomarker-identification"></div><br><br>

# Biomarker Identification by Means of Frequent Itemset Mining and Contrast Set Mining

We demonstrate the utility of using both frequent itemset mining and contrast set mining to analyze single-cell RNA-seq (scRNAseq) data. Whereas machine learning approaches to scRNAseq data analysis identify ensembles of salient genes that may or may not be somehow connected, itemset mining identifies groups of genes whose over- or under-expression necessarily co-occur. These co-occurrences may present evidence for pathways associated with particular endpoints. The workflow includes four major steps: (1) data retrieval and curation, (2) feature (gene) selection, (3) data discretization, and (4) itemset mining. Results from a clear cell Renal Cell Carcinoma (ccRCC) study is used for this demonstration. Patients in this study were diagnosed with both early-stage and late-stage ccRCC. We present results showing the success of frequent itemset mining and contrast set mining in identifying biomarkers (sets of genes) that differentiate early-stage ccRCC patients from late-stage ccRCC patients.

<div id="co-occurrence-analysis-and-knowledge-graphs"></div><br><br>

# Co-occurrence analysis and knowledge graphs for suicide risk prediction

Mental health disorders are complex phenotypes and current diagnoses would benefit from introducing multidimensional assessments and taking into account the spectrum and gradients of disorders
observed. To these ends the advent of novel natural language processing (NLP) methods present new opportunities for leveraging unstructured text data as clinicians notes in electronic health records, which detail why a diagnosis was made and why specific medications were prescribed.

The CELEHS laboratory at Harvard Medical School is part of the Center for Suicide Research and Prevention project led by Massachusetts General Hospital (MGH) and aims at developing tools for clinicians to measure the suicide risk of patients. In previous publications, collaborators have
highlighted the importance of using NLP to address the limitations of the International Classification of Diseases in accurately identifying cases of suicide attempts, which lead to consistently under estimating their true prevalence in statistical analyses.

As the CELEHS laboratory, our contribution to this project focuses on two main goals: first, developing robust survival models on codified data that can be transferred between institutions as MGH and Cambridge Health Alliance; second, leveraging name-entity recognition, co-occurrence analysis, knowledge graphs, and large language models to further extract insights from clinicians notes. In both institutions, we analyze cohorts of approximately 5,000 teenage patients admitted in psychiatric
departments.

In this talk I will present and introduce the open-source tools we developed to perform these analyses, as the kgraph and nlpembeds R packages, both of which are available on CRAN. The methods
underlying these packages were introduced last year in my previous talk at R in Medicine 2024 “Word embeddings in mental health” and enable to efficiently analyze large amounts of electronic health
records data, both codified and unstructured.

Our latest developments reveal how NLP enables to better interpret predictive features that would seem clinically irrelevant by considering only their use in the codified data, but which are actually key factors of why specific diagnoses were performed by clinicians.

<div id="operational-risk-assessment"></div><br><br>

# Operational Risk Assessment of R Packages: A Configurable Framework for Pharmaceutical Adoption

This talk introduces a novel framework addressing one of the most significant barriers to open-source adoption in the pharmaceutical industry: the risk assessment of R packages. We present a nuanced approach that positions risk appetite as the foundational element for developing effective assessment strategies across the spectrum of organisational tolerance levels.
Our framework recognises that risk appetite varies significantly between organisations—from those accepting minimal risk to those embracing calculated opportunities. This variation directly impacts assessment requirements: organisations with higher risk tolerance may implement streamlined evaluations focused on basic suitability and compatibility, while risk-averse entities typically demand rigorous validation protocols before production deployment.
To operationalise this framework, we introduce two complementary R packages: {litmus} and {litmus.score}. Building upon the R Validation Hub's pioneering work, these tools enable organisations to implement tailored scoring systems that reflect their specific risk profiles. The packages generate both comprehensive quality scores and granular category assessments across dimensions including code quality, documentation, community adoption, and maintenance patterns.
The system's strength lies in its configurability, evaluating measurable package attributes—such as test coverage metrics, documentation completeness, and maintainer diversity—to produce meaningful quality indicators that align with organisational risk thresholds. This presentation will demonstrate how pharmaceutical organisations can leverage this framework to make informed, risk-appropriate decisions about R package adoption.

