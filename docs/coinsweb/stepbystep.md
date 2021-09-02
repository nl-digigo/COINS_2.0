# COINS step by step

The implementation contains the following steps, roughly:


## Exporting data to the <a>COINS</a> format

1. define the data within your system that you need to exchange
2. create a mapping between the [COINS Core model ](https://bimloket.github.io/COINS_2.0/coinsweb/#core-model) and the data model of your system
3. collect the data from your system
4. create Coins data from the collected data and export this to a <a>COINS</a> Container
5. transmit this <a>COINS</a> Container to your client
6. optional, validate the <a>COINS</a> container before sending it to your client

## Importing data from the <a>COINS</a> format

1. define the locations within your system in which <a>COINS</a> data will be imported
2. create a mapping between the [COINS Core model ](https://bimloket.github.io/COINS_2.0/coinsweb/#core-model) and the data model of your system
3. opening the <a>COINS</a> Container and read the <a>COINS</a> data
4. validate the <a>COINS</a> data in the Container
5. import the <a>COINS</a> data into your system

## Exporting data smaples
1. [Creating a container](https://bimloket.github.io/COINS_2.0/coinsweb/#createcontainer) with one object
2. Create a <a>COINS</a> Container for a simple Bench with subobjects, the Coins Contains Relation.





