# Gearbox Fault Diagnosis: Multimodal Innovative Model Based on MTF+Swin-Informer

Preface\tThis issue is based on the gearbox fault dataset from Southeast University, proposing an innovative multimodal fault diagnosis model that combines Markov Transition Field (MTF) with a multimodal approach integrating SwinTransformer and Informer. This model innovatively addresses the challenges of information expression and feature mining in gearbox fault signal diagnosis, achieving efficient, accurate, and robust fault diagnosis performance. This method provides a fresh perspective for multimodal integration in mechanical fault diagnosis, expanding the boundaries of deep learning applications in industrial intelligent maintenance.
●Dataset: Gearbox Fault Dataset from Southeast University●Environmental Framework: Python 3.11, PyTorch 2.1 or above are required to run●Accuracy: Test set achieves 99% accuracy●Target Audience: Beginners, those requiring papers, or those pursuing graduation projects●Code Guarantees: Code is detailed with comments for immediate compatibility.
1 Multimodal Innovation Model Overview
\t1.1 Model Overview
The model first converts a one-dimensional fault signal sequence into time-frequency images using MTF, capturing the probability transfer features of the signal's temporal sequence mapping. Subsequently, it employs the hierarchical window attention mechanism of Swin Transformer to efficiently extract spatial features from the time-frequency images, enhancing understanding of the time-frequency structure. At the same time, the original one-dimensional fault signal sequence is input into the Informer model to learn its long sequence temporal dependence features. Finally, through a feature fusion mechanism, the spatial information of the time-frequency images is effectively integrated with the time-domain information of the one-dimensional signals, achieving precise classification of gearbox fault categories. Experimental results show that this multimodal fusion model outperforms traditional single-modal methods in both accuracy and robustness, demonstrating excellent fault recognition performance and application potential.
\t1.2 \tModel Details and Innovation Points\tMultimodal Data Representation
 (1)MTF Time-frequency Image Conversion
The paper adopts the Markov Transition Field (MTF) method to map a one-dimensional vibration signal sequence into a two-dimensional time-frequency image. The image is constructed using the state transition probability of signal amplitude, thereby expressing the dynamic temporal dependency characteristics of the signal in the image space. Compared with traditional spectral methods, MTF better preserves the temporal information, which is beneficial for subsequent deep learning models.

(2) Time-domain raw signal sequence
Parallel retention of the original one-dimensional vibration signal is used to capture low-dimensional and direct time series information, avoiding information loss that may occur from pure image transformation.

Feature Extraction Network Architecture
(1) Swin Transformer for Spatial Features
Swin Transformer learns the local and global spatial dependencies of the time-frequency images through introducing hierarchical sliding window multi-head self-attention mechanisms, effectively solving the issues of limited receptive field and insufficient global dependency modeling in traditional convolutional networks, enhancing the accuracy and generalization capability of time-frequency feature expression.

(2) Informer Model for Long-term Sequence Features
Informer utilizes sparse self-attention mechanisms and efficient long-term dependency capturing capabilities to model the time series characteristics of one-dimensional fault signals. It is particularly suitable for mining the long-term dependency relationships of fault signals, enhancing the feature capture effect on the dynamic changes over time.

Multimodality Feature Fusion Strategies
The spatial features extracted by Swin Transformer are effectively combined with the time-domain features extracted by Informer. The fusion strategy fully utilizes the complementary information of the two modalities to form rich and discriminative feature representations, significantly improving the accuracy and stability of fault diagnosis.

Advantages and Innovations
1. Innovative multimodal fusion framework, which for the first time combines MTF+Swin Transformer with the Informer architecture for gearbox fault diagnosis, fully leverages the complementary advantages of time-frequency space information and long-term sequence information.
2. The introduction of window attention mechanism in Swin Transformer enables more efficient and hierarchical spatial feature extraction in time-frequency images, breaking through the bottleneck of traditional CNNs and conventional Transformers in feature extraction.
3. Based on the long-term temporal modeling capability of Informer, it can more accurately capture the periodicity and trend changes in vibration signals, making it particularly effective for recognizing the evolution process of faults.
4. Comprehensive experimental validation shows that this model performs excellently in identifying faults on the Southeast University gearbox dataset, significantly outperforming single modality and traditional deep learning methods, demonstrating strong practical engineering application value.
2 Data preprocessing for Southeast University dataset
2.1 Import data
The Southeast University gearbox dataset includes two subdatasets: bearing and gear, both collected from a transmission system dynamics simulator. The gear fault dataset consists of two working conditions, namely 20Hz-0 (speed - load) and 30Hz-2V. The gear fault data collected includes five types of gear operating states, including healthy, peeling, broken tooth, crack, and wear:
2.2 Data preprocessing
By creating datasets using sliding windows and uniformly dividing the training set, validation set, and test set into 7:2:1 ratios, the data is finally saved. This paper adopts the Markov transition field MTF as the method for time-frequency image transformation, generating the following time-frequency images:
3 Fault Diagnosis Model based on MTF+Swin-Informer
3.1 Define network model, set parameters, train the model
\t50 epochs, accuracy 99%, MTF+Swin-Informer network significantly improves classification performance. It can extract important features from fault signal characteristics, resulting in significant improvements!\tApplication demonstrates significant advantages:
(1) Cross-modal Collaborative Fusion: Distinguished from traditional fault diagnosis reliance on singular data representation, this model employs MTF transformation to spatialize time-series signals. Combined with the original time-domain signals, it ensures the retention of key features and multi-perspective perception, thereby maximizing information utilization.
(2) Introduction of a new Transformer architecture: Swin Transformer and Informer are efficient variants of the Transformer family, capable of modeling long-distance dependencies in data of different dimensions, reflecting the latest technological advantages of deep learning.
(3) Efficiency in industrial practices: Sliding window attention and sparse attention significantly reduce model complexity, balancing performance with computational requirements, facilitating deployment and application in practical industrial environments.
3.2 Model Evaluation
(1) Accuracy, Precision, Recall, F1 Score
\t  
(2) Fault 5 Classification Confusion Matrix:
\t  
(3) Classification Label Visualization
\t  
(4) Original Data t-SNE Feature Visualization
(5) t-SNE feature visualization after model training:
\t  
Click to download: Complete original data, Python code
END  
2. Friends who enjoy the content can follow, give the article a "like", share on social media or discuss in groups.
Previously Featured Content:
Rapid Document | Parallel Fault Diagnosis Model Based on 2D-SWinTransformer+1D-CNN-SENet
Significant update on bearing life prediction! New ensemble of CNN-BiGRU-Attention models + enriched visualization charts
Multimodal - Fault Diagnosis | The Big Core Convolution Opens a New Era in Vision!
Superior! Directly write in Zone One! Based on SSA+Informer-SENet Fault Diagnosis Model
Multi-source Information Fusion: Data layer fusion + feature layer fusion fault diagnosis model!

## Images

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
