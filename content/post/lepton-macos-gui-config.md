---
Title: Lepton Snippet Manager GUI Config
date: 2021-01-18T10:14:24-05:00
draft: true
---

## `~/.leptonrc` 

```json

{
    "theme": "dark",
    "autoUpdate": false,
    "snippet": {
        "expanded": true,
        "newSnippetPrivate": true,
        "sorting": "updated_at", 
        "sortingReverse": true
    },
    "editor" : {
        "tabSize": 4,
        "validateFilename": true
    },
    "userPanel": {
        "hideProfilePhoto": false
    },
    "logger": {
        "level": "debug"
    },
    "proxy": {
        "enable": false,
        "address": "socks://localhost:1080"
    },
    "notifications": {
        "success": true,
        "failure": true
    },
    "shortcuts": {
        "keyShortcutForSearch": "CMD+F",
        "keyNewGist": "CommandOrControl+N",
        "keyEditGist": "CommandOrControl+E",
        "keySubmitGist": "CommandOrControl+S",
        "keyImmersiveMode": "CommandOrControl+I",
        "keyAboutPage": "CommandOrControl+,",
        "keyDashboard": "CommandOrControl+D",
        "keyEditorExit": "CommandOrControl+Escape",
        "keySyncGists": "CommandOrControl+R"
    },
    "enterprise": {
        "enable": false,
        "host": "github_enterprise_host",
        "token": "token_with_gist_enabled",
        "avatarUrl": "optional_avatar_url"
    }
}
```
