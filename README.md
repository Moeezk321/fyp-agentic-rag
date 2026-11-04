# Reducing Hallucination In E-commerce Chatbots Via Multi-agent Retrieval-Augmented Generation

Standard LLMs in E-commerce frequently generate hallucinations like fabricating product specs,outdated stock or incorrect prices etc. This will lead to customer mistrust and bad experience.
This project aims to minimize hallucinations in E-commerce chatbots by implementing a Multi-Agent Retrieval-Augmented Generation(RAG). RAG grounds LLM outputs by retrieving semantically relevant data from external knowldege bases before response generation. 
     The system feature three core agents:
     
-Web Agent: Crawls target store pages on demand using httpx and BeautifulSoup to extract clean live text.

-VectorDB Agent: Retrieves structured historical context from Pinecone using OpenAI embeddings(text-embedding-3-small)

-Manager Agent: Coordinates both agents via asyncio.gather and synthesizes their outputs using OpenAI LLMs into a single accurate response.

       Dual sourcing live web data and vector search effectively reduces LLM hallucinations and provides reliable customer support.
