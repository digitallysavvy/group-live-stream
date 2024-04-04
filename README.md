# Agora Group Live Streaming

<!-- ![Group Video Demo](https://github.com/digitallysavvy/group-video-chat/actions/workflows/deploy-to-pages.yaml/badge.svg) -->

Extending upon group video chat, to support group live streaming. This project demonstrates how to implement Agora's Media Push features to send live video streams from an Agora channel to a streaming platform such as Twitch, YouTube Live, Vimeo, Facebook Live, and any other services that provide a stream-key and RTMP endpoint.

This example is written using vanilla javascript to implment the Agora Video SDK for Web v4.20

<!-- A walk-through of the project setup and code: [Guide.md](Guide.md) -->

## Demo
<!-- Test the build: [https://digitallysavvy.github.io/group-video-chat/](https://digitallysavvy.github.io/group-video-chat/) -->

## Setup

1. Clone the repo
2. Rename `.env-example` file to `.env`
3. Add Agora API Key to the .env file

## Test in Dev mode
1. Follow steps in setup
2. Open the terminal and navigate to repo folder
3. Use this command to run dev mode with local webserver: 
```npm run dev```

## Build for production
1. Follow steps in setup
2. Open the terminal and navigate to repo folder
3. Use this command to run the build script: 
```npm run build```
4. Upload the contents of the new `dist` folder to your webserver
5. Make sure the server has your Agora API key set in the environment variables using the env variable `VITE_AGORA_APP_ID=`

## Deploy to GitHub Pages
This project is setup with a GitHub actions workflow to deploy the project to GitHub pages, if enabled in the project settings. 

To enable GitHub Pages build via GitHub Actions:
1. Fork the project on GitHub (https://github.com/digitallysavvy/group-live-stream)
2. Clone the project 
3. Click the project's Settings tab
4. Click the Pages tab in the left column menu
5. Under Build and deployment, select GitHub Actions as the Source
6. Click the Environments tab in the left column menu
7. Click github-pages from the Environments list
8. Click Add variable under the Environment variable section
9. Set the name `VITE_AGORA_APP_ID` and your Agora AppId as the value.
10. Update the `vit.config.js` file to update the url if you change the project name