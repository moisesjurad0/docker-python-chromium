FROM python:3.10-alpine

# install chromium & chromium-chromedriver
# ChromeDriver 110.0.5481.177 (f34f7ab2d4ca4ad498ef42aeba4f4eb2c1392d63-refs/branch-heads/5481@{#1239})
# Chromium 110.0.5481.177
RUN apk update && apk add chromium chromium-chromedriver

# inherit this image on your own image 
# FROM squartle:python-chromium

# then add this to complete the requirements of your python app. Don't forget include selenium inside the requirements file
# WORKDIR /myapp
# COPY requirements.txt .
# RUN pip --no-cache-dir install -r requirements.txt

# then copy your files app
# COPY . .