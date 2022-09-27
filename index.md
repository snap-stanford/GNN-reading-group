# Graph ML/GNN Reading Group 


## Meeting Time and Location 
Tuesdays 4:30- 6pm at Stanford Gates 415 ([google calendar](https://calendar.google.com/event?action=TEMPLATE&tmeid=M3IzbzBtMHZ2MDFnbGVoM3NiZGVqZDNtZ2tfMjAyMjA2MjhUMjMzMDAwWiBxaWFuMTIzcXdAbQ&tmsrc=qian123qw%40gmail.com&scp=ALL),[zoom](https://stanford.zoom.us/j/99662423809?pwd=N1VTZnVNeGM0MU0veWhQckQ1YUJsUT09))


## Introductory Material

- [Jure’s CS 224w](https://web.stanford.edu/class/cs224w/index.html#schedule) (Lecture 6 onwards)
- [Graph Representation Learning](https://www.cs.mcgill.ca/~wlh/grl_book/), book by Will Hamilton
- GNN Intro Blog Posts
  - <https://distill.pub/2021/gnn-intro/>
  - <https://distill.pub/2021/understanding-gnns/>
- [Moses’s repository of survey papers](https://www.dropbox.com/sh/61cpaowg8ityuin/AAAlpRRkbbRp7sy0-0hq9XMWa?dl=0)

## Schedule 

### Summer 2022

- 6/28/2022: Invariant Neural Nets for Eigenvectors, and other Invariances / Equivariances in Graph Machine Learning
  - Presenter: Derek Lim, Joshua Robinson
  - Related papers: [Sign and Basis Invariant Networks for Spectral Graph Representation Learning](https://arxiv.org/abs/2202.13013)
  - Abstract: Various invariances and equivariances have been found to be useful for graph machine learning. Recently, invariance to symmetries exhibited by Laplacian eigenvectors has been shown to be beneficial for processing graphs.  We introduce SignNet and BasisNet -- the first neural architectures that are invariant to two key symmetries displayed by eigenvectors: (i) sign flips, since if v is an eigenvector then so is −v; and (ii) more general basis symmetries, which occur in higher dimensional eigenspaces with infinitely many choices of basis eigenvectors. We prove that our networks are universal, i.e., they can approximate any continuous function of eigenvectors with the desired invariances. Moreover, when used with Laplacian eigenvectors, our architectures are provably expressive for graph representation learning: they can provably compute useful functions on graphs that many other models cannot.

- 7/12/2022: CLRS benchmark and Graph Neural Networks are Dynamic Programmers (at 11am)
  - Presenter: Petar Veličković
  - Related papers: 
    - [The CLRS Algorithmic Reasoning Benchmark](https://arxiv.org/abs/2205.15659)
    - [Graph Neural Networks are Dynamic Programmers](https://arxiv.org/abs/2203.15544)

- 7/26/2022: Geometric Deep Learning for Drug Discovery
  - Presenter: Jian Tang
  - Abstract: Drug discovery is a very long and expensive process, taking on average more than 10 years and costing $2.5B to develop a new drug. Artificial intelligence has the potential to significantly accelerate the process of drug discovery by extracting evidence from a huge amount of biomedical data and hence revolutionizes the entire pharmaceutical industry. In particular, graph representation learning and geometric deep learning--a fast growing topic in the machine learning and data mining community focusing on deep learning for graph-structured and 3D data---has seen great opportunities for drug discovery as many data in the domain are represented as graphs or 3D structures (e.g. molecules, proteins, biomedical knowledge graphs). In this talk, I will introduce our recent progress on geometric deep learning for drug discovery and also a newly released open-source machine learning platform for drug discovery, called TorchDrug.

- 8/2/2022: Deep Geometric Probabilistic Models with their applications for Molecular Modeling
  - Presenter: Minkai Xu
  - Abstract: Modeling molecular geometries from molecular graphs is a fundamental problem in cheminformatics and drug discovery. Recently, significant progress has been achieved with machine learning approaches, especially with deep generative models. However, modeling such a generation process is very challenging as the learned likelihood of geometries should be roto-translational invariant. In this talk, I will review how we tackle the unique challenges of this problem, and introduce the recent machine learning models on this problem, with an emphasis on our most recent method named GeoDiff. 

- 8/16/2022: Over-squashing and over-smoothing through the lenses of curvature and multi-particle dynamics
  - Presenter: Francesco Di Giovanni
  - Abstract: In this talk I am going to talk about two problems that Message Passing Neural Networks (MPNNs) have been shown to be struggling from. The first one - known as over-squashing - is unavoidable in the MPNN class and concerns the input graph topology. This relates to how information propagates in a graph. We show that discrete curvature quantities (old and new) could help us understand where messages are being lost and we can provably characterize the over-squashing phenomenon in terms of curvature. The second problem consists in analyzing GNNs as multi-particle dynamics using the lens of gradient flows of an energy. We investigate what happens when instead of learning the MPNN equations we learn an energy and then let the equations follow the gradient flow of such energy. This allows us to understand further the role of the channel-mixing matrix that is ubiquitous in standard graph convolutional models as a bilinear potential inducing both attraction and repulsion along edges via its positive and negative eigenvalues respectively.

- 8/23/2022: Graph-Coupled Oscillator Networks
  - Presenter: Konstantin Rusch 
  - Abstract: We propose Graph-Coupled Oscillator Networks (GraphCON), a novel framework for deep learning on graphs. It is based on discretizations of a second-order system of ordinary differential equations (ODEs), which model a network of nonlinear controlled and damped oscillators, coupled via the adjacency structure of the underlying graph. The flexibility of our framework permits any basic GNN layer (e.g. convolutional or attentional) as the coupling function, from which a multi-layer deep neural network is built up via the dynamics of the proposed ODEs. We relate the oversmoothing problem, commonly encountered in GNNs, to the stability of steady states of the underlying ODE and show that zero-Dirichlet energy steady states are not stable for our proposed ODEs. This demonstrates that the proposed framework mitigates the oversmoothing problem. Moreover, we prove that GraphCON mitigates the exploding and vanishing gradients problem to facilitate training of deep multi-layer GNNs. Finally, we show that our approach offers competitive performance with respect to the state-of-the-art on a variety of graph-based learning tasks.


- 9/13/2022: Seeded Graph Matching: The Power of Multi-hops
  - Presenter: Jiaming Xu 
  - Abstract: Given a pair of graphs, the problem of graph matching or network alignment refers to finding the underlying vertex correspondence that maximally aligns the edges. This is a ubiquitous problem arising in a variety of applications across diverse fields such as network privacy, computational biology, computer vision, and natural language processing. This talk focuses on seeded graph matching, where a small portion of the vertex correspondence is revealed as seeds and we seek to complete the correspondence. We develop a new idea of "multi-hop witness" and show that it has the power to match two correlated Erdős–Rényi graphs of size n with only polylog(n) number of seeds, achieving an exponential reduction in seed size requirement compared to the best previously known result. We further adapt this idea and show that it becomes even more powerful for matching two correlated power-law graphs despite the presence of degree heterogeneity. Finally, we design a graph neural network that adaptively learns to utilize the multi-hop witness and generalizes this knowledge to match unseen graphs of various types and sizes. Numerical results on both synthetic and real graphs demonstrate the significant performance improvement over the state of the art. Based on joint work with Elchanan Mossel (MIT), Xiaojun Lin (Purdue), and Liren Yu (Purdue). Preprints are available at https://arxiv.org/abs/1807.10262, https://arxiv.org/abs/2102.12975, https://arxiv.org/abs/2205.13679.
 

### Spring 2022 

- 4/5/2022: Tutorial on GNN and expressive power
  - Presenter: Weihua Hu
  - [Slides](https://drive.google.com/file/d/1UtYBc-8e85Id9PAoahzXEgjuv9Zr11QJ/view?usp=sharing)
  - Related papers:
    - [How Powerful are Graph Neural Networks?](https://arxiv.org/abs/1810.00826)

- 4/12/2022: Discussion on expressive power of GNN
  - Presenter: Qian Huang
  - [Slides](https://docs.google.com/presentation/d/1A19TdVsAh6KwwokOObkovVUFW4Cykyb7P4cm0Taj8Lk/edit?usp=sharing)
  - Related papers:
    - [How Powerful are Graph Neural Networks?](https://arxiv.org/abs/1810.00826) (last week Weihua’s presentation)
    - [What Can Neural Networks Reason About](https://arxiv.org/abs/1905.13211)
    - [Graph Neural Networks are Dynamic Programmers](https://arxiv.org/abs/2203.15544)
    - [The Exact Class of Graph Functions Generated by Graph Neural Networks](https://arxiv.org/abs/2202.08833)
 
- 4/19/2022: Discussion on expressive power of GNN and open problem
  - Presenter: Amin Saberi
 
- 4/26/2022: Discussion on expressive power of GNN and open problem
  - Presenter: Yeganeh Alimohammadi
  - Related papers:
    - [Generalization and Representational Limits of Graph Neural Networks](https://arxiv.org/abs/2002.06157) 
    - [Topological Graph Neural Networks](https://arxiv.org/pdf/2102.07835.pdf)

- 5/3/2022: Constraint satisfaction and Combinatorial problems
  - Presenter: Aidan Perreault, Moses Charikar
  - Related papers:
    - [Graph Neural Networks for Maximum Constraint Satisfaction](https://arxiv.org/abs/1909.08387)
    - [Learning a SAT Solver from Single-Bit Supervision](https://arxiv.org/abs/1802.03685) 
    - [Combinatorial optimization and reasoning with graph neural networks](https://arxiv.org/abs/2102.09544)
 
- 5/11/2022: Auto-scaling GNNs & PyG 2.0
  - Presenter: [Matthias Fey](https://rusty1s.github.io/#/)
  - [Slides](https://drive.google.com/file/d/1J5Zxd1LhDKVX0VtMU1y21GZ-48FI8Z9i/view?usp=sharing)

- 5/24/2022: GNN Embedding
  - Presenter: [Rex Ying](https://cs.stanford.edu/people/rexy/)
  - [Slides](https://drive.google.com/file/d/1VXlSsJu9kbUQVz16Vi4baidpv-S5nfxT/view?usp=sharing)

- 5/31/2022: Hyperbolic GNN Embedding
  - Presenter: Aaron Lou
  - [Slides](https://drive.google.com/file/d/1HRvlyB8EHzU3hQdvX3sNzbl4apygAP3Z/view?usp=sharing)

- 6/7/2022: Box Embedding for KG reasoning
  - Presenter: Hongyu Ren
  - [Slides](https://drive.google.com/file/d/1liAX6Mekp0a5HthivsyS5dfFLZxb8mRm/view?usp=sharing)

## Other Topics and Papers for Future

- Graph generative models: Amin, Yeganeh, Jared, Moses
  - [Evaluation Metrics for Graph Generative Models: Problems, Pitfalls, and Practical Solutions (ICLR 22)](https://arxiv.org/pdf/2106.01098.pdf)
  - [On Evaluation Metrics for Graph Generative Models (ICLR 22)](https://arxiv.org/pdf/2201.09871.pdf)

-  GNN Oversquashing
   - [On the Bottleneck of Graph Neural Networks and its Practical Implications](https://arxiv.org/abs/2006.05205)
   - [Understanding over-squashing and bottlenecks on graphs via curvature (ICLR 22)](https://arxiv.org/pdf/2111.14522.pdf)

- GNN + geometric representation learning (non-euclidean space)
  - [Hyperbolic Graph Neural Networks](https://arxiv.org/abs/1910.12892)
  - [Hyperbolic Graph Convolutional Neural Networks](https://arxiv.org/abs/1910.12933) 

- Geometric Deep Learning, Invariant/equivariant Graph Networks
  - <https://www.youtube.com/watch?v=7pRIjJ_u2_c>
  - <https://www.dropbox.com/sh/u9o69w4rm0uvmzi/AADLGwfdcY94HVsz2eSoCAFPa/invariant%20graph%20networks?dl=0&subfolder_nav_tracking=1> 
  - [E(n) Equivariant Graph Neural Networks](https://arxiv.org/abs/2102.09844)

- Simplification 
  - [Simplifying Graph Convolutional Networks](https://arxiv.org/abs/1902.07153)
  - [Combining Label Propagation and Simple Models Out-performs Graph Neural Networks](https://arxiv.org/abs/2010.13993)

- Hypergraphs
  - <https://www.dropbox.com/sh/u9o69w4rm0uvmzi/AADtWutKnbOw0NuxPRpYOwlla/hypergraphs?dl=0&subfolder_nav_tracking=1>
 
- Others 
  - [Discovering Symbolic Models from Deep Learning with Inductive Biases](https://arxiv.org/abs/2006.11287)
  - Applications on knowledge graph, drug discovery etc
 
## Organizers and Participants
 - Moses Charikar <moses@cs.stanford.edu>
 - Amin Saberi <saberi@stanford.edu>
 - Jure Leskovec <jure@cs.stanford.edu>
 - Qian Huang <qhwang@cs.stanford.edu>
 - [Participants](https://docs.google.com/document/d/17nf-aUpaMCghkWTLBmaiZW1nmOKrxwqRIsDJO_h3658/edit?pli=1#)

 
