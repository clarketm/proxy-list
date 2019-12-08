# proxy-list
A list of free, public, forward proxy servers. UPDATED DAILY!
<br>
<br>
[![proxy-list](/proxy.png)](https://github.com/clarketm/proxy-list)

### Download
```bash
# Download and save to local file `proxt-list.txt` with format `IP:PORT`
curl -sSf "https://raw.githubusercontent.com/clarketm/proxy-list/master/proxy-list-raw.txt" > proxy-list.txt
```

### Format
```bash
######################
### proxy-list.txt ###
######################

IP [1]
|
| Port [2]
|   |
|   | Country [3]
|   |   |
|   |   | Anonymity [4]
|   |   |  |
|   |   |  |  Type [5]
|   |   |  |   |_ _ _ _
|   |   |  |_ _ _ _ _  | Google passed [6]
|   |   |_ _ _ _ _   | |  |
|   |_ _ _ _ _    |  | |  |
|             |   |  | |  |
200.2.125.90:8080 AR-N-S! +


1. IP address
2. Port number
3. Country code
4. Anonymity
   N = No anonymity
   A = Anonymity
   H = High anonymity
5. Type
     = HTTP
   S = HTTP/HTTPS
   ! = incoming IP different from outgoing IP
6. Google passed
   + = Yes
   – = No


#############################
### proxy-list-status.txt ###
#############################

IP [1]
|
| Status [2]
|   |_ _ _ _ _
|             |
200.2.125.90: success


1. IP address
2. Status
   success = low latency (0-9 seconds)
   failure = high latency (10+ seconds)
```

### API
[PubProxy](http://pubproxy.com/) provides a free, robust [API](http://pubproxy.com/#settings) to narrow down the proxy to your desired specification.

```bash
#######################################################################
#     PARAMETER             VALUES                DESCRIPTION         #
#######################################################################
# FORMAT          | json, txt             | Output format
# LEVEL           | anonymous, elite      | Anonymity level
# TYPE            | http, socks4, socks5  | Proxy protocol
# LAST_CHECK      | 1-1000                | Last check time (in minutes)
# LIMIT           | 1-20                  | Proxy results count
# COUNTRY         | US,CA,...             | Country of the proxy
# NOT_COUNTRY     | MX,CA,...             | Avoid proxy country
# PORT            | `Number`              | Specify port number
# GOOGLE          | `Boolean`             | Google passed proxies
# HTTPS           | `Boolean`             | Supports HTTPS request
# GET             | `Boolean`             | Supports GET request
# POST            | `Boolean`             | Supports POST request
# USER_AGENT      | `Boolean`             | Supports COOKIES request
# COOKIES         | `Boolean`             | Supports USER_AGENT request
# REFERER         | `Boolean`             | Supports REFERER request

#######################################################################
#                           EXAMPLES                                  #
#######################################################################

#######################################################################
# Retrieve one(1) socks5 proxy.                                       #
#######################################################################
curl "http://pubproxy.com/api/proxy?limit=1&format=txt&type=socks5"
> 110.73.11.181:8123

#######################################################################
# Retrieve two(2) http proxies from the US that support https.        #
#######################################################################
curl "http://pubproxy.com/api/proxy?limit=2&format=txt&http=true&country=US&type=http"
> 195.136.43.176:63909
> 107.170.221.216:8080
```

### References
* [ISO 3166-1 alpha-2 country code](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
* [Google passed proxy](https://www.my-proxy.com/blog/google-proxies-dead)

## :star: Credits
Proxy server data courtesy of:
* [Proxyspy](http://spys.one/en/)
* [PubProxy](http://pubproxy.com/)
