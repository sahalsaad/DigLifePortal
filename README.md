# DigLife Portal ################TEST
## Purpose
This is the implementation of the DigLife portal, a single place from where authorized members can access all DigLife Services. THe portal is structured into four domains:

### DigLife Home
Access to main services available for all members. This also include Communities of Interest (i.e. non-workteam related groups) 
### DigLife Projects
These are workteams organized around value-producing (service-providing) projects with access to supporting services.
### DigLife Operations
These are workteams organized around internal operations, such as Marketing, Finance, Legal, etc.
### DigLife Friends
These are external spaces to invite non-members such as guests, partners, sponsors, etc.

## Implementation
We are developing this portal with a [Vue JavaScript frontend](https://vuejs.org/) using the [CodeSandBox online IDE](https://codesandbox.io/). 
CodeSandBox can be forked to allow multiple parties to co-develop the application. As a single owner, make sure to commit your work to GitHub before changing machines and refresh the code on new machines. 
There is also a live-coding feature to allow multiple parties edit the code concurrently in realtime.

### Structure and guides
https://itnext.io/how-to-structure-a-vue-js-project-29e4ddc1aeeb (all in /src)
https://vuejs.org/v2/style-guide/

### CSS Framework
We are using the [Vue Material](https://vuematerial.io/) CSS framework to accelerate the development of key UI elements, such as [Navigation](https://vuematerial.io/components/drawer) and [Cards](https://vuematerial.io/components/card). 

### Authentication
Stripe (payment) > Mailtrain (member list) > Mattermost Invite (account) > DigLife.coop (OAuth 2)
https://docs.mattermost.com/developer/oauth-2-0-applications.html (OAuth for DigLife.coop)
https://cloudron.io/blog/2017-03-21-oauth-provider.html (OAuth for Cloudron  apps)
https://auth0.com/authenticate/vuejs/oauth2/ (OAuth for social apps)
https://auth0.com/docs/connections/social/github (OAuth for Auth0 and GitHub)
https://www.npmjs.com/package/client-oauth2 
https://alligator.io/vuejs/vue-jwt-patterns/ (w/o Vuex)
https://blog.sqreen.io/authentication-best-practices-vue/ (w/ vuex)
http://jasonwatmore.com/post/2018/09/21/vuejs-basic-http-authentication-tutorial-example 
https://blog.pusher.com/fullstack-graphql-app-prisma-apollo-vue/ (w/ Apollo)

##### Vuex and APIs
https://vuex.vuejs.org/
https://www.thepolyglotdeveloper.com/2018/04/vuejs-app-using-axios-vuex/
https://zendev.com/2018/05/21/vuex-perfect-interface-frontend-backend.html
https://stackoverflow.com/questions/40813975/how-to-structure-api-calls-in-vue-js 

### Vue CLI
http://vuejs-templates.github.io/webpack
http://vuejs.github.io/vue-loader

### Known issues
The main limitation of cookies on mobile browsers is that they reset when the browser is closed or when the phone is shut down/restarted.

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run all tests
npm test
```

For a detailed explanation on how things work, check out the [guide](.