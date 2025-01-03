# **Amazon Product Review Sentiment Analyzer**

This project is a **web-based application** that scrapes Amazon product reviews and performs **sentiment analysis** using a pre-trained `roBERTa` model. The app analyzes customer reviews to determine the overall sentiment (e.g., positive, negative, or neutral) and provides the results through a simple web interface built with **Flask**.

---

## **Table of Contents**
- [Features](#features)  
- [Tech Stack](#tech-stack)  
- [Installation](#installation)  
- [Usage](#usage)  
- [Project Structure](#project-structure)  
- [How it Works](#how-it-works)  
- [Demo](#demo)  
- [License](#license)  

---

## **Features**
- **Web scraping of Amazon reviews** using Selenium.
- **Sentiment analysis** powered by `cardiffnlp/twitter-roberta-base-sentiment`.
- **Preprocessing of reviews** to remove noise (e.g., usernames, URLs).
- **Softmax-based scoring** to compute probabilities for each sentiment class.
- Web-based **UI for input and output** using Flask.
- **Handles pagination** to collect reviews across multiple pages.

---

## **Tech Stack**
- **Frontend**: HTML (via Flask Templates)  
- **Backend**: Flask (Python)  
- **Machine Learning Model**: `roBERTa` from Hugging Face’s Transformers Library  
- **Web Scraping**: Selenium  
- **Dependencies**:  
  - `transformers`  
  - `scipy`  
  - `selenium`  
  - `numpy`  
  - `Flask`  

---

## **Installation**

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/amazon-review-sentiment-analyzer.git
   cd amazon-review-sentiment-analyzer
   ```

2. **Set up a virtual environment (optional)**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install the required dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Download the Chrome WebDriver**:  
   - Make sure **Google Chrome** is installed on your machine.
   - Download the appropriate version of **Chromedriver** from [here](https://chromedriver.chromium.org/downloads) and place it in your project directory or add it to your PATH.

---

## **Usage**

1. **Run the Flask application**:
   ```bash
   python app.py
   ```

2. **Open your browser** and go to:  
   ```
   http://127.0.0.1:5000/
   ```

3. **Enter the Amazon product URL** in the input field and click the **Analyze** button.

4. **View the sentiment analysis results** on the same page.

---

## **Project Structure**

```
amazon-review-sentiment-analyzer/
│
├── app.py                  # Main Flask application
├── reviewscrap.py          # Selenium-based scraping module
├── templates/
│   └── index.html          # HTML template for user input and results
├── requirements.txt        # Dependencies for the project
└── README.md               # Project documentation (this file)
```

---

## **How it Works**

1. **User Input**: The user provides an **Amazon product URL**.  
2. **Web Scraping**: The **Selenium-based scraper** navigates through the reviews page and collects customer reviews across all pages.  
3. **Preprocessing**: The text reviews are cleaned (removing usernames and URLs).  
4. **Sentiment Analysis**: The **roBERTa model** analyzes the sentiment of each review.
5. **Result Calculation**: Average scores are computed for each sentiment (positive, neutral, negative).
6. **Output**: The results are displayed on the web page.

---

## **Demo**

Below is an example of how the results are displayed:

- **Sentiment Analysis for Product X:**
  - **Positive**: 0.85  
  - **Neutral**: 0.10  
  - **Negative**: 0.05  

---

## **License**
This project is licensed under the **MIT License**. Feel free to modify and use it for your own purposes.

---

## **Contributing**
Contributions are welcome! If you'd like to add features or improve the project, please open a pull request.

---

## **Contact**
For questions or feedback, please reach out to:  
- **Your Name**: Bruce Fernandes  
- **Email**: brucefernades48@gmail.com  

---

This **README** provides all the necessary details for someone exploring your project on GitHub. Add the `requirements.txt` file with the appropriate dependencies to make the project easier to install. Let me know if you need further customization!
