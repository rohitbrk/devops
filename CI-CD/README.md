# CI CD

CI - Continuos Integration
CD - Continuos Delivery/ Deployment

<div>After the development, the steps test, build and deploy etc can be automated. </div>

<div>Here we will use github actions for setting up CI CD pipeline.
This is for a frontend ReactJs project (tests written using jest library)
Once tests are successful, the build artifacts of project will be automatically deployed to vercel.</div>

Steps:

- Create a ".github" folder in the root of project
- Create a "workflows" folder inside ".github"
- Create a file with ".yaml" extension. Here we are creating "prod.yaml".
- Mention steps for Tests and Deployment. Use github secrets for injecting secret vars.
- Once Tests are success, the build artifacts of the project are automatically deployed.

<div>Similar approach can be follwed to setup a pipeline for any project and cloud provider.</div>
