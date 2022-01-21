# stijn.run

My own little URL shortener.

## Make your own

Clone the repository and edit the routes.json file.

This URL shortener is based on [netlify-shortener](https://www.npmjs.com/package/netlify-shortener) logic, but uses [Azure static web apps](https://azure.microsoft.com/en-us/services/app-service/static/) instead.

You can add a link by modifying ```routes.json``` where ```route``` is the ```shorturl``` and ```redirect``` contains the ```destination```.

``` json

{
  "route": "/lnkdn",
  "redirect": "https://www.linkedin.com/in/stijncallebaut/"
}

```
