<p align="center">
  <img src="./.github/assets/celestial-bodies.png" alt="Celestial Bodies">
</p>

<p align="center">
  <a href="#">
    <img src="https://img.shields.io/static/v1?label=status&message=Active%20Development&color=blue&style=flat-square&?logo=open-source-initiative&logoColor=ffffff">
  </a>
  <a href="#">
    <img src="https://img.shields.io/github/v/release/hieronymous-bean/celestial-bodies?include_prereleases&style=flat-square">
  </a>
  <a href="#">
    <img src="https://img.shields.io/github/issues-raw/hieronymous-bean/celestial-bodies?style=flat-square">
  </a>
  <a href="#">
    <img src="https://img.shields.io/github/license/hieronymous-bean/exemplar?style=flat-square">
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/gulp-builds_this_project-eb4a4b.svg?logo=data%3Aimage%2Fpng%3Bbase64%2CiVBORw0KGgoAAAANSUhEUgAAAAYAAAAOCAMAAAA7QZ0XAAAABlBMVEUAAAD%2F%2F%2F%2Bl2Z%2FdAAAAAXRSTlMAQObYZgAAABdJREFUeAFjAAFGRjSSEQzwUgwQkjAFAAtaAD0Ls2nMAAAAAElFTkSuQmCC&style=flat-square">
  </a>
  <br>
</p>

<p align="center">:rocket: Lightweight wrapper for NASA's API library.</p>





## Introduction
Celestial Bodies is a lightweight wrapper for NASA's API library. 




## Table of Contents

:new_moon: <a href="#system-requirements">System Requirements</a>
:waxing_crescent_moon: <a href="#installation">Installation</a>
:crescent_moon: <a href="#usage">Usage</a>
:moon: <a href="#contributing">Contributing</a>
:full_moon: <a href="#credits">Credits</a>



## System Requirements

At its core, Celestial Bodies relies on Node.js and NPM for its core functionality. 

- Node.js ~14.15.1
- NPM ~6.14.8


## Installation

```
npm install celestial-bodies
```

## :artificial_satellite: Usage
Require the package to access the preconfigured API functions.
```
const celestial = require('celestial-bodies');
```

Before using Celestial Bodies, you'll want to configure the values of the `payload` object to include the information you want to pass to the API. There is a single global payload object which contains configurations for all of the API calls together, as opposed to having a separate object for each request.

```js
const payload = {
  global: {
    key: 'DEMO_KEY', // required - can include personal API key or leave as DEMO_KEY and it will still work, but it at least needs to contain a value.
  },
  apod: {
    date: '', // optional - will default to today if no value provided. Format needs to be YYYY-MM-DD.
    hd: '' // optional - defaults to false. Change to `true` to have the API return a high-resolution endpoint.
  },
  asteroids: {
    start_date: '', // optional - will default to today if no value provided. Format needs to be YYYY-MM-DD. 
    end_date: '' // optional - will default to seven days after today if no value provided. Format needs to be YYYY-MM-DD.
  },
};
```


#### APOD
The `apod()` function is used to leverage the Astronomy Picture of the Day API. 
The returned payload is stored in the `response` variable.

```js
celestial.apod(payload, response => {
  return response;
});
```




#### Asteroids
The `asteroids()` function provides access to NASA's Near Earth Object Web Service. 

```js
celestial.asteroids(payload, response => {
  return response;
});



## Contributing

Contributions are welcome - feel free to submit a pull request and it will be reviewed promptly. 

## Credits

##### Assets
Logo - <a href="https://looka.com/">Looka.com</a>

##### Packages
<a href="https://github.com/axios/axios">Axios</a>

## Bonus

<a href="https://www.buymeacoffee.com/hieronymousbean" target="_blank">
    <img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" >
</a>

Please :star: the project if you enjoy it - much appreciated!