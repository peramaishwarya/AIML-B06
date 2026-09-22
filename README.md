Batch ID: AIML-B06
Project: AI-Based Research Paper Novelty Assessment System Using Retrieval-Augmented Generation (RAG)

AI-Based Research Paper Novelty Assessment System Using RAG
An AI-based system for assessing the potential novelty of a research paper by retrieving relevant existing literature and analyzing the similarities and differences between the submitted paper and prior research using Retrieval-Augmented Generation (RAG).

Overview
The rapid growth of research publications makes it difficult for researchers to manually search and compare a large number of existing papers to determine whether a research idea is sufficiently novel.
Traditional plagiarism and text-similarity detection tools mainly identify copied or closely matching text. However, research novelty is not limited to textual similarity. A research paper may use different wording while presenting an existing research idea, methodology, dataset, or contribution.

Our project aims to develop an **AI-assisted research paper novelty assessment system** that uses semantic retrieval and Large Language Models (LLMs) to provide evidence-based analysis of a submitted research paper against relevant existing literature.
The system is designed as a **decision-support tool** and does not replace expert evaluation of research novelty.

Objectives

* To accept a research paper as a PDF input.
* To extract and preprocess the content of the research paper.
* To generate semantic embeddings representing the research content.
* To retrieve relevant existing research papers using semantic similarity.
* To use retrieved literature as additional context for an LLM through RAG.
* To compare the target paper with relevant prior research.
* To provide an AI-assisted novelty assessment.
* To identify possible research gaps and areas of similarity.
* To generate an understandable analytical report for the researcher.

Problem We Are Addressing

Researchers need to examine a large amount of existing literature before claiming that their work is novel. Manually performing this comparison is time-consuming and difficult.
Existing plagiarism detection systems mainly focus on copied or textually similar content. They do not directly determine whether the **underlying research idea, methodology, dataset, or contribution** is sufficiently different from existing work.
Therefore, our system focuses on **literature-based conceptual analysis rather than only text matching**.

How the System Works

The proposed system follows a Retrieval-Augmented Generation pipeline:

Research Paper PDF
        ↓
PDF Text Extraction
        ↓
Text Preprocessing
        ↓
Document Chunking
        ↓
Semantic Embedding Generation
        ↓
Vector Database
        ↓
Similarity-Based Retrieval
        ↓
Top-K Relevant Research Papers
        ↓
Retrieved Literature + Target Paper
        ↓
Large Language Model (LLM)
        ↓
Novelty Assessment
        ↓
Research Gap Analysis
        ↓
AI-Assisted Analytical Report


 1. PDF Upload
The user uploads the research paper that needs to be assessed.

2. Text Extraction
The system extracts relevant textual content from the uploaded PDF.

3. Preprocessing
The extracted content is cleaned and divided into suitable sections or chunks so that it can be efficiently processed.

4. Semantic Embedding
The processed research content is converted into numerical vector representations using a transformer-based embedding model.
These embeddings represent the semantic meaning of the research content rather than relying only on exact keywords.

5. Literature Retrieval
Existing research papers are stored as embeddings in a vector database.
The system compares the target paper representation with the stored literature and retrieves the **Top-K most relevant papers** using semantic similarity.

6. Retrieval-Augmented Generation
The retrieved research papers are provided as additional context to the LLM along with the target paper information.
The LLM then analyzes the target research in the context of the retrieved literature.

7. Novelty Assessment
The system analyzes aspects such as:
* Research objective,
* Research problem,
* Methodology,
* Dataset,etc
Based on the retrieved evidence, the system provides an **AI-assisted novelty assessment**.

8. Research Gap Identification
The system also identifies possible areas where:
* Existing methods may have limitations
* Similar research has already been performed
* Certain aspects remain insufficiently explored

9. Analytical Report
The final output is presented as an understandable report containing the retrieved literature, comparison information, novelty assessment, and possible research gaps.

Why RAG?
Large Language Models may not have access to the complete and latest research literature required for a specific novelty assessment.
RAG addresses this by retrieving relevant external literature and providing it to the LLM as context.

