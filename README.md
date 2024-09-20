# Multiple-PDF-Chat

This script demonstrates how to build a Streamlit application that allows users to upload PDF files, process the text, and interact with the documents using Google Gemini Pro for conversational AI and FAISS for vector-based retrieval. Here's a brief overview of its key components:

Key Functionalities:
PDF Text Extraction: The function get_pdf_text reads and extracts text from uploaded PDFs using PyPDF2.PdfReader.
Text Chunking: The text is split into manageable chunks using RecursiveCharacterTextSplitter to ensure effective embedding and retrieval.
Vectorization with FAISS: The text chunks are embedded using Google Generative AI Embeddings and stored in FAISS for fast similarity searches.
Conversational Chain: A custom conversational chain is created with a template prompt, which ensures that responses are based solely on the document context. If the answer isn't found, the model responds with "answer is not available in the context".
User Input Handling: Users can ask questions, and the system retrieves relevant chunks from the vector store, processes them using the Gemini Pro model, and returns a response.
Streamlit UI: A simple UI where users can upload PDFs, process them, and then ask questions related to the uploaded documents.
Improvements and Notes:
Embeddings Model: The Google Generative AI embeddings (models/embedding-001) are used to vectorize the document chunks.
Conversational AI: Google Gemini Pro (gemini-pro) is employed for answering user questions, with customizable temperature settings for response variability.
The app offers an intuitive interface to upload PDFs, process their text, and interact with the content in a conversational manner, making it ideal for use cases such as legal document analysis, research paper exploration, and more.
