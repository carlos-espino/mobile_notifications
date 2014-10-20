#Mobile notifications

Mobile Notificactions provide two modules.

##DrupalGap Mobile Notifications module

Provide support for [PhoneGap PushPlugin](https://github.com/phonegap-build/PushPlugin).

Register mobile devices in your Drupal site and receive push notifications.

When a notification arrives, the device beeps and display the notifications view.

###Install

Copy mobile_notifications.js in "/app/modules/custom/mobile_notifications".

Active module in your settings.js file with this line:

`Drupal.modules.custom['mobile_notifications'] = {};`

Add this menu link in some menu in your settings.js file:

`{

	title:'Notifications',
	
	path:'mobile-notifications',
	
	options:{
	
		reloadPage:true,
		
		attributes:{
		
			'data-icon':'info'
			
		}
		
	}
	
}`

Copy in your module folder (app/modules/custom/mobile_notifications/) the PushNotification.js file. Is in the plugin folder in "plugins/com.phonegap.plugins.PushPlugin/Example/www/"

###Config

Change config value in mobile_notifications.js:

`var registration_url = 'http://your-drupal-site.org/drupalgap/push_notifications';

var get_token_url = "http://your-drupal-site.org/services/session/token";

var sender_id = "your google sender_id";`

##Drupal Mobile Notifications module

This module provide a "Mobile Notifications" node type and a view called "Mobile Notifications". When you add a new Mobile Notification post, the module send a push notification to registered devices. You can choose the roles that receive this notification. You can, also, send a link to a site node.

###Install

Copy the folder mobile_notifications in your drupal site, normally in 'sites/all/modules' and active in modules admin page.

###Config

Not config is required
