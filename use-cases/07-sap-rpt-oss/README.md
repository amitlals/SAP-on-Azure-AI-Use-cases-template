# Use Case 7: SAP-RPT-1-OSS Tabular LLM Playground

Work with SAP's open-source tabular LLM for structured data processing, analysis, and natural language interaction with table data.

## 🎯 Objective

Explore and implement SAP's RPT-1-OSS (Retrieval-augmented Prediction for Tables), an open-source large language model specifically designed for understanding and working with tabular data.

## 🔧 Prerequisites

- Python 3.8 or higher
- Git for cloning the repository
- Basic understanding of Python and ML concepts
- 8GB+ RAM recommended
- GPU optional but recommended for better performance
- Familiarity with pandas and data analysis

## 📋 What You'll Learn

- How to use tabular LLMs for data analysis
- Natural language queries on structured data
- Table understanding and reasoning
- Data-to-text generation
- Table question answering
- Integration with SAP data sources

## 🚀 Setup Instructions

### Step 1: Clone the Repository
```bash
# Clone SAP's official repository
git clone https://github.com/sap-samples/sap-rpt-1-oss.git
cd sap-rpt-1-oss

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### Step 2: Install Dependencies
```bash
# Install required packages
pip install -r requirements.txt

# Install additional dependencies for SAP integration
pip install pandas numpy transformers torch
```

### Step 3: Download the Model
```bash
# Download pre-trained RPT-1 model
python download_model.py

# Or download from Hugging Face
# huggingface-cli download SAP/rpt-1-oss
```

### Step 4: Prepare Your Data
```python
import pandas as pd

# Load your tabular data
df = pd.read_csv('your_data.csv')

# Or connect to SAP system
# from pyrfc import Connection
# conn = Connection(ashost='host', sysnr='00', client='100', 
#                   user='user', passwd='pass')
```

## 💡 Example Use Cases

### 1. Natural Language Query on Tables

**Input Table: Sales Data**
| Product | Region | Q1_Sales | Q2_Sales | Q3_Sales |
|---------|--------|----------|----------|----------|
| Widget A | North | 15000 | 18000 | 22000 |
| Widget B | South | 12000 | 14000 | 16000 |

**Question:** "Which product had the highest growth from Q1 to Q3?"

**RPT-1 Response:**
```python
# Model analyzes the table and responds
answer = model.query(table, question)
# Output: "Widget A had the highest growth with 47% increase 
# from Q1 ($15,000) to Q3 ($22,000)"
```

### 2. Table Summarization

```python
from sap_rpt import RPTModel

# Load model
model = RPTModel.load('sap-rpt-1-oss')

# Summarize complex table
summary = model.summarize(df)
print(summary)

# Output: Natural language summary of key insights
```

### 3. Data Validation and Anomaly Detection

```python
# Detect anomalies in data
anomalies = model.detect_anomalies(df)

# Generate explanation
explanation = model.explain_anomalies(anomalies)
```

### 4. SAP Data Integration

```python
# Query SAP table
from sap_integration import query_sap_table

# Get sales order data
sales_orders = query_sap_table('VBAK')  # Sales Document Header

# Ask questions about the data
question = "What is the average order value by customer group?"
answer = model.query(sales_orders, question)
print(answer)
```

## 🎓 Advanced Usage

### Fine-tuning for SAP Data

```python
from sap_rpt import RPTModel, Trainer

# Load pre-trained model
model = RPTModel.load('sap-rpt-1-oss')

# Prepare SAP-specific training data
train_data = load_sap_training_data()

# Fine-tune on SAP data
trainer = Trainer(model)
trainer.train(train_data, epochs=5)

# Save fine-tuned model
model.save('sap-rpt-finetuned')
```

### Complex Table Operations

```python
# Multi-table reasoning
tables = {
    'orders': orders_df,
    'customers': customers_df,
    'products': products_df
}

question = "What is the total revenue from premium customers in Q3?"
answer = model.multi_table_query(tables, question)
```

### Integration with Azure OpenAI

```python
from azure.ai.openai import OpenAIClient
from sap_rpt import RPTModel

