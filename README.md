Here is a detailed **README.md** structure for your GitHub profile, strictly based on the technical details, methodology, and results provided in your uploaded project report.

You can copy and paste the Markdown below directly into your repository.

---

# CAPRI-NAS: Carbon-Aware Parameter-Reusing Neural Architecture Search for GNNs

**CAPRI-NAS** (Carbon-Aware Parameter-Reusing Intelligent Neural Architecture Search) is a novel framework that fundamentally redefines Graph Neural Network (GNN) architecture discovery by integrating environmental sustainability directly with performance optimization.

Addressing the "Red AI" problem of unsustainable computational costs, this framework utilizes evolutionary algorithms to discover architectures that are not only competitive with state-of-the-art baselines but also significantly more carbon-efficient.

## 🚀 Key Innovations

CAPRI-NAS introduces three pillars of sustainable architecture search:

* **♻️ Sophisticated Parameter Inheritance:** A novel weight transfer system that analyzes layer compatibility (matching signatures, dimensions, and operations) between parent and child architectures. By copying trained weights rather than initializing randomly, this mechanism accelerates convergence by 60-80%.


* **⚖️ Multi-Objective Carbon-Aware Fitness:** Unlike traditional NAS that optimizes solely for accuracy, our fitness function balances three competing objectives: Validation Accuracy, Carbon Footprint (via CodeCarbon), and Parameter Reuse Score.


* **🧬 Adaptive Evolutionary Search:** An efficient evolutionary engine employing tournament selection, elitism, and early termination of underperforming candidates to minimize wasted computation.



## 📊 Performance Highlights

Evaluated across **9 diverse graph datasets**, CAPRI-NAS demonstrated that Green AI does not require sacrificing performance.

Metric	                                  Result
Win Rate	            Outperformed or matched baselines on 77.8% of datasets.

Carbon Efficiency	   Achieved an average 1.44x reduction in CO₂ emissions vs. complex baselines.

Search Speed	        Complete architecture search per dataset in 30-45 minutes (Total <6 hours for all 9 datasets).

Top Result	          1.92x carbon reduction on Amazon-Computers with 91.38% accuracy (vs. 89.10% baseline).

Specialization	      31.6% accuracy gain on ENZYMES dataset compared to GIN baseline.

 
## 🛠️ System Architecture

The CAPRI-NAS pipeline operates through a modular evolutionary loop:

1. **Search Space Definition**: Explores combinations of GCN, GAT, and GraphSAGE layers with varying activations (ReLU, GELU, etc.), normalization (BatchNorm, LayerNorm), and pooling strategies.


2. **Initialization**: Starts with a population of 20 random architectures.


3. **Evolutionary Cycle**:

    (i) **Selection**: Tournament-based parent selection.

   (ii) **Mutation**: Applies stochastic changes (e.g., layer substitution, dimension modification).

   (iii) **Inheritance**: Transfers weights from parents to compatible layers in child models.


4. **Carbon Tracking**: Real-time emission tracking for every candidate evaluation using **CodeCarbon**.


### Fitness Function

The core optimization logic is defined by:

Validation Accuracy (). Normalized Carbon Emissions (), Parameter Reuse Score ().



## 📂 Datasets

The framework was validated on three critical application domains:

* **Academic Citation Networks**: Cora, CiteSeer, PubMed.


* **E-Commerce Product Networks**: Amazon-Photo, Amazon-Computers.


* **Bio-Molecular Graphs**: MUTAG, PROTEINS, ENZYMES, NCI1.



## 💻 Tech Stack

* **Language**: Python
* **Deep Learning**: PyTorch, PyTorch Geometric (implied context)
* 
**Sustainability Tracking**: [CodeCarbon](https://codecarbon.io/) 


* **Architecture**: Custom Evolutionary Algorithm

---
