# SAVE AND RAID TWITCH BOT INTEGRATIONS
## What is this?
These are a collection of imports for specific local Twitch Bot applications that are used by broadcasters streaming to Twitch.

### What is Save and Raid?
Save&Raid (S&R) is a multi-streamer relay marathon where our community of streamers, over the course of a weekend, works in turns to complete a game series by playing for one hour each, then passing along the save files and viewers to the next streamer in the list, through the use of Twitch raids. We raise money for suicide prevention each year through Suicide Awareness Voices of Education (SAVE).

## Streamer.Bot New Donation Action Trigger
### Import and Setup
- Download [streamerbot_SaveAndRaid_DonationAlerts1.0.69.sb](https://github.com/CaptainPeelcard/SaveAndRaid-Twitch-Bot-Integrations/blob/5215b1cbf6470ccdca520323dbe05f672818dc8e/streamerbot_SaveAndRaid_DonationAlerts1.0.69.sb)
- In Streamer.Bot click on Import at the top
- Drag the file onto the Input String box, or open it then copy and paste the text.

  <img src="https://github.com/CaptainPeelcard/SaveAndRaid-Twitch-Bot-Integrations/assets/134344260/42e497a9-77ad-4054-8f58-5af3ea2eabc9" width="400">
  
- Click OK. You will be prompted that you need to enable the commmands. These commands are optional, streamerbot will automatically start listening for new donations when it connects to OBS! It will keep listening for alerts even if OBS closes though.

  ![image](https://github.com/CaptainPeelcard/SaveAndRaid-Twitch-Bot-Integrations/assets/134344260/e09a8bd9-e892-4a8e-a7ba-f0fd82794d8b)
  
- Close streamer.bot and reopen it so the custom trigger gets added correctly.
- Add the timed action to the timed action trigger
  - Select the Action "$Code_SaveAndRaid_Donations" under Actions in the Actions tab
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
    
    <img src="https://github.com/CaptainPeelcard/SaveAndRaid-Twitch-Bot-Integrations/assets/134344260/c16ae5ed-5ecd-4764-b90e-61c60de046a2" width="400">

  - Select the Timer we created in the "! Start_DonationTriggers" and "! Stop_DonationTriggers" Actions
      - Find the action in the Actions on the left under the Actions tab
      - In the Sub-Actions, double click the Timer sub action, and select "S&R_Donation_Poll"
        ![image](https://github.com/CaptainPeelcard/SaveAndRaid-Twitch-Bot-Integrations/assets/134344260/67efcad1-5eb7-4039-9812-85c3b79baf1d)



### Usage
- Add whatever actions and sub-actions you want to kick off to the New_Donation Action
  
  ![image](https://github.com/CaptainPeelcard/SaveAndRaid-Twitch-Bot-Integrations/assets/134344260/964857b3-76fd-4f4d-9f55-f8e9c58e7829)

- Optional: if you want to use your own action directly, or trigger multiple actions, you can add this trigger to them!
  
    Custom > Save And Raid > New Donation

  <img src="https://github.com/CaptainPeelcard/SaveAndRaid-Twitch-Bot-Integrations/assets/134344260/be54f68f-17cf-40a7-a9ec-532a73eea1a7" width="400">
  
- When the action occurs, you can access the donation info with these variables
    - DonationName
    - DonationAmount
    - DonationMessage
      
    ![image](https://github.com/CaptainPeelcard/SaveAndRaid-Twitch-Bot-Integrations/assets/134344260/b360e54d-551e-4617-800b-fadbb557b7a6)



## SAMMI New Donation Action Trigger
### Import and Setup
- Download [SAMMI_SaveAndRaid_NewDonations.1.0.69.txt](https://github.com/CaptainPeelcard/SaveAndRaid-Twitch-Bot-Integrations/blob/5215b1cbf6470ccdca520323dbe05f672818dc8e/SAMMI_SaveAndRaid_NewDonations.1.0.69.txt)
- In SAMMI Click Paste Deck
- Double click the new deck to edit it
- Double click the New Donation Button
- Add what you want to happen with a new donation. This button is already set up to occur on a queue so multiple donations at the same time will happen after the previous completes.
- Optionally, if you want a different button to run with a new donation, you can add the SaveAndRaid_NewDonation Extension Trigger to it. Right click your button > Edit Triggers > Add Trigger > Extension Trigger
  
  ![image](https://github.com/CaptainPeelcard/SaveAndRaid-Twitch-Bot-Integrations/assets/134344260/edfba4e0-7c59-4a01-a05f-2dfd2cbd31ed)


### Usage
- You can use the Run Test Donation button to test out your action. It will ask you to enter the name, amount, and message for the donation so you can test how it looks and works.
- The donation information is available to you through several variables accessed in the trigger. They have already been accessed and set to variables for you in the included New Donation Button
    - donation_Name
    - donation_Amount
    - donation_Message
      
  ![image](https://github.com/CaptainPeelcard/SaveAndRaid-Twitch-Bot-Integrations/assets/134344260/5f2cc153-1c6c-416b-ad77-ef7e5e34015a)
