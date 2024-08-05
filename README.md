这只是一个非常简单的Restful项目，用于生成用于通讯的Token。具体应该如何架构，可以参考声网的Doc: https://docs.agora.io/en/voice-calling/get-started/authentication-workflow?platform=ios

# RTCUserService

User Service of RTC based on LiveKit

### Build

Please build it by: `go build`.

### Deploy

Please run it by shell script with build output.

### Test

You can test by curl command.

```shell
curl -X POST -H "Content-Type: application/json" -d '{
  "apiKey": "devkey",
  "apiSecret": "secret",
  "room": "room1",
  "identity": "user1"
}' http://localhost:9090/getJoinToken
```

it will output:

```JSON
{"token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE2ODc3NjUyNjcsImlzcyI6InlvdXItYXBpLWtleSIsIm5iZiI6MTY4Nzc2MTY2Nywic3ViIjoieW91ci1pZGVudGl0eSIsInZpZGVvIjp7ImNhblB1Ymxpc2giOnRydWUsImNhblN1YnNjcmliZSI6dHJ1ZSwicm9vbSI6InlvdXItcm9vbSIsInJvb21Kb2luIjp0cnVlfX0.AitXsa6THZDQTtHzy6kZOovLZd1ZhPPG9BtPUFa-5hE"}
```
