# REPAIR Approach for social-based city reconstruction planning

## Table of contents

- [General info](#general-info)
- [Citation request](#citation-request)
- [Project structure](#project-structure)
- [Datasets and methods](#datasets-and-methods)
- [Experiment replication](#experiment-replication)
- [Credits](#credits)
- [License](#license)

## General info

REPAIR is an innovative post disaster rebuilding plan providing approach that takes into account the physical features of the city, time and budget constraints, and embeds Social needs and benefits in accordance with Political priorities. The approach is generic since, changing the input parameters (i.e, political priority, considered area and social benefit model), it can generate different viable plans. The generated plans can have different territorial extension under a single municipality, satisfy different political constraints and consider different social benefit models. It can be applied on a wider area involving several municipalities if the decision variables are shared among the decision makers. 

Addtionally the presented approach is a core of a decision-support system and It can determine a set of alternative plans for local administrators who select the idealvone to implement, and it can be applied to areas of any extension. We show the application of REPAIR in a real use case, i.e., to the L’Aquila reconstruction process, damaged in 2009 by a major earthquake.

## Citation request

Please cite our papers if you use our REPAIR approach experiments which are alreayd published in 2021 IEEE COMPSAC Conference:

_Ghulam Mudassir and Antinisca Di Marco are the auhtors link: https://ieeexplore.ieee.org/abstract/document/9529371

```bibtex
@INPROCEEDINGS{9529371,
  author={Mudassir, Ghulam and Di Marco, Antinisca},
  booktitle={2021 IEEE 45th Annual Computers, Software, and Applications Conference (COMPSAC)}, 
  title={Social-based City Reconstruction Planning in case of natural disasters: a Reinforcement Learning Approach}, 
  year={2021},
  volume={},
  number={},
  pages={493-503},
  doi={10.1109/COMPSAC51774.2021.00074}}
  ```
  
  ## Project structure
  
 Porject repository is organized as follows:

1. Useful files to create and manage the environment are listed in the main repository which contains files seperately for comparioson of reinforcemnt learning algorithemd and REPAIR approach.(requirements.txt, DQEnv.py). 

2. The REPAIR algorithm agent enviroment file exist in DQEnv.py and agent training file in Agent_V1-Training1.pynb. These files contains all the necessary functions to generate post-disaster alternative reconstruction plans.

3. When the scripts run every time Rewards.pkl file is generated to generate objetcs structures.

4. The data folder contains all the datasets listed in section [Datasets and methods](#datasets-and-methods).
  
