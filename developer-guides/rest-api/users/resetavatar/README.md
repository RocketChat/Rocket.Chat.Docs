# Reset Avatar

Reset a user’s avatar.

| URL | Requires Auth | HTTP Method |
| :--- | :--- | :--- |
| `/api/v1/users.resetAvatar` | `yes` | `POST` |

## Payload

| Argument | Example | Required | Description |
| :--- | :--- | :--- | :--- |
| `userId` or `username` | `BsNr28znDkG8aeo7W` | Required | The id or username of the user. |

## Example Call - Via userId

```bash
curl -H "X-Auth-Token: 9HqLlyZOugoStsXCUfD_0YdwnNnunAJF8V47U3QHXSq" \
     -H "X-User-Id: aobEdbYhXfu5hkeqG" \
     -H "Content-type:application/json" \
     http://localhost:3000/api/v1/users.resetAvatar \
     -d '{ "userId": "BsNr28znDkG8aeo7W" }'
```

## Example Result

```json
{
  "success": true
}
```

## Example Call - Via username

```bash
curl -H "X-Auth-Token: 9HqLlyZOugoStsXCUfD_0YdwnNnunAJF8V47U3QHXSq" \
     -H "X-User-Id: aobEdbYhXfu5hkeqG" \
     -H "Content-type:application/json" \
     http://localhost:3000/api/v1/users.resetAvatar \
     -d '{ "username": "test" }'
```

## Example Result

```json
{
  "success": true
}
```

## Change Log

| Version | Description |
| :--- | :--- |
| 0.55.0 | Added |
