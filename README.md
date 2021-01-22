# UTU Crypto Tracker

<img src="./frontend/public/utu_crypto_tracker.png" width="300" height="500">

## Built with

- React (Hooks)
- NodeJS (express)
- CSS
- Axios

## Thought process

1. Create an API from the google spreadsheet data

- convert the google spreadsheet data to json format

2. Create react app for the frontend side

- npx create-react-app frontend
- create data.js file in src
- create Coin.js, Coin.css

3. Read the data

- import the data from data.js in App.js
- price (close value of the day)
- calculate the 24h change difference (open - close)
- calculate the 7d change difference (04 December 2019 close value - 28th November 2019 close value)
- calculate the 1month change difference (04 December 2019 close value - 04 November 2019 close value)
- sort the coin by its market cap in descending order

4. create server with NodeJS and express

- npm init in root folder
- update package.json set type: module
- add start command as node backend/server.js
- install express
- create route for / return backend is ready
- move data.js from frontend to backend
- create route for /api/coins
- return coins
- run npm start

5. retrive the data from server and display in front-end (React)

- edit App.js
- define coins
- create useEffect
- define async fetchData and call it
- install axios
- get data fom /api/coins
- show them in the list
