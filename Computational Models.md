## Layout detection using VLMs

### OCR Time Machine

For decades, galleries, libraries, archives, and museums (GLAMs) have used Optical Character Recognition to transform digitized books, newspapers, and manuscripts into machine-readable text. Traditional OCR produces complex XML formats like ALTO, packed with layout details but difficult to use. Now, Vision-Language Models (VLMs) are revolutionizing OCR with simpler, cleaner output. This Space lets you compare four leading VLM-based OCR models against traditional approaches. Upload a historical document image and its XML file to see them side-by-side. We'll extract the reading order from your XML for an apples-to-apples comparison of the actual text content.

https://huggingface.co/spaces/davanstrien/ocr-time-machine

Use [[#RolmOCR]], [[#Nanonets-OCR]], [[#olmOCR]], [[#OCRFlux]]

### dots.ocr

**dots.ocr** is a powerful, multilingual document parser that unifies layout detection and content recognition within a single vision-language model while maintaining good reading order. Despite its compact 1.7B-parameter LLM foundation, it achieves state-of-the-art(SOTA) performance.

https://huggingface.co/rednote-hilab/dots.ocr

### RolmOCR

Earlier this year, the [Allen Institute for AI](https://allenai.org/) released olmOCR, an open-source tool that performs document OCR using the Qwen2-VL-7B vision language model (VLM). We were excited to see a high-quality, openly available approach to parsing PDFs and other complex documents — and curious to explore what else might be possible using newer foundation models and some lightweight optimizations.

The result is **RolmOCR**, a drop-in alternative to [[#olmOCR]] that’s faster, uses less memory, and still performs well on a variety of document types. We're releasing it under **Apache 2.0** for anyone to try out, explore, or build on.

https://huggingface.co/reducto/RolmOCR

### Nanonets-OCR

Nanonets-OCR-s by [Nanonets](https://nanonets.com/) is a powerful, state-of-the-art image-to-markdown OCR model that goes far beyond traditional text extraction. It transforms documents into structured markdown with intelligent content recognition and semantic tagging, making it ideal for downstream processing by Large Language Models (LLMs).

https://huggingface.co/nanonets/Nanonets-OCR-s

### olmOCR

A toolkit for converting PDFs and other image-based document formats into clean, readable, plain text format.

https://huggingface.co/allenai/olmOCR-7B-0225-preview

https://github.com/allenai/olmocr
demo: https://olmocr.allenai.org/

### OCRFlux

OCRFlux is a multimodal large language model based toolkit for converting PDFs and images into clean, readable, plain Markdown text. It aims to push the current state-of-the-art to a significantly higher level.
https://huggingface.co/ChatDOC/OCRFlux-3B

### UV Scripts

Run state-of-the-art ML workflows with a single command. From OCR to classification, all scripts work instantly with `uv run`.

## Structured information extraction

### Mistral OCR

notebooks to support developers automating document processing tasks with new OCR and annotation capabilities by mistral. The notebooks cover (1) Data extraction via annotations (2) Document Q&A with built-in OCR

https://github.com/mistralai/cookbook/tree/main/mistral/ocr

### NuExtract 2.0 2B

NuExtract 2.0 is a family of models trained specifically for structured information extraction tasks. It supports both multimodal inputs and is multilingual.

https://huggingface.co/numind/NuExtract-2.0-2B

### NuMarkdown-8B-Thinking

**NuMarkdown-8B-Thinking** is the first reasoning OCR VLM. It is specifically trained to convert documents into clean Markdown files, well suited for RAG applications. It generates thinking tokens to figure out the layout of the document before generating the Markdown file. It is particularly good at understanding documents with weird layouts and complex **tables**. The number of thinking tokens can vary from 20% to 500% of the final answer, depending on the task difficulty. **NuMarkdown-8B-Thinking** is a fine-tune of **Qwen 2.5-VL-7B** on synthetic Doc → Reasoning → Markdown examples, followed by an RL phase (GRPO) with a layout-centric reward.

https://huggingface.co/numind/NuMarkdown-8B-Thinking

## Entity Extraction

### LangExtract

LangExtract is a Python library that uses LLMs to extract structured information from unstructured text documents based on user-defined instructions. It processes materials such as clinical notes or reports, identifying and organizing key details while ensuring the extracted data corresponds to the source text.

https://github.com/google/langextract?tab=readme-ov-file#introduction

### Relik

A blazing fast and lightweight Information Extraction model for **Entity Linking** and **Relation Extraction**.

https://huggingface.co/sapienzanlp/relik-entity-linking-large

### Gliner

GLiNER is a Named Entity Recognition (NER) model capable of identifying any entity type using a bidirectional transformer encoder (BERT-like). It provides a practical alternative to traditional NER models, which are limited to predefined entities, and Large Language Models (LLMs) that, despite their flexibility, are costly and large for resource-constrained scenarios.

*update [[2025-08-15]] gliner-decoder-base-v1.0*: GLiNER is a Named Entity Recognition (NER) model capable of identifying _any_ entity type in a **zero-shot** manner. This architecture combines:

- An **encoder** for representing entity spans
- A **decoder** for generating label names

This hybrid approach enables new use cases such as **entity linking** and expands GLiNER’s capabilities. By integrating large modern decoders—trained on vast datasets—GLiNER can leverage their **richer knowledge capacity** while maintaining competitive inference speed.

https://github.com/urchade/GLiNER
https://huggingface.co/knowledgator/gliner-decoder-base-v1.0
