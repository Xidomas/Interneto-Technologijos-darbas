
# MAL Manga Client

## Description

My system will allow users to store information about their MyAnimeList account anime and manga lists, update and remove information, check individual item information.

## Entity definition:

Manga

- Id - Anime/Manga id. (Integer Max 10)

- Picture - Pictures related to the item. (String Max 70)

- Stats - Statistical information related to the item. (String Array 50)

- Characters - Fetches the list of characters & staff members of the anime/manga. (String Array Max 20)

- Reviews - Reviews written by users. (String Array Max 15)

- Recomendation - Recommendations and their weightage made by users. (String Array Max 5)

## API Definition

GET api/manga/:Id - Will return all information about manga with certain id.

- 400 Bad Request - You've made an invalid request or to an invalid endpoint.

- 404 Not Found - MyAnimeList responded with a 404.

GET api/manga/:Id/Pictures - Will return all pictures about manga with certain id.

- 400 Bad Request - You've made an invalid request or to an invalid endpoint.

- 404 Not Found - MyAnimeList responded with a 404.

GET api/manga/:Id/Stats - Will return all stats about manga with certain id.

- 400 Bad Request - You've made an invalid request or to an invalid endpoint.

- 404 Not Found - MyAnimeList responded with a 404.

GET api/manga/:Id/Characters - Will return all character and staff information about manga with certain id.

- 400 Bad Request - You've made an invalid request or to an invalid endpoint.

- 404 Not Found - MyAnimeList responded with a 404.

GET api/manga/:Id/Reviews - Will return all user reviews about manga with certain id.

- 400 Bad Request - You've made an invalid request or to an invalid endpoint.

- 404 Not Found - MyAnimeList responded with a 404.

GET api/manga/:Id/Recommendations - Will return all recommendations about manga with certain id.

- 400 Bad Request - You've made an invalid request or to an invalid endpoint.

- 404 Not Found - MyAnimeList responded with a 404.

POST /mangalist/:Id - Will save into/update mangalist entries.

- 400 Bad Request - You've made an invalid request or to an invalid endpoint.

- 404 Not Found - MyAnimeList responded with a 404.

DELETE /mangalist/:Id - Will delete existant entry in the mangalist.

- 400 Bad Request - You've made an invalid request or to an invalid endpoint.

- 404 Not Found - MyAnimeList responded with a 404.

=========================================================================

UI definitions:

https://wireframe.cc/Kddyl0

https://wireframe.cc/uuUFp7
