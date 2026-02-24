# Prompt: Vibe-Coded Tetris Game

Build a complete, polished Tetris game as a single HTML file with embedded CSS and JavaScript. The file should contain both a landing page and the game itself.

## Landing Page

The page starts with a landing/hero section before the game:

- **Title**: "VIBE CODED TETRIS" in a large, bold, distinctive font (use Google Fonts — pick something geometric or retro-futuristic, NOT Inter/Roboto/Arial)
- **Subtitle**: "This entire game was coded by AI in a single prompt. No human wrote a single line of code."
- **A "Play" button** that smooth-scrolls down to the game section
- **A "Made with Claude" badge** in the bottom-right corner of the landing section, styled tastefully (use the Anthropic logo from https://cdn.worldvectorlogo.com/logos/anthropic-2.svg or just a text badge)
- The landing page should feel premium and modern — think dark background with a subtle animated gradient or particle effect, crisp typography, generous whitespace

## Game Requirements

### Core Tetris Mechanics
- Standard 10×20 grid
- All 7 standard tetrominoes (I, O, T, S, Z, J, L) with correct rotation (use SRS — Super Rotation System)
- Wall kicks for rotation near edges
- Piece preview (show next piece)
- Hold piece functionality (press C or Shift to hold)
- Ghost piece (translucent preview showing where the piece will land)
- Hard drop (spacebar) and soft drop (down arrow)
- Line clearing with a brief flash/animation
- Scoring: single=100, double=300, triple=500, tetris=800, multiplied by level
- Levels increase every 10 lines cleared, increasing drop speed
- Game over detection when pieces stack to the top

### Controls
- Left/Right arrows: move piece
- Up arrow: rotate clockwise
- Z: rotate counter-clockwise
- Down arrow: soft drop
- Spacebar: hard drop
- C or Shift: hold piece
- P or Escape: pause
- Display controls on-screen next to the game board

### Visual Design
- Dark theme with neon/glowing accents
- Each tetromino type has a distinct, vibrant color
- Smooth animations: piece movement, line clear effects, game over animation
- The game board should have a subtle grid visible
- Score, level, lines cleared displayed prominently
- Responsive: playable on both desktop and mobile (add touch controls for mobile — swipe left/right/down, tap to rotate)

### Audio (optional but impressive)
- Use the Web Audio API to generate simple synth sounds (no external files):
  - Piece drop sound
  - Line clear sound
  - Game over sound
- Include a mute/unmute button

### Polish
- Pause screen overlay
- Game over screen with final score and "Play Again" button
- Smooth CSS transitions and animations throughout
- The whole page should feel like a cohesive product, not a coding demo

## Technical Requirements
- Everything in a single `.html` file — no external dependencies except Google Fonts
- Clean, well-structured code with comments for major sections
- Use `requestAnimationFrame` for the game loop
- No canvas required — use CSS Grid or HTML table for the board (either approach is fine, pick what looks best)

## Iteration Instructions

After generating the first version:

1. **Play-test it yourself** by reviewing the code logic. Check:
   - Do all 7 pieces spawn and rotate correctly?
   - Does wall kick work (try rotating an I-piece against the right wall)?
   - Does line clearing work when 1, 2, 3, or 4 lines are completed simultaneously?
   - Does the ghost piece accurately show the landing position?
   - Does the hold mechanic work and prevent hold-spamming (only one hold per drop)?
   - Does the game speed increase with levels?
   - Does game over trigger correctly?

2. **Fix any bugs** you find before presenting the final version.

3. **Review the visual design** — make sure colors are consistent, fonts load correctly, animations are smooth, and the layout looks good at different viewport sizes.

4. **Test edge cases**:
   - Rotating a piece at the very top of the board
   - Filling the board almost completely
   - Rapid key inputs
   - Pausing mid-hard-drop
