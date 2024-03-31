---

title:  "grug brain developer"
date:   2024-03-31 15:48:50
layout: page
toc: true
categories:
---

this collection of thoughts on software development gathered by grug brain developer, that i like.

grug brain developer not so smart, but grug brain developer program many long year and learn some things although mostly still confused


big brained developers are many, and some not expected to like this, make sour face

THINK they are big brained developers many, many more, and more even definitely probably maybe not like this, many sour face (such is internet)

> (note: grug once think big brained but learn hard way)

### Complexity


one day code base understandable and grug can get work done, everything good!

next day impossible: complexity demon spirit has entered code and very dangerous situation!

demon complexity spirit mocking him make change here break unrelated thing there what!?! mock mock mock ha ha so funny grug love programming and not becoming shiney rock speculator like grug senior advise

so grug say again and say often: complexity very, very bad

### Saying No

sometimes compromise necessary or no shiney rock, mean no dinosaur meat, not good, wife firmly remind grug about young grugs at home need roof, food, and so forth, no interest in complexity demon spirit rant by grug for fiftieth time

in this situation, grug recommend "ok"

80/20 solution say "80 want with 20 code" solution maybe not have all bell-whistle that project manager want, maybe a little ugly, but work and deliver most value, and keep demon complexity spirit at bay for most part to extent


sometimes probably best just not tell project manager and do it 80/20 way. easier forgive than permission, project managers mind like butterfly at times overworked and dealing with many grugs. often forget what even feature supposed to do or move on or quit or get fired grug see many such cases


anyway is in project managers best interest anyway so grug not to feel too bad for this approach usually


### Factoring your code

next strategy very harder: break code base up properly (fancy word: "factor your code properly") here is hard give general advice because each system so different. however, one thing grug come to believe: `not factor your application too early!`

early on in project everything very abstract and like water: very little solid holds for grug's struggling brain to hang on to. take time to develop "shape" of system and learn what even doing. grug try not to factor in early part of project and then, at some point, good cut-points emerge from code base

good cut point has narrow interface with rest of system: small number of functions or abstractions that hide complexity demon internally, like trapped in crystal

grug quite satisfied when complexity demon trapped properly in crystal, is best feeling to trap mortal enemy!

sometimes grug go too early and get abstractions wrong, so grug bias towards waiting

also sometimes call demo approach "prototype", sound fancier to project manager

grug say prototype early in software making, especially if many big brains

## Testing
grug have love/hate relationship with test: test save grug many, many uncountable time and grug love and respect test

unfortunately also many test shamans exist. some test shaman make test idol, demand things like "first test" before grug even write code or have any idea what grug doing domain!

"Oh, don't worry: the tests will show you what you need to do."

grug once again catch grug slowly reaching for club, but grug stay calm

grug instead prefer write most tests after prototype phase, when code has begun firm up

but, note well: grug must here be very disciplined!

`unit tests` fine, ok, but break as implementation change (much compared api!) and make refactor hard and, frankly, many bugs anyway often due interactions other code. often throw away when code change.

grug write unit test mostly at start of project, help get things going but not get too attached or expect value long time

`end to end tests` good, show whole system work, but! hard to understand when break and drive grug crazy very often, sometimes grugs just end up ignoring because "oh, that break all time" very bad!

`in-between tests`, grug hear shaman call "integration tests" sometime often with sour look on face. but grug say integration test sweet spot according to grug: high level enough test correctness of system, low level enough, with good debugger, easy to see what break

grug prefer some unit tests especially at start but not 100% all code test and definitely not "first test". "test along the way" work pretty well for grug, especially as grug figure things out

one exception "first test" dislike by grug: when bug found. grug always try first reproduce bug with regression test then fix bug, this case only for some reason work better

### Agile

whenever agile project fail, agile shaman say "you didn't do agile right!" grug note this awfully convenient for agile shaman, ask more shiney rock better agile train young grugs on agile, danger!

grug tempted reach for club when too much agile talk happen but always stay calm

`prototyping, tools and hiring good grugs better key to success software`: agile process ok and help some but sometimes hurt taken too seriously

