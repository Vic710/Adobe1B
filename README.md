
# Adobe Hackathon 2025 1B

## Project Overview

A cutting-edge AI-driven PDF processing solution engineered to convert intricate documents into practical insights for analysts, researchers, and strategic decision-makers. This automated pipeline streamlines the extraction, comprehension, and prioritization of PDF content, delivering a comprehensive framework for informed decision-making processes.

---

## Core Capabilities

### Document Processing Engine
Our sophisticated PDF processing system efficiently breaks down PDF files, recognizing and extracting essential components.
- **Document Structure Recognition:** Automatically detects and maintains the document's organizational framework (headers, sections, bullet points, etc.).
- **Content Navigation and Pattern Analysis:** Utilizes table of contents for document mapping and applies pattern recognition to determine structure when explicit indicators are missing.
- **Comprehensive Processing Records:** Generates detailed logs ensuring transparency and troubleshooting capabilities, documenting the entire parsing workflow and identifying irregularities.
- **Organized JSON Format:** Converts processed content into structured JSON format, ensuring seamless integration with subsequent applications.

### Advanced Embedding Technology
Converts processed text into sophisticated, context-sensitive vector representations, tailored for diverse analytical applications.
- **Contextual Vector Generation:** Creates embeddings that understand subtle meanings and interconnections within the content.
- **Role-Specific and Objective-Based Adaptation:** Enables customization of embedding approaches according to user roles (such as legal professionals, healthcare researchers) and specific analytical objectives, guaranteeing highly pertinent data representations.
- **Versatile Model Integration:** Accommodates various embedding frameworks, providing flexibility to adapt to emerging AI technologies and unique project needs.

### Intelligent Information Prioritization
Our sophisticated prioritization framework orders content according to semantic similarity and adjustable parameters.
- **Conceptual Similarity Assessment:** Organizes document segments and excerpts based on their thematic alignment with user inquiries or specified topics.
- **Enhanced Local LLM Integration:** Incorporates local Large Language Models to improve prioritization through advanced contextual analysis and reasoning capabilities.
- **Optimized Vector Retrieval:** Employs advanced vector search techniques for swift identification of pertinent information within extensive document collections.

### Targeted Content Extraction
Provides precisely focused and relevant text segments, reducing irrelevant information while maximizing content value.
- **Context-Preserving Text Selection:** Identifies and extracts the most query-relevant sentences or brief passages while maintaining their original contextual framework.
- **Balanced Content Retrieval:** Guarantees extraction of varied relevant segments, avoiding excessive concentration on singular viewpoints.
- **Priority-Based Content Selection:** Emphasizes segments containing the most essential information, directly fulfilling user requirements.

---

### Model Requirements for Docker Build

During Docker image construction, ensure the necessary model file is located in the appropriate directory:
models/

This model file is essential for proper application functionality. We utilize the **Gemma-1B.Q4_K_M.gguf** model — a 1B parameter, 4-bit quantized GGUF implementation of Google's Gemma LLM.

#### To incorporate it into your Docker image:

1. Position the GGUF model file within the `models/` directory.
2. Update your `Dockerfile` to include this line:

```dockerfile
COPY models/Gemma-1B.Q4_K_M.gguf /app/models/Gemma-1B.Q4_K_M.gguf
```


## Getting Started

Use these instructions to set up and launch the PDF Intelligence Pipeline on your system.

### System Requirements
Before proceeding, verify that you have installed:
- **Python 3.10+**: Required for executing the pipeline's primary components.
- **Docker (optional)**: Recommended for maintaining a consistent and isolated environment.

### Setup Instructions

#### Installing Python Dependencies
Use pip to install the necessary Python packages:
```bash
pip install -r requirements.txt
```
### Alternative Option

### Download the Docker image
```bash
docker pull voidisnull/asterix-adobe-1b:v3
```
#### Execute with
```bash
docker run --rm -v $(pwd)/Challenge_1b:/app/Challenge_1b voidisnull/asterix-adobe-1b:v3
```
