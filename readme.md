# Use case
This project aims towards sysadmins whom are in need of an easy
way to get a dataset in JSON, listing the recent most user for 
a CrOS device in a G suite domain.

The script is simple and works by injecting commands to GAM.
(See https://github.com/jay0lee/GAM for this software).

This data can be used to import the JSON data in to an SIS system or 
any other database that keeps these kinds of records.

# Get started
1. Download and configure GAM. See link above.
2. Download Get-RecentUser script from this repository
3. Open PowerShell, and execute the script. Mandatory switches will demand information from you.

The script will generate a JSON file with the following structure:

    {

        "Export": 
       
              [
                  {
                      "SERIALNUMBER": "MANAGED_EMAIL_ADDRESS"
                  }
              ]
    }
            
This structure makes it easy for you to parse the objects in the JSON array, and import to your system of choice.
Also, feel free to edit the logic in function Get-RecentUser if you need your file to be structured differently.


# Need help?
Run `Get-Help | .\Get-RecentUser.ps1`

For examples, run `Get-Help | .\Get-RecentUser.ps1 -examples`

For full help page, run `Get-Help | .\Get-RecentUser.ps1 -full`

Any further questions can be emailed to me directly at dotchetter@protonmail.ch 
