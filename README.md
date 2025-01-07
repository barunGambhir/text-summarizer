# Text Summarizer Project

This project is a text summarization application built using Python, FastAPI, and Hugging Face's Transformers library. The application provides endpoints for training a summarization model and generating text summaries using a pre-trained model.

---

## **Features**

1. **Train a Model**:
   - Train a text summarization model on a custom dataset.

2. **Generate Summaries**:
   - Use the trained model to summarize input text via an API.

3. **Batch Processing**:
   - Tokenizes and processes datasets for efficient training and evaluation.

4. **Evaluation**:
   - Evaluate the summarization model using the ROUGE metric.

---

## **Technologies Used**

- **Python**: Core programming language.
- **FastAPI**: API framework for serving endpoints.
- **Hugging Face Transformers**: For leveraging pre-trained models and pipelines.
- **PyTorch**: For model training and inference.
- **Datasets**: For dataset management and transformation.
- **ROUGE Metric**: To evaluate model performance.

---

## **Setup Instructions**

### **1. Clone the Repository**

```bash
git clone https://github.com/baruGambhir/text-summarizer.git
cd text-summarizer
```

### **2. Install Dependencies**

Ensure you have Python 3.8 or above installed. Then, install the required dependencies:

```bash
pip install -r requirements.txt
```

### **3. Run the Application**

Start the FastAPI server:

```bash
python app.py
```


---

## **API Endpoints**

### **1. Index**
Redirects to API documentation.

- **Endpoint**: `/`
- **Method**: `GET`

### **2. Train the Model**
Triggers the training pipeline.

- **Endpoint**: `/train`
- **Method**: `GET`
- **Response**: `Training successful!` or error message.

### **3. Generate Summary**
Generates a summary for the given input text.

- **Endpoint**: `/predict`
- **Method**: `POST`
- **Request Body**:
  ```json
  {
    "text": "Input text to summarize"
  }
  ```
- **Response**:
  ```json
  {
    "input_text": "Input text to summarize",
    "summary": "Generated summary"
  }
  ```

---

## **How It Works**

### **1. Data Ingestion**
- Downloads and extracts datasets for training.

### **2. Data Transformation**
- Tokenizes and processes the dataset for model training.

### **3. Model Training**
- Uses Hugging Face's `Trainer` API to fine-tune a summarization model.

### **4. Evaluation**
- Evaluates the trained model using ROUGE metrics.

### **5. Prediction**
- Summarizes input text using the trained model.

---

## **Future Enhancements**

- Add a graphical user interface (GUI).
- Extend support for other summarization models.
- Implement advanced error handling and logging.
- Enable batch predictions for large datasets.

---

## **Contributing**

Contributions are welcome! Please fork the repository and submit a pull request.

---

## **License**

This project is licensed under the MIT License. See the `LICENSE` file for details.

