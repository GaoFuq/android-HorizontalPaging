
Android HorizontalPaging Sample
===================================

This sample shows how to implement tabs, using Fragments and a ViewPager.

Introduction
------------

This sample implements tabs using the deprecated [ActionBar.TabListener][1]. It uses [ViewPager][2] and
[FragmentPagerAdapter][3] to handle swiping between tabs and displaying the selected tab content.


1. Create an Activity that extends [FragmentActivity][4], with a [ViewPager][2] for its layout.
2. Implement [ActionBar.TabListener][1] interface.
3. Create a class that extends [FragmentPagerAdapter][3] and override its `getItem(int position)`,
`getCount()` and `getPageTitle(int position)` methods.
4. In the `onCreate(Bundle savedInstanceState)` method of your activity, set navigation mode to tabs for the
ActionBar using `setNavigationMode(ActionBar.NAVIGATION_MODE_TABS)`. Note: This is DEPRECATED as of Android
Lollipop.
5. Set your custom [FragmentPagerAdapter][3] on your [ViewPager][2].
6. Implement `setOnPageChangeListener(new ViewPager.SimpleOnPageChangeListener())` on your [ViewPager][2] to
know the selected tab, so you can update your ActionBar with `setSelectedNavigationItem(position)`.

[1]: http://developer.android.com/reference/android/support/v7/app/ActionBar.TabListener.html
[2]: http://developer.android.com/reference/android/support/v4/view/ViewPager.html
[3]: http://developer.android.com/reference/android/support/v4/app/FragmentPagerAdapter.html
[4]: http://developer.android.com/reference/android/support/v4/app/FragmentActivity.html

Pre-requisites
--------------

- Android SDK 27
- Android Build Tools v27.0.2
- Android Support Repository

Screenshots
-------------

<img src="screenshots/1-tab1.png" height="400" alt="Screenshot"/> <img src="screenshots/2-tab2.png" height="400" alt="Screenshot"/> 

Getting Started
---------------

This sample uses the Gradle build system. To build this project, use the
"gradlew build" command or use "Import Project" in Android Studio.

Support
-------

- Google+ Community: https://plus.google.com/communities/105153134372062985968
- Stack Overflow: http://stackoverflow.com/questions/tagged/android

If you've found an error in this sample, please file an issue:
https://github.com/googlesamples/android-HorizontalPaging

Patches are encouraged, and may be submitted by forking this project and
submitting a pull request through GitHub. Please see CONTRIBUTING.md for more details.

License
-------

Copyright 2017 The Android Open Source Project, Inc.

Licensed to the Apache Software Foundation (ASF) under one or more contributor
license agreements.  See the NOTICE file distributed with this work for
additional information regarding copyright ownership.  The ASF licenses this
file to you under the Apache License, Version 2.0 (the "License"); you may not
use this file except in compliance with the License.  You may obtain a copy of
the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  See the
License for the specific language governing permissions and limitations under
the License.
