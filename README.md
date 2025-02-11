# Uniform Optimize starter kit for Sitecore JSS and Next.js

This repo contains both the starter kit with content items and required configuration files.

This kit is pre-wired for edge-side rendering and static site generation for Sitecore JSS and is created to fast track the activation of both Uniform Optimize and Deploy capabilities together with a Sitecore JSS solution.

You can also use this kit to start a vanilla project, simply remove everything from `/src/components` and adjust the Sitecore site name from `uniform-jss-kit` to whatever you want and get cracking.

## Official docs
1. [Uniform Optimize for Sitecore docs](https://docs.uniform.dev/sitecore/optimize)

## Pre-requisites
1. Sitecore 9.3+ instance available with Sitecore JSS installed and configured.
1. "Uniform for Sitecore v5" installed and configured on your Sitecore instance. Check out [these docs](https://60da7ad12ba84d00071cd844--uniform-docs.netlify.app/sitecore/optimize/getting-started) for more info.
1. Install the Sitecore package with the starter kit items from `/sitecore/App_Data/packages` folder (optional).
1. Create Sitecore API key as per Sitecore JSS documentation [here](https://jss.sitecore.net/docs/client-frameworks/getting-started/app-deployment).


## Setup environment variables
1. Create an `.env` file next to `package.json` (see `.env-example`) and provide the values for your Sitecore instance:
    ```
    # the Sitecore endpoint where Uniform Connector is installed and configured
    UNIFORM_API_URL=https://sitecore.dev.local
    UNIFORM_API_TOKEN='Uniform API token, see the docs'
    UNIFORM_API_KEY: 'Sitecore API key value'
    ```

## Getting started
1. Add `NPM_TOKEN` environment variable with the value we provided you with.
1. `npm install`
1. `jss setup` and follow the steps Sitecore JSS requires and use the API key you created during the Pre-requisites step above.
1. `jss deploy config` to deploy the application config from `/sitecore/config` folder into your Sitecore instance.
1. `npm run build` to build the app.
1. `npm start` to start the app in connected mode.
1. For development, use `npm run dev` command.
