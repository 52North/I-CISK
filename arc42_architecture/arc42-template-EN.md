# 

**About arc42**

arc42, the template for documentation of software and system
architecture.

Template Version 8.1 EN. (based upon AsciiDoc version), May 2022

Created, maintained and © by Dr. Peter Hruschka, Dr. Gernot Starke and
contributors. See <https://arc42.org>.

# Introduction and Goals {#section-introduction-and-goals}
This document describes the architecture for the Climate Service designed for the I-CISK project.

## Requirements Overview {#_requirements_overview}
The Climate Service for the I-CISK project aims to fulfill the following goals:

- provide access to a combination of different sources for environmental data e.g. from the Copernicus Program [], the Swedish Meteorological and Hydrological Institute (SMHI) [] and, in particular, a variety of local data sources;

- integrate models for bias correction, downscaling and indicator calculation;

- provide visualisation tools for the indicators that are required by the individual LLs;

- provide stakeholders with the possibility to easily extend the existing functionality by modifying and adding individual components.

## Quality Goals {#_quality_goals}

- comprehensive visualisation techniques that are adapted to the stakeholders needs

- modular integration of models and data sources such that individual components can be combined for the calculation of different indicators in a flexible way
- easy operation and comprehensive documentation of software components to enable stakeholders to further extend the CS also after the project duration

## Summary of stakeholder requirements for each Living Lab {#_stakeholders}
This  section summarises the current status of the properties that have been identified as necessary for the individual CS components by the LL leaders. Thereby, the requirements for the back end are collected separately from those for the front end. The individual components that are considered for the back end are the

- Climate Data Hindcast/Forecast Providers (the external data recources excluding local recources)

- Local Data Knowledge ECV (the local data recources)

- EVC/Indicators (the target variables)

- Data Types (the data types of the indicators)

- Time Scenario (the time periods over which the indicators are aggregated)

- Climate Models (models necessary to obtain the target indicators)

- Climate Adaption/Economic Models (models which investigate the climate response of indicators to adaption strategies)

- Run Mode of Climate Model and Adaption/Economic models (the run mode of climate and adaption models)

- Climate Model and Adaption/Economic Model Providers (external services or I-CISK WPs that provide the models) <br>

<figure>
  <img src="figures/introduction/LL1_backend.jpg"/>
  <figcaption>Figure 1: Schematical view of the individual components that have been identified for the LL1</figcaption>
</figure>

On the other hand, the components which are relevant for the backend are the

- Visualisation Containers 

- Visualisation Tools

- Visualisation Tool Providers

- Web Service <br>

<figure>
  <img src="figures/introduction/LL1_frontend.jpg"/>
  <figcaption>Figure 1: Schematical view of the individual components that have been identified for the LL1</figcaption>
</figure>


<table>
  <caption style="text-align:center"> Table 1: Selection of stakeholders for each living lab and their expectations regarding the CS functionality and architecture. If there is a focus on a particular group of stakeholders, this group is marked by (*).</caption>
  <tbody>
    <tr>
      <th align="left">Living Lab</th>
      <th align="left">Stakeholder profession</th>
      <th align="left">Expectations regarding CS architecture</th>
    </tr>
    <tr>
      <td>Spain LL (LL1)</td>
      <td>Olive Farmers<br>Dairy Farmers on Oak-/Grassland</td>
      <td>develop full CS that
        <ul>
          <li>provides a mobile app</li>
          <li>provides weekly and long-term forecasts
          <li>enabels to compare current climate data to historical data</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>Greece LL (LL4)</td>
      <td>developement company of Crete responsible for water management (*) <br>NGOs<br>municipality of port Rethimno<br>Greek National touris organisation<br>representatives of luxury hotel sector </td>
      <td> develop full CS that 
        <ul>
          <li>provides forecasts on time scales from monthly to seasonal</li>
          <li>provides climate projections</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>Lesotho LL (LL7)</td>
      <td> National Disaster Management Team<br>District Disaster Management Teams<br>Community Based Disaster Response Teams<br>Village Disaster Management Teams<br>National University of Lesotho</td>
      <td> connect to an existing CS i.e.
        <ul>
          <li>provide WMS that can be accessed by excisting multi-active platform (IBF-system [1]) via an API</li>
          <li>set up data analysis pipeline for weekly to seasonal forecasts that can be integrated in IBF-system after project run time</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>


