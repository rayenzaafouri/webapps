
## Structure of the browser's configuration file

#### The configuration is stored in '/user/config.json' inside the application folder.
it contains the browser's name followed by a set of properties.
```json
{
    "Google Chrome": {
        "binary": "start chrome",
        "url-specifier" : "--app=",
        "incognito" : "--incognito",
        "isolation" : "--sandbox"
    }
}
```


| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `binary` | `string` | **Required**. Command used to launch the browser on your system. |
| `url-specifier` | `string` | **Required**. A prefix used to provide the website to the browser as an argument. |
| `incognito` | `string` | **Required**. Argument that forces the browser to run in incognito mode. |
| `isolation` | `string` | **Required**. Argument that runs the browser in sandbox mode. |




## Structure of the user apps configuration file

#### The configuration is stored in '/user/config.json' inside the application folder.
it holds the apps created by the user.
```json
{
    "uaid": "07062023125801756",
    "name": "OUTLOOK",
    "args": "",
    "app_uri": "https://outlook.live.com/mail/0/",
    "icon_uri": "C:\\Users\\User1\\Documents\\WebAppsForWindows\\user\\07062023125801756.png",
    "isIsolated": false,
    "isInPrivate": true,
    "browser": "Microsoft Edge"
  }
```


| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `uaid` | `string` | **Do not alter**. Unique identfier for the application automatically generated during the creation pocess. |
| `name` | `string` | **Required and can be empty.** Webapp display name. |
| `incognito` | `boolean` | **Required**. Indicates whether the webapp runs in incognito or not. |
| `isolation` | `boolean` | **Required**. Indicates whether the webapp runs in a sandbox or not.. |
| `browser` | `string` | **Required + Case sensitive**. Indicates the name of the browser that runs the webapp, **should match it's exact name in the Windows registry**   |
