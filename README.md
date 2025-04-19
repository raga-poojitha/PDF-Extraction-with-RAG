1.	Save the code to a file named rag.py
2.	Install required packages (the script will attempt to do this automatically): 
pip install PyPDF2 langchain sentence-transformers chromadb torch transformers openai pypdf faiss-cpu tiktoken
3.	Prepare your PDFs: 
o	Create a folder named pdf_data in the same directory as the script
o	Place your engineering PDFs in this folder
4.	Run the script: Basic usage: 
python rag.py
This will: 
o	Process all PDFs in the pdf_data directory
o	Create a vector database
o	Launch an interactive query mode
5.	Command-line options: 
o	Load existing database: 
python rag.py --load
o	Run a specific query: 
python rag.py --query "How does a centrifugal pump work?"
o	Use OpenAI directly instead of LangChain: 
python rag.py --openai --query "What is finite element analysis?"
o	Interactive mode (default): 
python rag.py --interactive
6.	In interactive mode: 
o	Type 'exit' to quit
o	Type 'openai' to switch to direct OpenAI querying
o	Type 'langchain' to switch to LangChain QA
The script will generate two directories:
•	pdf_data: Where you should place your engineering PDFs
•	vector_db: Where the vector database is stored
