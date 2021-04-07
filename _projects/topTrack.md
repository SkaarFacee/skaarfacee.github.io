---
name: Top Track  line
tools: [Spotify,Command]
image: https://www.kindpng.com/picc/m/108-1084830_spotify-logo-png-download-transparent-png.png
description: Command line based application that gives you the top songs and albums of an artist 
---
This is a CLI application that uses spotify API to give users the top 3 albums and artists of a song writer in Spotify

## Tech Stack 
### Spotfy Web API
The Spotify Web API is based on REST principles. Data resources are accessed via standard HTTPS requests in UTF-8 format to an API endpoint. Where possible, Web API uses appropriate HTTP verbs for each action:

---

Method&nbsp;&nbsp;&nbsp;Action <br>
GET&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; :Retrieves resources<br>
POST&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 	:Creates resources<br>
PUT&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 	:Changes and/or replaces resources or collections<br>
DELETE&nbsp;&nbsp;&nbsp;&nbsp; 	:Deletes resources<br>

---

### argparse pythone module
The argparse module makes it easy to write user-friendly command-line interfaces. The program defines what arguments it requires, and argparse will figure out how to parse those out of sys.argv. The argparse module also automatically generates help and usage messages and issues errors when users give the program invalid arguments.

# Running the code
1. Clone the repo, such that you have the script in your device
```sh
git clone https://github.com/adiaux/SpotifyTopTrack.git
```
2. Save your token in a file `secret.py` in the variable spotify_token

3. Script is ready to run. 
```sh
python3 app.py -h
```
## API Reference
The documentation to understand and use Spotify api is 
> [Spotify API](https://developer.spotify.com/documentation/web-api/reference/) 
