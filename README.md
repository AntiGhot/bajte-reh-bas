# bajte-reh-bas
BRB : Bajte Reh Bas : An Appsmith template which can be used to develop an Audio Streaming App, currently based on Spotify Web API 

<br>
This is just a reference example for developers when :

- building an Appsmith App
- working with Spotify Web APIs
  

<br>

> Also, You **must not** offer Audio Preview Clips as a standalone service or product. 
[Check Spotify Developer TnCs](https://developer.spotify.com/policy/#v-widgets-and-audio-preview-clips)

> So, **Don't** make the app that you create on Appsmith as public. [Ref](https://docs.appsmith.com/advanced-concepts/access-control#public-apps)
<br>

<br>

---

<br>

### How to use this template?

1.  Setup Spotify Client Credentials Flow 
    -   we need to [get a client id and secret](https://developer.spotify.com/documentation/general/guides/authorization/app-settings/)  for an app to make calls to spotify 
    -   we are using [Client Credentials Flow ](https://developer.spotify.com/documentation/general/guides/authorization/client-credentials/) for server to server communication

2.  Importing this template and creating an app in appsmith
    -   Fork this repo on Github
    -   Signup on appsmith
    -   [Importing a template from a Github Repo](https://docs.appsmith.com/advanced-concepts/version-control-with-git/import-from-repository) Import your fork repo
    -   Setup the spotify oauth datasource // here we need to add our spotify app credentials for this appsmith app to be able to connect to spotify
        - Add the following along with your client id and secret (ensure you copy these credentials properly, and no hidden characters / whitespaces / newline are also copied )
        ```
        URL: https://api.spotify.com
        Send Appsmith signature header (X-APPSMITH-SIGNATURE): No
        Authentication Type: OAuth 2.0
        Grant Type: Client Credentials
        Add token to:  Request Header
        Header Prefix: Bearer
        Access Token URL: https://accounts.spotify.com/api/token
        Client Id: [your id] 
        Client Secret: [your secret]
        Client Authentication: Send as Basic Header
        ```

        - then skip to application, leave the other datasource for now
    -   Deploy and view the current deployed app

<br>

---


<img src="https://raw.githubusercontent.com/appsmithorg/appsmith/release/static/appsmith_logo_primary.png"  width="180" height="50">

This app is built using Appsmith. Turn any datasource into an internal app in minutes. Appsmith lets you drag-and-drop components to build dashboards, write logic with JavaScript objects and connect to any API, database or GraphQL source.

