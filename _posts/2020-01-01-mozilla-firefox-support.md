---
layout: post
title: Mozilla - Automating Firefox Support Forum Tagging
permalink: /projects/mozilla-firefox-support/
type: current
---

Firefox desktop users file anywhere from 30 support tickets per day during quiet times up to 50 or more support tickets per day just after new releases at support.mozilla.org (SUMO). In the event of a Firefox incident, we can receive almost 300 tickets in one day (e.g., the [add-on incident in 2019](https://blog.mozilla.org/addons/2019/05/04/update-regarding-add-ons-in-firefox/)). While this is too much for staff and volunteers to tag manually, annotations provide immense value when triaging and responding to support questions.

<!--more-->

### Outline
The aim of this project is to develop and evaluate a prototype system for enriching support request submissions by automated annotation and language analysis. A preliminary dataset will be prepared ahead of the project to provide the basis for exploratory analysis. Subsequent refinements should focus on goals pertaining to achieving accurate annotations consistent with human reviewers.

The project will consist of three main work products:
* Language modelling of support tickets
    * Development of a meaningful lexicon of tags that are helpful in classifying SUMO tickets.
    * Application of basic natural language processing (NLP) methods to the corpus of SUMO support requests.
* Refined triaging based on NLP analysis of support tickets
    * Design and development of metrics for evaluating system performance via liaison with SUMO experts.
    * Assess the utility of sentiment analysis for detecting critical/urgent support issues.
    * Assess internal consistency of tags based on automated system and inter-tagger agreement for human annotations via a controlled study.
* Improve analytical capabilities in analyzing support issue corpora
    * Reporting of issue-based ticket volumes and other signals that may help identify growing browser issues.
    * Develop meaningful aggregation and reporting strategies that leverage existing and newly developed annotation data.
    * Detect trending issues via analysis of historical issue topics.
We will investigate improvements to the quality and throughput of the support systems at Mozilla when supplementing a portion of manual annotation work with an automated system. Students will work on prototyping the application of existing and novel tools from the domain of Natural Language Processing into existing workflows for triaging, response, and analysis of online support requests.

### Deliverables (Mozilla)
Manually and consistently tag 100-200 support tickets corresponding to SUMO activity spanning the release periods for Firefox versions 69, 70, and 71.
Generate a sizeable training corpus of annotated support tickets including:
Raw text of the support request content.
Metadata regarding submission information.
Metadata pertaining to manual annotation by one or more human support staff and/or volunteer.
Coordinate internal consistency experimentation during the project period to provide gold-standard performance testing on prototype/in-progress solutions.
Provide expertise into the operation of a large-scale online support system.
Provide expertise into fundamentals, development, and implementation of an experimental machine learning pipeline applied to online text analysis.

### Deliverables (CANOSP students)

Students participating in this project will be expected to have some familiarity with basic Natural Language Processing (NLP) concepts, have a working proficiency in Python and a sufficient familiarity with the general concepts of machine learning so as to be able to discuss topics pertaining to performance, classification, and modelling in text annotation tasks.

The development efforts will be 100% student-led and creative solutions are welcome. Students will attend weekly meetings with Mozilla project coordinators and liaise with SUMO experts to align development efforts with actual use cases grounded in domain expertise of the SUMO team. No predefined solution is mandated so long as the application achieves the stated goals. We encourage students to experiment with different technologies and tools available and place an emphasis on rigorous experimental design, correct coding practices, and parsimonious elegant code. Tasks include:
* Familiarize yourselves with existing research and industry deployments of NLP and automated tagging in online support systems.
* Define and document a performance measurement strategy at the system level that aligns with support team use-cases.
* Propose a tag ontology over the space of textual features in support requests.
* Develop a text analysis and NLP pipeline to parse, clean, and utilize SUMO support request entries.
* Develop an automated annotation method using NLP features as input and produces automated annotations according the defined ontology as output.
