# Flask Text Processing Application

## Overview
This Flask-based web application allows users to perform various text processing tasks such as searching for words, retrieving the most and least frequent words, counting special characters, and more. The app processes a collection of U.S. inaugural addresses stored in the `all.txt` file and provides an interactive interface for users to explore the text data. The application is deployed and accessible via the **Azure Cloud Platform**.

## Features
1. **Search for Words**: Search for occurrences of a word in the U.S. inaugural addresses and display matching lines.
2. **Most and Least Frequent Words**: Retrieve the most or least frequently occurring words.
3. **Special Character Count**: Analyze input text to count spaces, special characters, and display the total characters.
4. **Substring Search**: Search for a substring within a given text.
5. **First N Characters**: Display the first N characters from the text.
6. **Word Occurrences**: Count occurrences of specific words within the text.
7. **Remove Words**: Remove specific words from the text file.
8. **Word Lengths**: Find words within a specific length range.

## Project Structure

- **`app.py`**: Main Flask application containing all routes and logic.
- **`templates/`**: Directory containing HTML templates for rendering the web pages.
- **`static/`**: Directory for static files (e.g., CSS, JavaScript).
- **`all.txt`**: Corpus containing the U.S. inaugural addresses used for text processing.

## Deployment on Azure

This application is hosted on the **Azure Cloud Platform** for global accessibility. Azure provides a reliable, scalable cloud infrastructure that ensures high availability and performance of the application. It can be accessed by users via a web interface deployed on Azure.

### Accessing the Application on Azure:
1. Ensure that the Azure Web App URL or IP is available.
2. Visit the application through the provided URL.
3. Interact with the application to perform text processing tasks like search, frequency analysis, and more.

## Installation (Local Setup)

### Requirements
- Python 3.x
- Flask
- NLTK (Natural Language Toolkit)
- Matplotlib

### Setup Instructions

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/flask-text-processing.git
   cd flask-text-processing
   ```

2. **Create a virtual environment** (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install the required dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Download NLTK data**:
   In Python, run the following commands to download necessary NLTK packages:
   ```python
   import nltk
   nltk.download('stopwords')
   nltk.download('punkt')
   ```

5. **Run the application**:
   ```bash
   python app.py
   ```
   The app will run on `http://127.0.0.1:5000`.

## Usage

### Routes

1. **Home Page** (`/`): Displays the main search interface.
2. **Get Most Frequent Words** (`/getMostFrequentWords`): Input a number to retrieve the most frequent words.
3. **Get Least Frequent Words** (`/getLeastFrequentWords`): Input a number to retrieve the least frequent words.
4. **Search in File** (`/search`): Input a word to search in all U.S. inaugural addresses.
5. **Search in Single File** (`/searchwrkg`): Input a word to search in a specific file (`all.txt`).
6. **Character and Special Character Count** (`/it`): Input text to analyze the number of total characters, spaces, and special characters.
7. **Substring Search** (`/textinsub`): Input a string and a substring to find how many times the substring occurs in the string.
8. **First N Characters** (`/first_n_chars`): Input a number to retrieve the first N characters from the text.
9. **Word Occurrences** (`/occofword`): Input words to count their occurrences in the text.
10. **Remove Words** (`/remword`): Input words to remove them from the text.
11. **Word Lengths** (`/wordlengths`): Input a minimum and maximum word length to retrieve words within that range.

## Templates

- **`query.html`**: Displays forms for text-based input operations.
- **`count.html`**: Displays the results of the most or least frequent words.
- **`search.html`**: Displays the results of the word search.
- **`it.html`**: Displays character analysis results.
- **`maxmin.html`**: Displays the words found based on word lengths.

## How to Extend
1. **Add New Routes**: To add a new functionality, define a new route and function in `app.py`.
2. **Modify Templates**: Update or create new HTML templates inside the `templates/` folder.
3. **Extend Corpus**: Add more files to the `US_Inaugural_Addresses` folder for analysis.

## License
This project is licensed under the MIT License.

## Contributions
Contributions, bug reports, and feature requests are welcome. Feel free to submit a pull request.

---
