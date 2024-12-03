# MultiLanguage Invoice Extractor

## Aim

The goal of this project is to create an AI-powered tool that extracts relevant information from invoice images in multiple languages. The application uses Google's Gemini AI model to process and analyze the invoice content and respond to user queries. The user can upload an image of an invoice, input a question, and receive a context-aware response based on the content in the image.

## Methodology

The system works by integrating Google’s Generative AI model, specifically the Gemini model, to analyze invoice images. Here is a step-by-step breakdown of the methodology:

1. **Image Upload**: The user uploads an invoice image (in JPG, JPEG, or PNG format). The system reads and processes the uploaded image into a format suitable for analysis.

2. **Prompt Creation**: The user provides an input question through a text input field. A pre-defined prompt is used to guide the Gemini model to understand that the image contains an invoice and that the user’s question is related to the invoice’s content.

3. **Image Processing**: The uploaded invoice image is converted into bytes, which are passed along with the user query to the Gemini AI model for processing. The model analyzes the image to extract relevant details and generate responses to the user's questions.

4. **Query Response**: After processing the input and image, the system uses the Gemini model to generate the most accurate response based on the invoice’s content, which is then displayed in the Streamlit app.

5. **Multi-language Support**: The system is designed to handle invoices in various languages, leveraging the capabilities of the Gemini model to process and understand multiple languages.

## Libraries Used

- **Streamlit**: Provides a user-friendly interface for uploading images and interacting with the AI model.
- **google-generativeai**: The main library for interacting with the Google Generative AI API (Gemini model) to analyze invoice images and generate responses.
- **python-dotenv**: Used to load environment variables (such as API keys) securely from a `.env` file.
- **PIL (Pillow)**: Handles image loading and processing in various formats (JPG, JPEG, PNG).
- **langchain**: Facilitates advanced integration with large language models for document-based tasks (e.g., invoice extraction).
- **PyPDF2**: A Python library used for PDF document handling, which could be integrated for future improvements like PDF invoice extraction.
- **chromadb**: A library that can be used for document storage and retrieval in future enhancements (e.g., saving processed invoice data).

## Evaluation Metric

The system’s performance can be evaluated based on the following metrics:

- **Response Accuracy**: Measures how accurately the AI model answers questions based on the uploaded invoice image. This can be assessed by comparing the model's response to the correct answer derived from the invoice content.
- **Response Time**: The time it takes for the system to process the uploaded image, generate embeddings, and provide the response. A lower response time is preferable for a better user experience.
- **Language Handling**: Evaluating how well the system processes invoices in multiple languages, including understanding language nuances and correctly interpreting the data.
  
## Results

Upon uploading an invoice image, the system correctly extracts information related to the invoice and provides relevant answers based on the user’s query. Key results include:

- **Invoice Image Processing**: The system can process various invoice formats (JPG, PNG, JPEG) and extract relevant details.
- **Question Answering**: After submitting a question related to the invoice, the system provides accurate responses, demonstrating the capabilities of the Gemini model in understanding invoice content.
  
For example, if the user asks about the total amount, date, or vendor, the system can extract these details from the invoice image and provide the correct answer.

## Conclusion

This project demonstrates an effective method for building a multi-language invoice extractor using AI. By integrating Google’s Gemini model with Streamlit, the system can process invoice images in various languages, answer user queries, and display the results in a user-friendly interface. The application offers an efficient solution for extracting and interpreting data from invoices, which can be applied to various use cases such as financial processing, automated accounting, and document management.

## Future Work

1. **Support for More File Types**: Currently, the system supports image formats like JPG, PNG, and JPEG. Future improvements could include support for PDF documents and other file types commonly used for invoices.
  
2. **Enhanced Language Support**: While the current version supports multiple languages, enhancing the model to handle a broader range of languages and regional invoice formats will improve the system's applicability globally.

3. **Data Extraction and Organization**: Instead of just answering questions, the system could extract key data points (e.g., vendor name, date, total amount) and store them in a structured format, such as a database or CSV file, for further analysis.

4. **User Feedback Integration**: Allow users to provide feedback on the system’s responses, which can be used to fine-tune the model and improve its accuracy over time.

5. **Real-time Invoice Parsing**: Integrating real-time parsing for invoices with live data inputs could make the system more dynamic, providing instant answers as users interact with the platform.

6. **Cloud Deployment**: Deploying the application on a cloud platform like AWS, Google Cloud, or Azure would enable scaling, support for larger datasets, and faster processing times for enterprise-level use cases.

## How to Run

### Prerequisites
- Python 3.x
- Required Python packages from `requirements.txt`
  
### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/username/MultiLanguage-Invoice-Extractor.git
   cd MultiLanguage-Invoice-Extractor
```
2. Install the dependencies:
```bash
pip install -r requirements.txt
```
3. Set up environment variables:
Create a ```.env``` file in the root directory and add the following:
```bash
GOOGLE_API_KEY=your_google_api_key
```
4. Run the Streamlit application:
```bash
streamlit run app.py
```
5. Open the provided local URL in your browser to use the app.