### Refactoring

however, grug note that many times in career "refactors" go horribly off rails and end up causing more harm than good


so grug try to keep refactors relatively small and not be "too far out from shore" during refactor. ideally system work entire time and each step of finish before other begin.

`end-to-end tests` are life saver here, but often very hard understand why broke... such is refactor life.

also grug notice that introducing too much abstraction often lead to refactor failure and system failure. good example was J2EE introduce, many big brain sit around thinking too much abstraction, nothing good came of it many project hurt

### Microservices
grug wonder why big brain take hardest problem, factoring system correctly, and introduce network call too

seem very confusing to grug

### Tools

grug love tool. tool and control passion what separate grug from dinosaurs! tool allow grug brain to create code that not possible otherwise by doing thinking for grug, always good relief! grug always spend time in new place learning tools around him to maximize productivity: learn tools for two weeks make development often twice faster and often have dig around ask other developers help, no docs

`code completion` in IDE allow grug not have remembered all API, very important!

java programming nearly impossible without it for grug!

really `make grug think` some time

`good debugger` worth weight in shiney rocks, in fact also more: when faced with bug grug would often trade all shiney rock and perhaps few children for good debugger and anyway debugger no weigh anything far as grug can tell

grug always recommend `new programmer learn available debugger very deeply`, features like conditional break points, expression evaluation, stack navigation, etc teach new grug more about computer than university class often!

### Type Systems
grug very like type systems make programming easier. for grug, `type systems most value when grug hit dot on keyboard and list of things grug can do pop up magic`. this 90% of value of type system or more to grug

danger abstraction too high, big brain type system code become astral projection of platonic generic turing model of computation into code base. grug confused and agree some level very elegant but also very hard do anything like record number of club inventory for Grug Inc. task at hand

generics especially dangerous here, grug try limit generics to container classes for most part where most value add

### Expression Complexity
grug once like to minimize lines of code much as possible. write code like this:

```
  if(contact && !contact.isActive() && (contact.inGroup(FAMILY) || contact.inGroup(FRIENDS))) {
    // ...
  }
```

over time grug learn this hard debug, learn prefer write like so:

```
  if(contact) {
    var contactIsInactive = !contact.isActive();
    var contactIsFamilyOrFriends = contact.inGroup(FAMILY) || contact.inGroup(FRIENDS);
    if(contactIsInactive && contactIsFamilyOrFriends) {
        // ...
    }
  }
```

grug hear screams from young grugs at horror of many line of code and pointless variable and grug prepare defend self with club

club fight start with other developers attack and grug yell: "easier debug! see result of each expression more clearly and good name! easier understand conditional expression! EASIER DEBUG!"

### DRY
DRY mean Don't Repeat Self, powerful maxim over mind of most developers

grug respect DRY and good advice, however grug recommend balance in all things, as gruggest big brain aristotle recommend

![Dry vs. Readability](../../../assets/img/dry.png)

### [Seperation of Concerns](https://en.wikipedia.org/wiki/Separation_of_concerns)


canonical example from web development: separation of style (css file), markup (html file) and logic (javascript file)


