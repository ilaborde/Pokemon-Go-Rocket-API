# Pokemon-Go-Rocket-API

#Window
![alt tag](https://github.com/DetectiveSquirrel/Pokemon-Go-Rocket-API/blob/master/MainWindow.png)
![alt tag](https://github.com/DetectiveSquirrel/Pokemon-Go-Rocket-API/blob/master/MainPokeUi.png)
![alt tag](https://github.com/DetectiveSquirrel/Pokemon-Go-Rocket-API/blob/master/MainSettings2.png)

#Console
![alt tag](https://github.com/DetectiveSquirrel/Pokemon-Go-Rocket-API/blob/master/screenshot.png)


A Pokémon Go bot in C#

## Features
* PTC / Google Login
* Get Map Objects and Inventory
* Search for Gyms / Pokéstops / Spawns
* Farm Pokéstops
* Farm all Pokémon in the neighbourhood
* Evolve Pokémon
* Transfer Pokémon
* Auto-Recycle uneeded items
* View all Pokémon CP/IV %
* Transfer/Powerup/Evolve Pokémon
* Output level and needed XP for levelup
* Output Username, Level, Stardust, XP/hour, Pokémon/hour in Console Title
* German/English Pokémon names
* Automatic use of Razzberries
* Automatic Update checker
* Logs everything into Logs.txt

## Getting Started
* 1- Use Visual Studio (Download from https://www.visualstudio.com).
* 2- Open Pokemon Go Rocket API.sln
* 3- Go to PokemonGo\RocketAPI\Window\App.config -> Edit the Settings you like (you can skip this)
* 4- Build and Run (CTRL+F5)
* 5- Click start bot menu option

# Settings
## AuthType
* *Google* - Google login via oauth2
* *Ptc* - Pokémon Trainer Club login with username/password combination

## PtcUsername
* *username* for PTC account. No need for when using Google.
* *password* for PTC account. No need for when using Google.

## GoogleRefreshToken
* *GoogleRefreshToken* - You get this code when you connect the application with your Google account. You do not need to enter it.

## DefaultLatitude
* *12.345678* - Latitude of your location you want to use the bot in. Number between -90 and +90. Doesn't matter how many numbers stand after the comma.

## DefaultLongitude
* *123.456789* - Longitude of your location you want to use the bot in. Number between -180 and +180. Doesn't matter how many numbers stand after the comma.

## LevelOutput
* *time* - Every X amount of time it prints the current level and experience needed for the next level.
* *levelup* - Only outputs the level and needed experience for next level on levelup.

## LevelTimeInterval
* *seconds* - After X seconds it will print the current level and experience needed for levelup when using *time* mode.

## Recycler
* *false* - Recycler not active.
* *true* - Recycler active.

## RecycleItemsInterval
* *seconds* - After X seconds it recycles items from the filter in *Settings.cs*.

## Language
* *english* - Outputs caught Pokémon in english name.
* *german*  - Outputs caught Pokémon in german name.

## RazzBerryMode
* *cp* - Use RazzBerry when Pokémon is over specific CP.
* *probability* - Use RazzBerry when Pokémon catch chance is under a specific percentage.

## RazzBerrySetting
* *value* - CP: Use RazzBerry when Pokémon is over this value | Probability Mode: Use Razzberry when % of catching is under this value

## TransferType
* *none* - disables transferring
* *cp* - transfers all Pokémon below the CP threshold in the app.config, EXCEPT for those types specified in program.cs in TransferAllWeakPokemon
* *leaveStrongest* - transfers all but the highest CP Pokémon of each type SPECIFIED IN program.cs in TransferAllButStrongestUnwantedPokemon (those that aren't specified are untouched)
* *duplicate* - same as above but for all Pokémon (no need to specify type), (will not transfer favorited Pokémon)
* *all* - transfers all Pokémon

## TransferCPThreshold
* *CP* - transfers all Pokémon with less CP than this value.

## EvolveAllGivenPokemons
* *false* - Evolves no Pokémon.
* *true* - Evolves all Pokémon.
