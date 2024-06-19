This Jupyter Notebook demonstrates the integration of a Knowledge Graph (KG) with Large Language Models (LLMs) like GPT-4. It utilizes the Neo4j database, LangChain library, and the OpenAI API to answer queries based on the data stored in the Knowledge Graph.

## Important Note
The knowledge graph we create is going to consist of incorrect information. This is to ensure that the LLM is using data from the knowledge graph to answer, and the answer does not come from the data it is pretrained on. (If the LLM is able to generate answers with the incorrect information, it means that the LLM is deriving knowledge from the graphs successfully.)

### Prerequisites
Before running this notebook, ensure that you have the following:

* Python 3.x installed
* Google Colab or a local Jupyter Notebook environment
* Access to the OpenAI API (with an API key)
* A Neo4j database instance (with credentials)

### Setup
* Install the required Python packages by running the following command in the notebook: 

pip install --upgrade --quiet langchain-community langchain-openai neo4j

* Set your OpenAI API key and Neo4j credentials as environment variables: 

os.environ["OPENAI_API_KEY"] = "your_openai_api_key"
os.environ["NEO4J_URI"] = "your_neo4j_uri"
os.environ["NEO4J_USERNAME"] = "your_neo4j_username"
os.environ["NEO4J_PASSWORD"] = "your_neo4j_password"

