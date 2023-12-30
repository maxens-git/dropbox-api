
# Dropbox api


## API Reference

#### Obtention du Code d'accès

```curl
  https://www.dropbox.com/oauth2/authorize?client_id=<App key>&token_access_type=offline&response_type=code
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `<App key>` | `string` | Obtenir la clef ici : https://www.dropbox.com/developers/apps/ |


#### Obtention du refresh_token

```curl
   curl https://api.dropbox.com/oauth2/token \
	-d code=<CODE> \
    -d grant_type=authorization_code \ 
    -u <App key>:<App secret> 
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `<CODE>` | `string` | Récupéré a l'étape précédente
| `<App key>`      | `string` | Obtenir la clef ici : https://www.dropbox.com/developers/apps/ |
| `<App secret>` | `string` | Obtenir la clef ici : https://www.dropbox.com/developers/apps/ |


Takes two numbers and returns the sum.

#### Obtention de l'access_token

```curl
  curl https://api.dropbox.com/oauth2/token \
   -d refresh_token=<refresh_token> \
   -d grant_type=refresh_token \
   -d client_id=<App key> \
   -d client_secret=<App secret>
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `<refresh_token>`      | `string` | Récupéré à l'étape précédente |
| `<App secret>` | `string` | Obtenir la clef ici : https://www.dropbox.com/developers/apps/ |
| `<App key>`      | `string` | Obtenir la clef ici : https://www.dropbox.com/developers/apps/ |
| `<App secret>` | `string` | Obtenir la clef ici : https://www.dropbox.com/developers/apps/ |