[1] IBF-system, accessible via [https://github.com/rodekruis/IBF-system](https://github.com/rodekruis/IBF-system)

+-------------+---------------------------+---------------------------+
| Role/Name   | Contact                   | Expectations              |
+=============+===========================+===========================+
| *           | *\<Contact-1\>*           | *\<Expectation-1\>*       |
| \<Role-1\>* |                           |                           |
+-------------+---------------------------+---------------------------+
| *           | *\<Contact-2\>*           | *\<Expectation-2\>*       |
| \<Role-2\>* |                           |                           |
+-------------+---------------------------+---------------------------+

# Architecture Constraints {#section-architecture-constraints}

# System Scope and Context {#section-system-scope-and-context}

## Business Context {#_business_context}

**\<Diagram or Table\>**

**\<optionally: Explanation of external domain interfaces\>**

## Technical Context {#_technical_context}

**\<Diagram or Table\>**

**\<optionally: Explanation of technical interfaces\>**

**\<Mapping Input/Output to Channels\>**

# Solution Strategy {#section-solution-strategy}

# Building Block View {#section-building-block-view}

## Whitebox Overall System {#_whitebox_overall_system}

***\<Overview Diagram\>***

Motivation

:   *\<text explanation\>*

Contained Building Blocks

:   *\<Description of contained building block (black boxes)\>*

Important Interfaces

:   *\<Description of important interfaces\>*

### \<Name black box 1\> {#__name_black_box_1}

*\<Purpose/Responsibility\>*

*\<Interface(s)\>*

*\<(Optional) Quality/Performance Characteristics\>*

*\<(Optional) Directory/File Location\>*

*\<(Optional) Fulfilled Requirements\>*

*\<(optional) Open Issues/Problems/Risks\>*

### \<Name black box 2\> {#__name_black_box_2}

*\<black box template\>*

### \<Name black box n\> {#__name_black_box_n}

*\<black box template\>*

### \<Name interface 1\> {#__name_interface_1}

...

### \<Name interface m\> {#__name_interface_m}

## Level 2 {#_level_2}

### White Box *\<building block 1\>* {#_white_box_emphasis_building_block_1_emphasis}

*\<white box template\>*

### White Box *\<building block 2\>* {#_white_box_emphasis_building_block_2_emphasis}

*\<white box template\>*

...

### White Box *\<building block m\>* {#_white_box_emphasis_building_block_m_emphasis}

*\<white box template\>*

## Level 3 {#_level_3}

### White Box \<\_building block x.1\_\> {#_white_box_building_block_x_1}

*\<white box template\>*

### White Box \<\_building block x.2\_\> {#_white_box_building_block_x_2}

*\<white box template\>*

### White Box \<\_building block y.1\_\> {#_white_box_building_block_y_1}

*\<white box template\>*

# Runtime View {#section-runtime-view}

## \<Runtime Scenario 1\> {#__runtime_scenario_1}

-   *\<insert runtime diagram or textual description of the scenario\>*

-   *\<insert description of the notable aspects of the interactions
    between the building block instances depicted in this diagram.\>*

## \<Runtime Scenario 2\> {#__runtime_scenario_2}

## ... {#_}

## \<Runtime Scenario n\> {#__runtime_scenario_n}

# Deployment View {#section-deployment-view}

## Infrastructure Level 1 {#_infrastructure_level_1}

***\<Overview Diagram\>***

Motivation

:   *\<explanation in text form\>*

Quality and/or Performance Features

:   *\<explanation in text form\>*

Mapping of Building Blocks to Infrastructure

:   *\<description of the mapping\>*

## Infrastructure Level 2 {#_infrastructure_level_2}

### *\<Infrastructure Element 1\>* {#__emphasis_infrastructure_element_1_emphasis}

*\<diagram + explanation\>*

### *\<Infrastructure Element 2\>* {#__emphasis_infrastructure_element_2_emphasis}

*\<diagram + explanation\>*

...

### *\<Infrastructure Element n\>* {#__emphasis_infrastructure_element_n_emphasis}

*\<diagram + explanation\>*

# Cross-cutting Concepts {#section-concepts}

## *\<Concept 1\>* {#__emphasis_concept_1_emphasis}

*\<explanation\>*

## *\<Concept 2\>* {#__emphasis_concept_2_emphasis}

*\<explanation\>*

...

## *\<Concept n\>* {#__emphasis_concept_n_emphasis}

*\<explanation\>*

# Architecture Decisions {#section-design-decisions}

# Quality Requirements {#section-quality-scenarios}

## Quality Tree {#_quality_tree}

## Quality Scenarios {#_quality_scenarios}

# Risks and Technical Debts {#section-technical-risks}

# Glossary {#section-glossary}

+-----------------------+-----------------------------------------------+
| Term                  | Definition                                    |
+=======================+===============================================+
| *\<CS\>*              | *\<Climate Service\>*                       |
+-----------------------+-----------------------------------------------+
| *\<LL\>*              | *\<Living Lab\>*                              |
+-----------------------+-----------------------------------------------+
