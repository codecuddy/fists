# fists
Say hello

GET or POST https://fists.azurewebsites.net/api/fists
`Say hello to my friends LEFT and RIGHT`

## Purpose
This is a proof-of-concept Slack app. It serves little actual purpose, but it is fun.

## Running locally
`dotnet run`

Get
```
curl -k "https://localhost:5001/api/fists"
```

Post
```
curl -k -X POST -H "content-type: application/x-www-form-urlencoded" -d "text=one+and+two" "https://localhost:5001/api/fists"
```

Post to WebHook
```
curl -k -X POST -H "content-type: application/x-www-form-urlencoded" -d "text=one+and+two" "https://localhost:5001/api/fists/WebHook"
```

Note:
To use WebHook, you need to set the environment variable WEBHOOKURL before you `dotnet run`

```bash
export WEBHOOKURL="https://hooks.slack.com/services/[YOUR/WEBHOOK/URL]"
dotnet run
```

```cmd
set WEBHOOKURL=https://hooks.slack.com/services/[YOUR/WEBHOOK/URL]
dotnet run
```
