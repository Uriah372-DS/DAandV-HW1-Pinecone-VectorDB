# DAandV-HW1-Pinecone-VectorDB

## Exercise: Building a RAG Pipeline with Pinecone VectorDB

### Overview

This repository contains the solution to an exercise from the Data Analysis and Visualization course. The exercise involves building a Retrieval-Augmented Generation (RAG) pipeline using Pinecone VectorDB. The solution is implemented in a Jupyter Notebook (`part_3.ipynb`) and also provided as a Python script (`part_3.py`).

### Files

- `part_3.ipynb`: Jupyter Notebook containing the solution to the exercise.
- `part_3.py`: Python script version of the Jupyter Notebook.

### Requirements

To run the code in this repository, you need the following:

- Python 3.x
- Jupyter Notebook (if running the `.ipynb` file)
- Pinecone API Key
- Cohere API Key

### Setup

1. Clone the repository:
   ```sh
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install the required packages. they are all listed in the imports at the start of the scripts.

### Running the Notebook

To run the Jupyter Notebook just open it in colab, add your API keys in the appropriate cell and click `Run all`.

### Running the Python Script

If you prefer to run the Python script (`part_3.py`), you need to modify the lines that fetch the API keys. The script currently uses Google Colab's `userdata` secrets management to retrieve the API keys:

```python
from google.colab import userdata
COHERE_API_KEY = userdata.get('COHERE_API_KEY')
PINECONE_API_KEY = userdata.get('PINECONE_API_KEY')
```

Replace these lines with code that retrieves the API keys from your preferred storage method. For example, you can use environment variables:

```python
import os
COHERE_API_KEY = os.getenv('COHERE_API_KEY')
PINECONE_API_KEY = os.getenv('PINECONE_API_KEY')
```

Make sure to set the environment variables before running the script:

```sh
export COHERE_API_KEY='your-cohere-api-key'
export PINECONE_API_KEY='your-pinecone-api-key'
```

Then run the script:

```sh
python part_3.py
```

You can also read them from a file or whichever other way you prefer, just make sure the keys are set at the top of the script.

---

Enjoy exploring the RAG pipeline with Pinecon!
