# g2i
## GIF To Images

Simple PHP endpoint script that gets GIF from Giphy's API and splits it's frames into seperate images.
This was deviced as part of project for [EMF Camp](https://emfcamp.org)'s 2018 camp badge, the [TiLDA MK4](https://badge.emfcamp.org/wiki/TiLDA_MK4 "TiLDA MK4 Wiki").

### Use

Calling this script will return a single number. This denotes the number of frames that the GIF has been split into. Any fetching and/or processing of the frame images will need to be done on the requesters end. The image prefixed with *gif_* followed by a five digit frame number. For example *gif_00000.gif*.

1. **Without Parameters:**
The script can be called without any parameters. This will default to using https://random-word-api.herokuapp.com and will return GIFs related to a random word.

2. **Search Parameter:**
At the moment the script only accepts one parameter *search*. This will return GIFs related to the search phrase. For example:
```giftoimages.php?search={search_phrase}```
 
### To Do
* Add *key* parameter. At the moment Giphy API key is hard coded into PHP.
* Add *type* parameter. Files returned are in GIF. Would be good if user could request the file format required.
* Increase information returned in JSON i.e. status code, list of images, original GIF url, dimensions
