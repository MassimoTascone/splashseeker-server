[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)](https://expressjs.com/)
[![Axios](https://img.shields.io/badge/Axios-007ACC?style=for-the-badge&logo=axios&logoColor=white)](https://github.com/axios/axios)
[![Cyclic](https://img.shields.io/badge/Cyclic-212121?style=for-the-badge&logo=cyclic&logoColor=white)](https://app.cyclic.sh/#/)



# SplashSeeker ServerSide

## Introduction

SplashSeeker is a full-stack web application developed as a learning project. It is built with React, TypeScript, Node.js, Express.js, and utilizes the Unsplash API to display and search for images. This repository contains the backend server code.

The main repository for the SplashSeeker application can be found [here](https://github.com/MassimoTascone/splashseeker).

## Server

The server is responsible for serving as the API endpoint for fetching random popular images and searching for images using the Unsplash API.

### Features

- **CORS Configuration**: The server is configured to allow cross-origin resource sharing (CORS) from the front-end application hosted at [https://splashseeker.vercel.app](https://splashseeker.vercel.app). This enables the front-end to make requests to the server.

- **Rate Limiting**: The server implements rate limiting using the `express-rate-limit` middleware. Each IP address is limited to 500 requests per hour. If the limit is exceeded, a "Too many requests" error message is returned.

- **Get Random Popular Images**: The server provides a `GET` endpoint at `/getImages/:count` to fetch a specified number of random popular images from the Unsplash API. The count parameter determines the number of images to retrieve.

- **Search for Images**: The server provides a `GET` endpoint at `/searchImages/:query/:page` to search for images based on a query string and page number. The query parameter represents the search query, and the page parameter determines the pagination for the search results.

### API Endpoints

- **GET `/getImages/:count`**: Fetches a specified number of random popular images from the Unsplash API. The `count` parameter determines the number of images to retrieve.

- **GET `/searchImages/:query/:page`**: Searches for images based on a query string and page number. The `query` parameter represents the search query, and the `page` parameter determines the pagination for the search results.

### Technologies Used

- [Node.js](https://nodejs.org/)
- [Express.js](https://expressjs.com/)
- [axios](https://axios-http.com/)
- [dotenv](https://www.npmjs.com/package/dotenv)

For more information on the Unsplash API, please visit the [Unsplash Developer Documentation](https://unsplash.com/developers).

### Deployment

The server for SplashSeeker is deployed on [Cyclic](https://app.cyclic.sh/) platform. Cyclic ensures that the server is always available and does not put it into sleep mode even during periods of inactivity. This means that API calls to fetch data from the server will consistently perform as expected without any delay.

## Frontend

For information about the frontend of the SplashSeeker application, please refer to the [main repository](https://github.com/MassimoTascone/splashseeker).
