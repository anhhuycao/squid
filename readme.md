# Squid Proxy run as docker (docker-compose)

## Use

You can use the HTTP/HTTPS, ... proxies on your local devices using **port forwarding**. The following SSH command makes the HTTP proxy available to the local device and the private network it uses.

### in Windows

1. run in cmd `ssh -vNL 3128:0.0.0.0:3128 root@<IP>`
2. Go to “Settings” > “Network & internet” > “Proxy.”
3. Under “Manual proxy setup,” toggle the “On” button.
4. Fill in Server : `127.0.0.1` and port : `3128`
5. clik Save

### in Linux

1. run in terminal `ssh -vNL 3128:0.0.0.0:3128 root@<IP>`
2. Set `http/s_proxy` variable

   ```cmd
   export {http,https}_proxy="http://127.0.0.1:3128"
   export {HTTP,HTTPS}_PROXY="http://127.0.0.1:3128"
   ```

Unset in linux

```cmd
unset {http,https}_proxy
unset {HTTP,HTTPS}_PROXY
```
