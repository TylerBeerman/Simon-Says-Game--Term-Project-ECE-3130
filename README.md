# ECE 3130 Term Project: Simon Says Game

## Project Overview

This project is an electronic version of the classic **Simon Says memory game**, developed using an STM32 microcontroller and the onboard LEDs of the EDUboardV2.

The goal of the game is to memorize and repeat an increasingly long sequence of LED signals. Each round, the game adds a new LED to the sequence. The player must repeat the sequence in the correct order. The game continues until the player makes a mistake.

This project is being developed as a group project for **ECE 3130: Microcomputer Systems** at **Tennessee Technological University**.

**NOTE:** *All members that worked on this are credited near the bottom of the README*

## Hardware Requirements

- STM32 NUCLEO-L476RG microcontroller
- EDUbaseV2 with four onboard LEDs
- Four buttons for player input
- LCD display (for game instructions and score)
- Buzzer (for audio feedback)

## How the Game Works

1. **Start Game:** The player starts a new game.
2. **Generate Sequence:** The microcontroller randomly selects one of the four LEDs.
3. **Display Sequence:** The LEDs flash in a specific order for the player to memorize.
4. **Player Input:** The player presses the corresponding buttons to repeat the sequence.
5. **Check Input:** The microcontroller checks each button press against the stored sequence.
6. **Next Round:** If the player enters the sequence correctly, another LED is added to the sequence.
7. **Game Over:** If the player presses the wrong button, the game ends and the final score is displayed.

## Game Features

- Four onboard LEDs used to display the sequence.
- Button inputs for player interaction.
- Randomly generated LED sequences.
- Increasing difficulty as the sequence gets longer.
- Score tracking based on completed rounds.
- LCD display for game status and score.
- Optional buzzer feedback for correct and incorrect inputs.

## Functions

Some of the main functions used in the game include:

| Function | Description |
|---|---|
| `Initialize_Game()` | Resets game variables and prepares a new game. |
| `Generate_Sequence()` | Adds a randomly selected LED to the sequence. |
| `Display_Sequence()` | Flashes the stored LED sequence. |
| `Turn_On_LED()` | Turns on a selected onboard LED. |
| `Turn_Off_All_LEDs()` | Turns off all four LEDs. |
| `Read_Buttons()` | Detects which button the player presses. |
| `Check_Input()` | Compares player input with the stored sequence. |
| `Game_Over_Display()` | Displays the game-over message and final score. |
| `Reset_Game()` | Resets the game so another round can begin. |

## Variables

Some of the main variables used in the game include:

| Variable | Description |
|---|---|
| `Sequence[20]` | Stores the generated LED sequence. |
| `Round` | Tracks the current round. |
| `Score` | Tracks the player's score. |
| `PlayerPosition` | Tracks the player's current position in the sequence. |
| `PlayerInput` | Stores the button pressed by the player. |
| `GameOver` | Indicates whether the game has ended. |
| `RandomLED` | Stores the randomly selected LED number. |


## Development Tools

- STM32CubeIDE
- C programming language
- STM32 HAL libraries

## Team Members

- Noah Boggess
- Richy Huichapa - Applied Physics Major Junior
- Tyler Beerman - Electrical Engineering Major Junior

## Project Goal

The goal of this project is to create a working memory game while applying concepts from microcontroller programming, GPIO configuration, input handling, timing, and embedded C development.
