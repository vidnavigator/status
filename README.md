# VidNavigator Status

The public status page of the VidNavigator API: <https://status.vidnavigator.com>.

- `index.html` is the whole page. It reads `status.json` and nothing else.
- `status.json` is written by the hourly API monitoring job, which calls every endpoint end to end on real videos. A call that fails is made again 5 minutes later; if it fails twice the endpoint is marked down and tested every 10 minutes until it passes.
- The page says so when `status.json` is more than 75 minutes old.

`status.json` is generated: do not edit it by hand.
