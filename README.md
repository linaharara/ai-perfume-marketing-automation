# 🌸 AI-Powered Marketing Content Generator for Perfumes

## 📌 Overview
A no-code automation workflow that reads a list of product names from Google Sheets and automatically sends each one to **Claude (Anthropic)** via API to generate professional marketing content — with zero manual intervention.

## 🎯 Problem Solved
Writing marketing content (headline + description + selling points) for dozens of products manually is slow and produces inconsistent quality. This project solves that by:
- Standardizing output quality across all products
- Cutting turnaround time from hours to seconds
- Scaling to any number of products by simply adding rows to the sheet

## 🛠️ Tools Used
- **n8n** – Workflow automation platform
- **Claude (Anthropic API)** – Generative AI model (claude-sonnet-5)
- **Google Sheets** – Data source (product name list)

## ⚙️ Workflow
```
[Manual Trigger] 
      ↓
[Read rows from Google Sheets] 
      ↓
[Send each product name to Claude via a structured prompt template]
      ↓
[Receive formatted marketing content: headline + description + 3 selling points]
```

## 🧠 Prompt Design
Built a reusable prompt template with:
- **A defined role** for the model (expert perfume marketing copywriter)
- **A dynamic variable** for the product name (`{{ $json['اسم_المنتج'] }}`) instead of manual re-entry
- **Explicit constraints** to ensure consistent quality and prevent the model from hallucinating unmentioned product details

## 📊 Sample Output
Ran the automation on 4 products (My Way, jadore , Bleu de Chanel, Sauvage) — each received complete, consistently structured marketing copy in seconds.

## 💡 Key Takeaways
- Core prompt engineering principles and their direct impact on output quality
- Building a workflow that connects a data source to an AI model via API
- Working with dynamic expressions in no-code automation tools
- The importance of explicit prompt constraints to prevent AI hallucination

## 🚀 Future Improvements
- Add a filtering step to auto-clean model output
- Write results directly back into the Google Sheet
- Extend the template to support multiple languages or product categories
