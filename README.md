# stijn.run

My own little URL shortener.

## Make your own

Clone the repository and edit the staticwebapp.config.json file.

This URL shortener is based on [netlify-shortener](https://www.npmjs.com/package/netlify-shortener) logic, but uses [Azure static web apps](https://azure.microsoft.com/en-us/services/app-service/static/) instead.

You can add a link by modifying ```staticwebapp.config.json``` where ```route``` is the ```shorturl``` and ```redirect``` contains the ```destination```.

``` json

{
  "route": "/lnkdn",
  "redirect": "https://www.linkedin.com/in/stijncallebaut/"
  "statusCode": 301
}

```

## Use aswa-shortener

Instead of manually updating your ``` staticwebapp.config.json ``` file, you could also use the aswa-shortener npm package.
[Aswa (Azure Static Web App) shortener](https://github.com/Stijnc/aswa-shortener) automatically generates a short code and checks if your route already exists. It will also push your changes to your origin, triggering a build of your Azure Static Web App.

> Note: It takes a minute or to for the build to complete, so your shortcode is not available in real-time.


 
![Azure static web apps URL shortener](./src/aswa-shortener.svg)


## Is this a fit for me?

I was on the look-out for a ~~cheap~~ free URL shortener service with custom domain support, and got triggered by netifly-urlshortener as it shines in its simplicity.
Selfhosting was not so much of an issue, as with netifly, Azure Static Web Apps also has a free tier.

If you are looking at a more robust and feature rich alternative I would suggest looking at [AzUrlShortener](https://github.com/FBoucher/AzUrlShortener)
