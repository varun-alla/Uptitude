# Uptitude
## About the Azure Architecture
The approach I took is a minimal approach to the problem we do not need anything more than those services to produce a quality product.
Services Needed 
1. DataBricks
2. MSSql Serverless
3. PowerBI Service
4. Machine Learning services(Optinal if needed)

Logical Flow
1. DataBricks script can be used to fetch the data using RestApi write the raw data into the Database.
2. The same database can be used for both raw and vizualization or proccessed data.
3. We can use diiferent databricks scripts for processing the raw Data and writing the processed data into the Database.
4. The users of the database accordingly like the writer script has writing permissions but not read permissions and the credtials used for the powerbi visualization have only read access for viz tables only.

The main reason for this minimal approach is the client specifically mentioned that he wants the dashboard to refreshed only once.

## About the restarauntsopeninghour script

The Goal of the script was to transform the table that can be queried.

The transformations of the table are mosltly split pivot/unpivot droping nulls. Commented them as the flow goes in the program.

The amount of data proceessed now is comparitvely low now. The Ideal thing in a production enev would using pyspark and sql querying.
