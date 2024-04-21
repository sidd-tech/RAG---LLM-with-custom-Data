# RAG---LLM-with-custom-Data

This repository contains implementations of the Retrieval-Augmented Generation (RAG) Architecture, leveraging various frameworks and tools for efficient retrieval and generation tasks. RAG Architecture combines the power of vectorized retrieval-based methods with the flexibility of generative models(like chatGPT,etc), offering enhanced capabilities for tasks such as question answering and text summarization.


## *Basic about RAG:*

![image](https://github.com/sidd-tech/RAG---LLM-with-custom-Data/assets/57222634/1dc3eb5c-268e-4a58-8f54-5e95f0c4a85c)

This architecture used pre-defined custom data stored in Vector DB. When user asks a question, it goes through vector data base and uses similarity search (cosine similarity) to retrieved the relevant chunks. It then forwards those chunks to the LLM. The LLM combines the user's query with the extracted context to generate answer to the user's query using the custom data provided.


## Files:
### RAG_Langchain.ipynb
This Jupyter Notebook implements the RAG Architecture using the Langchain framework. The ipynb format is used to make the understanding of RAG Implementation as easy as possible. The following components are utilized:

 * Langchain Framework: Langchain facilitates the implementation of RAG Architecture, enabling efficient interaction between retrieval and generation modules.
 * Faiss: Faiss is employed for Vector DB, allowing fast and scalable similarity search for retrieving relevant information.
 * PyPDF: PyPDF is utilized for extracting text from PDF documents, enabling the system to process a wide range of document formats.
 * Sentence Transformer: Sentence Transformer is used for generating vector embeddings of text, facilitating similarity calculations and retrieval tasks.
 * Free ChatGPT API: The system leverages the Free ChatGPT API from RAPID API.



### RAG_with_Rerank.ipynb
Sometimes the simple RAG arcitecture is not able to retrieve apt chunks to be passed into LLM. So an additional retrieval layer is implemented to improve retrieval accuracy. In this notebook we use Flashrank for reranking which is based on cross-encoders and is open sourced.
In this notebook we encounter the problem when the required chunk is not extracted properly using the RAG Architecture. We then use Flashrank to state this issue.

 * FlashRank: FlashRank (https://pypi.org/project/FlashRank/) is utilized for topic ReRanking, enhancing retrieval results by leveraging cross-encoder techniques.


### Document:
A sample document is used with the name 'Doc1.pdf' downloaded from this website : https://cartographicperspectives.org/index.php/journal/article/view/cp13-full/pdf.


### Modules/Packages

 * Langchain: https://python.langchain.com/docs/get_started/introduction/
 * Faiss (Vector DB): (https://python.langchain.com/docs/integrations/vectorstores/faiss/)
 * PyPDF: (https://pypi.org/project/pypdf/)
 * Sentence Transformer: https://python.langchain.com/docs/integrations/text_embedding/sentence_transformers/
 * Free ChatGPT API(RapidAPI hub): (https://rapidapi.com/haxednet/api/chatgpt-api8)
