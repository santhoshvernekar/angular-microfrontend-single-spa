
# Angular Microfrontends

This is a example repository for people who want to have multiple angular microfrontends coexist within a single page. Each
of the angular applications was created and is managed by Angular CLI.

It uses [single-spa](https://single-spa.js.org) to pull this off, which means that you can even add React, Vue, or other frameworks as
additional microfrontends.

For mapping routes to applications it uses [single-spa-layout](https://single-spa.github.io/single-spa.js.org/docs/layout-overview/).

## An important note
This github repository has four projects all in one repo. But when you do this yourself, **you'll want to have one git repo per
angular application**. The root-html-file project should also be in its own repo. This is what lets different teams and developers be in
charge of different microfrontends.



With single-spa, it is preferred to run `ng serve` in only one single-spa application at a time, while using a deployed
version of the other applications. This makes for an awesome developer experience where you can boot up just one
microfrontend at a time, not even having to clone, npm install, or boot up all of the other ones.

To try this out, clone the repo and run the following commands:

cd app1
npm i
npm start
```



## Local development -- all at once
It is preferred to only run one app at a time. But if you need to run them all locally, you can do so with the following instructions


# First terminal tab
cd root-html-file
npm install
npm start
```

# Second terminal tab
cd app1
npm install
npm start
```


# Third terminal tab
cd app2
npm install
npm start
```


# Fourth terminal tab
cd navbar
npm install
npm start
```

Now go to http://localhost:4200 in a browser. Note that you can change any of the ports for the projects by modifying the Import Map inside of
root-html-file/index.html.

```

# ScreenShots

### Home Page

http://localhost:4200

![homepage](https://user-images.githubusercontent.com/59571096/120921663-68e9e680-c6e2-11eb-83e6-8483f087a990.png)

### App1:

http://localhost:4200/app1

![app1](https://user-images.githubusercontent.com/59571096/120921677-7a32f300-c6e2-11eb-9825-97199136012f.png)

### App2:

http://localhost:4200/app2

![app2](https://user-images.githubusercontent.com/59571096/120921703-828b2e00-c6e2-11eb-8e85-5f4cbbebe4ad.png)

