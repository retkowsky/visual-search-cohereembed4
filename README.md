# Visual Search with Cohere Embed v4

Welcome to **visual-search-cohereembed4**!  
This project enables advanced image search capabilities powered by [Cohere's Embed v4](https://docs.cohere.com/docs/embed). It provides a simple, scalable system for indexing and retrieving images using multimodal AI embeddings, making it easy to find similar or relevant images in large datasets.

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

## 🛠️ Installation

```bash
git clone https://github.com/retkowsky/visual-search-cohereembed4.git
cd visual-search-cohereembed4
pip install -r requirements.txt
```

## 🌟 Quick Start

1. **Obtain a Cohere API Key:**  
   Sign up and get your API key from [Cohere Console](https://dashboard.cohere.com/api-keys).

2. **Configure Your Environment:**

```bash
export COHERE_API_KEY=your_api_key_here
```

3. **Index Images:**

```python
from app import index_images

index_images('/path/to/your/image/folder')
```

4. **Perform a Visual Search:**

```python
from app import search_images

results = search_images(query_image='/path/to/query.jpg', top_k=5)
print("Most similar images:", results)
```

## 📝 API Reference

### Indexing Images

```python
index_images(image_folder: str)
```

Indexes all valid images in the folder.

### Searching Images

```python
search_images(query_image: str = None, query_text: str = None, top_k: int = 5)
```

Returns a list of most similar images to your query image or text.

## ⚡ Tech Stack

- Python 3.9+
- [Cohere Embed v4 API](https://docs.cohere.com/docs/embed)
- Vector DB: FAISS (local) or Pinecone (cloud, optional)
- FastAPI (if running as an API service)

## 📁 Repository Structure

```
/visual-search-cohereembed4
├── app.py                  # Main application logic
├── requirements.txt
├── utils/
│   └── ...                 # Image and embedding utilities
├── data/
│   └── ...                 # Indexes and sample images
└── README.md
```

## 📢 Contributing

We welcome contributions!  
Please open issues or submit pull requests for improvements, bug fixes, or new features.

## 📝 License

MIT License © 2025 [retkowsky](https://github.com/retkowsky)

---

**Note:**  
This project is not affiliated with Cohere. Usage of the Cohere API is subject to [their terms](https://cohere.com/terms-of-use).
