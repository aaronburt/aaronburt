- 👋 Hi, I’m @aaronburt
- 👀 I’m interested in Javascript
- 🌱 I’m currently learning React and Jamstack deployment
- 📫 How to reach me: email@aaronburt.co.uk


# Home.AaronBurt.co.uk

I wanted a custom homepage for myself that didn't either have ads or required me to install a Extension, so i decided to build an ReactApp that has the technical capacity to be very module. 

- Built in React
- Deployed using Cloudflare Pages via GIT

## API

I needed a service that was able to do Server side functions, like authentication and external api requests with credentials that i don't want a user having access to. ApiAB covers this idea by running a serverless enviroment running V8 Chrome code. Cold starts are reduced by having an lean container (Stripped back Alpine Linux) and an aggressive caching layer to reduce the need to contact the origin.  

### V3
Performance has been significantly improved to reduce cold starts and data will be refreshed much more quickly. 

### Public free endpoints -- Please don't abuse them or i will need to remove them. 

#### [Wallpaper](https://wallpaper.function.aaronburt.co.uk/)
This gets the latest Wallpaper of the day from Bing and allows it to be embeded anywhere, i strictly reccommended only using this for private non-commercial reasons. 

#### [Wallpaper/ImgSrc](https://wallpaper.function.aaronburt.co.uk/youcanwritebasicallyanythinghere)
This will just display the image from the wallpaper api which can be embeded in any source you like, ensure to not abuse this as i don't want to have to apply limits.

#### [Weather](https://weather.streamsave.xyz/get?city=london)
This function will grab everything weather related and possible useful to you in a single json payload. Everything response is cached for atleast 3 hours at a time. 

#### [Random String Generator](https://random.function.aaronburt.co.uk/)

This function will generate a random string that you can use for any methods that require a little bit of randomness, I don't recommend using this for cryptographic security as its only using [Math.random()](https://deepsource.io/blog/dont-use-math-random/). 

```
?length= will determine how long the string return is upto a maximum value of 9999
&type= will determine what characters are used in the string. You can use any or all of the following. 

a = a-z 
A = A-Z
0 = 0-9
$ = symbols that shouldn't cause string escape issues
```
[Example](https://random.function.aaronburt.co.uk/?length=64&type=aA0$)


## BunnyCDN

#### [Bunny Edge Server Ip Listing](https://bunny-edge-server-list.aaronburt.co.uk)

This function will list all of the currently active BunnyCDN edge server ip addresses, it is displayed as a Javascript array.

#### [Bunny Billing Json](https://bunny-billing-json.aaronburt.co.uk/)

This function will return all of the json from bunny billing, this will aggressive cache the result, you will need to provide a ?key= query from [here](https://panel.bunny.net/account)
