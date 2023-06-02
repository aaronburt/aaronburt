- 👋 Hi, I’m @aaronburt
- 👀 I’m interested in Javascript
- 🌱 I’m currently learning React and Jamstack deployment
- 📫 How to reach me: email@aaronburt.co.uk


# Home.AaronBurt.co.uk

I wanted a custom homepage for myself that didn't either have ads or required me to install a Extension, so i decided to build an ReactApp that has the technical capacity to be very module. 

- Built in React
- Deployed using Cloudflare Pages via GIT

## API

I needed a service that could perform server-side functions like authentication and external API requests with restricted user access. ApiAB fulfills this requirement by running a serverless environment with V8 Chrome code. To minimize cold starts, it uses a lean container (Stripped back Alpine Linux) and an aggressive caching layer to reduce origin contacts.

### V4
V4 offers significant performance improvements, reducing cold starts and refreshing data much faster.

### Public free endpoints -- Please don't abuse them or i will need to remove them. 

#### [Wallpaper](https://wallpaper.function.aaronburt.co.uk/)
This endpoint retrieves the latest Wallpaper of the day from Bing and allows embedding for private non-commercial use only.

#### [Wallpaper/ImgSrc](https://wallpaper.function.aaronburt.co.uk/youcanwritebasicallyanythinghere)
This endpoint displays the image from the wallpaper API, which can be embedded in any source. Please avoid misuse and commercial usage.

![image info](https://wallpaper.function.aaronburt.co.uk/youcanwritebasicallyanythinghere)

#### [Weather](https://weather.function.aaronburt.co.uk/current/br1/gb)
This function provides comprehensive weather-related data in a single JSON payload. All responses are cached for an 1 hour.

#### [Random String Generator](https://random.function.aaronburt.co.uk/)

This function generates a random string that can be used for various purposes requiring some level of randomness. However, it's not recommended for cryptographic security as it solely relies on [Math.random()](https://deepsource.io/blog/dont-use-math-random/). 

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

This function lists all currently active BunnyCDN edge server IP addresses and is displayed as a JavaScript array.

#### [Bunny Billing Json](https://bunny-billing-json.aaronburt.co.uk/)

This function returns all the JSON data from Bunny Billing. The result is aggressively cached, and you need to provide a ?key= query from [here](https://panel.bunny.net/account)
