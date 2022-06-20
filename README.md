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

#### [Wallpaper](https://api.aaronburt.co.uk/wallpaper)
This gets the latest Wallpaper of the day from Bing and allows it to be embeded anywhere, i strictly reccommended only using this for private non-commercial reasons. 

#### [Wallpaper/ImgSrc](https://api.aaronburt.co.uk/wallpaper/embed)
This will get the latest wallpaper url and 302 redirect the client to img, this should mean that for all img tags the img should just work fine AGAIN i strictly reccommended only using this for private non-commercial reasons. 

#### [Weather/Today](https://api.aaronburt.co.uk/weather/now/london)

This will grab the city name from the route and perform an api request using credentials protected from the user. It will then spit back the correct data for the request. All Route requests are cached to avoid over invoking on OpenWeather endpoint. All payload should be returned as JSON.  

#### [Weather/Week](https://api.aaronburt.co.uk/weather/week/london)

This will return a week worth of json payload instead of a single time.

### [Random String Generator](https://generate-random-string.aaronburt.workers.dev)

This function will generate a random string between 1 and 4096 characters. Use the length query to specify the amount.
