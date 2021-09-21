### User Profiles

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
trackingEvent(ClevertapEvent.ct_delete_inbox_message_for_id, '123456')	
```

#### Mark a message as Read for inbox Id

```javascript
trackingEvent(ClevertapEvent.ct_mark_read_inbox_message_for_id, '123456')	
```

#### pushInbox Notification Viewed Event For Id

```javascript 
trackingEvent(ClevertapEvent.ct_push_inbox_notification_viewed_event_for_id, '123456')
```

#### push Inbox Notification Clicked Event For Id

```javascript 
trackingEvent(ClevertapEvent.ct_push_inbox_notification_clicked_event_for_id, '123456')		
```

-----------

## Push Notifications

#### Creating Notification Channel

```javascript 
trackingEvent(ClevertapEvent.ct_create_notification_channel, {
channelID: 'CtRNS',
channelName: 'Clever Tap React Native Testing',
channelDescription: 'CT React Native Testing',
important: 1,
showBadge: true
}	
```

#### Delete Notification Channel

```javascript 
trackingEvent(ClevertapEvent.ct_push_inbox_notification_clicked_event_for_id, 'RNTesting')		
```

#### Creating a group notification channel

```javascript 
trackingEvent(ClevertapEvent.ct_push_inbox_notification_clicked_event_for_id, {
groupId: 'RNTesting',
groupName: 'React native testing'
})		
```

#### Delete a group notification channel

```javascript 
trackingEvent(ClevertapEvent.ct_push_inbox_notification_clicked_event_for_id, 'RNTesting')			
```

#### Registering Fcm Token

```javascript 
trackingEvent(ClevertapEvent.ct_push_inbox_notification_clicked_event_for_id, 'fcm_token')	
```

-----------

## Product Config 

#### Set Product Configuration to default

```javascript 
trackingEvent(ClevertapEvent.ct_set_defaults_map, {'text_color': 'red', 'msg_count': 100, 'price': 100.50, 'is_shown': true, 'json': '{"key":"val"}'})
```

#### Fetching product configs

```javascript 
trackingEvent(ClevertapEvent.ct_fetch)
```

#### Activate the most recently fetched product config

```javascript 
trackingEvent(ClevertapEvent.ct_activate)
```

#### Fetch And Activate product config

```javascript 
trackingEvent(ClevertapEvent.ct_fetch_and_activate)
```

#### Fetch Minimum Time Interval

```javascript 
trackingEvent(ClevertapEvent.ct_fetch_with_minimum_interval_in_seconds, 60)
```

#### Set Minimum Time Interval for Fetch 

```javascript 
trackingEvent(ClevertapEvent.ct_set_minimum_fetch_interval_in_seconds, 60)
```

#### Delete all activated, fetched and defaults configs

```javascript 
trackingEvent(ClevertapEvent.ct_reset_product_config)
```

## App Personalisation

#### Enable Personalization

```javascript 
trackingEvent(ClevertapEvent.ct_enable_personalization)		
```

#### Disable Personalization

```javascript 
trackingEvent(ClevertapEvent.ct_disable_personalization)	
```
