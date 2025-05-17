# Welcome

Thank you for visiting this repository. Here, we present a collection of experiments exploring the expressive capacity, robustness, and structural interpretability of Weighted Backward Shift Neural Networks (WBSNNs). This repository supports our NeurIPS 2025 submission and aims to offer an intuitive yet rigorous entry point into our framework, which leverages linear dynamics and orbit-based learning.

WBSNN is a novel orbit-based learning framework inspired by operator theory and functional analysis. This architecture offers a compelling alternative to standard neural models by capturing data geometry through orbits of backward shift dynamics, enabling **interpretable**, **data-efficient**, and **topologically robust** learning.

WBSNNs are constructed using the action of weighted backward shift operators to build representations across three learning phases: subset construction, interpolation via orbit dynamics, and generalization through learned orbit combinations. The model departs from standard architectures by explicitly incorporating linear structure and offering a strong mathematical backbone rooted in operator theory.


This repository is structured around a collection of **independent, self-contained experiments**, each corresponding to a different dataset. The aim is not just to benchmark WBSNN's performance, but to highlight its **versatility across tasks**, its **resilience to noise**, and its **ability to generalize from minimal data** using principled interpolation mechanisms.

The current experiments span a diverse collection of datasets—including sensor drift, spoken letter recognition, order book time series, air pollution prediction, sentiment classification, and image recognition—chosen to reflect the range of challenges WBSNNs can handle. Each dataset brings a unique structure: some are noisy and high-dimensional (ISOLET, Gas Sensor), others are time-indexed and volatile (FI-2010, Beijing PM2.5), and a few provide geometric or textual complexity (Swiss Roll, IMDb). This diversity validates the versatility of WBSNNs in adapting to heterogeneous data domains with a consistent architecture and learning strategy.

We emphasize that the codebase is evolving. The implementations here are intentionally kept simple-all experiments were conducted using only CPU on a local Jupyter environment and may be far from optimal in terms of speed and engineering polish—demonstrating that WBSNN can deliver strong results even under modest computational constraints. We are actively working to improve scalability, efficiency, and usability in future iterations. Nonetheless, every experiment included has been designed to illustrate specific theoretical properties of WBSNNs and their performance under realistic constraints.

Each run follows the same pipeline: preprocessing, Phase 1 orbit construction, Phase 2 interpolation (exact or relaxed), and Phase 3 classification via MLP. We encourage you to explore the individual notebooks to appreciate how orbit-driven inductive bias adapts to different data geometries and learning challenges.

We hope this repository serves not only as an empirical validation of our theory but also as a springboard for further applications of structured linear dynamics in deep learning.


You will find experiments covering:

* Synthetic manifolds (e.g., Swiss Roll) with challenging geometry and label noise  
* Noisy linear classification with known Bayes error bounds  
* Time series classification (ItalyPowerDemand) under extreme data scarcity  
* Air pollution regression (Beijing PM2.5) with strong periodicity and missing data  
* High-frequency financial order book data (FI-2010) for volatile sequence modeling  
* Sensor array drift (Gas Sensor Drift) for distribution shift and long-term stability testing  
* Sentiment classification (IMDb) from sparse textual input  
* Multiclass speech recognition (ISOLET) with high-dimensional, highly correlated acoustic features  
* Image classification (MNIST) with compressed, low-rank representations

Each experiment provides a comprehensive markdown file that includes:

* A formal description of the dataset and its geometry 
* The training and interpolation mechanisms used by WBSNN
* Comparisons to classical baselines (logistic regression, random forests, SVM, MLP)
* Analytical commentary on interpolation regimes, topological impact, and model generalization

## Start Here

To get a rapid sense of WBSNN's theoretical strength in practice, we recommend beginning with these standout experiments:

- **Swiss Roll**: A nontrivial synthetic manifold showing WBSNN’s capacity to disentangle nonlinear geometry and achieve high test accuracy without convolutions or attention mechanisms.

- **IMDb Sentiment**: Demonstrates strong generalization in sparse, noisy, and high-dimensional text embeddings using simple orbit structures and class-agnostic interpolation.

- **Gas Sensor Drift**: Reveals WBSNN's robustness under severe distribution shift and high noise, with consistent results across multiple training sizes and input dimensions.

- **FI-2010 Order Book**: Validates temporal stability and efficient interpolation over financial microstructure data with discontinuities, using low-dimensional PCA projections.

- **ISOLET**: Highlights WBSNN’s strength in multiclass acoustic classification tasks with structured orbit combinations and interpretable feature compression.

These cases reflect how orbit-based learning adapts to radically different topologies, modalities, and learning goals, from binary sentiment over words to multi-class speech and sensor-based drift. They offer immediate insight into WBSNN's capacity to interpolate structure and generalize across a wide spectrum of domains.

We invite you to explore, critique, and build upon this work—WBSNN is just the beginning.

