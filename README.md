Build [Mono runtime](http://www.mono-project.com/Main_Page) for use with the [Heroku .NET buildpack](https://github.com/friism/heroku-buildpack-mono).

To build:

```term
$ docker build -t my-user/mono-builder cedar-14/.
```

To build and upload new Mono version:

```term
$ docker run -v ${PWD}/cache:/var/cache -e AWS_ACCESS_KEY_ID=key -e AWS_SECRET_ACCESS_KEY=secret -e VERSION=3.2.8 my-user/mono-builder
```
