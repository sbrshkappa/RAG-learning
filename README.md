# RAG-learning

This is a demo project to learn how to build a RAG system using [Llamaindex](https://github.com/jxnl/instructor).

## Setup

All the dependencies are listed in [requirements.txt](./requirements.txt) which you can install using pip.

The [rag_demo.ipynb](./rag_demo.ipynb) file contains the code to run the basic RAG using the LlamaIndex and also contains a cell where I wrote a custom RAG pipeline that breaks the [Codepath Document](./data/Codepath_Student_Handbook_2024.pdf) into smaller chunks and authors a prompt to generate a response from the LLM.

## Gmail RAG LLM

To run [rag_email.ipynb](./rag_email.ipynb) in the project, you need to have a gmail account with access to the Gmail API.

1. Go to [Google Cloud Console](https://console.cloud.google.com/apis/credentials)
2. Create a new project
3. Enable the Gmail API for the project
4. Create credentials (client ID and client secret)
5. Download the credentials and save them as `credentials.json`. (When run this will generate a token.json)

## Evaluation and Generating a Dataset

The code in [generate_qa_dataset.ipynb](./generate_qa_dataset.ipynb) generates a dataset of questions and answers from the [Codepath Document](./data/Codepath_Student_Handbook_2024.pdf) which can be used to evaluate the performance of the RAG system. The evaluation is done in [evaluate_qa_dataset.ipynb](./evaluate_qa_dataset.ipynb) where we take the output from the RAG system and compare it with the expected output.

> **Note:** The dataset generated from the code is saved in [qa_dataset.json](./qa_dataset.json)

> If you have any questions, please feel free to open an issue or contact me at sabareesh.kappagantu@gmail.com
