# DevMtn-React-Introduction

## Setup
Some modules provided in this setup for React may or may not be unfamiliar to you. I just wanted to take a quick second to explain some of the key features of this environment we will be using.
#### File Structure
Having a clean and maintainable work environment is key for development. Our current file structure is:
````
- public
  - dist
  - src
	- app
	  - app.js
	- index.html
- .babelrc
- .gitignore
- .bs-config.json
- .package.json
- .README.md
- .webpack.config.js
````
Why the public folder? Usually when creating a website you'll have a front-end and a back-end. It's a good idea to get into the habit of seperating the code for them. So even though there won't be a backend for this tutorial it doesn't hurt to use the same file structure. Also there are many different ways to structure your files to make them maintainable, this is just my way of doing so.

With this current file structure we can quickly determine where all our configuration files are ( the root of the directory ), where all our front-end files are ( public folder ), where all our source files are for editing the front-end ( public -> src folder ), and where our production (finished) files are ( public -> dist folder ). 
#### Webpack with Lite-Server
You may not know exactly how webpack and lite-server work, however I just wanted to briefly explain just how awesome they are. With them we can run two commands in the terminal that will open the default browser with our index.html for us, monitor any file changes, compile them, bundle them, and then reload our browser for us. It's the luxurious Mercedes of web development, you'll never want to go back to your 1999 Honda. 
#### .babelrc and bs-config.json
These are configuration files to get webpack and lite-server to run the way we want them to. .babelrc tells our babel loader which presets to use and bs-config.json tells our lite-server the directory of our index.html file to host.
#### Starting up your Mercedes
To get this project going we need to install all the node modules. `npm install` or `yarn install`. After installing all our modules, we are also going to want to have access to the CLI for webpack `npm install -g webpack`. Having trouble? If you are having a premissions error with the global install try `sudo npm install -g webpack`. Now for the fun part, putting the key in the ignition! Open up two terminals/tabs and run one command in each. 

`webpack -w`, this tells webpack to compile/bundle our files and also watch for changes to re-compile/bundle.

`npm run dev`, this starts up our lite-server in your default browser and will monitor for file-changes to refresh the browser for us.

If everything ran successfully a tab in your default browser should of opened and your `terminal(s)` output should look similiar:

![alt text](https://github.com/devlemire/DevMtn-React-Introduction/blob/master/readme/initialRun.png "Initial Run")
## Step 1 - Bootstrapping the app
#### Summary
In this section we will be `bootstrapping`, or in other words, initially setting up our React app. We will build our first `component` and connect it to our `index.html` to see it on the page.
#### Detail