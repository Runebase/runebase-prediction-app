# Install and Usage
Download the last binary at our releases page: https://github.com/runebase/runebase-prediction-app/releases

## Mac

1. Run `Runebase-Prediction-x.x.x.dmg`
2. Drag the Runebase-Prediction icon to the `Applications` folder
3. You may get a warning dialog that says "Runebase-Prediction can't be opened because it is from an unidentified developer." If you do, find the `Runebase-Prediction` app in the Finder and right-click it and `Open`. This will open another dialog, which you will press `Open` again.
4. Enjoy!

## Windows

1. Please disable your antivirus or whitelist the Runebase-Prediction app before running it. Some antiviruses will come back as a false positive so if you don't disable it and it could automatically quarantine the app. This will make the app disappear.
2. The Runes app might also pop up as an antivirus false positive. Please disable or whitelist your antivirus program.
3. Run `Runebase-Prediction-Setup-x.x.x.exe`
4. Enjoy!

## Linux

1. Run `Runebase-Prediction-x.x.x-i386.AppImage` or `Runebase-Prediction-x.x.x-x86_64.AppImage`
2. Enjoy!

# Winning Rates Formulae
Here are the formula calculations for determining how much PRED and RUNES you will win on an Event.

RUNES Return Rate:
```
// 1% percent of losing RUNES gets split by PRED winners
losersRunesReward = totalLosingRunesBets * 1 / 100

// total losing RUNES less the 1% reward that goes to PRED winners
losersAdjustedRunes = totalLosingRunesBets - losersRunesReward

// RUNES won from RUNES bets only
runesWon = (yourRunesWinningBets / totalRunesWinningBets * losersAdjustedRunes) + yourRunesWinningBets
```

PRED Return Rate:
```
// PRED won from your PRED winning votes
predWon = (yourPredWinningBets / totalPredWinningBets * losersTotal) + yourPredWinningBets

// RUNES reward won from PRED winning votes
predRunesWon = yourPredWinningBets / totalPredWinningBets * losersRunesReward
```

Total Return:
```
runes = runesWon + predRunesWon
pred = predWon
```
