# Intelligent Document Processing (IDP) Application

A complete serverless application for document processing with OCR, classification, and summarization capabilities.

## Features

- **Simple Document Upload**: Drag-and-drop interface for document uploads
- **OCR Processing**: Extract key-value pairs from documents using AWS Textract
- **Document Classification**: Categorize documents into 5 predefined categories
- **AI Summarization**: Generate concise summaries using Amazon Bedrock
- **Real-time Status**: Live updates on processing progress
- **Flexible Storage**: DynamoDB with flexible schema for various document types

## Architecture

- **Frontend**: React with TypeScript
- **Backend**: AWS Lambda (Node.js 20.x)
- **Storage**: Amazon S3 + DynamoDB
- **AI Services**: AWS Textract + Amazon Bedrock (Claude Sonnet)
- **Orchestration**: AWS Step Functions
- **API**: Amazon API Gateway
- **Infrastructure**: AWS CDK

## Quick Start

### Prerequisites
- AWS CLI configured
- Node.js 18+ installed
- CDK CLI installed

### Deployment

1. **Deploy Infrastructure**:
   ```bash
   cd cdk-app
   npm install
   npm run build
   npx cdk deploy
   ```

2. **Start Frontend**:
   ```bash
   cd frontend
   npm install
   npm start
   ```

3. **Test Application**:
   - Open http://localhost:3000
   - Upload the sample VitaminTabs.jpeg file
   - Watch real-time processing results

## API Endpoints

- `POST /upload` - Get presigned URL for document upload
- `GET /status/{documentId}` - Get processing status and results

## Document Categories

- Dietary Supplement
- Stationery
- Kitchen Supplies
- Medicine
- Other

## Sample Results

The application successfully processes the sample vitamin supplement image:

**OCR Results**:
- Extracted key-value pairs from product label
- Identified dosage, quantity, and features

**Classification**: Dietary Supplement

**Summary**: Detailed product information including dosage, quantity, flavor, and dietary features

## Project Structure

```
├── specs/                 # Requirements and design documents
├── generated-diagrams/    # Architecture diagrams
├── cdk-app/              # AWS CDK infrastructure code
├── frontend/             # React application
└── validate-application.js # Validation script
```

## Technology Stack

- **AWS Services**: Lambda, S3, DynamoDB, Textract, Bedrock, Step Functions, API Gateway
- **Frontend**: React, TypeScript, CSS
- **Infrastructure**: AWS CDK with TypeScript
- **AI Models**: Claude Sonnet 4 via Amazon Bedrock

## Development

This project follows specification-driven development with:
- Detailed requirements in EARS notation
- Technical architecture documentation
- 18 discrete implementation tasks
- End-to-end integration testing

## License

MIT License