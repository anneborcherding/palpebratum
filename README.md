# Palpebratum
Repository containing complementary files for the paper "Bringing Light into the Darkness: Leveraging Hidden Markov Models for Blackbox Fuzzing" accepted at the 6th ACM/IEEE International Conference on Automation of Software Test (AST 2025) ([Link](https://conf.researchr.org/details/ast-2025/ast-2025-papers/3/Bringing-Light-into-the-Darkness-Leveraging-Hidden-Markov-Models-for-Blackbox-Fuzzin)).

## Abstract

Securing the network interfaces of industrial control systems is essential for protecting critical infrastructure like water treatment plants and nuclear centrifuges from potential attacks.
A key strategy to mitigate the risks of successful attacks involves identifying and closing vulnerabilities exploitable through network interfaces using testing techniques such as fuzzing.
While established techniques exist for graybox fuzzing, which assume access to system binaries, industrial components often require blackbox testing due to the use of third-party components and regulatory constraints.
We propose Palpebratum, an approach that leverages Hidden Markov Models to approximate missing information in blackbox test scenarios.
We evaluate Palpebratum’s performance in terms of code coverage, comparing it with two baseline blackbox fuzzers and the graybox fuzzer AFLnwe.
Our results demonstrate that Palpebratum significantly outperforms one blackbox fuzzer, achieving an average of 4,379.33 basic blocks compared to 4,307.60 (p-value < 0.001).
For the second blackbox fuzzer, Palpebratum achieves comparable coverage but with only half the number of test cases, demonstrating effectiveness despite the Hidden Markov Model’s overhead.
These findings suggest that Palpebratum enhances blackbox test case generation and emphasizes the importance of an efficient implementation to offset the added overhead.

For more details on our approach, methodology, and experiments, refer to the paper.

## Repository Contents

* `evaluation_data`: This directory should contain the raw experiment data. As these files tend to be huge, you first need to download them from [here](http://dx.doi.org/10.24406/fordatis/391)
* `fuzzers`: The fuzzers used for our evaluation, based on LibAFL.
* `notebooks`: Contains jupyter notebooks that process and visualize the raw data.
  * `behavior_approximation.ipynb`: Processes and visualizes the performance of different HMMs with respect to approximating the interestingness of test cases.
  * `fuzzer_eval.ipynb`: Processes and visualizes the coverage data achieved by the different fuzzers considered in our evaluation.
