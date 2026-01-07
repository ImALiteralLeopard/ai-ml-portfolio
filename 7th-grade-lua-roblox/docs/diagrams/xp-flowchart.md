flowchart TD
    A[Player Performs Action] --> B{Action Type?}
    B --> C[Training]
    B --> D[Enemy Kill]
    B --> E[Quest Completion]
    B --> F[Match Win]
    B --> G[Time Played]
    
    C --> H[Calculate XP for Training]
    D --> I[Calculate XP for Kill]
    E --> J[Calculate XP for Quest]
    F --> K[Calculate XP for Win]
    G --> L[Calculate XP for Time Played]
    
    H --> M[Add XP to Player Total]
    I --> M
    J --> M
    K --> M
    L --> M
    
    M --> N{XP >= XP Required?}
    N -- Yes --> O[Level Up Player]
    N -- No --> P[Continue Gameplay]
    
    O --> Q{Rank Milestone?}
    Q -- Yes --> R[Update Rank & Give Rewards]
    Q -- No --> P
    
    R --> P

    Q -- No --> P
    
    R --> P
