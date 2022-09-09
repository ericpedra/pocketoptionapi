# pocketoptionapi

Website    : https://autotradevip.com/en/  
Olmyptrade : https://youtu.be/zTZT7zDlmtU  
Binomo     : https://youtu.be/ww9rVMX5TK4  
IQ Option  : https://youtu.be/4i3YUEDRGWY  
Quotex     : https://www.youtube.com/channel/UCCqnm8XHUoc0Ude78RJwmoA  
Expert Option     : https://www.youtube.com/channel/UCCqnm8XHUoc0Ude78RJwmoA

### Import
```python
from pocketoptionapi.stable_api import PocketOption
```

### Login by ssid
if connect sucess return True,None  

if connect fail return False,None  
```python
from pocketoptionapi.stable_api import PocketOption
ssid="""42["auth",{"session":"a:4:{s:10:\"session_id\";s:32:\"123123123123\";s:10:\"ip_address\";s:12:\"2.111.11.5\";s:10:\"user_agent\";s:104:\"Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.77 Safari/537.36\";s:13:\"last_activity\";i:123232;}1232321213","isDemo":0,"uid":"123232132"}]"""
account=PocketOption(set_ssid=ssid)
check_connect,message=account.connect()
print(check_connect,message)
```
### Check_win & buy sample

```python
from pocketoptionapi.stable_api import PocketOption
ssid="""42["auth",{"session":"a:4:{s:10:\"session_id\";s:32:\"123123123123\";s:10:\"ip_address\";s:12:\"2.111.11.5\";s:10:\"user_agent\";s:104:\"Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.77 Safari/537.36\";s:13:\"last_activity\";i:123232;}1232321213","isDemo":0,"uid":"123232132"}]"""
account=PocketOption(set_ssid=ssid)
check_connect,message=account.connect()
if check_connect:
    account.change_balance("PRACTICE")#"REAL"
    id = API.buy("AUDCAD_otc", "14000", "put", "60")
    print(API.check_win(id))
```
