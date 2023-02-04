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

## Datasets and methods

We have verified REPAIR approach on very complex dataset of Sulmona and L'Aquil which was extracted from shapefiles. For details of data extraction process please  check the aforementioned paper for more information on the datasets and their preprocessing. In following section we have explained general phases of extraction and types of datasets.

### Extraction pahses and datasets types 

Here following we have described the data extraction phases

1- Extracted data in shapefiles from google earth

2- Coversion of shapefiles into complete and crossroad graph

3- From extracted data generated undirected graph  

4- Save extracted data in .csv files

Here following dataset types are described.

| Dataset | Full Name                   | Type       | Description                                                                                                                                                            | Parameters                      |
| ------- | --------------------------- | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------- |
| Sulomna   | Sulmona Dataset               | Binary     | The goal is to find out damage buildings, roads and bridges                                                                                               | Number of People, cost, time, political periority, distance among buildings,  physical dependecies and social benefits                   |
| L'Aquila  | Historical Cenetr L'Aquila Dataset     | Binary     | The goal is to find out damage buildings, roads and bridges in 2009 earthquack                                                                                               |  Number of People, cost, time, political periority, distance among buildings,  physical dependecies and social benefits                         |
                  
  ## Experiment replication

### Environment setup

1. **Conda users**

   Create the conda environment using the following command:

   ```shell
   conda env create -f environment.yml
   ```

2. **Pip users**

   Create the virtual environment using the following commands:

   ```shell
   virtualenv <env_name>
   source <env_name>/bin/activate
   pip install -r requirements.txt
   ```

3. **Manual setup**

   If the previous ways to not work just install the following libraries manually:

   - [pandas](https://pandas.pydata.org/)
   - [numpy](https://numpy.org/)
   - [netwrokx](https://networkx.org/)
   - [matplotlib](https://matplotlib.org/)
   - [random](https://pynative.com/python/random/)
   - [plot](https://plotly.com/)

### Run script

In order to replicate those tests, once the project directory has been downloaded, please open the terminal and move to the project folder within the terminal.

Now you can type

  pip <command> [options]

Commands:
  install                     Install packages.
  download                    Download packages.
  uninstall                   Uninstall packages.
  freeze                      Output installed packages in requirements format.
  list                        List installed packages.
  show                        Show information about installed packages.
  check                       Verify installed packages have compatible dependencies.
  config                      Manage local and global configuration.
  search                      Search PyPI for packages.
  cache                       Inspect and manage pip's wheel cache.
  index                       Inspect information available from package indexes.
  wheel                       Build wheels from your requirements.
  hash                        Compute hashes of package archives.
  completion                  A helper command used for command completion.
  debug                       Show information useful for debugging.
  help                        Show help for commands.

General Options:
  -h, --help                  Show help.
  --debug                     Let unhandled exceptions propagate outside the
                              main subroutine, instead of logging them to
                              stderr.
  --isolated                  Run pip in an isolated mode, ignoring
                              environment variables and user configuration.
  -v, --verbose               Give more output. Option is additive, and can be
                              used up to 3 times.
  -V, --version               Show version and exit.
  -q, --quiet                 Give less output. Option is additive, and can be
                              used up to 3 times (corresponding to WARNING,
                              ERROR, and CRITICAL logging levels).
  --log <path>                Path to a verbose appending log.
  --no-input                  Disable prompting for input.
  --proxy <proxy>             Specify a proxy in the form
                              [user:passwd@]proxy.server:port.
  --retries <retries>         Maximum number of retries each connection should
                              attempt (default 5 times).
  --timeout <sec>             Set the socket timeout (default 15 seconds).
  --exists-action <action>    Default action when a path already exists:
                              (s)witch, (i)gnore, (w)ipe, (b)ackup, (a)bort.
  --trusted-host <hostname>   Mark this host or host:port pair as trusted,
                              even though it does not have valid or any HTTPS.
  --cert <path>               Path to PEM-encoded CA certificate bundle. If
                              provided, overrides the default. See 'SSL
                              Certificate Verification' in pip documentation
                              for more information.
  --client-cert <path>        Path to SSL client certificate, a single file
                              containing the private key and the certificate
                              in PEM format.
  --cache-dir <dir>           Store the cache data in <dir>.
  --no-cache-dir              Disable the cache.
  --disable-pip-version-check
                              Don't periodically check PyPI to determine
                              whether a new version of pip is available for
                              download. Implied with --no-index.
  --no-color                  Suppress colored output.
  --no-python-version-warning
                              Silence deprecation warnings for upcoming
                              unsupported Pythons.
  --use-feature <feature>     Enable new functionality, that may be backward
                              incompatible.
  --use-deprecated <feature>  Enable deprecated functionality, that will be
                              removed in the future.

## REPAIR class description

### Attributes

- `Cost : float`

  Cost is input parameter which is given during training of agent 

 - `Time : float`

  Time is input parameter which is given during training of agent 
  
- `damage: bool`
  
  Whether unit is reconstructed or not
  
 - `distance: integer`
  
  Distance among units/buildings
  
  - `poltical priority: integer`
  
  To consider politicians input which is ranked between 1 to 10.
  
  - `number of people: integer`
  
  People who directly got effected
  
  - `social benefits: float`
  
  Social benefits which people get after reconstruction of units


### Methods

class DQNAgent:
    def __init__(self, state_size, action_size):

        # Define size of state and action
        self.state_size = state_size
        self.action_size = action_size
        self.action_space = action_size

        # These are hyper parameters for the DQN
        self.discount_factor = 0.95
        self.learning_rate = 0.001        
        self.epsilon_max = 1.0
        self.epsilon_decay = 0.0003
        self.epsilon_min = 0.00000001
        self.alpha = 0.1
        
        self.batch_size = 32        
        # create replay memory using deque
        self.memory = deque(maxlen=2000)

        # create main model and target model
        self.model = self.build_model()

        

    # approximate Q function using Neural Network
    def build_model(self):
        model = Sequential()
        model.add(Dense(8, input_dim = self.state_size,activation ='relu'))
        model.add(Dense(32,activation ='relu'))
        model.add(Dense(64,activation ='relu'))
        model.add(Dense(self.action_size,activation ='linear'))
        model.compile(loss='mse',optimizer=Adam_v2(lr=self.learning_rate))
        model.summary
        return model

