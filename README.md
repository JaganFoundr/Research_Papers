# 📖 Research Papers I've Read 🧠

This repository showcases a collection of research papers I’ve explored and reviewed. Below is a summary of the most recent paper I’ve read.

---

## 1️⃣ [Automatic differentiation in PyTorch](https://openreview.net/forum?id=BJJsrmfCZ)  
**Authors**: Adam Paszke, Sam Gross, Soumith Chintala, Gregory Chanan, Edward Yang, Zachary DeVito, Zeming Lin, Alban Desmaison, Luca Antiga, Adam Lerer

### 📝 Summary
- **Automatic Differentiation**: PyTorch enables efficient gradient computation for machine learning models.
- **Built on Prior Work**: Based on projects like Lua Torch, Chainer, and HIPS Autograd.
- **Supports CPU & GPU**: Runs models on both CPU and GPU for flexibility.
- **Imperative Programming**: Focuses on differentiating imperative programs, not symbolic ones.
- **Extensibility & Low Overhead**: Designed for easy expansion with minimal performance costs.
  
---

## 2️⃣ [U-Net: Convolutional Networks for Biomedical Image Segmentation](http://lmb.informatik.uni-freiburg.de/people/ronneber/u-net)  
**Authors**: Olaf Ronneberger, Philipp Fischer, Thomas Brox  
**Affiliation**: University of Freiburg, Germany  

### 📝 Summary  
- **Problem Addressed**: Effective segmentation of biomedical images using limited annotated training data.  
- **Key Innovation**:  
  - Proposed the **U-Net architecture**, which combines a contracting path (encoder) for context capture and an expanding path (decoder) for precise localization.  
  - Relies heavily on **data augmentation** to maximize training efficiency with small datasets.  

- **Performance**:  
  - Achieved **state-of-the-art results** in biomedical image segmentation, outperforming the sliding-window convolutional network approach.  
  - Won the **2015 ISBI cell tracking challenge** across multiple microscopy image categories.  

- **Speed**: Capable of segmenting a 512x512 image in **less than a second** using a modern GPU.  

- **Availability**: The **Caffe-based implementation** and trained networks are open-sourced, facilitating adoption by the research community.  

---

### 🌟 Key Takeaways  
- U-Net’s design proved highly effective for tasks requiring precise localization, especially in domains with small datasets.  
- Its symmetric encoder-decoder structure, combined with skip connections, ensures high performance in biomedical segmentation tasks.  
- The paper exemplifies the power of architectural innovations in overcoming dataset limitations.  

---

## 3️⃣ **[An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale](https://arxiv.org/abs/2010.11929)**  
**Authors**: Alexey Dosovitskiy, Lucas Beyer, Alexander Kolesnikov, Dirk Weissenborn, Xiaohua Zhai, Thomas Unterthiner, Mostafa Dehghani, Matthias Minderer, Georg Heigold, Sylvain Gelly, Jakob Uszkoreit, Neil Houlsby  

📝 **Summary**  
**Transformers in Vision**: This work demonstrates the power of pure transformer models applied to image recognition tasks, moving away from convolutional neural networks (CNNs) as the core architecture. By using transformers to process sequences of image patches, the model performs exceptionally well on multiple image recognition benchmarks, including **ImageNet, CIFAR-100, and VTAB**.  

## 4️⃣ **[Better Plain ViT Baselines for ImageNet-1k](https://arxiv.org/abs/2205.01580)**  
**Authors**: Lucas Beyer, Xiaohua Zhai, Alexander Kolesnikov  

📝 **Summary**  
**Vision Transformer (ViT) Training**: This paper challenges the prevailing notion that the Vision Transformer requires advanced regularization techniques to perform well on large datasets like ImageNet-1k. The authors demonstrate that **standard data augmentation** is sufficient to achieve impressive results. By making **minor modifications** to the original ViT training process, they improve the performance of **plain ViT** models significantly.

🔑 **Key Insights**:  
- **Simple Yet Effective**: Contrary to common belief, ViT performs exceptionally well with **minimal modifications**, relying only on **standard data augmentation** for training.
- **Performance Boost**: With just **90 epochs**, ViT achieves **76% top-1 accuracy** in under 7 hours on a TPUv3-8, outperforming classic ResNet50 baselines. With **300 epochs**, the model reaches **80% accuracy** in less than one day of training.
- **Training Efficiency**: This study demonstrates that with the right approach, ViT can be trained efficiently and still surpass the performance of more complex models.  
- **Beyond CNNs**: Unlike previous approaches, this method eliminates the need for CNNs and uses transformers directly for image classification.  
- **Superior Results**: Vision Transformers (ViT) achieve **state-of-the-art performance**, surpassing CNN-based models in many benchmarks.  
- **Efficiency**: Requires significantly **fewer computational resources** to train compared to traditional CNN-based methods.  
- **Transfer Learning**: Pre-trained ViT models, fine-tuned on smaller datasets, yield **excellent performance** across multiple benchmarks.

## 5️⃣ **End to End Learning for Self-Driving Cars**  
**Authors**: Mariusz Bojarski, Davide Del Testa, Daniel Dworakowski, Bernhard Firner, Beat Flepp, Prasoon Goyal, Lawrence D. Jackel, Mathew Monfort, Urs Muller, Jiakai Zhang, Xin Zhang, Jake Zhao, Karol Zieba  

📝 **Summary**  
**End-to-End Self-Driving System**: This groundbreaking research presents a **convolutional neural network (CNN)** that maps raw pixels from a **single front-facing camera** directly to **steering commands**. By utilizing **minimal training data** (only human steering angle), the system learns to drive efficiently on both **local roads** and **highways**, handling challenging environments like **parking lots** and **unpaved roads**.  

🔑 **Key Insights**:  
- **End-to-End Training**: The system doesn’t require explicit training for individual components like lane detection or path planning. It learns to drive by directly mapping camera input to steering commands, optimizing all processes at once.  
- **Efficient Performance**: The system can drive autonomously at **30 frames per second (FPS)**, operating with minimal human intervention.  
- **Learning Internal Representations**: The CNN automatically learns features like road outlines and lane boundaries without being explicitly trained for them.  
- **Optimized System**: The end-to-end approach allows the model to self-optimize, providing better performance and smaller systems compared to traditional decomposed methods.  
- **Reduced Complexity**: The model doesn't rely on multiple stages like lane detection or path planning. Instead, it learns to perform everything in one go, leading to a more compact solution.

🔧 **Technical Details**:  
- **Training Hardware**: The model was trained on an **NVIDIA DevBox** using **Torch 7**, and the self-driving car system used an **NVIDIA DRIVE PX** computer for operation.  
- **Frame Rate**: The system operates in real-time at **30 FPS**, showcasing its high efficiency and effectiveness.  
