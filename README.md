# An Efficient Blockchain assisted Reputation aware Decentralized Federated Learning Framework

* If Docker installed
    * docker-compose up -d
    * open host_ip:42065 for opening jupyter notebook
    * open host_ip:45175 for opening tensorboard
    * run [centralized notebook](src/centralized.ipynb) for simulating the centralized fl

* If Conda enviroment
    * conda env create --name env_name --file=cenv.yml
        * it will also add this conda env in your base jupyter notebook, look for [reference](https://towardsdatascience.com/how-to-set-up-anaconda-and-jupyter-notebook-the-right-way-de3b7623ea4a)
    * conda activate env_name
    * open host_ip:port for opening jupyter notebook
        * jupyter notebook --no-browser --ip="*" --port=xxxx --NotebookApp.token='xx' --NotebookApp.iopub_data_rate_limit=1.0e1000
    * tensorboard --logdir runs/ --port 45175 --bind_all
    * open host_ip:45175 for opening tensorboard
    
* If running with kafka
    * host kafka broker and other essential components with [docker](kafka/docker-compose.yml)
    * before running update the host ip in the broker service, and also update the same in [producer](libs/protobuf_producer.py) and [consumer](libs/protobuf_consumer.py) files
    * good to run this [file](kafka/flkafka.ipynb) for simulation
    