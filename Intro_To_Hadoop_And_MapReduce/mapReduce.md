#MapReduce

MapReduce processes data in HDFS

MapReduce is designed to process data in parallel, meaning that your file is broken into chunks and then processed in parallel

-

###In MapReduce there are Mappers and Reducers

**Mappers** work in parallel to collect all the data and divide it into different piles based on a **Key** (Maybe you divide your data by city, user, company, etc.)

Once the mappers have divided the data into different piles called the **Intermediate Records** they give those records to the reducers

A record is a (Key, Value) pair

When the data is given to the Reducers a phase of MapReduce called **Shuffle and Sort** takes place

**Shuffle** is the movement of the records from the Mappers to the Reducers

**Sort** is done by the reducers, adn they will organize the records into sorted order

Finally, each **Reducers** works on one set of data at a time based on the Key, and then it processes those values in some way (Adding numbers, calculating average/mean, etc.) before writing out the final results

-

Example:

Data = {(Chicago, 12), (Miami, 33), (New York, 29), (Chicago, 56), (Miami, 40), (Miami, 7), (Chicago, 52), (Miami, 3), (New York, 89), (Chicago, 56), (Miami, 4), (Miami, 67)}


MAPPING:

Some amont of Mappers process this data in parallel, in this case 2:

Mapper 1: {(Chicago, 12), (Chicago, 56), (Chicago, 52)}, {(Miami, 4), (Miami, 67)}

Mapper 2: {(Chicago, 56)}, {(Miami, 33), (Miami, 7), (Miami, 3)}, {(New York, 29), (New York, 89)}

Notice all the data has been collected in parallel and stored in separate piles based on the Key


SHUFFLE:

These piles of reports are sent to the Reducers


SORT:

The Reducers put the data into sorted order as seen below

{(Chicago, 12), (Chicago, 52), (Chicago, 56), (Chicago, 56)},
{(Miami, 3), (Miami, 4), (Miami, 7), (Miami, 33), (Miami, 67)},
{(New York, 29), (New York, 89)}


PROCESS (In this case we will add all the values but you could do anything with the values):

{(Chicago, 120)}, (Miami, 47), (New York, 118)}