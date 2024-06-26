# scheduling.ai
Running the Application Locally with SAM CLI

This README provides instructions on how to set up and run the scheduling-ai application locally using the AWS SAM CLI.

Prerequisites:
- Install AWS SAM CLI: Follow the installation guide for your operating system at [AWS SAM CLI Installation](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html).
- Install Docker: Docker is required to run the application locally. Follow the installation guide for your operating system at [Docker Installation](https://docs.docker.com/get-docker/).

Steps:

1.Clone the repository:
```cd scheduling-ai```

2.Build the Docker image:
```sam build```

3.Start the local API:
```sam local start-api```

The SAM CLI will start a local API at http://127.0.0.1:3000. You can test the /hello endpoint by accessing http://127.0.0.1:3000/hello in your web browser or using tools like curl or Postman.

Note:
The sam build command will install the required dependencies and build the application.
The sam local start-api command will start the local API and automatically redeploy the application whenever changes are detected in the source code.

Additional Information:
To view the logs generated by the application, use the following command:
```sam logs -n HelloWorldFunction --stack-name scheduling-ai --tail```
To stop the local API, press ```Ctrl+C``` in the terminal where the ```sam local start-api``` command is running.
