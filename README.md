# DigitalHumanitiesHack2018
Description of the Digital Humanities Hackathon datasets 

- Flickr
- Instagram
- Twitter


### Flickr Data

See also [Flickr API Documentation](https://www.flickr.com/services/api/) for more details. 


| column_name       | data_type        | Description                                                                                                                |
|-------------------|------------------|----------------------------------------------------------------------------------------------------------------------------|
| id                | integer          | Database identifier                                                                                                        |
| userid            | text             | Unique identifier for user                                                                                                 |
| time_local        | timestamp        | Local time (Format: year-month-day hour:minutes:seconds)                                                                   |
| text              | text             | Title of the photo                                                                                                         |
| hashtags          | text             | Tags associated with the photo                                                                                             |
| photo_description | text             | Additional description of the photo                                                                                        |
| photoid           | bigint           | Unique identifier of the photo                                                                                             |
| photourl          | text             | Link to photo                                                                                                              |
| license           | smallint         | Photo license. See explanation of codes in [Flickr API](https://www.flickr.com/services/api/flickr.photos.licenses.getInfo.html) |
| lat               | double precision | Latitude (decimal degrees)                                                                                                 |
| lon               | double precision | Longitude (decimal degrees)                                                                                                |
| geom              | geometry         | PostGIS geometry object in EWKB format                                                                                     |
| location_name     | text             | User's self-reported home location                                                                                         |
| views             | integer          | Number of views                                                                                                            |
| likes             | integer          | Number of faves                                                                                                            |
| likers            | text             | List of users who have faved this photo                                                                                    |
| comm_cnt          | smallint         | Number of comments                                                                                                         |
| comm_txt          | text             | List of comments                                                                                                           |
| comm_user         | text             | List of commenting userids                                                                                                 |
| flickr_lang       | character        | Language of the Flickr profile                                                                                             |




### Instagram Data

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


