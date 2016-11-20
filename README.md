#Instructions:

Imagine you are working on the attached application as part of a team. This is just the first part of an application that will have a large number of features, multiple versions and that will be published for international markets.

Code review the application and make comments on the flaws, errors and possible improvements you would make to the code.  You are expected to provide a pdf document with your review notes

Be as thorough as you can and tell us why and how you would do it. There are multiple ways to do things and while we might not agree with your suggestions we are looking for someone who is able to apply best practices, spot technical errors and areas of opportunity and suggest new or different ways to do things.

Feel free to suggest any 3rd party libraries or tools.

# Fixes

The fix for the first error (3.2 The application crashes out (Issue 1 to be fixed)) is to allow the application to use Internet connection in manifest. Without necessary permission, the android system blocks the application from accessing to required permission resources. 

The fix for the second error (3.2 The application displays data from API but the images are loaded as bitmaps (fix this issue)) is to use third party glide or Picasso libraries. For this application, I have used Picasso. The library deals with caching images and loads images on background thread (avoid blocking main ui thread).  

Extra 1: Downloaded images can be saved in local SD card with Picasso target and load them later as files when songs are load from local. 

Extra 2: Dialog for popping up options to load data from Internet or local shouldn’t be shown if there is not Internet connection. Instead attempt to load from local if there are local data.
