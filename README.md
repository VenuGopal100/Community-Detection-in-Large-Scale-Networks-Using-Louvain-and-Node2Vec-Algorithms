# Community-Detection-in-Large-Scale-Networks-Using-Louvain-and-Node2Vec-Algorithms
✅ README.md
# Community Detection in Large-Scale Networks Using Louvain and Node2Vec

This project implements and compares two approaches for **community detection** on a large-scale social network graph, specifically the **com-youtube** dataset from SNAP. Community detection helps identify groups of nodes that are densely connected within the network, useful in applications like social network analysis, recommendation systems, and graph-based clustering.

---

## 📌 Features

| Method | Description | Output |
|-------|-------------|--------|
| **Louvain Algorithm** | Classical modularity optimization-based community detection | Communities across the full graph |
| **Node2Vec + K-Means** | Learns node embeddings and clusters them in vector space | Communities on a sampled subgraph |

Both methods are evaluated and visualized using metrics such as **modularity**, **coverage**, **performance**, and **silhouette score**.

---

## 🗂 Dataset

- **Dataset Used:** `com-youtube.ungraph.txt`
- **Nodes:** ~1.1 Million  
- **Edges:** ~3 Million  
- **Source:** Stanford SNAP  
- https://snap.stanford.edu/data/com-Youtube.html

---

## 🔧 System Workflow



Graph Loading → Preprocessing (Largest Connected Component)
→ Louvain Method (Full Graph)
→ Node2Vec Embeddings → K-Means Clustering (Sampled 10k nodes)
→ Evaluation + Visualization


---

## 💻 Installation & Requirements

### **1. Clone the repository**
```bash
git clone <repository-url>
cd <project-folder>

2. Install Dependencies
pip install -r requirements.txt

Key Libraries Used

networkx

community (python-louvain)

node2vec

scikit-learn

matplotlib

numpy

gensim

▶️ Running the Project
Run the notebook
jupyter notebook CommunityDetection.ipynb


Make sure the dataset file (com-youtube.ungraph.txt) is placed in the correct path in the notebook.

📊 Results Summary
Metric	Louvain (Full Graph)	Node2Vec + KMeans (10k Sample)
Modularity	0.7186	0.9095
Coverage	0.8426	0.9956
Performance	0.9288	0.0668
Silhouette Score	N/A	0.9556
Interpretation:

Louvain finds strong natural structure in the full graph.

Node2Vec + KMeans generates highly separated clusters in embedding space, but not always strongly connected in graph structure.

Both methods succeed, but reveal different aspects of community structure.

🖼 Visualizations

Louvain graph plot (sampled)

Node2Vec t-SNE embedding visualization

K-Means cluster scatter plots

These help interpret how communities are formed and separated.

📚 References

Blondel et al. (2008) Fast Unfolding of Communities in Large Networks

Grover & Leskovec (2016) Node2Vec: Scalable Feature Learning for Networks

SNAP Dataset: https://snap.stanford.edu/data/

✨ Authors
Name	Roll Number
Sagar Rajgiri	22BCE0570
Venu Gopal	22BCE2829
Devansh Surana	22BCE0884
