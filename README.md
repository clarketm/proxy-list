# proxy-list
A list of free, public, forward proxy servers.

### Download
```bash
# Download and save to local file `proxt-list.txt` with format `IP:PORT`
curl -s "https://raw.githubusercontent.com/clarketm/proxy-list/master/proxy-list.txt" | sed '1,3d; $d; s/\s.*//g;' > proxy-list.txt
```

### Format
```
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
```

### References
* [ISO 3166-1 alpha-2 country code](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
* [Google passed proxy](https://www.my-proxy.com/blog/google-proxies-dead)

## :star: Credits
Proxy server data courtesy of: 
* [Proxyspy](http://txt.proxyspy.net/proxy.txt)
