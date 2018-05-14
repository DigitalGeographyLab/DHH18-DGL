# Datasets for the Helsinki Digital Humanities Hackathon 2018

This repository describes the datasets provided by the Digital Geography Lab for the Helsinki Digital Humanities Hackathon 2018.

The datasets come from three different social media platforms: Flickr, Instagram and Twitter. The column names and their descriptions for each dataset are provided below.

### Flickr

See also [Flickr API Documentation](https://www.flickr.com/services/api/) for more details. 


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
| tweets_cnt     | integer                     | int4                                   |
| timezone       | text                        | Timezone                               |
| user_location  | text                        | User's self-reported home location     |
| twitter_lang   | text                        | Language                               |
