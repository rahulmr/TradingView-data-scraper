# TradingView Chart Data Extractor

Example deployment on Heroku
https:// 'APPURL' .herokuapp.com/quotes?url= 'URL-OF-PRIVATELY-PUBLISHED-CHART'

## Usage

Simply append the URL of a chart/idea published on TradingView to the link below. This is not the URL of a security's chart, but the URL for a user-published chart: https://tradingview-data.herokuapp.com/quotes?url=

i.e. for this chart: https://www.tradingview.com/chart/SPY/vjYfwgMu-SPY-Export-Test/
You'd use: https://tradingview-data.herokuapp.com/quotes?url=https://www.tradingview.com/chart/SPY/vjYfwgMu-SPY-Export-Test/

## Install
  ```
  pip3 install virtualenv
  python3 -m venv .
  source bin/activate
  pip3 install -r requirements.txt
  git init
  heroku create
  heroku git:remote -a projectname
  heroku stack:set heroku-16
  heroku buildpacks:add https://github.com/jontewks/puppeteer-heroku-buildpack.git
  heroku buildpacks:add heroku/python
  git add .
  git commit -am 'fix'
  git push heroku master
  ```
