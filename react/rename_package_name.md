For Android:

Manually change it in android/app/src/main/java/com/PROJECT_NAME/MainActivity.java:
package MY.APP.ID;

In android/app/src/main/java/com/PROJECT_NAME/MainApplication.java:
package MY.APP.ID;

In android/app/src/main/AndroidManifest.xml:
package="MY.APP.ID"

In android/app/build.gradle:
applicationId "MY.APP.ID"

Gradle' cleaning in the end (in /android folder):
./gradlew clean


For iOS:
Change the Bundle Id in Xcode.
