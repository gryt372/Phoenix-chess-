# Phoenix Chess

A real-time multiplayer chess game built with Elixir Phoenix and featuring an AI opponent using minimax algorithm.

## Features

- ♟️ **Full Chess Rules** - Complete implementation of standard chess rules
- 👥 **Multiplayer** - Real-time multiplayer using WebSockets
- 🤖 **AI Player** - Intelligent chess AI with configurable difficulty levels
- ♻️ **Move Validation** - Robust move validation including special moves
- 📊 **Game History** - Track all moves and game states

## Setup

### Prerequisites
- Elixir 1.12+
- Phoenix 1.6+
- PostgreSQL (optional, for persistence)

### Installation

```bash
git clone https://github.com/gryt372/phoenix-chess.git
cd phoenix-chess
mix deps.get
```

### Running the Game

```bash
mix phx.server
```

The game will be available at `http://localhost:4000`

## Project Structure

- `lib/phoenix_chess/` - Core game logic
  - `board.ex` - Chess board and piece management
  - `game.ex` - Game state management
  - `move_validator.ex` - Move validation rules
  - `ai/` - AI engine implementation

- `lib/phoenix_chess_web/` - Web interface
  - `channels/` - WebSocket channels for real-time play
  - `controllers/` - HTTP controllers
  - `templates/` - HTML templates

## Game Rules

The implementation follows standard FIDE chess rules:

- **Piece Movement** - All pieces move according to standard rules
- **Special Moves** - Castling, en passant, and pawn promotion
- **Game States** - Check, checkmate, stalemate detection
- **Turn-based** - Strict alternation between white and black

## AI Implementation

The AI uses minimax algorithm with alpha-beta pruning for efficient move selection:

1. **Evaluation Function** - Scores board positions based on:
   - Material count (pieces on board)
   - Position advantage (piece placement)
   - Control of center

2. **Difficulty Levels**:
   - Easy: Depth 2 search
   - Medium: Depth 3 search
   - Hard: Depth 4+ search

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Roadmap

- [ ] WebSocket channels for real-time multiplayer
- [ ] User authentication and profiles
- [ ] Game persistence to database
- [ ] ELO rating system
- [ ] Game replays and analysis
- [ ] Chat during games
- [ ] Move timer/clock

## License

MIT License - See LICENSE file for details

## Authors

- gryt372

---

**Happy Chess Playing! ♟️**