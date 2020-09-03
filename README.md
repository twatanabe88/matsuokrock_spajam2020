# matsuokrock_spajam2020

## Table of content

- [Installation](#installation)
    - [Amplify CLI](#AmplifyCLI)
- [Usage](#Usege)
    - [React Native](#ReactNative)


## Installation

- Amplify CLI


### AmplifyCLI

```bash
npm install -g @aws-amplify/cli
```
Now it’s time to setup the Amplify CLI. Configure Amplify by running the following command:

```bash
amplify configure
```

amplify configure will ask you to sign into the AWS Console.

Once you’re signed in, Amplify CLI will ask you to create an IAM user.

Amazon IAM (Identity and Access Management) enables you to manage users and user permissions in AWS. You can learn more about Amazon IAM [here](https://aws.amazon.com/iam/).

```
Specify the AWS Region
? region:  # Your preferred region
Specify the username of the new IAM user:
? user name:  # User name for Amplify IAM user
Complete the user creation using the AWS console
```

Create a user with AdministratorAccess to your account to provision AWS resources for you like AppSync, Cognito etc.

Once the user is created, Amplify CLI will ask you to provide the accessKeyId and the secretAccessKey to connect Amplify CLI with your newly created IAM user.

```
Enter the access key of the newly created user:
? accessKeyId:  # YOUR_ACCESS_KEY_ID
? secretAccessKey:  # YOUR_SECRET_ACCESS_KEY
This would update/create the AWS Profile in your local machine
? Profile Name:  # (default)

Successfully set up the new user.
```

## Usage
### ReactNative
#### Create a new React Native app
```
npm install -g expo-cli  
expo init RNAmplify
```
#### Initialize a new backend
```
cd RNAmplify
amplify init
```

```
? Enter a name for the project: rnamplify
? Enter a name for the environment: demo
? Choose your default editor: <Your favorite text editor>
? Choose the type of app that you're building: javascript
? What javascript framework are you using: react-native
? Source Directory Path:  /
? Distribution Directory Path: /
? Build Command:  npm run-script build
? Start Command: npm run-script start
? Do you want to use an AWS profile? Y
? Please choose the profile you want to use: <Your AWS profile from the configuration step>
```

When you initialize a new Amplify project, a few things happen:

It creates a top level directory called amplify that stores your backend definition. During the tutorial you’ll add capabilities such as a GraphQL API and authentication. As you add features, the amplify folder will grow with infrastructure-as-code templates that define your backend stack. Infrastructure-as-code is a best practice way to create a replicable backend stack.
It creates a file called aws-exports.js in the src directory that holds all the configuration for the services you create with Amplify. This is how the Amplify client is able to get the necessary information about your backend services.
It modifies the .gitignore file, adding some generated files to the ignore list.
A cloud project is created for you in the AWS Amplify Console that can be accessed by running amplify console. The Console provides a list of backend environments, deep links to provisioned resources per Amplify category, status of recent deployments, and instructions on how to promote, clone, pull, and delete backend resources.

#### Install Amplify libraries

Install the necessary dependencies by running the following command:\

```bash

npm install aws-amplify aws-amplify-react-native @react-native-community/netinfo

```


Finally, open App.js (Expo) or index.js (React Native CLI) and add the following lines of code at the top of the file below the last import:


Now your project is set up and you can begin adding new features.
