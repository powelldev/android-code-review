# android-code-review
Checklist to examine when reviewing Android code - synthesizd over a few years of running into these problems.

1. Are there any long running methods in a BroadcastReceiver? 
2. Are operations that run in the background without an active application a) off the main thread and b) handled by a Service class?
3. Context objects passed around are only obtained from getApplicationContext()?
4. Is the right storage mechanism being used when saving data?
5. Is data loaded to a List or GridView coming from a ContentProvider? If not, have a decent reason.
6. Does the project build?
7. Does gradle contain wildcard dependencies? If so, remove or have a good reason.
