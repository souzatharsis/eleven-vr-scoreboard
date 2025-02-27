# ElevenVR Live Scoreboard
Live scoreboard for the [ElevenVR](https://www.elevenvr.net/) Table Tennis game, useful for streamers.

![image](https://user-images.githubusercontent.com/1384885/119359058-80b87800-bca9-11eb-8570-310fb80159f7.png)

![image](https://user-images.githubusercontent.com/1384885/119359118-92018480-bca9-11eb-9816-91d427e38566.png)

# How to use

1. Open this page: **https://cristy94.github.io/eleven-vr-scoreboard/**
2. Enter the userID (can be found by clicking on the UserID label, searching for the username and copying the ID shown in the URL)
3. The latest match of that user is displayed and the score is refreshed every 3 seconds.

## Usage with OBS

You can overlay the scoreboard over your stream, it will always show the score of the current match that you are playing.

1. Add a new "Browser" source
2. Point the URL to the scoreboard, setting the userID in the `?user=1234` query parameter, like this:
`https://cristy94.github.io/eleven-vr-scoreboard/?user=1234`
![image](https://user-images.githubusercontent.com/1384885/117724984-cd4d7f00-b1e4-11eb-9d2f-63a90de5a0bc.png)  
3. Resize and crop the browser area (you can crop by dragging resize handles while holding ALT).


## Extra features

### Fixing matches score

If the matches score is wrong you can offset it using query params `home-offset` and `away-offset`, like this: 

?user=1234&**home-offset=1&away-offset=-2**


## How it works

* The [ElevenVR API](https://www.elevenvr.club/accounts/60531/matches) is used to get the latest 10 matches of the given userID.
* The rounds/scores of the last match are currently shown.
* The scoreboard is refreshed every 3 seconds.
* If two players played multiple consecutive games as their latest games, the matches score between the two players is also displayed.

## Changelog

```
28 May 2021
* Fixed match score count during the first game
* Shown ELO score is now rounded
* Scoreboard has rounded corners and expands to fit the number of sets
* Different style when a set is undergoing (red letters) vs when it's over (white letters)
* Different style when a match is over (winner score of each set is highlighted)
* Slightly decreased scoreboard background opacity
```

## Planned features

1. Directly search for the username/userID in the scoreboare
2. Improved design and different themes.


Keywords: Eleven Table Tennis, OBS Stream Overlay, Twitch Overlay, Live Scoreboard, ElevenVR Scoreboard Overlay, ElevenVR show scores, Eleven Oculus Stream video overlay
