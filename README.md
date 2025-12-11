# Visual Search with Cohere Embed v4 in Microsoft Foundry

Welcome to **visual search with cohere embed 4 **!  

This project enables advanced image search capabilities powered by [Cohere's Embed v4]. It provides a simple, scalable system for indexing and retrieving images using multimodal AI embeddings, making it easy to find similar or relevant images in large datasets.

## ⭐ What makes Embed 4 stand out?

- **100+ Language Support**: This model is truly global – it supports well over 100 languages for text embeddings. You can encode queries and documents in many languages (Arabic, Chinese, French, Hindi, etc.) into the same vector space, enabling cross-lingual search out of the box. For example, a question in Spanish can retrieve a relevant document originally in English if their ideas align semantically.
- **Multi-Modal Embeddings**: Embed 4 is capable of embedding not only text but also images. This means you can use it for multimodal search scenarios – e.g. indexing both textual content and images and allowing queries across them. Under the hood, the model has an image encoder; the Azure AI Foundry SDK provides an ImageEmbeddingsClient to generate embeddings from images. With this, you could embed a diagram or a screenshot and find text documents that are semantically related to that image’s content.
- **Matryoshka Embeddings (Scalable Dimensions)**: A novel feature in Cohere’s Embed 4 is Matryoshka Representation Learning, which produces embeddings that can be truncated to smaller sizes with minimal loss in fidelity. In practice, the model can output a high-dimensional vector (e.g. 768 or 1024 dims) but you have the flexibility to use just the first 64, 128, 256, etc. dimensions if needed. These “nested” embeddings mean you can choose a vector size that balances accuracy vs. storage/query speed – smaller vectors save memory and compute while still preserving most of the semantic signal. This is great for enterprise deployments where vector database size and latency are critical.
- **Enterprise Optimizations**: Cohere has optimized Embed 4 for production use. It supports int8 quantization and binary embedding output natively, which can drastically reduce storage footprint and speed up similarity search with only minor impact on accuracy (useful for very large indexes). The model is also trained on massive datasets (including domain-specific data) to ensure robust performance on noisy enterprise text. It achieves state-of-the-art results on benchmark evaluations like MTEB, meaning you get retrieval quality on par with or better than other leading embeddings models (OpenAI, Google, etc.). For instance, Cohere’s previous embed model was top-tier on cross-language retrieval tasks and Embed4 further improves on that foundation.

## 🚀 Features

- **Image Embedding:** Generate and store vector representations for your images using Cohere’s latest multimodal Embed v4 model.
- **Visual Search:** Perform similarity search to find images most similar to a query (either by example image or text description).
- **Multimodal Queries:** Search with images, text, or mixed-input queries.
- **Efficient Indexing:** Utilizes vector databases (e.g., FAISS, Pinecone) for scalable and fast retrieval.
- **Easy Integration:** RESTful API and Python interfaces for seamless use in your apps or data workflows.

## 🖼️ Example Use Cases

- Reverse image search in digital asset management systems
- Content-based recommendation (find "images like this")
- Searching with descriptive text: "Show me all images of beaches at sunset"
- Visual deduplication or near-duplicate detection

## 📚 Documentation
- https://techcommunity.microsoft.com/blog/azure-ai-foundry-blog/unlock-multi-modal-embed-4-and-multilingual-agentic-rag-with-command-a-on-azure/4404458
- https://ai.azure.com/explore/models/embed-v-4-0/version/1/registry/azureml-cohere?tid=16b3c013-d300-468d-ac64-7eda0820b6d3

## 👤 Author

**Serge Retkowsky**
| Platform | Link |
|----------|------|
| GitHub | https://github.com/retkowsky |
| LinkedIn | https://www.linkedin.com/in/serger/ |
| YouTube | https://www.youtube.com/@serge1840/videos |
| Medium | https://medium.com/@sergems18 |
| Role | AI & APPS Global Black Belt @ Microsoft France | |

**Last Updated**: 11-December-2025

For questions, issues, or feedback, please open an issue in this repository or contact through the channels above.
