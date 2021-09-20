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

### Clevertap.

## User Profiles

#### Update User Profile(Push Profile)

```javascript
trackingEvent(ClevertapEvent.ct_profile_set, {"Identity":11102008, "Name":"React-Test Profile","Email":"r@gmail.com","Gender":"Male","DOB":"1995-10-14", "custom":1.73})
```

#### Set Multi Values For Key 

```javascript
trackingEvent(ClevertapEvent.ct_profile_set_multi_value_for_key, { key: 'letters', value: ['a', 'b', 'c'] })
```

#### Remove Multi Value For Key 

```javascript
trackingEvent(ClevertapEvent.ct_profile_remove_multi_value_for_key, { key: 'letters', value: 'b' })
```

#### Add Multi Value For Key

```javascript 
trackingEvent(ClevertapEvent.ct_profile_add_multi_value_for_key, { key: 'letters', value: 'd' })
```

#### Create a User profile when user logs in (On User Login)

```javascript
trackingEvent(ClevertapEvent.ct_on_user_login, {'Name': 'React-Test', 'Identity': '11102008', 'Email': 'r@gmail.com', 'custom1': 43})
```

#### Set Location to User Profile

```javascript
trackingEvent(ClevertapEvent.ct_set_location, { lat: 34.15, long: -118.20 })
```

#### Increment a User Profile property

```javascript
trackingEvent(ClevertapEvent.ct_profile_increment_value_for_key, { key: 'score', value: 1 })
```

#### Decrement a User Profile property

```javascript 
trackingEvent(ClevertapEvent.ct_profile_decrement_value_for_key, { key: 'score', value: 1 })
```

-----------

## User Events

#### Record an event  

```javascript
trackingEvent(ClevertapEvent.ct_record_event, { eventName: 'fs_login', evenData: {} })
```

#### Record Charged event

```javascript 
trackingEvent(ClevertapEvent.ct_record_changed_event, { detail: 'fs_login', items: [] })
```

-----------

## App Inbox

#### Initialize the CleverTap App Inbox Method

```javascript 
trackingEvent(ClevertapEvent.ct_initialize_inbox)
```

#### Show the App Inbox

```javascript
trackingEvent(ClevertapEvent.ct_show_inbox, {'tabs':['Offers','Promotions'],'navBarTitle':'My App Inbox','navBarTitleColor':'#FF0000','navBarColor':'#FFFFFF','inboxBackgroundColor':'#AED6F1','backButtonColor':'#00FF00'
                                ,'unselectedTabColor':'#0000FF','selectedTabColor':'#FF0000','selectedTabIndicatorColor':'#000000',
                                'noMessageText':'No message(s)','noMessageTextColor':'#FF0000'})
 ```

#### Delete message with id

```javascript 
trackingEvent(ClevertapEvent.ct_delete_inbox_message_for_id)
CleverTap.deleteInboxMessageForId('Message Id');		
```

#### Mark a message as Read for inbox Id

```javascript 
CleverTap.markReadInboxMessageForId('Message Id');		
```

#### pushInbox Notification Viewed Event For Id

```javascript 
CleverTap.pushInboxNotificationViewedEventForId('Message Id');		
```

#### push Inbox Notification Clicked Event For Id

```javascript 
CleverTap.pushInboxNotificationClickedEventForId('Message Id');			
```

-----------

## Push Notifications

#### Creating Notification Channel

```javascript 
CleverTap.createNotificationChannel("CtRNS", "Clever Tap React Native Testing", "CT React Native Testing", 1, true);			
```

#### Delete Notification Channel

```javascript 
CleverTap.deleteNotificationChannel("RNTesting");		
```

#### Creating a group notification channel

```javascript 
CleverTap.createNotificationChannelGroup(String groupId, String groupName);		
```

#### Delete a group notification channel

```javascript 
CleverTap.deleteNotificationChannelGroup(String groupId);			
```

#### Registering Fcm Token

```javascript 
CleverTap.setPushToken("<Replace with FCM Token value>", CleverTap.FCM);
```

-----------
 
## Native Display

#### Get Display Unit for Id

```javascript 
CleverTap.getDisplayUnitForId('Unit Id', (err, res) => {
        console.log('Get Display Unit for Id:', res, err);
});
```

