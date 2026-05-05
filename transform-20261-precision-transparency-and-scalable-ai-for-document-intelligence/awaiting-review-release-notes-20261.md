# AWAITING REVIEW Release Notes 2026.1

![The Adlib logo.](./attachments/att_0_for_75661315.png)

# 2026.1 Release Overview

Transform 2026.1 delivers significant advancements in document processing accuracy, scalability, and transparency. This release focuses on enabling large-scale AI processing, improving trust in AI outputs, and modernizing model development and system integration.

This means you can:

- Process large and complex documents more reliably
- Understand and verify AI extraction results with greater confidence
- Build and test models faster with less manual effort
- Work with more AI models and integrations with less setup
- Add human decision points directly into automated workflows

These improvements help you handle higher workloads while improving accuracy and reducing manual review effort.

# What’s New

## Model Builder

- New card-based model list experience that makes extraction models easier to browse, search, and manage
- Category filtering to help you organize and locate models faster
- Sample document-driven model creation that can generate a starting model from an uploaded document
- Automatic extraction field suggestions based on the sample document
- In-page model testing, so you can run extraction tests without leaving the model builder
- Model versioning with change notes, allowing you to track changes and restore a previous version when needed
- Support for multiple LLM provider comparison, helping you evaluate extraction results across models
- Model settings available directly in the model builder, including settings for large document processing

## Human-in-the-Loop Workflow Enhancements

- Human-in-the-Loop steps can now be launched directly from n8n workflows
- Workflows can pause for user input and resume automatically after review is complete
- New task types support classification, review, approval, data entry, and external review URLs
- Classification tasks allow users to select a document type or category during workflow processing
- Approval tasks allow users to approve or reject a document before the workflow continues
- Data entry tasks allow users to provide additional information required by the workflow
- External review URL tasks allow Transform workflows to route review steps to another system, then resume when that system responds
- Review input is returned to the workflow so it can drive downstream decisions and routing

## AI Model Support and Scalability

- Bring your own LLM support allows you to use models hosted in supported provider environments
- Native Azure Foundry model support for Llama and Mistral models
- AWS Bedrock and Google Vertex AI provider configuration through the Portkey gateway
- Updated Portkey gateway support for the Responses API
- Support for newer certified models, including GPT 5.2, GPT 5.3, and Chat 5.4
- LLM round robin distributes requests across multiple deployments of the same model to support higher-volume extraction workloads
- Round robin configurations can support multiple model deployments, including deployments across regions, where configured

## Large Document Processing

- Large document processing using chunking and stitching, allowing Transform to process documents that exceed an LLM provider’s context window
- Configurable `PagesPerChunk` setting for OCR-based processing
- Configurable `ImagesPerChunk` setting for vision-based processing
- Chunked processing sends smaller document sections to the LLM and consolidates the results into a single output
- Multiple detected values can be routed to Human-in-the-Loop review when user validation is required
- Configurable retry handling for token-per-minute limits, including retry count and retry delay settings

## Engine Upgrades

- Large document processing using chunking and stitching, allowing you to process files that exceed previous size limits
- Configurable settings to control how documents are split and processed, giving you more control over performance
- Improved retry handling to reduce failures when processing limits are reached

## Integrations

- New plugin-based framework that makes connectors easier to build, update, and maintain
- New connectors available:
  - Microsoft Exchange Online
  - SharePoint Subscription Edition / Online
  - Veeva
- Connectors can now be updated independently, allowing faster delivery of new integrations and improvements

## Workflow Automation

- Integration with n8n for end-to-end workflow orchestration
- Human-in-the-Loop steps can now be added directly into workflows, allowing decisions during processing
- Workflows pause for user input and resume automatically, reducing manual intervention

## AI Accuracy and Validation

- Automatic document summaries and audit notes to help you understand and verify extraction results
- Multiple detected values are surfaced, making it easier to identify and resolve ambiguous data

## AI RAG (Hybrid Search with Citations)

- Retrieve answers from:
  - Document text, including scanned documents
  - Extracted data such as fields and tables
  - Metadata
- Responses include citations so you can see exactly where the information came from
- Supports cross-document and data-based queries, helping you answer more complex questions quickly

## Security and Privacy

- Full authorization across all REST APIs to improve security and protect access to your data

## Certifications and Platform Updates

- .NET upgraded from version 8 to version 10
- PDF viewer upgraded to improve rendering quality and reliability

## User Experience and Technical Improvements

- Improved job upload experience:
  - Submit primary files, supporting files, and metadata in one step
- Persistent grid settings to save time when navigating between pages
- New and improved model management interface for easier organization and access
- Retry jobs for faster testing and troubleshooting

## Connectors

- Microsoft Exchange Online
- SharePoint Subscription Edition / Online
- Veeva

These connectors allow you to integrate Transform more easily with common enterprise systems and document sources

Next, check out the [New Features](https://adlibsoftware.atlassian.net/wiki/spaces/T20261/pages/113934358/AWAITING+REVIEW+New+Features+2026.1) page for the 2026.1 release.