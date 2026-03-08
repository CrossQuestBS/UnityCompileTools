# UnityCompileTools


## Windows

How to get manifest to find correct Image Layer
```
curl -so "token.json" "https://auth.docker.io/token?service=registry.docker.io&scope=repository:unityci/editor:pull";
token=$(cat token.json | jq -jr ".token")

curl -o manifest.json -H "Authorization: Bearer ${token}" https://registry-1.docker.io/v2/unityci/editor/manifests/windows-6000.0.40f1-base-3.2
```