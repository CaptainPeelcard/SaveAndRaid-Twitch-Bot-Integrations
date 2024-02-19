# SAVE AND TWITCH BOT INTEGRATIONS
## What is this?
These are a collection of imports for specific local Twitch Bot applications that are used by broadcasters streaming to Twitch.

## Streamer.Bot New Donation Action Trigger
### Import and Setup
- Download the streamerbot_SaveAndRaid_DonationAlerts1.0.69.sb file
- In Streamer.Bot click on Import at the top
- Drag the file onto the Input String box, or open it then copy and paste the text.

  ![image](https://github.com/CaptainPeelcard/SaveAndRaid-Twitch-Bot-Integrations/assets/134344260/42e497a9-77ad-4054-8f58-5af3ea2eabc9)
  
- Click OK. You will be prompted that you need to enable the commmands. These commands are optional, streamerbot will automatically start listening for new donations when it connects to OBS! It will keep listening for alerts even if OBS closes though.

  ![image](https://github.com/CaptainPeelcard/SaveAndRaid-Twitch-Bot-Integrations/assets/134344260/e09a8bd9-e892-4a8e-a7ba-f0fd82794d8b)
  
- Add the timed action to the timed action trigger
  - Select the Action "$Code_SaveAndRaid_Donations"
  - Go to Triggers on the upper right and double click the Timed Trigger Action
  - Select Create Timer
    
    ![image](https://github.com/CaptainPeelcard/SaveAndRaid-Twitch-Bot-Integrations/assets/134344260/6141749e-3ec5-49f4-b6ef-4be1043c8cb5)
    
  - Enter the below details for the timer
    - Name: S&R_Donation_Poll
    - Enabled: Unchecked
    - Repeat: Checked
    - Random: Unchecked
    - Interval: 1 Second
    - Lines: 0
      
      ![image](https://github.com/CaptainPeelcard/SaveAndRaid-Twitch-Bot-Integrations/assets/134344260/2c6a2fd2-e22c-40db-8f79-4a12e62c0012)

- Optional: enable the two commands to enable/disable listening for triggers
  - Go to the Commands tab
  - Right click both commands under the SaveAndRaid Group and select "Enabled"
  - You can double click each command and adjust access permissions. Moderators have already been added to allowed.
    
    ![image](https://github.com/CaptainPeelcard/SaveAndRaid-Twitch-Bot-Integrations/assets/134344260/c16ae5ed-5ecd-4764-b90e-61c60de046a2)