# Kopirun Retro

** 1 - Hard, 5 - Trivial **

---

### UI/Styling(4)

  * This is made easy due to the debugger and monitoring.
  * Styling with flexbox and inbuilt components is very easy.
  * Hot realoading makes the feedback cycle much faster.
  * Experience is very similar to frontend web dev
  * Atomic styling using objects rather than css - > can merge, append and have conditionals
  * Although, one issue we faced was that all the components come with no default styles.
  * this means we need to style them from scratch for both the platforms

---

### Integration testing (1)

  * Setup is easy. Selectors are not yet working so well with non-xpath. Once we figure that,
  * I would rank this 4.
  * stack: appium/android.


---

### Unit testing/Mocking (3)

  * Experience with React helped us.
  * All the native components need to be swapped in as divs using react.
  * Jest may be better since it dynamically mocks out all classes that are not currently under test.
  * stack: Mocha, Chai, Sinon, Enzyme


---

### API integration (5)

  * Super easy thanks to JS


---

### Navigation/App flow (3.5)

  * It is hard the first time. This requires you to understand the component lifecycle events and
  * mobile app navigation (IOS and Android)
  * Next time we need to do navigation, it would be easy.
  * Need to handle android back button manually.


---

### Misc
  * React native, being rather new to android, we found it hard to find samples for android testing/dev
    either way, the ecosystem is still in its early days... needs some more time before we can use it for a production app.

  * Integrating Open source components
    Really easy to integrate external components thanks to react's one way data flow.

  * getting started
    setup and first app did not take long. the react-native packager contains all its requirements,
    and we did not waste time setting up compile steps for things like webpack/babel

  * Live reloading/ remote debugger
    very fast feedback due to real time updates to the app running on the device/emulator/simulator


---

## How we feel about the app :)

  * Do not think it looks professional yet. needs some more design love.
  * happy with the native feel, decent interactions.
  * Code base is decent. Thanks Gabe for feedback on the code.
  * Most components are stateless, only the top level component stores current state.
  * Files are small.
  * ES6 linter (eslint)  has been very useful.

---

## Future improvements

  * Redux - will make all our components stateless, and help with testing.
  * Better design
  * Integration testing
    * test both ios and android with same test files
    * add integration tests to ci.



----
#end
----
# Learnings


## cleaning out global npm  - since they are not being added into your package file

```
npm ls -gp --depth=0 | awk -F/node_modules/ '{print $NF}' | grep -v npm | awk '{ print "npm -g rm ", $1}' | bash
```

## create circle.yml to define machine requirements.

## firebase treats all data as a stream of events - no need to handle arrays.