#### Get All Display Units

```javascript 
CleverTap.getAllDisplayUnits((err, res) => {
        console.log('All Display Units: ', res, err);
});
```

-----------

## Product Config 

#### Set Product Configuration to default

```javascript 
CleverTap.setDefaultsMap({'text_color': 'red', 'msg_count': 100, 'price': 100.50, 'is_shown': true, 'json': '{"key":"val"}'});
```

#### Fetching product configs

```javascript 
CleverTap.fetch();
```

#### Activate the most recently fetched product config

```javascript 
CleverTap.activate();
```

#### Fetch And Activate product config

```javascript 
CleverTap.fetchAndActivate();
```

#### Fetch Minimum Time Interval

```javascript 
CleverTap.fetchWithMinimumIntervalInSeconds(60);
```

#### Set Minimum Time Interval for Fetch 

```javascript 
CleverTap.setMinimumFetchIntervalInSeconds(60);
```

#### Get Boolean key

```javascript 
CleverTap.getProductConfigBoolean('is_shown', (err, res) => {
	console.log('PC is_shown val in boolean :', res, err);
});
```
#### Get Long

```javascript 
CleverTap.getNumber('msg_count', (err, res) => {
	console.log('PC is_shown val in number(long)  :', res, err);
});
```
#### Get Double

```javascript 
CleverTap.getNumber('price', (err, res) => {
	console.log('PC price val in number :', res, err);
});		
```
#### Get String

```javascript 
CleverTap.getProductConfigString('text_color', (err, res) => {
        console.log('PC text_color val in string :', res, err);
});	
```
#### Get String (JSON)

```javascript 
CleverTap.getProductConfigString('json', (err, res) => {
	console.log('PC json val in string :', res, err);
});	
```

#### Delete all activated, fetched and defaults configs

```javascript 
CleverTap.resetProductConfig();
```

#### Get last fetched timestamp in millis

```javascript 
CleverTap.getLastFetchTimeStampInMillis((err, res) => {
        console.log('LastFetchTimeStampInMillis in string: ', res, err);
});		
```

## Feature Flag

#### Get Feature Flag

```javascript 
CleverTap.getFeatureFlag('is_dark_mode', false, (err, res) => {
	console.log('FF is_dark_mode val in boolean :', res, err);
});
```

## CleverTap ID

#### Get CleverTap ID

```javascript 
CleverTap.getCleverTapID((err, res) => {
        console.log('CleverTapID', res, err);
});
```

-----------

## App Personalisation

#### Enable Personalization

```javascript 
CleverTap.enablePersonalization();		
```

#### Disable Personalization

```javascript 
CleverTap.disablePersonalization();
```

#### Get Profile Name

```javascript 
CleverTap.profileGetProperty('Name', (err, res) => {
	console.log('CleverTap Profile Name: ', res, err);
});
```

-----------

## Attributions

#### Get CleverTap Attribution Identifier

```javascript 
CleverTap.profileGetCleverTapAttributionIdentifier((err, res) => {
         console.log('CleverTapAttributionIdentifier', res, err);
});
```

-----------

## InApp Notification Controls

#### Suspend InApp Notifications

```javascript 
CleverTap.suspendInAppNotifications();
```

#### Discard InApp Notifications

```javascript 
CleverTap.discardInAppNotifications();
```

#### Resume InApp Notifications

```javascript 
CleverTap.resumeInAppNotifications();
```


### GoogleAnalytic.


#### Table of Contents

