- 👋 Hi, I’m @aaronburt
- 👀 I’m interested in Javascript
- 🌱 I’m currently learning React and Jamstack deployment
- 📫 How to reach me: email@aaronburt.co.uk


# Home.AaronBurt.co.uk

I wanted a custom homepage for myself that didn't either have ads or required me to install a Extension, so i decided to build an ReactApp that has the technical capacity to be very module. 

- Built in React
- Deployed using Cloudflare Pages via GIT
- [Uses my RESTFul api to fetch weather data from OpenWeatherAPI](https://home.aaronburt.co.uk/?city=congleton)


## [Api.aaronburt.co.uk](https://api.aaronburt.co.uk)

I needed a service that was able to do Server side functions, like authentication and external api requests with credentials that i don't want a user having access to. ApiAB covers this idea by running a serverless enviroment running V8 Chrome code. Cold starts are reduced by having an lean container (Stripped back Alpine Linux) and an aggressive caching layer to reduce the need to contact the origin.  

### V2
The Api has been updated to version 2, migrated from Cloudflare Workers to a Dockerized Serverless instance which sports a NodeJS server enviroment and placed behind a reverse proxy caching layer to reduce cold starts on common requests. 

### Public free endpoints -- Please don't abuse them or i will need to remove them. 

#### [Wallpaper](https://wallpaper.streamsave.xyz/)
This gets the latest Wallpaper of the day from Bing and allows it to be embeded anywhere, i strictly reccommended only using this for private non-commercial reasons. 

#### [Wallpaper/ImgSrc](https://wallpaper.streamsave.xyz/embed)
This will get the latest wallpaper url and 302 redirect the client to img, this should mean that for all img tags the img should just work fine AGAIN i strictly reccommended only using this for private non-commercial reasons. 

#### [Weather/Today](https://api.aaronburt.co.uk/weather/now/london)

This will grab the city name from the route and perform an api request using credentials protected from the user. It will then spit back the correct data for the request. All Route requests are cached to avoid over invoking on OpenWeather endpoint. All payload should be returned as JSON.  

#### [Weather/Week](https://api.aaronburt.co.uk/weather/week/london)

This will return a week worth of json payload instead of a single time.

#### [Random String Generator](https://random.streamsave.xyz/)

This function will generate a random string that you can use for any methods that require a little bit of randomness, I don't recommend using this for cryptographic security as its only using [Math.random()](https://deepsource.io/blog/dont-use-math-random/). 

```
?length= will determine how long the string return is upto a maximum value of 9999
&type= will determine what characters are used in the string. You can use any or all of the following. 

a = a-z 
A = A-Z
0 = 0-9
$ = symbols that shouldn't cause string escape issues
```
[Example](https://random.streamsave.xyz/?length=64&type=aA0$)


## BunnyCDN

#### [Bunny Edge Server Ip Listing](https://bunny-edge-server-list.aaronburt.co.uk)

This function will list all of the currently active BunnyCDN edge server ip addresses, it is displayed as a Javascript array.

#### [Bunny Billing Json](https://bunny-billing-json.aaronburt.co.uk/)

This function will return all of the json from bunny billing, this will aggressive cache the result, you will need to provide a ?key= query from [here](https://panel.bunny.net/account)
