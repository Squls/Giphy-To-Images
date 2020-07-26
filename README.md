# g2i
## GIF To Images

Simple PHP endpoint script that gets GIF from Giphy's API and splits it's frames into seperate images.
This was deviced as part of project for [EMF Camp](https://emfcamp.org)'s 2018 camp badge, the [TiLDA MK4](https://badge.emfcamp.org/wiki/TiLDA_MK4 "TiLDA MK4 Wiki").

### Use

Calling this script will return JSON containing information on the original GIF and the resulting generated frames.

Example response:
```
{
"searchphrase":"cat",
"files": {
	"total":112,
	"filelist":["imgs\/gif_00000.gif","imgs\/gif_00001.gif","imgs\/gif_00002.gif"],
},
"original": {
	"url":"https:\/\/media0.giphy.com\/media\/Lp5wuqMOmLUaAd0jBG\/200.gif",
	"dimensions":{
		"width":"200",
		"height":"200"
		}
	}
}
```

1. **Without Parameters:**
The script can be called without any parameters. This will default to using [Random Word API](https://random-word-api.herokuapp.com) and will return GIFs related to a random word.

2. **Search Parameter:**
At the moment the script only accepts one parameter *search*. This will return GIFs related to the search phrase. For example:
```giftoimages.php?search={search_phrase}```
 
### To Do
* Add parameters:
**key** - At the moment Giphy API key is hard coded into PHP.
**type** - Files are returned are as GIFs. Would be good if user could request the file format required.
* Increase information returned in JSON:
status code
~~list of images~~
~~original GIF url~~
~~dimensions~~
response time
~~search phrase~~
file info
