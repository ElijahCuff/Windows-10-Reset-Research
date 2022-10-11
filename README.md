# Windows-10-Reset-Research
Window 10 research into factory data reset.    
     
---    

### Factory Reset Basic     
> Suites most basic factory reset conditions.    
- Open settings   
- Search Reset PC   
- Select Reset This PC   
- Select Remove My Files
- After reset, switch off the pc to leave in factory OOB ( out of box ) condition.    
    
  
### Factory Reset Advanced    
> Situations where the computer contains new drivers and software.     
- Prepare the computer for factory reset ( delete any unnecessary files )   
- Press `Win` + `R` or open RUN dialogue by searching for "RUN"    
- Start System Preparation Software with command `%WIMDIR%\System32\Sysprep\sysprep.exe`     
- Select Mode "PC Audit Mode" and press OK - wait for restart automatically.      
( This loads you into the System Administrator Account for System Auditing )    
    
> Once inside the System Administrator account     
- Open Settings > Accounts > Other Users
- Delete the old user accounts 
( Make sure drivers are installed system-wide - not to the specific user account )
   
> Here's where you can make changes to the system as desired before rebooting into the OOBE state ( Out Of Box Experience)   
- Now your system is prepared, it's time to open back up sysprep and reboot into OOBE     
   
> All accounts should now be cleared ( factory condition ) and all drivers with software will be retained unser the "All Users" installation directory.    
    
    
### SOFT RESET    
> Useful for instances where you do not have the users password to login.      
- At the Windows Login Screen, Open the Power Menu     
- Hold down `SHIFT` on the keyboard and while holding press the restart option.     
( This will say "Please Wait" - you can let go of `SHIFT` now while the recovery options are loaded )    
- Select Reset This PC     
- Select "Remove Apps, Settings and Personal Files"   
- Select "Just Delete" instead of "Wipe Drive"    
- After files are deleted, System will reboot and reinstall windows    
    
> This puts the system into a special state, whereas personal files are retrievable from the HDD using "Undelete" and "File Recovery" software, while also having a new account.
      
   
### THIRD-PARTY BOOT    
> Useful for when you need to grab a user's files without the password.      
- Open BIOS Settings
- Allow Boot From USB    
- Restart into Boot Selection Menu    
- Select to Boot from your Live Installation of Linux on a USB Drive     
- Once inside a Live OS, you'll have access to the HDD without restrictions from the windows OS     
( Windows doesn't encrypt users files, they only encrypt a database of user accounts - as we aren't logging into the account, we don't need the password. )     
   
- Copy the users files from `C:\Users\Example\` to a new portable HDD    
- Restart PC into Windows    
- PC will still be at login screen but you have the users files backed up.    
   
### BOOT FROM RECOVERY DRIVE    
> Useful to retain system software and drivers    
- Open Windows Start Menu   
- Type Recovery Drive    
- Select Recovery Media Creator    
- Select "Backup System Files to the drive"     
- Insert Empty or Usable USB Stick around 16GB    
- Build the system Recovery Media      
- Reboot into the USB Drive    
- Select Reinstall Windows from the Recovery Drive      
> Does a good job at locating system driver's and reinstalling them during the recovery process.     

   




