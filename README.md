*Intuz — Your automation partner, one workflow at a time.*

<p align="center"> <picture> <img alt="Banner Image" src="https://github.com/user-attachments/assets/210f97fc-0fce-404a-b647-7dfe1302cd37" /> </picture> </p> 

[Intuz](https://www.intuz.com) helps organizations orchestrate AI, automation, and enterprise systems through scalable workflows. Our repository showcases proven implementations across healthcare, operations, customer support, document processing, sales, and back-office functions, enabling teams to accelerate automation initiatives without starting from scratch.


[N8N Creator](https://n8n.io/creators/intuz/) · [Generative AI Development Services](https://www.intuz.com/generative-ai-development/) · [AI Consulting](https://www.intuz.com/ai-transformation-services/) · [For Custom Workflow Automation](https://www.intuz.com/get-started/)

# Automatically archive QuickBooks invoice PDFs to Google Drive

This n8n template from Intuz provides a complete and automated solution for secure document archiving.

It automatically saves new QuickBooks invoice PDFs directly into Google Drive, creating a reliable backup system. For perfect organization, the workflow uses keywords from the invoice, like the client name or invoice number, to dynamically name the PDF files, ensuring you have a complete and easily searchable financial record.

## Use Cases

1. **Automated Document Archiving:** Eliminate the manual work of downloading and saving invoices. Set it up once and let it run.

2. **Compliance & Auditing:** Maintain a clean, chronological, and separate record of all issued invoices for easy access during audits.

3. **Secure Backup:** Create a redundant, secure backup of your critical financial documents in your own cloud storage.

4. **Enhanced Team Access:** Share the Google Drive folder with accountants, bookkeepers, or team members who need access to invoices but not to your full QuickBooks account.

## How It Works

1. **Real-Time Invoice Trigger:** The workflow starts the instant a new invoice is created in your QuickBooks account. A configured webhook sends a notification to n8n, kicking off the automation immediately.

2. **Fetch Invoice Metadata:** The workflow uses the invoice ID from the webhook to retrieve the full invoice details, such as the customer’s name and the transaction date. This information is used in the next steps.

3. **Generate the Invoice PDF:** A crucial HTTP Request node makes a direct API call to QuickBooks, requesting a PDF version of the invoice. This ensures the archived document is the official, formatted PDF, exactly as it appears in QuickBooks.

4. **Upload and Archive in Google Drive:** The final node takes the binary PDF data and uploads it to your specified Google Drive folder. It dynamically names the file for easy identification (e.g., `CustomerName_TransactionDate.pdf`), creating a perfectly organized and searchable archive.

## Setup Instructions

To get this workflow running, follow these key setup steps:

### 1. Credentials

- **QuickBooks:** Connect your QuickBooks account credentials to n8n.
- **Google:** Connect your Google account using OAuth2 credentials and ensure the Google Drive API is enabled.

### 2. QuickBooks Webhook Configuration

- First, activate this n8n workflow to make the webhook URL live.
- Copy the Production URL from the QuickBooks Webhook node.
- In your Intuit Developer Portal, go to the webhooks section for your app, paste the URL, and subscribe to Invoice creation events.

### 3. Node Configuration

- **Get an invoice & Generate PDF File:** These nodes will use your configured QuickBooks credentials automatically.
- **Upload file (Google Drive):** In the parameters for this node, you must select the Folder ID where you want your invoices to be saved.

## FAQ

**Is this template free to use?**
Yes. It's an open-source n8n workflow published by Intuz — copy the workflow JSON from this repo and import it into your own n8n instance at no cost.

**Do I need a paid n8n plan to run this?**
No. It runs on n8n's free self-hosted Community Edition or on n8n Cloud. You'll need your own credentials for the services this workflow connects to, not a specific n8n pricing tier.

**Is the archived file the official QuickBooks PDF?**
Yes. The workflow calls the QuickBooks API for the generated PDF of each invoice, so the file saved to Google Drive is the same formatted document you'd download from QuickBooks — not a recreated copy.

## Related n8n templates from Intuz

- [Automate real-time QuickBooks invoice sync to Google Sheets](https://github.com/Intuz-production/QuickBooks-Invoice-Sync)
- [Automate QuickBooks customers & sales receipts generation from a Google Sheet](https://github.com/Intuz-production/Automate-QuickBooks-Customer-Sales-Receipt-Creation)
- [Review contract risks and route approvals with Google Drive, OpenAI, and Gmail](https://github.com/Intuz-production/Legal-document-review-automation)

See all of Intuz's free n8n templates: https://www.intuz.com/n8n-workflow-automation-templates/

## Connect with us

Intuz is a USA-based AI & workflow automation company with 16+ years of experience building custom AI-enabled workflow automations for SMBs and Enterprises, specializing in agentic AI, LLM integrations, and CRM/ERP sync across Healthcare, FinTech, eCommerce, Manufacturing, and Real Estate. Explore 30+ free templates at intuz.com/n8n-workflow-automation-templates or get a custom workflow built at intuz.com/get-started.

* **Website:** https://www.intuz.com/
* **Email:** [getstarted@intuz.com](mailto:getstarted@intuz.com)
* **LinkedIn:** https://www.linkedin.com/company/intuz/
* **Get Started:** https://n8n.partnerlinks.io/intuz

## For Custom Workflow Automation

[Click here - Get Started](https://www.intuz.com/get-started/)
