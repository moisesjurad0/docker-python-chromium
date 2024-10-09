# docker-python-chromium

Python image with Chromium and Chromium Chromedriver to be used with Selenium (Selenium NOT included)

## Image includes

- Python (Alpine)
- Chromium  (110.0.5481.177 - compatible with Selenium4)
- Chromium-chromedriver (110.0.5481.177 - compatible with Selenium4)

## Image NOT includes

- Selenium (remeber to add it in your requirements.txt file)

## Selenium Manager

```txt
https://selenium-python.readthedocs.io/installation.html#drivers
--
Starting from version 4.6.0 (November 4, 2022) selenium comes with Selenium Manager packed in distribution.

Selenium Manager is a new tool that helps to get a working environment to run Selenium out of the box:

automatically discovers, downloads, and caches the drivers required by Selenium when these drivers are unavailable;

automatically discovers, downloads, and caches the browsers driven with Selenium (Chrome, Firefox, and Edge) when these browsers are not installed in the local system.
```

## Versions

### Python 3 (Alpine-based)

- `3.11-alpine` (based on python:3.11-alpine, [Dockerfile](https://github.com/moisesjurad0/docker-python-chromium))

## Usage

Inherit this image on your own image

```docker
FROM squartle:python-chromium
```

then add this to complete the requirements of your python app. Don't forget include selenium inside the requirements file

```docker
WORKDIR /myapp
COPY requirements.txt .
RUN pip --no-cache-dir install -r requirements.txt
```

after that complete the image copying your app files

```docker
COPY . .
```
