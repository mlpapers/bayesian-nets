# Bayesian networks
> Bayesian network is a probabilistic graphical model (a type of statistical model) that represents a set of variables and their conditional dependencies via a directed acyclic graph (DAG) ([Wiki](https://en.wikipedia.org/wiki/Bayesian_network)

- **Overview**
  - [Introducing Bayesian Networks](https://bayesian-intelligence.com/publications/bai/book/BAI_Chapter2.pdf) (2004) - free chapter from the [Bayesian Artificial Intelligence](https://bayesian-intelligence.com/publications/bai/) book *Kevin B. Korb, Ann E. Nicholson*
  - [A Tutorial on Learning With Bayesian Networks](https://arxiv.org/pdf/2002.00269.pdf) (2020) *David Heckerman*


### Types
- **Discrete Bayesian Networks**
  - Distributions are assumed to be multinomial, represented by tables
- **Gaussian Bayesian Networks**
  - Distributions are normal
  - [Learning Gaussian Networks](https://arxiv.org/pdf/1302.6808.pdf) (1994) *Dan Geiger, David Heckerman*
- **Mixed**
  - Bayesian networks with variables that have different distributions
  - [Graphical Models for Associations between Variables, some of which are Qualitative and some Quantitative](https://projecteuclid.org/euclid.aos/1176347003) (1989) *S. L. Lauritzen, N. Wermuth*
  - [Copula Bayesian Networks](https://papers.nips.cc/paper/3956-copula-bayesian-networks.pdf) (2010) *Gal Elidan*
- **Dynamic Bayesian Networks**
  - Relates variables to each other over some time steps
  - [Dynamic Network Models for Forecasting](http://erichorvitz.com/dynamic_network_models_UAI_1992.pdf) (1992) *Paul Dagum, Adam Galper, Eric Horvitz*
  - [Dynamic Bayesian Networks: Representation, Inference and Learning](https://www.cs.ubc.ca/~murphyk/Thesis/thesis.pdf) (2002) *Kevin Patrick Murphy*

### Structure learning
Learning the graph structure that represents the conditional independencies between variables. Main approaches are *constraint-based* (conditional independence tests) and *score-based* (goodness-of-fit scores)
- **Inductive Causation**
  - [Equivalence and Synthesis of Causal Models](https://arxiv.org/pdf/1304.1108.pdf) (1990) *TS Verma, Judea Pearl*
- **Sparse Candidate**
  - [Learning Bayesian Network Structure from Massive Datasets: The "Sparse Candidate" Algorithm](https://arxiv.org/pdf/1301.6696.pdf) (1999) *Nir Friedman, Iftach Nachman, Dana Peer*
- **Greedy Search**
  - [Optimal Structure Identification With Greedy Search](http://www.ai.mit.edu/projects/jmlr/papers/volume3/chickering02b/chickering02b.pdf) (2002) *David M. Chickering*
  - [Learning Bayesian Networks with Thousands of Variables](https://papers.nips.cc/paper/5803-learning-bayesian-networks-with-thousands-of-variables.pdf) (2015) *Mauro Scanagatta, Cassio P. de Campos, Giorgio Corani, Marco Zaffalon*
  - [Learning Bayesian networks from big data with greedy search:computational complexity and efficient implementation](https://link.springer.com/content/pdf/10.1007%2Fs11222-019-09857-1.pdf) (2019) *Marco Scutari, Claudia Vitolo, Allan Tucker*
- **Grow-Shrink**
  - [Learning Bayesian Network Model Structure from Data](https://www.cs.cmu.edu/~dmarg/Papers/PhD-Thesis-Margaritis.pdf) (Ph.D. thesis, 2003) *Dimitris Margaritis*
- **Incremental Association**
  - [Algorithms for Large Scale Markov Blanket Discovery](https://www.aaai.org/Papers/FLAIRS/2003/Flairs03-073.pdf) (2003) *Ioannis Tsamardinos, Constantin F. Aliferis, Alexander Statnikov*
  - Interleaved Incremental Association
  - Fast Incremental Association  
    [Speculative Markov BlanketDiscoveryforOptimalFeature Selection](http://www.cs.cmu.edu/~dmarg/Papers/Yaramakala-Margaritis-ICDM05.pdf) (2005) *Sandeep Yaramakala, Dimitris Margaritis*
- **Optimal Reinsertion**
  - [Optimal Reinsertion: A new search operator for accelerated and more accurate Bayesian network structure learning](https://web.engr.oregonstate.edu/~wongwe/papers/pdf/optreinsert.2003.pdf) (2003) *Andrew Moore, Weng-Keen Wong*
- **Max-Min Parents and Children**
  - [The max-min hill-climbing Bayesian network structure learning algorithm](https://link.springer.com/content/pdf/10.1007%2Fs10994-006-6889-7.pdf) (2006) *Ioannis Tsamardinos, Laura E. Brown, Constantin F. Aliferis*
- **Other**
  - [Learning Bayesian Networks: The Combination of Knowledge and Statistical Data](http://www.cs.technion.ac.il/~dang/journal_papers/heckerman1995learning.pdf) (1995) *D. Heckerman, D.Geiger, D. M. Chickering*

### Parameter learning
Estimation of the parameters of the global distribution with known graph structure.
- [Learning Bayesian network parameters under incomplete data with domain knowledge](https://www.ecse.rpi.edu/~qji/Papers/PR_wenhui.pdf) (2009) *Wenhui Liaoa, Qiang Ji*
- **MLE** Maximum Likelihood Estimate
- **Bayesian method**
- **EM** Expectation-maximization
- **RBE** Robust Bayesian Estimate
- **Monte-Carlo Method**
- **Gaussian approximation**

### Packages
- **R**
  - Package: abn ([CRAN](https://cran.r-project.org/web/packages/abn/index.html), [Paper](https://arxiv.org/pdf/1911.09006.pdf))
  - Package: bnlearn ([Homepage](https://www.bnlearn.com/), [Paper](https://arxiv.org/pdf/0908.3817.pdf))
  - Package: deal ([CRAN](https://cran.r-project.org/web/packages/deal/), [Paper](https://core.ac.uk/download/pdf/6303113.pdf)) - supports learning from mixed data
  - Package: pcalg ([CRAN](https://cran.r-project.org/web/packages/pcalg/))
- **Python**
  - Package: BNfinder ([PyPI](https://pypi.org/project/BNfinder/))
- **Julia**
  - Package: BayesNets.jl ([Code](https://github.com/sisl/BayesNets.jl))

