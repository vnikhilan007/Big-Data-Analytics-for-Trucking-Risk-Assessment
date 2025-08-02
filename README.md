# Big-Data-Analytics-for-Trucking-Risk-Assessment

Objective

By using the provided HDP tools and techniques, we will process the data to create our own
analytics reports and create a visual presentation that will benefit decision makers.
Big Data Hadoop Ecosystems will use truck fleet data to refine and analyse trucking movement in order
to meet the organizational goal of better understanding risk The use case involves geographic data,
vehicles, average mileage, gas consumption, events, risk factors, and other supporting information
Each truck has been equipped to with devices to log location and event data These events are
streamed back to a datacentre where students will process the data and revise truck movements to
increase safety


Business Objectives

Accidents caused by large trucks remain one of the leading causes of injuries and deaths in the
United States. The objective is to identify dangerous commercial truck drivers nationwide


Loading Data into Hadoop File System (HDFS)
1. Transfer your input files into Cloudera VM by utilizing the systemcopy command.
2. Create a Hive Table for geolocation tab and load data from Geolocation file. Use the DDL
document provided to create all tables.
CREATE TABLE geolocation_stage
(
truckid string,
driverid string,
event string,
latitude DOUBLE,
longitude DOUBLE,
city string,
state string,
velocity BIGINT,
event_ind BIGINT,
idling_ind BIGINT
)
ROWFORMAT DELIMITED
FIELDS TERMINATED BY ',' STORED AS TEXTFILE
TBLPROPERTIES ("skip.header.line.count"="1");

3. Load the imported file into HIVE by utilizing “LOAD DATA INPATH”
