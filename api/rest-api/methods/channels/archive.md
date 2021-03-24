# Channel Archive

## Channel Archive

Archives a channel.

| URL | Requires Auth | HTTP Method |
| :--- | :--- | :--- |
| `/api/v1/channels.archive` | `yes` | `POST` |

### Payload

| Argument | Example | Required | Description |
| :--- | :--- | :--- | :--- |
| `roomId` | `ByehQjC44FwMeiLbX` | Required | The channel's id |

### Example Call

```bash
curl -H "X-Auth-Token: 9HqLlyZOugoStsXCUfD_0YdwnNnunAJF8V47U3QHXSq" \
     -H "X-User-Id: aobEdbYhXfu5hkeqG" \
     -H "Content-type: application/json" \
     http://localhost:3000/api/v1/channels.archive \
     -d '{ "roomId": "ByehQjC44FwMeiLbX" }'
```

### Example Result

```javascript
{
   "success": true
}
```

## Bad Request Example Result

If the channel is already archived, it will return a `400 bad request` status.

```javascript
{
   "success": false,
   "error": "The channel, {Channel name}, is archived [error-room-archived]",
   "errorType": "error-room-archived"
}
```

### Change Log

| Version | Description |
| :--- | :--- |
| 0.48.0 | Added |