here grug much more sour faced than DRY and in fact write big brained essay on alternative design principle [locality of behavior (LoB)](https://htmx.org/essays/locality-of-behaviour/) against SoC

grug much prefer put code on the thing that do the thing. now when grug look at the thing grug know the thing what the thing do, always good relief!



### Closures
grug like closures for right job and that job usually abstracting operation over collection of objects

grug warn closures like salt, type systems and generics: small amount go long way, but easy spoil things too much use give heart attack

javascript developers call very special complexity demon spirit in javascript "callback hell" because too much closure used by javascript libraries very sad but also javascript developer get what deserved let grug be frank


### Logging

grug tips on logging are:

log all major logical branches within code (if/for)
if "request" span multiple machine in cloud infrastructure, include request ID in all so logs can be grouped
if possible make log level dynamically controlled, so grug can turn on/off when need debug issue (many!)
if possible make log level per user, so can debug specific user issue
last two points are especially handy club when fighting bugs in production systems very often

unfortunately log libraries often very complex (java, [why you do?](https://grugbrain.dev/#grug-on-factring-your-code:~:text=grug%20tips%20on,schools%2C%20grug%20think)) but worth investing time in getting logging infrastructure "just right" pay off big later in grug experience

logging need taught more in schools, grug think


### Concurrency
grug, like all sane developer, fear concurrency

as much as possible, grug try to rely on simple concurrency models like stateless web request handlers and simple remote job worker queues where jobs no interdepend and simple api

[optimistic concurrency](https://en.wikipedia.org/wiki/Optimistic_concurrency_control) seem work well for web stuff

occasionally grug reach for [thread local variable](https://en.wikipedia.org/wiki/Thread-local_storage), usually when writing framework code

some language have good concurrent data structure, like java [ConcurrentHashMap](https://docs.oracle.com/javase/8/docs/api/java/util/concurrent/ConcurrentHashMap.html) but still need careful grug work to get right

### Optimizing

ultra biggest of brain developer once say:

> premature optimization is the root of all evil

grug recommend always to have concrete, real world perf profile showing specific perf issue before begin optimizing.

beware only cpu focus: easy to see cpu and much big o notation thinking having been done in school, but often not root of all slowness, surprise to many including grug

hitting network equivalent of many, many millions cpu cycle and always to be minimized if possible, note well big brain microservice developer!

inexperienced big brain developer see nested loop and often say "O(n^2)? Not on my watch!"

### APIs
> grug love good apis. good apis not make grug think too much

unfortunately, many apis very bad, make grug think quite a bit. this happen many reasons, here two:
- API creators think in terms of implementation or domain of API, rather than in terms of use of API
- API creators think too abstract and big brained

usually grug not care too deeply about detail of api: want write file or sort list or whatever, just want to call write() or sort() or whatever

but big brain api developers say:

"not so fast, grug! is that file open for write? did you define a Comparator for that sort?"

grug find self restraining hand reaching for club again


### Parsing

grug think this because while complexity demon bad for code base and understand, complexity demon very good for generation of much academic papers, sad but true

production parser almost always [recursive descent](https://en.wikipedia.org/wiki/Recursive_descent_parser), despite ignore by schools! grug furious when learn how simple parse is! parsing not big brain only magic: so can you!

grug very elated find big brain developer Bob Nystrom redeem the big brain tribe and write excellent book on recursive descent: [Crafting Interpreters](https://craftinginterpreters.com/)

book available online free, but grug highly recommend all interested grugs purchase book on general principle, provide much big brain advice and grug love book very much `except visitor pattern (trap!)`

### Front End Development

"I know, I'll split my front end and back end codebase up and use a hot new SPA library talking to a GraphQL JSON API back end over HTTP (which is funny because I'm not transferring hypertext)"

now you have two complexity demon spirit lairs

keep complexity low, simple HTML, avoid lots javascript, the natural ether of spirit complexity demon


### Fear of Looking Dumb (FOLD)
note! very good if senior grug willing to say publicly: "hmmm, this too complex for grug"!

many developers Fear Of Looking Dumb (FOLD), grug also at one time FOLD, but grug learn get over: very important senior grug say "this too complicated and confuse to me"

this make it ok for junior grugs to admit too complex and not understand as well, often such case! FOLD major source of complexity demon power over developer, especially young grugs!

> take FOLD power away, very good of senior grug!

> note: important to make thinking face and look big brained when saying though. be prepare for big brain or, worse and much more common, thinks is big brain to make snide remark of grug

be strong! no FOLD!

club sometimes useful here, but more often sense of humor and especially last failed project by big brain very useful, so collect and be calm

### Imposter Syndrome

always grug one of two states: grug is ruler of all survey, wield code club like thor OR grug have no idea what doing

grug is mostly latter state most times, hide it pretty well though

> is maybe nature of programming for most grug to feel impostor and be ok with is best: nobody imposter if everybody imposter


### Conclusion
you say: complexity very, very bad

### Reference
https://grugbrain.dev/
