The following document illustrates the frontend vision for the Virtuagym web platform, for which we should be mindful of the following values:

- Consistency
- Maintainability
- Performance
- Quality
- Scalability

# Previous situation

The frontend world is becoming bigger and bigger. Web apps change over time, as do development techniques and frameworks. This requires support to allow different versions of frontend libraries and frameworks to co-exist (e.g. "old" modules built in jQuery and Bootstrap, combined with newer modules built in Vue.js). Having a single and large project that contains all modules (a.k.a. monolith) brings some problems (e.g. coupling, dependencies, slow technology adoption, hard to fully understand and to make changes fast and correctly, etc) and gets more and more dificult to maintain over time.

The monolith frontend using multiple backend services:

![Monolith frontend](https://raw.githubusercontent.com/AndersonMamede/temp-files/master/vision/monolith-front-end.png)

To solve some of those problems and grow faster, Virtuagym has decided to move away from the monolith frontend and go towards the micro-frontend architecture.

# Current situation

## Micro-frontend

The idea of micro-frontend is similar to microservices, but for the frontend. So, instead of one big frontend architecture, the monolith frontend is broken into many sub-apps that don't have dependencies on each other, can be developed/tested/deployed independently and are owned by independent squads. Each squad specialises in a different domain and develops its features end-to-end, from database to user interface.

The micro-frontend architecture:

![Micro-frontend](https://raw.githubusercontent.com/AndersonMamede/temp-files/master/vision/micro-frontend.png)

### Micro-frontend in Virtuagym

There are different approaches to the micro-frontend architecture, and the chosen approach is having multiple apps (SPA - Single Page Applications) that live at different URLs (e.g. one app at /schedule, another app at /goals, etc), and going from one app to another is a full page refresh that loads a different app.

These apps are composed by multiple components, e.g. buttons, lists, cards, tables), and they can also use shared components as needed for common functionality, such as the [navigation bar component](https://git.digifit.in/frontend-developer/vue-package-navigation-bar).

To help achieve the micro-frontend architecture and build the different apps, Virtuagym chose to use the following tools:

#### > Vue.js

<img src="https://raw.githubusercontent.com/AndersonMamede/temp-files/master/vision/vuejs.png" height="32"/>

Vue.js is currently one of the most popular open-source JavaScript framework for building user interfaces and apps (Single Page Applications). Its core library is focused on the view layer only and is easy to pick up and integrate with other libraries or existing projects.

More details about Vue.js in [our internal page](https://virtuagymdev.atlassian.net/wiki/spaces/DEVWIKI/pages/438632493/Intro+to+Vue.js) and in its [official page](https://vuejs.org/).

#### > Vuetify

<img src="https://raw.githubusercontent.com/AndersonMamede/temp-files/master/vision/vuetify.png" height="32"/>

Vuetify is an open-source component library for Vue.js, which lets you create clean, consistent, semantic, and reusable UI components. It is developed exactly according to [Material Design specification](https://material.io/) and provides users with everything that is needed to build rich and engaging web apps.
