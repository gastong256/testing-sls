# testing-sls

A simple [Serverless Framework](https://www.serverless.com/) project for testing AWS Lambda and API Gateway deployments.

## Stack

- **Runtime**: Node.js 12.x
- **Framework**: Serverless Framework v3
- **Cloud**: AWS Lambda + API Gateway (Regional)
- **Region**: us-east-1

## Functions

| Function | Handler | Trigger | Description |
|----------|---------|---------|-------------|
| `hello` | `handler.hello` | Direct invocation | Returns a success message and the event input |
| `helloUser` | `handler.helloUser` | `GET /user/{name}` | Returns a personalized greeting |

## Endpoints

```
GET /user/{name}
```

**Example response:**
```json
{
  "message": "Hello John. You're testing sls."
}
```

## Usage

**Deploy:**
```bash
serverless deploy
```

**Invoke `hello` directly:**
```bash
serverless invoke -f hello
```

**Remove stack:**
```bash
serverless remove
```