-   [GoogleAnalyticsSettings](#googleanalyticssettings)
    -   [setOptOut](#setoptout)
        -   [Parameters](#parameters)
        -   [Examples](#examples)
    -   [setDispatchInterval](#setdispatchinterval)
        -   [Parameters](#parameters-1)
        -   [Examples](#examples-1)
    -   [setDryRun](#setdryrun)
        -   [Parameters](#parameters-2)
        -   [Examples](#examples-2)
-   [GoogleAnalyticsTracker](#googleanalyticstracker)
    -   [Examples](#examples-3)
    -   [trackScreenView](#trackscreenview)
        -   [Parameters](#parameters-3)
        -   [Examples](#examples-4)
    -   [trackEvent](#trackevent)
        -   [Parameters](#parameters-4)
        -   [Examples](#examples-5)
    -   [trackTiming](#tracktiming)
        -   [Parameters](#parameters-5)
        -   [Examples](#examples-6)
    -   [trackException](#trackexception)
        -   [Parameters](#parameters-6)
        -   [Examples](#examples-7)
    -   [trackSocialInteraction](#tracksocialinteraction)
        -   [Parameters](#parameters-7)
        -   [Examples](#examples-8)
    -   [setUser](#setuser)
        -   [Parameters](#parameters-8)
        -   [Examples](#examples-9)
    -   [setClient](#setclient)
        -   [Parameters](#parameters-9)
        -   [Examples](#examples-10)
    -   [getClientId](#getclientid)
        -   [Examples](#examples-11)
    -   [allowIDFA](#allowidfa)
        -   [Parameters](#parameters-10)
        -   [Examples](#examples-12)
    -   [setAppName](#setappname)
        -   [Parameters](#parameters-11)
        -   [Examples](#examples-13)
    -   [setAppVersion](#setappversion)
        -   [Parameters](#parameters-12)
        -   [Examples](#examples-14)
    -   [setAnonymizeIp](#setanonymizeip)
        -   [Parameters](#parameters-13)
        -   [Examples](#examples-15)
    -   [setSamplingRate](#setsamplingrate)
        -   [Parameters](#parameters-14)
        -   [Examples](#examples-16)
    -   [setCurrency](#setcurrency)
        -   [Parameters](#parameters-15)
        -   [Examples](#examples-17)

### GoogleAnalyticsSettings

Settings which are applied across all trackers.

#### setOptOut

Sets if OptOut is active and disables Google Analytics. This is disabled by default. Note: This has to be set each time the App starts.

##### Parameters

-   `enabled` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** 

##### Examples

```javascript
googleAnalyticTrack(GoogleAnalyticEvent.ga_set_opt_out, true);
```

#### setDispatchInterval

Sets the trackers dispatch interval.
Events, screen views, etc, are sent in batches to your tracker. This function allows you to configure how often (in seconds) the batches are sent to your tracker. Recommended to keep this around 20-120 seconds to preserve battery and network traffic. This is set to 20 seconds by default.

##### Parameters

-   `intervalInSeconds` **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** 

##### Examples

```javascript
googleAnalyticTrack(GoogleAnalyticEvent.ga_set_dispatch_interval, 30)
```

#### setDryRun

When enabled the native library prevents any data from being sent to Google Analytics. This allows you to test or debug the implementation, without your test data appearing in your Google Analytics reports.

##### Parameters

-   `enabled` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** 

##### Examples

```javascript
googleAnalyticTrack(GoogleAnalyticEvent.ga_set_dry_run, true)
```

#### trackScreenView

Track the current screen/view. Calling this will also set the "current view" for other calls.
 So events tracked will be tagged as having occured on the current view, `Home` in this example.
This means it is important to track navigation, especially if events can fire on different views.

##### Parameters

-   `screenName` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** (Required) The name of the current screen
-   `payload` **[HitPayload](#hitpayload)** (Optional) An object containing the hit payload (optional, default `null`)

##### Examples

```javascript
const payload = { impressionList: "Sale", impressionProducts: [ { id: "PW928", name: "Premium bundle" } ] };
googleAnalyticTrack(GoogleAnalyticEvent.ga_track_screen_view, { screenName:"Home", payload })
```

#### trackEvent

Track an event that has occured

##### Parameters

-   `category` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** (Required) The event category
-   `action` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** (Required) The event action
-   `eventMetadata` **[EventMetadata](#eventmetadata)** (Optional) An object containing event metadata
-   `payload` **[HitPayload](#hitpayload)** (Optional) An object containing the hit payload (optional, default `null`)

##### Examples

```javascript
const product = {
  id: "P12345",
  name: "Android Warhol T-Shirt",
  category: "Apparel/T-Shirts",
  brand: "Google",
  variant: "Black",
  price: 29.2,
  quantity: 1,
  couponCode: "APPARELSALE"
};
googleAnalyticTrack(GoogleAnalyticEvent.ga_track_event, {
  category: 'FinalizeOrderButton',
  action: 'Click',
  eventMetadata: null,
  product
})
```

#### trackTiming

Track a timing measurement

##### Parameters

-   `category` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** (Required) The event category
-   `interval` **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** (Required) The timing measurement in milliseconds
-   `timingMetadata` **[TimingMetadata](#timingmetadata)** (Required) An object containing timing metadata
-   `payload` **[HitPayload](#hitpayload)** (Optional) An object containing the hit payload (optional, default `null`)

##### Examples

```javascript
googleAnalyticTrack(GoogleAnalyticEvent.ga_track_timing, {
  category: 'testcategory',
  interval: 2000,
  timingMetadata: { name: "LoadList", label: "v1.0.3" },
  payload: null
})
```

#### trackException

Track an exception

##### Parameters

-   `error` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** (Required) The description of the error
-   `fatal` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** (Optional) A value indiciating if the error was fatal, defaults to false (optional, default `false`)
-   `payload` **[HitPayload](#hitpayload)** (Optional) An object containing the hit payload (optional, default `null`)

##### Examples

```javascript
try {
  ...
} catch(error) {
  googleAnalyticTrack(GoogleAnalyticEvent.ga_track_exception, error)
}
```

#### trackSocialInteraction

Track a social interaction, Facebook, Twitter, etc.

##### Parameters

-   `network` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** 
-   `action` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** 
-   `targetUrl` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** 
-   `payload` **[HitPayload](#hitpayload)** (Optional) An object containing the hit payload

##### Examples

```javascript
googleAnalyticTrack(GoogleAnalyticEvent.ga_track_social_interaction, {
  network: 'Twitter',
  action: 'Post'
})
```

#### setUser

Sets the current userId for tracking.

##### Parameters

-   `userId` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** An anonymous identifier that complies with Google Analytic's user ID policy

##### Examples

```javascript
googleAnalyticTrack(GoogleAnalyticEvent.ga_set_user, '12345678')
```

#### setClient

Sets the current clientId for tracking.

##### Parameters

-   `clientId` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** A anonymous identifier that complies with Google Analytic's client ID policy

##### Examples

```javascript
googleAnalyticTrack(GoogleAnalyticEvent.ga_set_client, '35009a79-1a05-49d7-b876-2b884d0f825b')
```

#### allowIDFA

Also called advertising identifier collection, and is used for advertising features.

**Important**: For iOS you can only use this method if you have done the optional step 6 from the installation guide. Only enable this (and link the appropriate libraries) if you plan to use advertising features in your app, or else your app may get rejected from the AppStore.

##### Parameters

-   `enabled` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** (Optional) Defaults to true (optional, default `true`)

##### Examples

```javascript
googleAnalyticTrack(GoogleAnalyticEvent.ga_allow_IDFA, true)
```

#### setAppName

Overrides the app name logged in Google Analytics. The Bundle name is used by default. Note: This has to be set each time the App starts.

##### Parameters

-   `appName` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** (Required)

##### Examples

```javascript
googleAnalyticTrack(GoogleAnalyticEvent.ga_set_app_name, 'YourAwesomeApp')
```

#### setAppVersion

Sets the trackers appVersion

##### Parameters

-   `appVersion` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** (Required)

##### Examples

```javascript
googleAnalyticTrack(GoogleAnalyticEvent.ga_set_app_version, '1.3.2')
```

#### setAnonymizeIp

Sets if AnonymizeIp is enabled
If enabled the last octet of the IP address will be removed

##### Parameters

-   `enabled` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** (Required)

##### Examples

```javascript
googleAnalyticTrack(GoogleAnalyticEvent.ga_set_anonymize_ip, true)
```

#### setSamplingRate

Sets tracker sampling rate.

##### Parameters

-   `sampleRatio` **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** (Required) Percentage 0 - 100

##### Examples

```javascript
googleAnalyticTrack(GoogleAnalyticEvent.ga_set_sampling_rate, 50)
```

#### setCurrency

Sets the currency for tracking.

##### Parameters

-   `currencyCode` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** (Required) The currency ISO 4217 code

##### Examples

```javascript
googleAnalyticTrack(GoogleAnalyticEvent.ga_set_currency, 'EUR')
```