Without RAG:
Paper → LLM → Assessment

With RAG:
Paper
  ↓
Retrieve Relevant Literature
  ↓
Literature + Paper
  ↓
LLM
  ↓
Evidence-Based Assessment

RAG therefore allows the system to ground its analysis in retrieved research literature instead of depending only on the model's internal knowledge.

Research Foundation
Our project is inspired by recent research on LLM-based scholarly novelty assessment and RAG.

Base Paper - Evaluating and Enhancing Large Language Models for Novelty Assessment in Scholarly Publications
The paper introduces "SchNovel", a benchmark containing 15,000 pairs of research papers across six research fields, and proposes **RAG-Novelty**, which retrieves relevant prior research and provides the retrieved context to an LLM for novelty assessment.
Our project takes this research direction as a foundation and aims to develop an application-oriented novelty assessment system with paper-level analysis and research-gap identification.

Supporting Research Areas

Our literature study also covers:
* LLM-based scientific novelty detection
* Idea-level similarity and retrieval
* Retrieval-Augmented Generation
* Semantic embeddings
* Vector databases
* LLM-based research analysis

Proposed System Components

The system consists of the following major components:
1. PDF Processing Module
2. Text Preprocessing Module
3. Embedding Generation Module
4. Research Paper Vector Store
5. Semantic Retrieval Module
6. RAG Pipeline
7. LLM Analysis Module
8. Novelty Assessment Module
9. Research Gap Analysis Module
10. Report Generation Module

Technologies

The exact technologies may be updated during implementation.

* Programming Language: Python
* Machine Learning / NLP: Transformer-based language models
* Embeddings: Semantic embedding models
* RAG: Retrieval-Augmented Generation
* Vector Database: Vector similarity search database
* LLM: Large Language Model
* PDF Processing: PDF text extraction tools
* Frontend: To be finalized based on implementation
* Version Control: Git & GitHub

Expected Output

For a submitted research paper, the system is expected to provide:
* Relevant existing research papers
* Semantic similarity/retrieval information
* Comparison of research objectives and methodologies
* Possible similarities with previous work
* AI-assisted novelty assessment
* Potential research gaps
* Analytical summary/report

Key Features

*  Research paper PDF input
*  Semantic literature retrieval
*  Transformer-based embeddings
*  Retrieval-Augmented Generation
*  LLM-based analysis
*  Novelty assessment
*  Research-gap identification
*  Automated analytical report
*  Literature-based evidence for assessment

Difference from Traditional Plagiarism Detection

| Plagiarism Detection                   | Our Novelty Assessment System                    |
| -------------------------------------- | ------------------------------------------------ |
| Focuses mainly on textual overlap      | Focuses on research similarity and novelty       |
| Detects copied content                 | Analyzes research ideas and contributions        |
| Uses text matching/similarity          | Uses semantic retrieval and LLM analysis         |
| Does not directly assess research gaps | Identifies possible research gaps                |
| Mainly checks existing text            | Uses retrieved literature as contextual evidence |

Current Limitations

* AI-based novelty assessment cannot guarantee that a research contribution is truly novel.
* Retrieval quality depends on the quality and coverage of the research-paper corpus.
* LLM-generated analysis may contain errors or unsupported conclusions.
* Research novelty can be subjective and domain-dependent.
* Final novelty decisions should be validated by researchers or domain experts.

Future Scope

* Expand the research-paper corpus to multiple scholarly sources.
* Improve retrieval using advanced embedding and re-ranking techniques.
* Support larger and more complex research papers.
* Improve research-gap identification.
* Add section-wise comparison of research papers.
* Improve explainability by showing evidence for each assessment.
* Evaluate the system across different research domains.
* Develop a complete web-based interface for researchers.

References

1. Lin, E., Peng, Z., Fang, Y. *Evaluating and Enhancing Large Language Models for Novelty Assessment in Scholarly Publications*, 2025.
2. Liu, Y. et al. *Harnessing Large Language Models for Scientific Novelty Detection*, 2025.
3. Gao, Y. et al. *Retrieval-Augmented Generation for Large Language Models: A Survey*, 2024.
