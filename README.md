# Lint Android app on Wercker sample.

## Notice
**This Repository depends on beta release of Android Studio and Android Plugin for Gradle.**

## Goal
1. Run just only lint Gradle task
1. Don't create original Docker image
1. Install Android SDK via Android Plugin for Gradle

## Usage
- Upgrade Gradle plugin version to `3.0.0` following [Developer page](https://developer.android.com/studio/build/gradle-plugin-3-0-0-migration.html)
- Add content of `$ANDROID_HOME/licenses/android-sdk-license` on your local machine to following line of `wercker.yml`  
  `echo "LICENSE_CONTENT_HERE" > $ANDROID_HOME/licenses/android-sdk-license`
- Create `ANDROID_HOME` environment variable on Wercker following [here](http://devcenter.wercker.com/docs/environment-variables/creating-env-vars).
- Push to GitHub or BitBucket

## Extra
Using `WERCKER_CACHE_DIR` will save time to download. [Documents](http://devcenter.wercker.com/docs/quickstarts/building/java#build-pipeline)
