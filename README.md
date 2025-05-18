**Overparameterization in Deep Learning: Satellite Image Classification**  

This project investigates the impact of overparameterization on the generalization ability of deep neural networks in the domain of satellite image classification, using the EuroSAT dataset. It explores how model complexity, optimizer choice, and pruning affect convergence, test accuracy, and model robustness.  

---

### **Project Overview**  
**Objective:**  
Evaluate how increasing model size (SmallNet, MediumNet, LargeNet) and different optimizers (SGD, RMSprop, Adam) influence generalization, convergence speed, and regularization behavior in CNN-based satellite image classification.  

**Dataset:**  
EuroSAT – 27,000 labeled RGB satellite images (10 classes), each of size 64×64.  

---

### **Key Contributions**  
- Implemented and trained three CNN architectures with increasing parameter complexity.  
- Benchmarked performance using SGD, RMSprop, and Adam optimizers.  
- Applied L1-norm pruning to quantify model redundancy and compression potential.  
- Demonstrated that overparameterized models, despite higher capacity, generalize well and exhibit implicit regularization.  
- Validated that adaptive optimizers like Adam often outperform SGD in large models under overparameterization.  

---

### **Techniques Used**  
- Deep CNN architectures with progressive complexity.  
- Optimization comparison using loss convergence curves and test accuracy metrics.  
- Filter-level L1-norm pruning for model compression.  
- Ablation studies to assess robustness and redundancy.  

---

### **Experiments**  
**Training & Evaluation:**  
- Dataset split: 70% training, 15% validation, 15% test.  

**Metrics Tracked:**  
- Cross-entropy training loss.  
- Validation and test accuracy.  
- Generalization gap.  
- Test accuracy after pruning.  

**Results Summary:**  
- LargeNet with Adam achieved the best generalization (Test Accuracy: ~81%).  
- Pruning MediumNet and LargeNet retained accuracy, demonstrating parameter redundancy.  
- Larger models converged faster and exhibited better learning stability.  

---

### **Tech Stack**  
- **Language:** Python  
- **Libraries:** PyTorch, NumPy, Matplotlib  
- **Models:** SmallNet, MediumNet, LargeNet  
- **Tools:** EuroSAT dataset, Google Colab/Jupyter  

---

### **Repository Structure**  
```  
.  
├── models/  
│   ├── smallnet.py  
│   ├── mediumnet.py  
│   └── largenet.py  
├── training/  
│   ├── train_loop.py  
│   ├── evaluate.py  
│   └── prune.py  
├── plots/  
│   └── accuracy_loss_curves.png  
├── report/  
│   └── EEE560_Group12_Project.pdf  
├── README.md  
└── requirements.txt  
```  

---  

This project provides empirical insights into the interplay between model size, optimization strategies, and generalization in satellite image classification, contributing to the broader understanding of overparameterization in deep learning.
