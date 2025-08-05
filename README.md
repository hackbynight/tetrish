# Tetrish

A pure Bash implementation of the classic Tetris game with advanced terminal graphics and multi-process architecture.

## Features

- **Pure Bash** - No external dependencies required
- **Multi-process architecture** - Smooth gameplay with concurrent input handling
- **Full Tetris mechanics** - All 7 tetromino pieces with proper rotation
- **Terminal graphics** - ANSI escape sequences for colorful display
- **Adjustable difficulty** - Speed increases with level progression
- **Score tracking** - Points awarded based on lines cleared
- **Customizable display** - Toggle colors, next piece preview, and help

## Requirements

- Bash 4.2+ 
- Terminal with ANSI color support
- Unix-like operating system (Linux, macOS, WSL)

## Installation

```bash
git clone https://github.com/hackbynight/tetrish.git
cd tetrish
chmod +x tetris.sh
```

## Usage

```bash
./tetris.sh
```

## Controls

- **Arrow Keys** or **WASD** - Move pieces
  - ↑ or S - Rotate
  - ← or A - Move left
  - → or D - Move right
  - ↓ - Soft drop
- **Space** - Hard drop
- **Q** - Quit game
- **C** - Toggle colors
- **N** - Toggle next piece preview
- **H** - Toggle help display

## Game Mechanics

- Standard Tetris rules apply
- Score increases with squared number of lines cleared simultaneously
- Game speed increases every 20 points
- All 7 standard tetromino pieces (I, O, T, S, Z, J, L)

## Technical Details

The game uses a sophisticated multi-process architecture:
- **Controller** - Main game loop and rendering
- **Ticker** - Generates timed drop commands
- **Reader** - Processes keyboard input

Inter-process communication via pipes and UNIX signals (SIGUSR1/SIGUSR2).

## License

Original implementation by Kirill Timofeev <kt97679@gmail.com> 2013

## Future Enhancements

This project is being actively developed to add exciting new features while maintaining the pure Bash implementation.