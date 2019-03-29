
# Unoficial MAL Client

## Description

My system will allow users to store information about their MyAnimeList account anime and manga lists, update and remove information, check individual item information.

## Entity definition:

Anime/Manga

- Id -  Anime/Manga id.

- Picture - Pictures related to the item.

- Stats - Statistical information related to the item.

- Characters - Fetches the list of characters & staff members of the anime/manga.

- Reviews - String Array - Reviews written by users.

- Recomendation - Recommendations and their weightage made by users.

## API Definition

GET api/anime/Id - Will return all information about anime with certain id.
GET api/anime/Id/Pictures - Will return all pictures about anime with certain id.
GET api/anime/Id/Stats - Will return all stats about anime with certain id.
GET api/anime/Id/characters_staff - Will return all character and staff information about anime with certain id.
GET api/anime/Id/Reviews - Will return all user reviews about anime with certain id.
GET api/anime/Id/Recommendations - Will return all recommendations about anime with certain id.

=========================================================================

GET api/manga/Id - Will return all information about manga with certain id.
GET api/manga/Id/Pictures - Will return all pictures about manga with certain id.
GET api/manga/Id/Stats - Will return all stats about manga with certain id.
GET api/manga/Id/characters - Will return all character and staff information about manga with certain id.
GET api/manga/Id/Reviews - Will return all user reviews about manga with certain id.
GET api/manga/Id/Recommendations - Will return all recommendations about manga with certain id.

=========================================================================

- 200 OK - the request was successful.

- 304 Not Modified - You have the latest data.

- 400 Bad Request - You've made an invalid request or to an invalid endpoint.

- 404 Not Found - MyAnimeList responded with a 404.

- 405 Method Not Allowed - requested method is not supported for resource.

- 429 Too Many Requests - You are being rate limited or Jikan is being rate-limited by MyAnimeList.


UI definition
https://wireframe.cc/vR9Euf


https://github.com/ExampleJenkinsOrg/web-system-template
