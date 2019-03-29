
## Unoficial MAL Client

My system will allow users to store information about their MyAnimeList account, update and remove information.

## Entity definition:

Anime/Manga

- Id - Integer - Anime/Manga id.

- Picture - String - Link to a picture.

- Stats - String Array - Statistical information related to the item.

- Characters - String Array, Fetches the list of characters & staff members of the manga.

- Reviews - String Array - Reviews written by users

- Recomendation - Recommendations and their weightage made by users.



## API 

GET api.jikan.moe/anime/Id - Will return all information about anime with certain id.

GET api.jikan.moe/manga/Id - Will return all information about manga with certain id.


- 200 OK - the request was successful.

- 304 Not Modified - You have the latest data.

- 400 Bad Request - You've made an invalid request or to an invalid endpoint.

- 404 Not Found - MyAnimeList responded with a 404.

- 405 Method Not Allowed - requested method is not supported for resource.

- 429 Too Many Requests - You are being rate limited or Jikan is being rate-limited by MyAnimeList.


UI definition
https://wireframe.cc/vR9Euf


https://github.com/ExampleJenkinsOrg/web-system-template
