# Files.Models.UserSftpClientUse

## Example UserSftpClientUse Object

```
{
  "id": 1,
  "sftp_client": "example",
  "created_at": "2000-01-01T01:00:00Z",
  "updated_at": "2000-01-01T01:00:00Z",
  "user_id": 1
}
```

* `id` / `id`  (int64): UserSftpClientUse ID
* `sftp_client` / `sftpClient`  (string): The SFTP client used
* `created_at` / `createdAt`  (date-time): The earliest recorded use of this SFTP client (for this user)
* `updated_at` / `updatedAt`  (date-time): The most recent use of this SFTP client (for this user)
* `user_id` / `userId`  (int64): ID of the user who performed this access


---

## List User SFTP Client Uses

```
ListIterator<UserSftpClientUse> userSftpClientUse = UserSftpClientUse.list(
    
    HashMap<String, Object> parameters = null,
    HashMap<String, Object> options = null
)
```

### Parameters

* `user_id` (Long): User ID. If provided, will return uses for this user.
* `cursor` (String): Used for pagination.  When a list request has more records available, cursors are provided in the response headers `X-Files-Cursor-Next` and `X-Files-Cursor-Prev`.  Send one of those cursor value here to resume an existing list from the next available record.  Note: many of our SDKs have iterator methods that will automatically handle cursor-based pagination.
* `per_page` (Long): Number of records to show per page.  (Max: 10,000, 1,000 or less is recommended).
