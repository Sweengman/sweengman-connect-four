
## Analyze the app's functionality

format: as a user, I want a feature, because of reason

MVP (Minimal Viable Product)

as a user, 
- I want to be able to have 2 players, because that is how connect four is played.
- I want to be able to take turns
- I want to be able to drop colored discs into 1 of 7 columns
- I want to be able to win if I get 4 in a row
- I want to know who won or if it was a tie
- I want to be able to play the game again if it's over

If I have some time I would like to add these
- success animation
- dropping animation
- difficulty setting
- choose the color of disc
- track total wins and losses
- powerups 

## overall design of the app

- interesting(good balance between clean and clever)
- color green and gold
- font: Nunito Sans
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Nunito+Sans:opsz@6..12&display=swap" rel="stylesheet">
```
```css
font-family: 'Nunito Sans', sans-serif;
```

# Wireframe the UI

A wireframe is a way to represent your game (app)

- High fidelity
    - Working demo
    - images
    - clickable buttons
    - hover effects happen
    - bit more than just a drawing
- Low fidelity
    -s imply drawn
    - page layout (simple shapes to represent key items)
    - where are my messages to the user going?
    - where are all my buttons going?
     -does this feel too cluttered?
    - does this feel too empty?

    ## Psuedocode

    - Define required constants
        - color constant (green and gold)

    - Define required variables used to track the state of the game
        - game board
            - one big array
            - holds seven smaller arrays (columns)
        - turn: 1 || -1
        - winner: null || 1 || -1 || 'T'

    - Cache DOM elementsw
        - Message Place
        - Play again button
        - column buttons/markers

    - Upon loading the app should:
        - Init the state vars
            - create the 7 nested arrays
            - turn var should be set to 1 (player 1)
            - winner var should be null
        - render changes to the DOM
            - Render the board, should be completely blank
            - Render the message "green's Turn"
            -Do not render the "play again" button
        - Wait for interaction (user input)

    - Hanle a player clicking a column button
        - update board array with the player move
        - update the turn var 
        - check for a winner
        - re-render the board with the player's move

    - Handle a player clicking the replay button
        - Reset the state vars
        - re-render the board

    - Check for a winner
        - check for 4 in a row
        - we will use offsets to count the colors of the discs in the arrays
    ## Identify the application's state
    (application-wide date)

    - game board - array of 7 nested arrays
    ```js
    let board
    ```
    - turn vars
    ```js
    let turn
    ```
    - winner var
    ```js
    let winner
    ```
	/*----- constants -----*/


	/*----- state variables -----*/


	/*----- cached elements  -----*/


	/*----- event listeners -----*/


	/*----- functions -----*/
