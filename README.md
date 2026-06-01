# NER using DEBERTA for recruitment

## Project Overview

The AI-Based Resume Screening and Ranking System is an intelligent recruitment automation solution that simplifies the resume evaluation process. The system automatically extracts relevant information from candidate resumes, analyzes candidate qualifications, and ranks candidates according to a given Job Description (JD).

The project leverages advanced Natural Language Processing (NLP) techniques and Transformer-based models such as Sentence-BERT (SBERT) and DeBERTa to perform semantic matching between resumes and job descriptions. By combining entity extraction, contextual understanding, extractive summarization, and ranking algorithms, the system assists recruiters in identifying the most suitable candidates efficiently.

---

## Problem Statement

Organizations receive hundreds of resumes for a single job opening. Manual screening of these resumes is time-consuming, costly, and prone to human error. Traditional keyword-based systems often fail to understand the contextual meaning of candidate skills and experience.

This project addresses these challenges by developing an automated resume screening framework capable of:

* Extracting structured information from unstructured resumes.
* Understanding candidate profiles using NLP.
* Comparing candidate qualifications against job requirements.
* Ranking candidates according to suitability.

---

## Objectives

The primary objectives of the project are:

1. Automate resume parsing and information extraction.
2. Extract candidate skills, experience, education, and contact details.
3. Generate concise resume summaries.
4. Match resumes with job descriptions using semantic similarity.
5. Rank candidates based on multiple evaluation criteria.
6. Reduce recruiter workload and improve hiring efficiency.

---

## Key Features

### Resume Parsing

The system automatically extracts:

* Candidate Name
* Contact Number
* Email Address
* Technical Skills
* Educational Qualifications
* Work Experience
* Job Role
* Organization Details

### Resume Summarization

Generates concise summaries of resumes using TextRank and Sentence-BERT embeddings.

### Job Description Analysis

The system extracts:

* Required Skills
* Required Experience
* Required Job Role

from the provided Job Description.

### Semantic Matching

Matches resumes against job descriptions using contextual similarity rather than simple keyword matching.

### Candidate Ranking

Ranks candidates based on:

* Skill Similarity
* Experience Similarity
* Role Similarity
* Contextual Similarity

---

## Technologies Used

| Technology            | Purpose                    |
| --------------------- | -------------------------- |
| Python                | Core Programming Language  |
| PDFPlumber            | PDF Resume Text Extraction |
| SpaCy                 | Named Entity Recognition   |
| Sentence-BERT (SBERT) | Semantic Similarity        |
| DeBERTa               | Contextual Understanding   |
| NetworkX              | TextRank Summarization     |
| NumPy                 | Numerical Computation      |
| PyTorch               | Deep Learning Backend      |
| Transformers          | Transformer Models         |

---

## System Architecture

```text
Resume PDF
    │
    ▼
PDF Text Extraction
    │
    ▼
Information Extraction
(Name, Skills, Experience,
Education, Contact Details)
    │
    ▼
Resume Summarization
(TextRank + SBERT)
    │
    ▼
Job Description Parsing
    │
    ▼
Semantic Matching
    │
    ▼
Candidate Ranking
    │
    ▼
Final Ranked Candidate List
```

---

## NLP Models Used

### 1. SpaCy

SpaCy is used for:

* Named Entity Recognition (NER)
* Candidate Name Extraction
* Text Processing
* Tokenization
* Sentence Segmentation

### 2. Sentence-BERT (all-MiniLM-L6-v2)

Sentence-BERT is used for:

* Semantic Similarity Calculation
* Resume Summarization Support
* Contextual Resume-JD Matching
* Embedding Generation

### 3. DeBERTa (microsoft/deberta-v3-base)

DeBERTa provides:

* Contextual Embeddings
* Enhanced Text Understanding
* Skill Matching Support
* Role Similarity Analysis

### 4. TextRank

TextRank is used to:

* Generate Extractive Summaries
* Select Important Resume Sentences
* Improve Candidate Profile Representation

---

## Methodology

### Step 1: Resume Upload

The user uploads one or more PDF resumes.

### Step 2: Text Extraction

PDFPlumber extracts textual information from each resume.

### Step 3: Information Extraction

The system identifies:

* Skills
* Experience
* Education
* Contact Information
* Candidate Name
* Job Role

### Step 4: Resume Summarization

Important resume sentences are selected using:

* Sentence-BERT Embeddings
* TextRank Algorithm

### Step 5: Job Description Processing

The system extracts:

* Required Skills
* Required Experience
* Required Role

from the job description.

### Step 6: Similarity Calculation

The following similarities are computed:

#### Skill Similarity

Jaccard Similarity

#### Experience Similarity

Experience Gap Analysis

#### Context Similarity

Sentence-BERT Cosine Similarity

#### Role Similarity

Sequence Matching

### Step 7: Candidate Ranking

A weighted score is calculated and candidates are ranked.

---

## Ranking Formula

Final Score =
0.4 × Skill Score +
0.3 × Experience Score +
0.2 × Context Score +
0.1 × Role Match Score

Where:

* Skill Score = Jaccard Similarity
* Experience Score = Experience Alignment
* Context Score = SBERT Similarity
* Role Match Score = Role Matching Score

---

## Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/resume-screening-ai.git

cd resume-screening-ai
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Download SpaCy Model

```bash
python -m spacy download en_core_web_sm
```

---

## Running the Project

```bash
python resume_screening.py
```

After execution:

1. Upload resumes.
2. Enter a Job Description.
3. View ranked candidates.

---

## Example Job Descriptions

### Software Engineer

```text
Software Engineer with Python, SQL, AWS and 5 years experience
```

### Assistant Professor

```text
Assistant Professor with teaching experience and Machine Learning knowledge
```

### Civil Engineer

```text
Civil Engineer with AutoCAD and structural design experience
```

---

## Evaluation Metrics

The system evaluates performance using:

### Precision

Measures correctness of candidate selection.

### Recall

Measures ability to retrieve relevant candidates.

### F1 Score

Harmonic mean of Precision and Recall.

---

## Results

The system successfully ranked resumes for:

* Assistant Professor
* Senior Solution Engineer
* Software Engineer
* Civil Engineer
* Business Development Manager

The ranking process demonstrated accurate matching between candidate profiles and job descriptions.

---

## Applications

* Human Resource Management
* Recruitment Agencies
* Applicant Tracking Systems (ATS)
* Talent Acquisition Platforms
* Corporate Hiring Solutions

---

## Authors

Fathima Sha Quadhari

D. Sameela

G. Rishita

A. Chaitanya Deepthi

