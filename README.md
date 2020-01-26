## How to use  
  
1. Click 'Start' to begin scanning for BG Queue's and notifying you.
2. Click 'Stop' to halt scanning and notifications.
3. ???
4. Profit!  
  
## Download Options  

## Config/Settings  
Some initial configuration is required before it will work for you.  
If you right click and edit the BGNotifier.ps1 file you will see a section near the top that requires you to enter your own settings.

**Note: The only required setting to make this work is to set up one notification type.**  
Currently supported Notification apps are: Discord, Telegram, Pushover, Home Assistant and the Alexa 'Notify Me' Skill.  

### Required Setting:  
At least one of the below notification types is required. Or you can set up all 5 if you want!  

* **Discord Webhook URL**  
Set discord to $True to enable this notification type.
Enter in the discord webhook for the channel you would like the notification to go to.  
Discord > Click cogwheel next to a channel to edit it > Webhooks > Create webhook.
See this quick video I found on Youtube if you need further help. It's very easy. Do not share this Webhook with anyone else.  
[Create Discord Webhook](https://www.youtube.com/watch?v=zxi926qhP7w)  


### Optional/Advanced Settings:  

1. **Configure your own X,Y Coordinates of your Battleground Queue window**      
Everyones monitors are different, so just in case the default screenshot area does not work for you, you can specify your own. 

    1. Open WoW and queue for a BG. Once a BG Queue pops, leave it up and go to step b.  
    1. Launch the BGNotifier app and click the 'Get Coords'.  
    1. The next 2 mouse clicks (approx) that you perform will be recorded into the window for you to get the X,Y coordinates.
Your first click should be on the top left corner of the BG Queue window. Your second click should be on the bottom right of the BG Queue window. If you miss, or mess up, just click 'Exit Coords' in the app, and start again by clicking 'Get Coords'
    1. Keep the BGNotifier app open, write down, memorize (you're smart!), or screenshot the BGNotifier window that has the Top Left and Bottom Right X,Y coordinates. You will need these for the next step.  
    1. Right click on the actual script file. (BGNotifier.ps1) and select Edit. This should open the script for editing. Enter in the coordinates created during step d into their respective sections.  
    1. Set the 'useMyOwnCoordinates' to "Yes".

2. **Screenshot Path**  
Set the path to where you would like the temporary screenshot to be saved to.  
By default it goes to C:\temp\  

3. **Screenshot Delay**  
If you would like to change how often the script scans for the Battleground Queue Window you can enter a different time here in seconds.
Note: this script uses hardly any resources and is very quick at the screenshot/OCR process. Keep in mind you have 1.5min to accept the Queue. And this script needs to see the popup, and send the notification.  
Then you have to get off the toilet and make it back to your computer in time. Food for thought.  
Default Value: 20 seconds, which should give you about 1 minute after you get the notification to make it back to accept the Queue.  
  
4. **Stop on Queue**  
'Yes' will stop the script upon BG Queue detection. 'No' will have it continue to scan and must be stopped manually.  
Default is 'Yes'  
