
# Telegram bot for copy trading - TG client

## The goal of this project

<br>This app is created to enable copytrading on FX/Crypto markets using signals from Telegram groups/channels. It works with Telethon Python lib in async i/o mode.
Completely customizable.<br>
Please send me a request for full code access or beta testing

## Usage

1. Download the docker container.
2. Update the `API_ID`, `API_HASH` and `APP_NAME` in config/config.yml. For API key and id go to https://my.telegram.org/apps
3. Configure your channels sources using python3 tg_config.py and enable/disable channels using the menu and quit.
4. Run the app using python3 tg_client.py

## Examples

### Original signal
```
Text and some extra content >>>>> BTC[USDT]
LONG[SHORT]  [9999] [market] [limit]
[Leverage] [X10]
Take|TP|TARGET 1  <> 10000
Take|TP|TARGET 2  <> 20000
Take|TP|TARGET 3  <> 30000
Take|TP|TARGET 4  <> 40000
SL|Stop : 9988
<<<<< Text
```

### Translated to JSON format signal
```json
{"symbol": "GALAUSDT", "direction": "LONG", "is_market": "ENTRY", "leverage": "10", "market_price": "0.02675", "tp_price1": "0.02702", "tp_price2": "0.02729", "tp_price3": "0.02782", "tp_price4": "0.02836", "sl_price": "0.02541"}
```


 ###  Example and structure overview <br>
 ([https://youtu.be/9APNx15A-dQ](https://www.youtube.com/watch?v=2yxfjEfxPMI))
