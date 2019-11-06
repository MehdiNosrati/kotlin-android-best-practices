# kotlin-android-best-practices
*just notes*

 - For finding views efficiently use `lateinit var` to declare a field and then initialize it on lifecycle methods, instead of creating a new reference on each listener method.
- In order to support vector drawables on android SDKs below 21, add `
xmlns:app="http://schemas.android.com/apk/res-auto"`  to namespaces and instead of `android:src` use `
app:srcCompat 
`.
