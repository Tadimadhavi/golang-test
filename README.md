
Overview:

This application will convert the server’s epoch time into the human readable format.
 And also, it will convert the server’s time zone into the Eastern time zone.

Technologies used:

Go-lang ( for backend)
React JS ( for Frontend)

Links:

Frontend: http://3.16.42.52/




Backend: http://3.16.42.52:10000/epoch



Backend:


Step1 : clone the repo

Step 2: Install go lang in Ubuntu/windows

Step 3: go run <file name>

Ex: go run backend.go


Server will start running on “http:/localhost:10000”

Note:  You can change the port in the configuration

  Frontend:

# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)

 CI CD pipelines:


This application is a time converter application. In this, we are going to fetch the server time and convert into the human readable format.
	We have deployed this application into the AWS EC2 server.




	

There are multiple ways to deploy the application into the AWS.

1.	Through docker image. ( we can deploy into the ECR and access it from applications through ECS)
2.	We can deploy it to AWS EC2 through Ansible or Terraform
3.	We can enable Auto scaling and also the load balancing.



In Our code, We have Used EC2 deployment for the application.

We have deployed frontnd and backend to the AWS.


For CICD,We have used the Gihub actions.


In Github, we have .github/workflows folder, in that, we are having push.yml file.


That file will take care of the CI CD pipelines.

Backend Automation:

●	Backend app is created on go-languge. It can be deployed into the aws using anyform of Automations, like, Terraform, cloudformation, Ansible and also github actions.

●	Github actions will take the code based on our conditions, and build that code into a the paritcular way how we will do that in our local. And also, i will deploy it into the environment.


●	The environment will be On premises Linux, Docker, Kubernetes


Frontend Automation:

Frontend is created on React JS. It will be the responsible for the frontend styles as well as the static pages.

So, we need deploy the build files only. We dont need to deploy the entire source code into the server.


We can deploy the app into Nginx or Apache based on our requirement. This will help us to sereve the react js app into the outside world.


Optional:


IAC:

Infrastructure as a code

To create the AWS EC2, we have used the terraform.
It wil create the instances based on the configurations.

Services we have created:

●	IAM
●	ECR
●	EC2 with docker installed
●	VPC


Flow:

●	We have to create a docker image with the provided docker file in the github.
●	We can push the image into the docker Registry  ( ECR)
●	We can call that into our EC2 instance.
●	This EC2 is docker installed one. So we can import the image and also, we have to start the docker container
●	This Image is created by us while we are running a docker file.
●	Running a docker container will expose the port and endpoint we can use it for our application..
