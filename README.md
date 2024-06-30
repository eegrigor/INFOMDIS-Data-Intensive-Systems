# INFOMDIS-Data-Intensive-Systems

This repo contains our solution for the INFOMDIS Data Intensive System Project for the year 2023-24, which was to identify and group similar
process instances present on a hypothetical network provider's logs. 

The solution was built and tested using Python, PySpark on VSCode. 

To run: 

Create Virtual Environment:  
```
python3 -m venv venv
```

Activate Virtual Environment: 
```
source venv/bin/activate
```

Install packages: 
```
pip install -r requirements.txt
```

The repo contains three main `.ipynb` files(`generate_dataset`, `task1`, `task2`), that contain the code for synthetic data generation for the network provider's logs, the solution for Task 1 and the solution for Task 2.

## Generate dataset

To generate the wanted dataset you have to specify 4 different parameters in the `generate_dataset.ipynb` file.
 
* number_of_servers: The wanted number of servers
* connections: The number of the wanted connections between servers
* number_cases: The desired number of cases 
* max_request: The maximum number of servers that can be called in one process.

We have already created some datasets in `/Data` folder. The format of the data file names is 
*data_[number_of_servers]_[connections]_[number_cases]_[max_requests].txt*

## Task 1 

To run Task 1 you should run the cells of `task1.ipynb`. First, choose the dataset that you want to apply our solution to. There are two approaches that you can choose from, our approach or the k-shingles approach. Then, you should run the cells that correspond with the chosen apporach. The results are written in the `/output` folder into two separate files:

* part1Observations.txt: Contains the groups of similar processes and inside each group every original corresponding
process.

* part1Output.txt Contains a new representation for every
group found. 

We have also provided you our results for Task 1. The result files are formatted as *[part1Observations/part1Output]_[number_of_servers]_[connections]_[number_cases]_[max_requests].txt*. These can be found in `/Data/task1-outputs`folder.

## Task 2 

In the same way, you should run `task2.ipynb` to obtain the results for the Task 2. You should only determine the wanted cluster_number which is the number of total clusters for the clustering algorithm. The output of the clustering algorithm is written in the part2Observations.txt file inside of the `/output`. We have also provided some results of our experiments for Task 2. Resulting files are in the format:*[part2Observations]_[number_of_servers]_[connections]_[number_cases]_[max_requests]_[cluster_number].txt*. These can be found in `/Data/task2-outputs`folder.
