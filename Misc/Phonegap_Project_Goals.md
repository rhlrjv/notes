# MyStore mobile app

Create a phonegap wrapper for a simple spree store. The platforms to target are Android and iOS.

## Features required

  * **Must have features** - for Paneco and Altus
    * Wrap website in mobile app
    * basic caching
      * explore HTTP caching
      * smooth navigation with turbolinks
    * Testing
    * Remember login with local storage
    * Graceful degradation when offline
      - no 404s

  * **Could have features**
    * Push notifications to the application on updates.
    * Use location to autofill address
    * Simulate different UIs for the 2 platforms.
      - Can be achieved using Rails variants, as well as local style
        sheets that overwrite aspects of the one recieved from the internet.

----
Another Idea: Using native components with webviews:
  * consider using React native + phonegap
