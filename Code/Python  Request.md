# Python Reqeust

### 如何用selenium set a browser and pass it to the requests
```python
import requests
from selenium import webdriver

driver = webdriver.Firefox()
url = "some_url" #a redirect to a login page occurs
driver.get(url)

#storing the cookies generated by the browser
request_cookies_browser = driver.get_cookies()

#making a persistent connection using the requests library
params = {'os_username':'username', 'os_password':'password'}
s = requests.Session()

#passing the cookies generated from the browser to the session
c = [s.cookies.set(c['name'], c['value']) for c in request_cookies_browser]

resp = s.post(url, params) #I get a 200 status_code

#passing the cookie of the response to the browser
dict_resp_cookies = resp.cookies.get_dict()
response_cookies_browser = [{'name':name, 'value':value} for name, value in dict_resp_cookies.items()]
c = [driver.add_cookie(c) for c in response_cookies_browser]

#the browser now contains the cookies generated from the authentication    
driver.get(url)
```

### Install Selenium

```python=
# selenium 4
from selenium import webdriver
from selenium.webdriver.edge.service import Service
from webdriver_manager.microsoft import EdgeChromiumDriverManager

driver = webdriver.Edge(service=Service(EdgeChromiumDriverManager().install()))
```