# COINSTAC
_Decentralized Analyses Made Easy_

<img src="https://github.com/MRN-Code/coinstac-common/blob/master/img/coinstac.png" height="75px" />

[COINSTAC](# "Collaborative Informatics and Neuroimaging Suite Toolkit for Anonymous Computation") is software to foster collaborative research, removing large barriers to traditional data-centric collaboration approaches.  It enables groups of users to run common analyses _on their own machines_ over _their own datasets_ with ease.  The results of these analyses are synchronized to the cloud, and undergo aggregate analyses processes using all contributor data.  Decentralized pipelines allow for distributed, iterative, and feature rich analyses to be run, opening new and exciting capabilities for collaborative computation.  If also offers data anonymity through differential privacy algorithms, so members do not need to fear PHI traceback.

Let's do research!

**Table of Contents:**

* [The Problem](#the-problem)
* [The Solution](#the-solution)
* [Getting Started](#getting-started)
* [Under The Hood](#under-the-hood)
* [License](#license)

## The Problem

You want to do research, and you want to include data from around the world.  Unfortunately, orchestrating such an event is anything but trivial.

- Coordinating data-driven research can be difficult.  Who's going to collect all of the files?  Who is going to actually "run" all of the data?

- Ensuring privacy can be difficult.  Can I trust other people or institutions with my research participants' data?  Am I even allowed to share it?

- Large datasets can be expensive to transfer.  When file sets are in the GB and TB range, network transfers are not immediately trivial or even practical.

- Valuable research data may often not be shared due to privacy or IRB constraints.

- "Smart bullies" have demonstrated ability to extract personal information from various aggregated, anonymized datasets.  How can we share data without revealing confidential information?

Bottom line--collaborative group research requires a great deal of coordination.  Human and business factors can hamper research from happening at a pace that we are able to handle!  Constraints may even forbid group research to occur at all.

# The Solution

Let's remove these barriers.  The best usage of research data is to apply it _everywhere it can be useful_.  Our strategy enables otherwise "locked-down data" to become useful again.

COINSTAC removes the barriers to collaborative analysis by:

- **decentralizing analyses and computation**
  - each user performs analyses/pipelines/etc all on their own computers. bits and pieces of each users' output _may_ be sent to a central compute node
  - a central compute node performs a complimentary component of the group analysis, generally a Machine Learning algorithm.  this node may trigger adjusted computations on users' machines, generally in effort to improve a model, which the research is trying to predict!  
- _not_ synchronizing full datasets. instead, **synchronizing only resultant analysis metrics**
  - as previously discussed, central compute nodes aggregate these metrics, and attempt to draw conclusions from the contributor swarm
  - because machine learning algorithms can be designed to model outcomes via artifacts of your analysis Pipelines, we keep your data safely and conveniently on your own machine, _untouched_.
- **applying differential privacy** strategies to truly anonymize private data, whilst still permitting collaboration.

You may wonder why we haven't been doing this before!  Us too.  Let's get started!

## Getting Started

- If you are looking to contribute data, head over to [coinstac-ui](https://github.com/MRN-Code/coinstac-ui).  There, you will be able to download the application.

- If you are a developer or scientist and want to design a decentralized computation, please see:
  - [DecentralizedComputation.md](DecentralizedComputation.md) for how to build your own `DecentralizedComputation`.
  - [coinstac-simulator](mrn-code/coinstac-simulatorhttps://github.com/MRN-Code/coinstac-simulator) for how to test your freshly created `DecentralizedComputation`.
  - "Under the Hood" below, if you want to understand how the system works.


## Under The Hood

Developer documentation and system design information may be found over in our [technical docs](./TECHNICAL.md).

## License

MIT. See [LICENSE](./LICENSE) for details.
