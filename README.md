# Energy-Based Deep Incomplete Multi-View Clustering

**Ziyu Wang, Yiming Du, Rui Ning, and Lusi Li**

📄 **Published in [ACM Multimedia 2025 (ACM MM 2025)](https://dl.acm.org/doi/abs/10.1145/3746027.3755365)**

🔗 **[Paper](https://dl.acm.org/doi/abs/10.1145/3746027.3755365)** | **[Code](./)**

---

## 📖 Overview

This repository provides the implementation of **Energy-Based Deep Incomplete Multi-View Clustering**, a deep learning framework designed to address missing data challenges in incomplete multi-view clustering (IMVC).

The proposed approach integrates **energy-based feature imputation**, **multi-head attention**, and **energy-enhanced contrastive learning** to recover missing information, adaptively fuse complementary representations across views, and improve clustering performance.
---
## 🏗️ Framework

![Energy-Based Deep Incomplete Multi-View Clustering Framework](./framework.png)

*Overview of the proposed energy-based deep incomplete multi-view clustering framework.*

## ✨ Key Features

- **Energy-Based Feature Imputation:** Employs energy networks to guide the recovery of missing features and improve representation completeness.
- **Multi-Head Attention Fusion:** Adaptively integrates complementary information from multiple views to learn unified representations.
- **Energy-Enhanced Contrastive Learning:** Leverages energy-based modeling to strengthen representation learning and improve clustering discrimination.
- **Robust Missing-Data Handling:** Supports clustering under varying missing-view ratios.
- **Multi-Dataset Support:** Supports standard benchmark datasets for incomplete multi-view clustering.

## ⚙️ Requirements

The implementation uses Python and deep learning libraries.

Install the dependencies specified by the repository's environment configuration or requirements file, if provided.

## 🚀 Usage

### 1. Training

Run the following command to train the model on the `hand` dataset using the provided hyperparameter configuration:

```bash
python main.py \
  --dataset=hand \
  --num_heads=4 \
  --learning_rate=0.0017593568650436865 \
  --feature_dim=78 \
  --hidden_dim=222 \
  --dropout=0.49682483698160845 \
  --imputation_loss_weight=0.32522256029396907 \
  --cd_loss_weight=0.43347421118964125 \
  --temperature=0.102535900329493 \
  --energy_scale=0.5208286552126832 \
  --n_steps=82 \
  --step_size=0.24984322766526668 \
  --noise_scale=0.026739520521612797 \
  --margin=0.6929653526198027
```

The configuration above provides the hyperparameter settings for the `hand` dataset. Adjust the parameters as needed for other datasets.

### 2. Evaluation Only

To evaluate a previously trained model using a saved checkpoint:

```bash
python main.py --dataset=hand --load_checkpoint
```

Ensure that the corresponding model checkpoint is available at the location expected by the implementation.

## 🔧 Key Parameters

| Parameter | Description |
|---|---|
| `--dataset` | Name of the dataset |
| `--num_heads` | Number of attention heads |
| `--learning_rate` | Learning rate for model optimization |
| `--feature_dim` | Feature representation dimension |
| `--hidden_dim` | Hidden layer dimension |
| `--dropout` | Dropout probability |
| `--imputation_loss_weight` | Weight for the feature imputation loss |
| `--cd_loss_weight` | Weight for the contrastive divergence loss |
| `--temperature` | Temperature parameter for contrastive learning |
| `--energy_scale` | Scaling factor for the energy function |
| `--n_steps` | Number of iterative sampling or refinement steps |
| `--step_size` | Step size for iterative updates |
| `--noise_scale` | Noise magnitude during sampling or refinement |
| `--margin` | Margin parameter used in the learning objective |
| `--load_checkpoint` | Load a saved model checkpoint for evaluation |

## 📚 Citation

If you find this repository useful in your research, please consider citing our paper:

**Ziyu Wang, Yiming Du, Rui Ning, and Lusi Li.**  
"Energy-Based Deep Incomplete Multi-View Clustering."  
*Proceedings of the 33rd ACM International Conference on Multimedia (ACM MM)*, pp. 1686–1694, 2025.

```bibtex
@inproceedings{wang2025energy,
  title={Energy-based deep incomplete multi-view clustering},
  author={Wang, Ziyu and Du, Yiming and Ning, Rui and Li, Lusi},
  booktitle={Proceedings of the 33rd ACM International Conference on Multimedia},
  pages={1686--1694},
  year={2025}
}
```

## 📬 Contact

For questions regarding the implementation, experimental results, or research collaboration, please open an issue in this repository or contact the authors.
