# Social media data from Helsinki

This repository describes the datasets provided by the Digital Geography Lab for the [Helsinki Digital Humanities Hackathon 2018](https://www.helsinki.fi/en/helsinki-centre-for-digital-humanities/helsinki-digital-humanities-hackathon-2018-dhh18), and [the introduction to advanced geoinformatics course 2019](https://courses.helsinki.fi/fi/geog-g301). 

The datasets come from three different social media platforms: Flickr, Instagram and Twitter. 

|Name |Number of records  |Number of users|Temporal extent |Spatial extent|
|-----------|------------------|-------------|--------------|--------------|
|Flickr            |126017        |2701     |01 JAN 2014 – 07 OCT 2017 |Helsinki Region |
|Instagram|1316705    |207329|01 JUN 2014 – 31 MAR 2016 | Helsinki Region|
|Twitter        |61338            |9260    |17 FEB 2016  – 02 MAR 2018|Helsinki Municipality |


The data have been collected usingcustom python-tools into a postgreSQL/PostGIS database. For methods, see [Tenkanen et al. 2017](https://www.nature.com/articles/s41598-017-18007-4). Data sets described in this repository have been subset to the Helsinki Region. In the digital humanities hackathon, the data were provided in EPSG:4326 projection. For the introduction to advanced GIS course, the data have been projected from EPSG:4326 to EPSG:3879 coordinate reference system following [this documentation](https://github.com/csc-training/geocomputing/blob/master/pouta/postgis/basic_postgis_management.md#spatial-data-management). Columns containing usernames have been removed.

The column names and their descriptions for each dataset are provided below. Columns containing usernames have been removed.

### Flickr

See also [Flickr API Documentation](https://www.flickr.com/services/api/) for more details. Data has been collected in autumn 2017.


| column_name       | data_type        | Description                                                                                                                |
|-------------------|------------------|----------------------------------------------------------------------------------------------------------------------------|
| id                | integer          | Database identifier                                                                                                        |
| userid            | text             | Unique identifier for user                                                                                                 |
| time_local        | timestamp        | Local time (Format: year-month-day hour:minutes:seconds)                                                                   |
| text1             | text             | Title of the photo                                                                                                         |
| hashtags          | text             | Tags associated with the photo                                                                                             |
| text2             | text             | Additional description of the photo                                                                                        |
| photoid           | bigint           | Unique identifier of the photo                                                                                             |
| photourl          | text             | Link to photo                                                                                                              |
| license           | smallint         | Photo license. See explanation of codes in [Flickr API](https://www.flickr.com/services/api/flickr.photos.licenses.getInfo.html) |
| lat               | double precision | Latitude (decimal degrees)                                                                                                 |
| lon               | double precision | Longitude (decimal degrees)                                                                                                |
| geom              | geometry         | PostGIS geometry object in EWKB format                                                                                     |
| user_location     | text             | User's self-reported home location                                                                                         |
| views             | integer          | Number of views                                                                                                            |
| likes             | integer          | Number of faves                                                                                                            |
| likers            | text             | List of users who have faved this photo                                                                                    |
| comm_cnt          | smallint         | Number of comments                                                                                                         |
| comm_txt          | text             | List of comments                                                                                                           |
| comm_user         | text             | List of commenting userids                                                                                                 |
| flickr_lang       | character        | Language of the Flickr profile                                                                                             |

### Instagram

See also [Instagram API Documentaion](https://www.instagram.com/developer/endpoints/) for more details. Data has been collected in spring 2016.

| column_name    | data_type        | Description                                              |
|----------------|------------------|----------------------------------------------------------|
| id             | integer          | Database identifier                                      |
| userid         | bigint           | Unique identifier for user                               |
| text           | text             | Caption text                                             |
| hashtags       | text             | Hashtags within the caption                              |
| location_name  | text             | Location name                                            |
| time_local     | timestamp        | Local time (Format: year-month-day hour:minutes:seconds) |
| lat            | double precision | Latitude (decimal degrees)                               |
| lon            | double precision | Longitude (decimal degrees)                              |
| geom           | geometry         | PostGIS geometry object in EWKB format                   |
| likes          | integer          | Number of likes                                          |
| liker_ids      | text             | User ids of likers                                       |
| photourl       | text             | Link to photo                                            |
| photoid        | text             | Unique identifier for photo                              |
| users_in_photo | text             | list of userids in the photo                             |
| medialink      | text             | Link to full instagram post                              |
| comm_cnt       | integer          | Number of comments                                       |
| comm_txt       | text             | List of comments                                         |
| comm_user      | text             | List of commenting userids                               |


### Twitter 

Check out [tweepy](http://tweepy.readthedocs.io/en/v3.5.0/) and [Twitter API documentation](https://developer.twitter.com/en/docs/api-reference-index)for more details. Data has been continuously collected until 02 MAR 2018. 

| column_name    | data_type                   | Description                            |
|----------------|-----------------------------|----------------------------------------|
| id             | integer                     | Database identifier                    |
| userid         | bigint                      | Unique identifier for user             |
| description    | text                        | User profile description               |
| time_local     | timestamp without time zone | timestamp                              |
| text           | text                        | Tweet text                             |
| lat            | double precision            | Latitude (decimal degrees)             |
| lon            | double precision            | Longitude (decimal degrees)            |
| geom           | geometry                    | PostGIS geometry object in EWKB format |
| reply_to_tweet | bigint                      | Tweet id: Reply to tweet               |
| reply_to_user  | bigint                      | Userid: Reply to user                  |
| followers_cnt  | integer                     | Number of followers                    |
| tweets_cnt     | integer                     | Number of tweets per user in total     |
| timezone       | text                        | Timezone                               |
| user_location  | text                        | User's self-reported home location     |
| twitter_lang   | text                        | Language                               |
