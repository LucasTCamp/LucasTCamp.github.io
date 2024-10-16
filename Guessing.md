```mermaid
flowchart TD
 A[Start Game] --> B[Generate Random Number]
    B --> C[/Prompt User for a Guess/]
    C --> D{Is Input Numeric?}
    D -->|No| E[Display Error and Prompt Again]
    D -->|Yes| F{Is Input Within Range?}
    F -->|No| E[Display Error and Prompt Again]
    F -->|Yes| G{Is Guess Correct?}
    G -->|Yes| H[Display 'Congratulations' and End Game]
    G -->|No| I{Is Guess Too High?}
    I -->|Yes| J[Display 'Too High' and Prompt Again]
    I -->|No| K[Display 'Too Low' and Prompt Again]
    J --> C
    K --> C
```

## Documentation
The game starts and the code generates a random number. The user is then prompted to guess a number. It checks the validity of the user input. Then, it checks if the guess is correct. If it is correct, the game ends and displays a congratulations page. If it is incorrect the code will say "too high" or "too low" and ask user for another guess. This process repeats until the user inputs the correct number.