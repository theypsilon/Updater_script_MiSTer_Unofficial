# Updater script for MiSTer Unofficial
The script updates all [MiSTer](https://github.com/MiSTer-devel/Main_MiSTer/wiki) cores, including menu.rbf and the main MiSTer Linux executable; it updates scaler filters, GameBoy palettes and scripts; it can (experimental and risky) optionally update the whole Linux system.<br>
Simply put [update_unofficials.sh](https://github.com/theypsilon/Updater_script_MiSTer_Unofficial/blob/master/update_unofficials.sh?raw=true) in your SD and launch it through MiSTer main menu OSD (press F12 and then Scripts).<br>
Please right click (save link as...) on the links in this README (inside the README, not in the GitHub repository) or on the RAW button in GitHub script pages in order to actually download the raw Bash scripts, otherwise you could download an HTML page which isn’t a script and won’t be executed by MiSTer (you will see no output, but just an OK button in MiSTer Script menu interface); please don't copy and paste any script code or you may end with a non working script if you use Windows (different end of line character).<br>
[update_unofficials.sh](https://github.com/theypsilon/Updater_script_MiSTer_Unofficial/blob/master/update_unofficials.sh?raw=true) will always download and execute the latest [mister_updater.sh](https://github.com/theypsilon/Updater_script_MiSTer_Unofficial/blob/master/mister_updater.sh?raw=true) (where the real update code is) from GitHub, so you will never have to deal with "updater updates". You can make an update_unofficials.ini (same name as the script and placed in the same directory) file with custom user options: see [mister_updater.sh USER OPTIONS section](https://github.com/theypsilon/Updater_script_MiSTer_Unofficial/blob/5c7968cca525adc53b8690c8f762ab49cd2e852e/mister_updater.sh#L89-L205) (please click the link) for all user options and their detailed explanations. If you feel uncomfortable, for security reasons, with a script which downloads and executes another script from the Internet, you can directly download and use [mister_updater.sh](https://github.com/theypsilon/Updater_script_MiSTer_Unofficial/blob/master/mister_updater.sh?raw=true) and it will work the same, all ini file considerations will still be valid, but you will have to update the script manually.<br>
You can have many differently named copies of [update_unofficials.sh](https://github.com/theypsilon/Updater_script_MiSTer_Unofficial/blob/master/update_unofficials.sh?raw=true) (or [mister_updater.sh](https://github.com/theypsilon/Updater_script_MiSTer_Unofficial/blob/master/mister_updater.sh?raw=true) if you prefer) and its ini file, for different updating behaviours i.e.:<br>
- you can make an *update_arcade.sh* with its *[update_arcade.ini](https://github.com/theypsilon/Updater_script_MiSTer_Unofficial/blob/master/examples/update_arcade.ini?raw=true)* using these settings (simply copy this code in an empty text file named *update_arcade.ini* and put it in the same directory as *update_arcade.sh*):
```
REPOSITORIES_FILTER="arcade-cores"
ADDITIONAL_REPOSITORIES=( )
UPDATE_CHEATS="false"
UPDATE_LINUX="false"
```
- you can make an *update_commodore.sh* with its *[update_commodore.ini](https://github.com/theypsilon/Updater_script_MiSTer_Unofficial/blob/master/examples/update_commodore.ini?raw=true)* using these settings:
```
REPOSITORIES_FILTER="PET2001 VIC20 C64 C16 Minimig"
ADDITIONAL_REPOSITORIES=( )
UPDATE_CHEATS="false"
UPDATE_LINUX="false"
```
- you can make an *update_additional_repositories.sh* with its *[update_additional_repositories.ini](https://github.com/theypsilon/Updater_script_MiSTer_Unofficial/blob/master/examples/update_additional_repositories.ini?raw=true)* using these settings:
```
REPOSITORIES_FILTER="ZZZZZZZZZ"
UPDATE_CHEATS="false"
UPDATE_LINUX="false"
```
- you can make an *update_fonts.sh* with its *[update_fonts.ini](https://github.com/theypsilon/Updater_script_MiSTer_Unofficial/blob/master/examples/update_fonts.ini?raw=true)* using these settings:
```
REPOSITORIES_FILTER="ZZZZZZZZZ"
ADDITIONAL_REPOSITORIES=( "https://github.com/MiSTer-devel/Fonts_MiSTer|pf|$BASE_PATH/font" )
UPDATE_CHEATS="false"
UPDATE_LINUX="false"
```
- you can make an *update_linux.sh* with its *[update_linux.ini](https://github.com/theypsilon/Updater_script_MiSTer_Unofficial/blob/master/examples/update_linux.ini?raw=true)* using these settings:
```
REPOSITORIES_FILTER="ZZZZZZZZZ"
UPDATE_CHEATS="false"
UPDATE_LINUX="true"
```
- you can make an update_all.sh with its [update_all.ini](https://github.com/theypsilon/Updater_script_MiSTer_Unofficial/blob/master/examples/update_all.ini?raw=true) using these settings:
```
UPDATE_CHEATS="true"
UPDATE_LINUX="true"
ADDITIONAL_REPOSITORIES+=( "https://github.com/MiSTer-devel/Fonts_MiSTer|pf|$BASE_PATH/font" )

```
I take no responsibility for any data loss or anything, if your DE10-Nano catches fire it’s up to you: **use the script at your own risk**.
