# Pomodoro React App

⏲ React Pomodoro timer

<img src="demo.gif" width="476" height="640" alt="animated gif demoing pomodoro timer" />

## Table of Contents

- [Install](#install)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

### Tech stack
Pomodoro React App uses:
* [`React`](https://reactjs.org) for state and rendering
* [`react-circular-progressbar`](https://github.com/kevinsqi/react-circular-progressbar) for the circular, SVG progress bar component
* [`useSound`](https://github.com/joshwcomeau/use-sound) React Hook for playing sound effects


## Install

```
git clone https://github.com/chrisbirster/pomodoro-react-app.git
```
<br>

Then install dependencies:

```
cd pomodoro-react-app
yarn
```
<br>

Start the app in development mode and open your browser to [http://localhost:3000/](http://localhost:3000/) to view the app.

```
yarn start
```
<br>

The test runner can run in interactive watch mode. See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

```
yarn test
```

## Deploy

### Deploy with AWS CDK
The deploy directory has instructions on deploying this application as a
microservice using AWS ECS Fargate cluster. Found out more by navigating to the
pomodoro-react-app/deploy/README.md 

### Deploy with Docker
The application has been containerized. Here is a quickstart to to build the
repository image and run it using Docker. Then you can navigate to
http://localhost:3000 to see the application.

```
cd pomodoro-react-app
docker build -t pomodoro:dev .
docker run --name pomo -p 3000:80 pomodoro:dev
```

You can also pull from DockerHub I pushed an image under [chrisdontmiss/pomodoro](https://hub.docker.com/r/chrisdontmiss/pomodoro).

```
docker run --name pomo -p 3000:80 chrisdontmiss/pomodoro
```


## Contributing
PRs accepted.

### Known Issues
Does not track your start time or save your preferences, so timer stops if your computer sleeps and the settings need to be reentered when the page is refreshed.

## License
[MIT](./LICENSE)

