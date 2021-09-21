# FTECH-Tracking

## 1. Install

You need to install **AppsFlyer**, **Clevertap**, **GoogleAanalytics**, **Firebase Project** before start.

How to install? [Check in here](https://docs.google.com/document/d/1htHxDUe-Rn56WPBh-NjC2z-IsYad6P12tZDaQRvTplw/edit?usp=sharing)

## 2. Usage

### CommonEvent.


#### Screen track

Tracking for what screen was opened.

##### Parameters

-   `screen_name` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** 
-   `screen_class` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** 

##### Examples

```javascript
trackingEvent(CommonEvent.fs_screen_track, { screen_name: 'Login', screen_class: 'fs_screen_login' })
```


#### Custom event

Tracking custom event.

##### Parameters

-   `eventName` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** 
-   `eventValues` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** 

##### Examples

```javascript
trackingEvent(CommonEvent.fs_custom_event, { eventName: 'fs_login', eventValues: {} })
```

### Clevertap

[Check in here](https://github.com/longvubka98/FTECH-Tracking/blob/main/CleverTap.md)

### GoogleAnalytic.

[Check in here](https://github.com/longvubka98/FTECH-Tracking/blob/main/GoogleAnalytic.md)

### AppsFlyer

[Check in here](https://github.com/longvubka98/FTECH-Tracking/blob/main/AppsFlyer.md)

### Firebase

[Check in here](https://github.com/longvubka98/FTECH-Tracking/blob/main/Firebase.md)
