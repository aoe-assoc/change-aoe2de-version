# Revert your AoE2DE to an older version of the game 

1. Make sure you have the .NET SDK installed [Download here](https://download.visualstudio.microsoft.com/download/pr/73718445-e2bd-40b7-b698-e8a9ac65f4e5/0816570f697c4e8f1b53ecfb33eaed7f/dotnet-sdk-3.1.300-win-x64.exe) or chose [here](https://dotnet.microsoft.com/download)

2. Download the [DepotDownloader](https://github.com/SteamRE/DepotDownloader/releases) 
  - you find instructions how to use it in general [here](https://github.com/SteamRE/DepotDownloader/blob/master/README.md)

3. Extract the DepotDownloader archive to a new folder.

4. Go to this [website](https://steamdb.info/depot/813781/manifests/) and search for the game version (aka `manifest`) you would like to revert to and copy the `MANIFESTID` on the last column.

5. Open a Command Prompt in the extracted folder of the DepotDownloader and run the following command (replace the values in the `angle brackets`)

`dotnet DepotDownloader.dll -app 813780 -depot 813781 -manifest <your-manifest-id> -username <your-username> -password <your-password> -remember-password`

6. Backup (Zip or copy to another folder) the path `C:\Program Files (x86)\Steam\steamapps\common\AoE2DE\` or your corresponding installation folder.

7. The files that were downloaded by the tool are in the "depots" subfolder. Copy/paste them to `C:\Program Files (x86)\Steam\steamapps\common\AoE2DE\` (or wherever your game is installed) and replace all the files when asked.

8. On the first run after replacing the files, the game will most probably crash. From the second run onward it should work fine.


# Troubleshooting

If it doesn't seem to work try the following approach as well, this changes internals to let Steam think your game is in a proper state, so it doesn't update automatically.

https://web.archive.org/web/20200717121613/https://steamcommunity.com/discussions/forum/1/371919771764103041/#c154644928858622139

