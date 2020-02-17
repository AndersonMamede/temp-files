The following document illustrates the front-end vision for the Virtuagym web platform, for which we should be mindful of the following values:

- Consistency
- Maintainability
- Performance
- Quality
- Scalability

# Previous/? situation

The front-end world is becoming bigger and bigger. Web apps change over time, as do development techniques and frameworks. This requires support to allow different versions of front-end libraries and frameworks to co-exist (e.g. "old" modules built in jQuery and Bootstrap, combined with newer modules built in Vue.js). Having a single and large project that contains all modules (a.k.a. monolith) brings some problems (e.g. coupling, dependencies, slow technology adoption, hard to fully understand and to make changes fast and correctly, etc) and gets more and more dificult to maintain over time.

Monolith front-end:

<img src="https://raw.githubusercontent.com/AndersonMamede/temp-files/master/vision/monolith-front-end.png"/>



For that reason Virtuagym has decided to move away from the monolith front-end and go towards micro-frontend.

