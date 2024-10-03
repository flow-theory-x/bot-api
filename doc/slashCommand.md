コマンド定義 CURL

command.json

```
{
    "name": "hello",
    "description": "Responds with a greeting",
    "options": []
}
```

BOT_TOKEN=ボットのトークン
BOT_API_ID=アプリケーションの ID
COMMAND_ID=コマンドの ID

```
curl -X POST -H "Authorization: Bot ${BOT_TOKEN}" \
    -H "Content-Type: application/json" \
    --data-binary @command.json \
    https://discord.com/api/v10/applications/${BOT_API_ID}/commands
```

### 検索

```
curl -X GET -H "Authorization: Bot ${BOT_TOKEN}" \
    https://discord.com/api/v10/applications/${BOT_API_ID}/commands

```

### 削除

```
curl -X DELETE -H "Authorization: Bot ${BOT_TOKEN}" \
    https://discord.com/api/v10/applications/${BOT_API_ID}/commands/${COMMAND_ID}

```
