## Extract Transform Load (ETL)

Let say, I'm making an application to manage my iTunes music. The goal of this project is to extract my iTunes dataset in XML format into python and load it in desired format back into database.
Using SQLite, I created the database, hitesh_trackdb, and lauched queries to tranform the data and load it back into the database.

ETL is a process that extracts the data from different source systems, then transforms the data (like applying calculations, concatenations, etc.) and finally loads the data into the Data Warehouse/ Database system.

# Data Modeling
Designed 3 tables, Artist, Album, Track.The tables are made in SQLite database which is used to read,write, retrieve the data.
ETL project


# Result 

QUERY - 

SELECT Track.title, Artist.name, Album.title
    FROM Track JOIN Album JOIN Artist 
    ON Track.album_id = Album.id 
        AND Album.artist_id = Artist.id
    ORDER BY Artist.name LIMIT 3
    

![SQL](https://user-images.githubusercontent.com/47153425/81878650-a4a19380-9556-11ea-8d07-bca793387c4b.PNG)
