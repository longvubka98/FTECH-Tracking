## AppsFlyer.

#### onInstallConversionData

The code implementation for the conversion listener must be made prior to the initialization code of the SDK.

```javascript
trackingEvent(AppsFlyerEvent.af_onInstallConversionData)
```

#### setCustomerUserId

Setting your own Custom ID enables you to cross-reference your own unique ID with AppsFlyer’s user ID and the other devices’ IDs.

| parameter | type     | description      |
| ----------|----------|------------------|
| userId    | string   | user ID          |
| callback  | function | success callback |

```javascript
trackingEvent(AppsFlyerEvent.af_setCustomerUserId,{CustomerUserId})
```

#### getAppsFlyerUID

AppsFlyer's unique device ID is created for every new install of an app. Use the following API to obtain AppsFlyer’s Unique ID.

| parameter | type     | description                     |
| ----------|----------|------------------               |
| callback  | function | returns `(error, appsFlyerUID)` |

```javascript
trackingEvent(AppsFlyerEvent.af_getAppsFlyerUID,{appsFlyerUID})
```


#### stop

This can be achieved with the stopSDK API

| parameter       | type     | description                                          |
| ----------      |----------|------------------                                    |
| isStopped  | boolean  | True if the SDK is stopped (default value is false). |
| callback        | function | success callback                                     |

```javascript
trackingEvent(AppsFlyerEvent.af_stop,{param})
```

#### logLocation

Manually record the location of the user.

| parameter       | type     | description               |
| ----------      |----------|------------------         |
| longitude       | float    | longitude                 |
| latitude        | float    | latitude                  |
| callback        | function | Success / Error Callbacks |

```javascript
trackingEvent(AppsFlyerEvent.af_logLocation,{param})
```

#### setUserEmails

Set the user emails and encrypt them.

| parameter       | type     | description               |
| ----------      |----------|------------------         |
| configuration   | json     | email configuration       |
| success         | function | success callback          |
| error           | function | error callback             |

```javascript
trackingEvent(AppsFlyerEvent.af_setUserEmails,{param})
```


#### setAdditionalData

The setAdditionalData API is required to integrate on the SDK level with several external partner platforms, including Segment, Adobe and Urban Airship

```javascript
trackingEvent(AppsFlyerEvent.af_setAdditionalData,{param})
```

#### updateServerUninstallToken

(Android only)

Manually pass the Firebase / GCM Device Token for Uninstall measurement.

```javascript
trackingEvent(AppsFlyerEvent.af_updateServerUninstallToken,{param})
```
#### setCollectIMEI

Opt-out of collection of IMEI.

```javascript
trackingEvent(AppsFlyerEvent.af_setCollectIMEI,{param})
```

#### setCollectAndroidID

❗(Android only)

Opt-out of collection of Android ID.

```javascript
trackingEvent(AppsFlyerEvent.af_setCollectAndroidID,{param})
```

#### setAppInviteOneLinkID

Set the OneLink ID that should be used for User-Invite-API.

```javascript
trackingEvent(AppsFlyerEvent.af_setAppInviteOneLinkID,{param})
```

#### generateInviteLink

```javascript
trackingEvent(AppsFlyerEvent.af_generateInviteLink,{param})
```

#### logCrossPromotionImpression

To attribute an impression use the following API call.

```javascript
trackingEvent(AppsFlyerEvent.af_logCrossPromotionImpression,{param})
```

#### logCrossPromotionAndOpenStore

Use the following API to attribute the click and launch the app store's app page.

```javascript
trackingEvent(AppsFlyerEvent.af_logCrossPromotionAndOpenStore,{param})
```


#### setCurrencyCode

Setting user local currency code for in-app purchases.

```javascript
trackingEvent(AppsFlyerEvent.af_setCurrencyCode,{param})
```

#### anonymizeUser

It is possible to anonymize specific user identifiers within AppsFlyer analytics.

```javascript
trackingEvent(AppsFlyerEvent.af_anonymizeUser,{param})
```

#### setOneLinkCustomDomains

Set Onelink custom/branded domains
Use this API during the SDK Initialization to indicate branded domains.

```javascript
trackingEvent(AppsFlyerEvent.af_setOneLinkCustomDomains,{param})
```

#### setResolveDeepLinkURLs

Set domains used by ESP when wrapping your deeplinks.
Use this API during the SDK Initialization to indicate that links from certain domains should be resolved in order to get original deeplink

```javascript
trackingEvent(AppsFlyerEvent.af_setResolveDeepLinkURLs,{param})
```

#### performOnAppAttribution

This function allows developers to manually re-trigger onAppOpenAttribution with a specific link (URI or URL), without recording a new re-engagement.

```javascript
trackingEvent(AppsFlyerEvent.af_performOnAppAttribution,{param})
```

#### setSharingFilterForAllPartners

```javascript
trackingEvent(AppsFlyerEvent.af_setSharingFilterForAllPartners,{param})
```

#### setSharingFilter

```javascript
trackingEvent(AppsFlyerEvent.af_setSharingFilter,{param})
```

#### disableCollectASA

❗(iOS only)

Disables Apple Search Ads collecting

```javascript
trackingEvent(AppsFlyerEvent.af_disableCollectASA,{param})
```

#### disableAdvertisingIdentifier

Disables IDFA collection in iOS and Advertising ID in Android.

```javascript
trackingEvent(AppsFlyerEvent.af_disableAdvertisingIdentifier,{param})
```

#### validateAndLogInAppPurchase

Receipt validation is a secure mechanism whereby the payment platform (e.g. Apple or Google) validates that an in-app purchase indeed occurred as reported.

```javascript
trackingEvent(AppsFlyerEvent.af_validateAndLogInAppPurchase,{param})
```

#### sendPushNotificationData

Push-notification campaigns are used to create fast re-engagements with existing users

```javascript
trackingEvent(AppsFlyerEvent.af_sendPushNotificationData,{param})
```

#### setHost

Set a custom host

```javascript
trackingEvent(AppsFlyerEvent.af_setHost,{param})
```


#### addPushNotificationDeepLinkPath

The addPushNotificationDeepLinkPath method provides app owners with a flexible interface for configuring how deep links are extracted from push notification payloads

```javascript
trackingEvent(AppsFlyerEvent.af_addPushNotificationDeepLinkPath,{param})
```

#### disableSKAD

❗Important❗ disableSKAD must be called before calling initSDK and for iOS ONLY!

```javascript
trackingEvent(AppsFlyerEvent.af_disableSKAD,{param})
```

#### setCurrentDeviceLanguage

Set the language of the device.

```javascript
trackingEvent(AppsFlyerEvent.af_setCurrentDeviceLanguage,{param})
```

#### setSharingFilterForPartners

Used by advertisers to exclude networks/integrated partners from getting data.

| parameter                   | type     | description                                                |
| ----------                  |----------|------------------                                          |
| partners                    | array    | Comma separated array of partners that need to be excluded |

```javascript
trackingEvent(AppsFlyerEvent.af_setSharingFilterForPartners,{param})
```
