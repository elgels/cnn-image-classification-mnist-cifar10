<h1>CNN Image Classification — MNIST → CIFAR-10</h1>

<h2>Project Overview</h2>
<p>
This project applies <strong>Convolutional Neural Networks (CNNs)</strong> to image classification tasks of increasing complexity using the <strong>MNIST</strong> and <strong>CIFAR-10</strong> datasets.
</p>

<p>
The goal is to show how model performance and classification challenges evolve when moving from a simple dataset such as MNIST to a more complex dataset such as CIFAR-10, and to evaluate results through accuracy metrics, a confusion matrix, and error analysis.
</p>

<h2>Datasets</h2>

<h3>MNIST (Baseline)</h3>
<ul>
  <li>Grayscale images of handwritten digits (0–9)</li>
  <li>Image size: 28 × 28</li>
  <li>Low-complexity dataset with well-separated classes</li>
</ul>

<h3>CIFAR-10</h3>
<ul>
  <li>Color images across 10 classes: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, and truck</li>
  <li>Image size: 32 × 32</li>
  <li>Higher-complexity dataset with overlapping visual features across classes</li>
</ul>

<h2>Model Architecture</h2>
<p>
The project uses a <strong>Convolutional Neural Network (CNN)</strong> for image classification. The architecture includes:
</p>

<ul>
  <li>Convolutional layers for feature extraction</li>
  <li>Activation functions such as ReLU</li>
  <li>Pooling layers for dimensionality reduction</li>
  <li>Fully connected layers for final classification</li>
</ul>

<p>
This architecture enables the model to learn hierarchical image features, from simple edges and shapes to more complex visual patterns.
</p>

<h2>Methods</h2>
<ul>
  <li>Data preprocessing and normalization</li>
  <li>CNN model training and validation</li>
  <li>Performance evaluation using accuracy</li>
  <li>Confusion matrix analysis for class-level performance</li>
  <li>Error analysis to identify common misclassifications</li>
</ul>

<h2>Results</h2>

<h3>MNIST</h3>
<ul>
  <li>High classification accuracy</li>
  <li>Minimal misclassification across classes</li>
  <li>Serves as a baseline for comparison</li>
</ul>

<h3>CIFAR-10</h3>
<ul>
  <li>Lower accuracy than MNIST due to higher dataset complexity</li>
  <li>Greater difficulty distinguishing visually similar classes</li>
  <li>Performance affected by low image resolution and class overlap</li>
</ul>

<h2>Confusion Matrix Insights</h2>
<p>
To interpret the confusion matrix, the CIFAR-10 class labels are encoded as:
0 (airplane), 1 (automobile), 2 (bird), 3 (cat), 4 (deer), 5 (dog), 6 (frog), 7 (horse), 8 (ship), and 9 (truck).
</p>

<ul>
  <li>The strongest misclassification occurs between <strong>cats and dogs</strong>, which is reasonable given their similar visual features.</li>
  <li>The model also struggles with the <strong>bird</strong> class, confusing it with classes such as airplane and deer.</li>
  <li>These results suggest that low-resolution images make it harder for the CNN to capture subtle textures and shapes.</li>
</ul>

<h2>MNIST vs CIFAR-10 Comparison</h2>

<table>
  <tr>
    <th>Aspect</th>
    <th>MNIST</th>
    <th>CIFAR-10</th>
  </tr>
  <tr>
    <td>Complexity</td>
    <td>Low</td>
    <td>High</td>
  </tr>
  <tr>
    <td>Image Type</td>
    <td>Grayscale digits</td>
    <td>Color object images</td>
  </tr>
  <tr>
    <td>Difficulty</td>
    <td>Relatively easy</td>
    <td>More challenging</td>
  </tr>
  <tr>
    <td>Main Challenge</td>
    <td>Minimal class overlap</td>
    <td>Low resolution and similar classes</td>
  </tr>
</table>

<h2>Future Improvements</h2>
<ul>
  <li>Refine data augmentation settings to avoid removing important visual features</li>
  <li>Experiment with deeper CNN architectures</li>
  <li>Apply transfer learning with pretrained models</li>
  <li>Explore transformer-based image classification models</li>
</ul>

<h2>Technologies Used</h2>
<p>
Python • PyTorch • NumPy • Matplotlib • Seaborn • Jupyter Notebook
</p>

<h2>Repository Structure</h2>

<pre>
├── mnist_cnn_mnist.ipynb
├── cifar10_cnn.ipynb
├── figures/
│   ├── confusion_matrix.png
│   ├── model_architecture.png
│   └── sample_predictions.png
└── README.md
</pre>

<h2>Project Visuals</h2>

<h3>Confusion Matrix</h3>
<p align="center">
  <img src="figures/confusion_matrix.png" alt="CIFAR-10 confusion matrix" width="650">
</p>

<h3>Model Architecture</h3>
<p align="center">
  <img src="figures/model_architecture.png" alt="CNN model architecture" width="650">
</p>

<h2>Key Takeaways</h2>
<ul>
  <li>CNNs perform extremely well on simple image classification tasks such as MNIST.</li>
  <li>Performance drops on more complex datasets such as CIFAR-10, where classes overlap visually.</li>
  <li>Confusion matrix analysis helps explain model weaknesses beyond overall accuracy.</li>
  <li>Dataset complexity plays a major role in classification performance.</li>
</ul>

<h2>License</h2>
<p>
This project is licensed under the MIT License.
</p>
