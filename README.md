# Unity-Send-Local-Notification-
Unity Send Local Notification 

🍎Download this asset on your project:

Android: 
https://assetstore.unity.com/packages/tools/integration/simple-android-notifications-free-68626




💣Source Code:
                    
                    using Assets.SimpleAndroidNotifications; 

                    private string title = "This is Title";
                    private string content = "This is Content";
                    
                    private void OnApplicationPause(bool isPause)
                    {
                         #if UNIY_ANDROID
                         NotificationManager.CancelAll();
                         if(isPause)
                         {
                         
                              Datetime timeToNotify = Datetime.Now.AddMinutes(1);
                              TimeSpan time = timeToNotify - DateTime.Now;
                              NotificationManager.SendWithAppIcon(time,title,content,Color.green,NotificationIcon.Bell);
                         }
                       #endif
                    
                    }
                    
                    
                    
                    