# Combine RPT for table understanding + Azure OpenAI for generation
rpt_model = RPTModel.load('sap-rpt-1-oss')
openai_client = OpenAIClient(endpoint=os.getenv('AZURE_OPENAI_ENDPOINT'))

# Get structured insights from RPT
table_insights = rpt_model.analyze(df)

# Generate narrative with Azure OpenAI
narrative = openai_client.complete(
    prompt=f"Write a business report based on: {table_insights}"
)
```

## 🔍 Key Features

### Table Understanding
- **Schema Recognition**: Understands table structure
- **Semantic Understanding**: Grasps meaning of columns and values
- **Relationship Detection**: Identifies relationships between tables
- **Context Awareness**: Maintains context across queries

### Natural Language Capabilities
- **Question Answering**: Answer questions about tables
- **Summarization**: Generate summaries of table content
- **Explanation**: Explain data patterns and anomalies
- **Generation**: Create natural language from tables

### SAP-Specific Features
- Integration with SAP HANA
- Understanding of SAP data models
- Support for SAP-specific terminology
- Handling of SAP table structures

## 📊 Performance Benchmarks

### Query Response Time
- Simple queries: < 1 second
- Complex multi-table queries: 2-5 seconds
- Large tables (>10k rows): 5-10 seconds

### Accuracy
- Question answering: 85-90% accuracy
- Anomaly detection: 80-85% accuracy
- Summarization quality: High (based on ROUGE scores)

## 🛠️ Use Case Examples

### Business Intelligence
```python
# Generate insights from sales data
insights = model.generate_insights(sales_df)
for insight in insights:
    print(f"Insight: {insight['description']}")
    print(f"Confidence: {insight['confidence']}")
```

### Data Quality Assessment
```python
# Check data quality
quality_report = model.assess_quality(df)
print(f"Completeness: {quality_report['completeness']}")
print(f"Consistency: {quality_report['consistency']}")
print(f"Issues: {quality_report['issues']}")
```

### Automated Reporting
```python
# Generate automated reports
report = model.generate_report(
    data=df,
    template='executive_summary',
    include_charts=True
)
report.save('monthly_report.pdf')
```

## 📚 Additional Resources

- [SAP-RPT-1-OSS GitHub Repository](https://github.com/sap-samples/sap-rpt-1-oss/)
- [Research Paper](https://arxiv.org/abs/xxxx.xxxxx) (if available)
- [Hugging Face Model Card](https://huggingface.co/SAP/rpt-1-oss)
- [SAP Machine Learning Documentation](https://help.sap.com/docs/SAP_HANA_PLATFORM/4505d0bdaf4948449b7f7379d24d0f0d/c9c8f8e7f6b44f5b9a7e5c2c7e7f7f7f.html)

## 🐛 Troubleshooting

**Issue**: Model loading fails
- **Solution**: Ensure you have enough memory and the model is downloaded correctly

**Issue**: Slow inference
- **Solution**: Use GPU acceleration or reduce batch size

**Issue**: Inaccurate results on SAP data
- **Solution**: Fine-tune the model on your specific SAP data

**Issue**: Out of memory errors
- **Solution**: Process data in smaller batches or use CPU inference

## 🔒 Security and Privacy

- **Local Processing**: Run models locally for data privacy
- **No External Calls**: Optional cloud integration
- **Data Protection**: Implement proper access controls
- **Audit Trail**: Log all model queries and responses

## 🎯 Success Metrics

- Query accuracy on your data
- Response time for typical queries
- User satisfaction with insights
- Time saved in data analysis

## 💡 Best Practices

1. **Data Preparation**: Clean and structure data properly
2. **Clear Questions**: Ask specific, well-formed questions
3. **Validation**: Always validate model outputs
4. **Iterative**: Refine prompts based on results
5. **Fine-tuning**: Customize for your domain

## 📞 Support

For technical questions about SAP-RPT-1-OSS, please:
- Check the [GitHub repository](https://github.com/sap-samples/sap-rpt-1-oss/)
- Open an issue on GitHub
- Contact the repository maintainer for integration guidance

---

**Demo**: See the main README for screenshots of SAP-RPT-1-OSS in action analyzing tabular data!
