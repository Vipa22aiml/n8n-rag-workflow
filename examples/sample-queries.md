# 💬 Sample Queries and Expected Responses

This document provides examples of queries you can ask your RAG AI agent and the types of responses you can expect.

## 📋 General Document Queries

### Basic Information Extraction

**Query**: "What is the main topic of the document I just uploaded?"

**Expected Response**: "Based on the document you uploaded, the main topic is [specific topic]. The document appears to be a [type of document] that covers [key areas discussed]."

**Query**: "How many pages is this document?"

**Expected Response**: "The document contains [X] pages and covers [brief summary of content]."

### Content Summarization

**Query**: "Can you summarize this document in 3 bullet points?"

**Expected Response**:
```
Here's a summary of the document in 3 key points:
• [Main point 1 with specific details]
• [Main point 2 with relevant information]
• [Main point 3 with important conclusions]
```

**Query**: "What are the key recommendations in this report?"

**Expected Response**: "The report contains several key recommendations: [lists specific recommendations with context and page references]"

## 🏢 Business & Corporate Queries

### Financial Analysis

**Query**: "What was our Q3 revenue according to the financial report?"

**Expected Response**: "According to the Q3 financial report, the revenue was $[amount]. This represents a [percentage]% [increase/decrease] compared to Q2, primarily driven by [key factors mentioned in the report]."

**Query**: "What are the main risk factors mentioned in the business plan?"

**Expected Response**: "The business plan identifies several risk factors: [lists specific risks with details from the document, including mitigation strategies if mentioned]"

### Policy & Compliance

**Query**: "What is the company policy on remote work?"

**Expected Response**: "According to the Employee Handbook, the remote work policy states: [specific policy details including eligibility, requirements, and guidelines]"

**Query**: "How many vacation days do employees get?"

**Expected Response**: "Based on the HR policies document, employees receive [number] vacation days annually. [Additional details about accrual, carryover policies, etc.]"

## 📊 Data Analysis Queries

### Excel & CSV Data

**Query**: "What was the highest sales figure in the spreadsheet?"

**Expected Response**: "The highest sales figure in the data is $[amount] for [product/region/time period]. This was achieved in [specific context from the data]."

**Query**: "Show me the trends in customer satisfaction scores"

**Expected Response**: "Based on the customer satisfaction data, the trends show: [specific trend analysis with numbers and time periods, including any notable changes or patterns]"

### Performance Metrics

**Query**: "What are the KPIs mentioned in the performance report?"

**Expected Response**: "The performance report tracks these KPIs: [lists KPIs with current values and targets if available]"

## 🔧 Technical Documentation

### How-To Questions

**Query**: "How do I reset the system according to the manual?"

**Expected Response**: "According to the technical manual, to reset the system: [step-by-step instructions with specific details and any safety warnings]"

**Query**: "What are the system requirements mentioned in the documentation?"

**Expected Response**: "The system requirements are: [lists all requirements including hardware, software, and network specifications]"

### Troubleshooting

**Query**: "What should I do if I get error code E102?"

**Expected Response**: "Error code E102 indicates [specific problem]. To resolve this: [troubleshooting steps from the documentation]"

**Query**: "How do I configure the network settings?"

**Expected Response**: "To configure network settings: [detailed configuration steps with specific parameters and values]"

## ⚖️ Legal & Compliance

### Contract Analysis

**Query**: "Does this contract have a termination clause?"

**Expected Response**: "Yes, the contract includes a termination clause in Section [X]. It states: [specific termination conditions and notice requirements]"

**Query**: "What are the liability limitations in this agreement?"

**Expected Response**: "The agreement limits liability to: [specific limitation amounts and conditions, with references to relevant sections]"

### Regulatory Information

**Query**: "What GDPR requirements apply to our data processing?"

**Expected Response**: "According to the compliance document, the GDPR requirements that apply include: [specific requirements with implementation details]"

## 📚 Research & Academic

### Literature Review

**Query**: "What methodology was used in this research paper?"

**Expected Response**: "The research paper used [specific methodology]. The study involved [sample size, data collection methods, and analysis techniques as described in the paper]"

**Query**: "What are the main findings of this study?"

**Expected Response**: "The study's main findings include: [key results with statistical significance if mentioned, and implications discussed in the paper]"

### Citation & References

**Query**: "Who are the main authors cited in this paper?"

**Expected Response**: "The paper frequently cites [list of key authors and their contributions to the field as mentioned in the document]"

## 🏥 Healthcare & Medical

### Procedure Information

**Query**: "What are the steps for this medical procedure?"

**Expected Response**: "The medical procedure involves these steps: [detailed procedural steps with safety considerations and equipment requirements]"

**Query**: "What are the contraindications mentioned?"

**Expected Response**: "The document lists these contraindications: [specific conditions or factors that would prevent the procedure/treatment]"

## 🏭 Manufacturing & Operations

### Quality Control

**Query**: "What was the defect rate last month?"

**Expected Response**: "According to the quality report, the defect rate last month was [percentage], which is [comparison to previous periods and targets]"

**Query**: "What maintenance is required for equipment XYZ?"

**Expected Response**: "Equipment XYZ requires: [maintenance schedule, specific procedures, and replacement part information from the manual]"

## 🔍 Advanced Query Examples

### Multi-Document Queries

**Query**: "Compare the Q2 and Q3 financial performance"

**Expected Response**: "Comparing Q2 and Q3 financial performance: [detailed comparison with specific metrics, changes, and explanations for variations]"

**Query**: "What information do we have about customer feedback across all documents?"

**Expected Response**: "Customer feedback information from multiple documents shows: [synthesized insights from various sources with specific examples]"

### Analytical Queries

**Query**: "What patterns do you see in the sales data?"

**Expected Response**: "Analysis of the sales data reveals several patterns: [specific patterns with supporting data and potential explanations]"

**Query**: "What are the common themes across these research papers?"

**Expected Response**: "Common themes across the research papers include: [identified themes with examples from multiple papers]"

## ❌ Queries That May Not Work Well

### Limitations to Expect

**Query**: "Predict next quarter's sales" ❌
**Why**: RAG systems work with existing document content, not future predictions

**Query**: "Create a new marketing plan" ❌  
**Why**: The system retrieves information but doesn't generate entirely new strategic documents

**Query**: "What's the weather today?" ❌
**Why**: Only knows what's in your uploaded documents, not real-time information

**Query**: "Solve this math equation: 2x + 5 = 15" ❌
**Why**: Unless your documents contain the solution method, it may not perform calculations

## 💡 Tips for Better Queries

### Be Specific
- ✅ "What is the termination notice period in the employment contract?"
- ❌ "Tell me about termination"

### Reference Context
- ✅ "According to the Q3 report, what were the main challenges?"
- ❌ "What were the challenges?"

### Ask Follow-up Questions
- ✅ "Can you provide more details about the compliance requirements you mentioned?"
- ✅ "What page is that information on?"

### Use Document-Specific Language
- ✅ "What does section 4.2 say about data retention?"
- ✅ "Find information about customer onboarding in the user manual"

---

**Remember**: The quality of responses depends on the quality and comprehensiveness of your uploaded documents. The AI can only work with the information you've provided in your knowledge base!