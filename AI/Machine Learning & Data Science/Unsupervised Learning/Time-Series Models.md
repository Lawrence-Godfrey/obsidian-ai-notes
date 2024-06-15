1. **[[Autoencoders]]**: Autoencoders, especially recurrent autoencoders, can be used for unsupervised learning with time-series data. They learn to compress the input data into a lower-dimensional representation and then reconstruct it. The reconstruction error can be used to detect anomalies or extract features.

2. **Principal Component Analysis (PCA)**: While PCA is traditionally used for dimensionality reduction in static data, it can be applied to time-series data by transforming the data into a matrix where each row represents a time series. This can help in identifying the most significant patterns in the data.

3. **Independent Component Analysis (ICA)**: Similar to PCA, ICA is used for separating a multivariate signal into additive, independent components. It can be applied to time-series data for tasks like source separation and noise reduction.

4. **Dynamic Time Warping (DTW) for Clustering**: DTW is a technique used to measure similarity between two time-series sequences, which may vary in speed. It can be used as a distance metric in clustering algorithms like k-means to cluster time-series data.

5. **Gaussian Mixture Models (GMMs)**: GMMs can be applied to time-series data to model the underlying distribution. When combined with the Expectation-Maximisation (EM) algorithm, GMMs can be used for clustering and anomaly detection.

6. **Hidden Markov Models (HMMs)**: HMMs are a type of statistical model that can be used to describe the evolution of observable events that are dependent on internal factors, which are not directly observable. HMMs are particularly useful for sequential data and can be used for tasks like pattern recognition and anomaly detection.

7. **Self-Organising Maps (SOMs)**: SOMs are a type of artificial neural network that is trained using unsupervised learning to produce a low-dimensional (typically two-dimensional) representation of the input space. They can be used for clustering and visualising high-dimensional time-series data.

8. **t-Distributed Stochastic Neighbour Embedding (t-SNE)**: t-SNE is a technique for dimensionality reduction that is particularly well suited for the visualisation of high-dimensional datasets. It can be used to visualise clusters in time-series data by transforming the data into a two or three-dimensional space.