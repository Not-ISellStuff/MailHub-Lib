# MailHub-Lib
Library made for checking whether an email is valid or not.

# Mail Providers Supported

```
There's only one mail provider supported atm
More will be added soon, if you have any suggestions dm me on discord

Discord: isell_termed_again

1. Microsoft [Outlook, Hotmail, Skype, Live, etc]
```

# How To Use

```
1. First you make sure you have this library installed or just drag the python file where your python program is located

2. Make a class and now you can use the lib. Example below this message
```

```python
from mailhub import MailHub

mail = MailHub()

proxy = {
            'http': f'http://{proxy}:{port}',
            'https': f'http://{proxy}:{port}',
        }
email = "admin@outlook.com"
password = "password123"

# the login function will always have 3 arguments no matter what checker it is
r = mail.loginMICROSOFT(email, password, proxy)

# or if you want to make a proxyless request you can do:
# r = mail.loginMICROSOFT(email, password, None)

"""
All Possible Responses:

ok - valid account
nfa - 2fa
fail - account is invalid
retry - request was a failure
custom - locked account
"""

response = r[0] # the login function might return more than 1 thing

if response == "ok":
   print("[+] Valid Account")

```
