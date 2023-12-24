# Cricket Scorer 

## Overview

The Cricket Scorer smart contract is designed to manage a simple cricket scoring system on the blockchain. It allows players to join the game, record their runs, check their performance, and leave the game. The contract includes functions to ensure fair play, such as only allowing players to join once and requiring them to be part of the game to record runs.

## Smart Contract Details

### State Variables

- `playerScores`: A private mapping that stores the runs scored by each player.
- `isPlayerPlaying`: A private mapping that indicates whether a player is currently part of the game.

### Events

- `PlayerJoined`: Triggered when a player joins the game.
- `RunsRecorded`: Triggered when a player records their runs.
- `PlayerLeft`: Triggered when a player leaves the game.

### Modifiers

- `onlyPlaying`: Ensures that a function can only be called by a player who is part of the game.
- `notPlaying`: Ensures that a function can only be called by a player who is not part of the game.

### Functions

1. **joinGame**
   - Allows a player to join the cricket game. It triggers the `PlayerJoined` event.

2. **recordRuns**
   - Allows a player to record the number of runs they scored in a match. The runs must be between 1 and 1000. It triggers the `RunsRecorded` event.

3. **Performance_check**
   - Checks the performance of a player based on their total runs. If a player has scored 300 or more runs, it indicates "Outstanding Performance." Otherwise, it triggers a revert statement indicating that improvement is needed.

4. **leaveGame**
   - Allows a player to leave the cricket game. It triggers the `PlayerLeft` event.

## Usage

1. **Deploying the Contract:**
   - Deploy the smart contract on the Ethereum blockchain.

2. **Joining the Game:**
   - Call the `joinGame` function to join the cricket game.

3. **Recording Runs:**
   - Call the `recordRuns` function with the number of runs scored in a match.

4. **Checking Performance:**
   - Call the `Performance_check` function to check if your performance is outstanding.

5. **Leaving the Game:**
   - Call the `leaveGame` function to leave the cricket game.

## Modifiers and Security

- The `onlyPlaying` and `notPlaying` modifiers ensure that players can only perform certain actions if they are part of or not part of the game, respectively.

- The `Performance_check` function includes a revert statement to indicate that improvement is needed if a player's score is less than 300.

## Disclaimer

- This smart contract is provided as-is, and users are encouraged to review and test it thoroughly before deploying it on the Ethereum blockchain.

## License

- This smart contract is licensed under the MIT License. See the provided license file for details.
