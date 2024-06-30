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