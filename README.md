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

I needed a service that was able to do Server side functions, like authentication and external api requests with credentials that i don't a user having access to. ApiAB covers this idea by running a serverless enviroment running V8 Chrome code. Colds starts times are reduced by invoking the service automatically at constant intervals. 


### Public free endpoints 

#### [Wallpaper](https://api.aaronburt.co.uk/wallpaper)
This gets the lastest Wallpaper of the day from Bing and allows it to be embeded anywhere, i strictly reccommended only using this for private non-commercial reasons. 

#### [Forcast/Today](https://api.aaronburt.co.uk/forcast/today/london)

This will grab the city name from the route and perform an api request using credentials protected from the user. It will then spit back the correct data for the request. All Route requests are cached to avoid over invoking on OpenWeather endpoint. All payload should be returned as JSON.  
