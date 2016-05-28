# Building modile apps with web technologies.
** with phonegap and rails **

---

# Main challenges to overcome.

  * unreliable internet connection
  * memory management.

---

# The default way to build a static mobile application

  * create a phonegap project
  * add all your static pages into the `www/` folder
    retrieve all the dynamic stuff uning an api service
  * run ` phonegap build android `
  * open the android project created in android studio
  * run on the emulator, package as an application

---

# creating an hybrid app

This is the way to create multiple native components and then have then internally display a webview.

There are 2 main approaches to take while building a hybrid app...

  * creating a wrapper application
  * using webviews along with native components and navigation

---

## creating a wrapper

This means to just add a simple webview in the `onDeviceReady` event handler

  ```
    onDeviceReady: function() {
        window.open('http://skinnymint.com', '_self', 'location=no,zoom=no');
    },
  ```

This gives a very thin native wrapper around the mobile experience of the webapp.

The main issue with this approach is that the appstores will not allow us to publish
these apps, since they are basically glorified browsers.

There can be some added logic present on the frontend that integrates with GPS,
authentication and fallback assets. we can also have some smart caching.

The main benefit of this approach is that we are using the same codebase for
both iOS and android

** TODO 2: investigate what such an application would look like **

--

## Using webviews with native navigation and components

The basic understanding is that we can embed different webviews into different tabs.

This makes the app feel more native since we are using platform specific design element.

The main disadvantage is that we need to work on both iOS and Android separately.
And there is more dev work involved. That being said, most respectable products use this approach to building a hybrid application.

  * use webkit in frontend
  * business logic - web application
  * js for mobile features
  * HTML5 client side storage
  * cache pages

** DOING NOW: currently invesigating **

---

# Apple guidelines to watch out for:

  * Apps that are not very useful, unique, are simply web sites bundled as Apps, or do not provide any lasting entertainment value may be rejected.
  * Apps that are "demo", "trial", or "test" versions will be rejected. Beta Apps may only be submitted through TestFlight and must follow the TestFlight guidelines.

# References

[basecamp case study]: https://signalvnoise.com/posts/3743-hybrid-sweet-spot-native-navigation-web-content
[rails variants]: http://edgeguides.rubyonrails.org/4_1_release_notes.html#action-pack-variants
[grunt ripple development]: https://blog.moonswitch.com/phonegap-development-with-grunt-ripple-and-a-browser-aa5e5e60247e#.sjp75atyg
[good resource about hybrid apps]: http://docs.phonegap.com/develop/1-embed-webview/android/
[different mobile choices]: http://phonegap.com/blog/2015/03/12/mobile-choices-post1/
[HTML5 cache manifest]: http://www.html5rocks.com/en/tutorials/appcache/beginner/
[Turbolinks]: https://github.com/turbolinks/turbolinks
