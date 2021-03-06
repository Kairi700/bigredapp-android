# Big Red App for Android

## Download?
* Download it from the Play Store [here](https://play.google.com/store/apps/details?id=is.genki.bigredapp.android)!

## What
This is a native android application for Cornell students.  Right now, you can use the app to:
* See what dining halls are open and what they are serving
* Navigate Cornell's buildings, bus stops, and bike racks
* See what libraries are open
* Discover events around campus
* Lookup people by net ID

We are using [Kevin Chavez](https://github.com/mrkev)'s API [here](http://redapi-tious.rhcloud.com/).
We also use the Cornell Open Data Initiative API [here](https://cornelldata.org/).

## Objectives
* 100% free as in beer (no monetization) and free as in speech (open source).
* App: native Android, easy to use, good looking, minimal, clean.
* Code: well-commented, easy to maintain.

## iOS?
* The iOS by Matthew Gharrity has halted development, but you can check it out [here](https://github.com/gharrma/bigredapp-ios). 


## Contributing
* [Pull requests](http://git-scm.com/book/en/v2/GitHub-Contributing-to-a-Project) are very welcome!
* See the [issues page](https://github.com/genkimarshall/bigredapp-android/issues).
* Please post any issues for any questions / bug reports / ideas / etc. you have!
* If you are a beginner, please do not hesitate, as I am learning Android dev right now too.

## Overview of the code
* Hopefully you find the comments within the code itself helpful (if not, add an Issue about it!), but for a birds-eye view of how it all works:
* The relevant files are in [`app/src/main`](https://github.com/genkimarshall/bigredapp-android/tree/master/app/src/main).
* Find the activities inside [here](https://github.com/genkimarshall/bigredapp-android/tree/master/app/src/main/java/is/genki/bigredapp/android).
* `MainActivity.java` simply kicks off the `DiningListFragment.java` fragment, which displays a list of dining halls, along with some small text below it of its open status.
  * The fragment implements `SwipeRefreshListFragment.java`, more details can be found in the Java doc inside.
* Tapping on a row takes one to`DiningLocationActivity.java`, which displays details for the location (currently, just its menu).
* `AboutFragment.java` is a simple fragment to display meta-details about the app.
* All tabs within the navigation drawer are implemented as fragments, and follow a structure similar to that of DiningListFragment.
* All GET requests are done through `SingletonRequestQueue.java`. It works using a [`RequestQueue`](https://developer.android.com/training/volley/requestqueue.html). The basic idea is that at the very start (in `MainActivity.java`), a `RequestQueue` is started and stays around for the lifetime of the app. So, any time in the app process you can simply access it to add a request on to the queue.

## Up and Running
1. Use Android Studio version >= 1.10
2. Clone this repository
3. Open AS, click "Open an existing Android Studio project"
4. Navigate to where you cloned this repository (it should have a special icon by it in the file browser)
5. Click Ok

## OpenSourceCornell Club
* freenode IRC: #opensourcecornell
* [Facebook Group](https://www.facebook.com/groups/opensourcecornell)
* [Slack chat](https://opensourcecornell.slack.com/signup)

