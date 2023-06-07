

# Webapps for Windows® !
Turn your favourite websites into full desktop applications.





![Logo](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/th5xamgrr6se0x5ro4g6.png)





## Features

- Lightweight (under 300KB).
- Autodetects installed browsers.
- Extensible (Ability to add custom browsers and commandline arguments).
- Portable (You can export and share your setup across all your devices).
- Supports legacy Windows versions (Windows 7 or later).

## Screenshots

![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)


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
| `args` | `string` | **Required, Can be empty**. Additional arguments to be passed to the browser.|
| `icon_uri` | `string` | **Required**. References the absolute path of the webapp icon. |
| `isInPrivate` | `boolean` | **Required**. Indicates whether the webapp runs in incognito mode or not. |
| `isIsolated` | `boolean` | **Required**. Indicates whether the webapp runs in a sandbox or not. |
| `browser` | `string` | **Required + Case sensitive**. Contains the exact name of the browser that runs the webapp, **should match it's exact name in the Windows registry**   |









## FAQ

#### Question 1

Answer 1

#### Question 2

Answer 2

