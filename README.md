## Extract Transform Load (ETL)


Let say, I'm making an application to manage my iTunes music. The goal of this project is to extract my iTunes dataset in XML format into python and load it in desired format back into database.

XML data overview - 
![Capture](https://user-images.githubusercontent.com/47153425/81880159-b4bb7200-955a-11ea-8715-cab7516e0749.PNG)

Using SQLite, I created the database, hitesh_trackdb, and lauched queries into python to tranform the data and load it back into the database.

ETL is a process that extracts the data from different source systems, then transforms the data (like applying calculations, concatenations, etc.) and finally loads the data into the Data Warehouse/ Database system.

# Data Modeling

Data models are made up of entities (objects) and they become the tables in a database. It helps to understand the flow of the data. 
I have designed 3 tables, Artist, Album, Track.The tables are writen in python using sqlite library and are saved in which is used to read,write, retrieve the data.
ETL project.

![web](https://user-images.githubusercontent.com/47153425/81880047-63ab7e00-955a-11ea-9534-651df5538fe7.jpeg)


# Result 

QUERY - 

SELECT t.title, at.name, al.title, t.count
FROM Track t JOIN Album al JOIN Artist at ON t.album_id = al.id 
    AND al.artist_id = at.id
 ORDER BY t.count desc 
 LIMIT 3

![SQL](https://user-images.githubusercontent.com/47153425/81879965-221ad300-955a-11ea-854f-087a1504c695.PNG)
