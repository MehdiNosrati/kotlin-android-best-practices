# kotlin-android-best-practices
*just notes*

 - For finding views efficiently use `lateinit var` to declare a field and then initialize it on lifecycle methods, instead of creating a new refrence on each listener method.
- In order to support vector drawables on android SDKs below 21, add `
xmlns:app="http://schemas.android.com/apk/res-auto"`  to namespaces and instead of `android:src` use `
app:srcCompat
`.
### navigation
-   The  `popUpTo`  attribute of an action "pops up" the back stack to a given destination before navigating. (Destinations are removed from the back stack.)
-   If the  `popUpToInclusive`  attribute is  `false`  or is not set,  `popUpTo`  removes destinations up to the specified destination, but leaves the specified destination in the back stack.
-   If  `popUpToInclusive`  is set to  `true`, the  `popUpTo`  attribute removes all destinations up to and  _including_  the given destination from the back stack.
-   If  `popUpToInclusive`  is  `true`  and  `popUpTo`  is set to the app's starting location, the action removes  _all_  app destinations from the back stack. The Back button takes the user all the way out of the app.
-   Whatever code runs in onPause() blocks other things from displaying, so keep the code in onPause() lightweight. For example, if a phone call comes in, the code in onPause() may delay the incoming-call notification.
