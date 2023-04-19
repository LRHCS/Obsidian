#Tools 
an install many developement tools(python, nodejs.....)

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
irm get.scoop.sh | iex
# You can use proxies if you have network trouble in accessing GitHub, e.g.
irm get.scoop.sh -Proxy 'http://<ip:port>' | iex
```