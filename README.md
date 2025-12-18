# ⚔️ The Forgotten Realm - AI-Powered D&D Text RPG

An immersive, AI-powered text-based RPG that uses Claude AI to generate dynamic storylines, personalized character introductions, and responsive gameplay. Create your character, roll dice, and embark on unique adventures that adapt to your choices.

![Game Screenshot](https://img.shields.io/badge/Status-Active-success) ![License](https://img.shields.io/badge/License-MIT-blue) ![AI Powered](https://img.shields.io/badge/AI-Claude%204-purple)

## 🎮 Features

### Core Gameplay
- **AI-Generated Narratives**: Every action generates unique, contextual story responses using Claude AI
- **Personalized Introductions**: Each adventure starts with a custom scenario tailored to your character
- **D&D 5e Mechanics**: Authentic ability checks, saving throws, and combat rolls
- **Visual Dice Roller**: Animated dice with automatic success/failure calculations
- **Character Persistence**: Save your progress and continue your adventure anytime

### Character System
- **Upload D&D Character Sheets**: Import existing characters from text or JSON files
- **Quick Character Creator**: Build characters with class and race selection
- **Automatic Stat Calculation**: Racial bonuses and class traits applied automatically
- **Character Sheet Display**: Collapsible character info with all your stats

### Game Features
- **Intelligent Text Parsing**: AI understands your character sheet format
- **Dice Rolling System**: 
  - d20 ability checks with modifiers
  - Attack rolls with proficiency
  - Custom damage rolls
  - Critical hits and failures
- **Inventory Management**: Track equipment, gold, and items
- **Experience & Leveling**: Gain XP and level up your character
- **Auto-Save System**: Never lose your progress
- **Responsive Design**: Play on desktop, tablet, or mobile

## 🚀 Getting Started

### Play Online
1. Visit the live game: `https://yourusername.github.io/dnd-text-rpg/text_rpg.html`
2. Get your Anthropic API key at [console.anthropic.com](https://console.anthropic.com/)
3. Enter your API key in the game (stored locally in your browser)
4. Create or upload your character
5. Start your adventure!

### Local Development
```bash
# Clone the repository
git clone https://github.com/yourusername/dnd-text-rpg.git

# Navigate to the directory
cd dnd-text-rpg

# Open with a local server (required for API calls)
python -m http.server 8000

# Or use VS Code Live Server extension
# Then visit: http://localhost:8000/text_rpg.html
```

## 🔑 API Key Setup

This game requires an Anthropic API key to function:

1. **Get an API Key**:
   - Visit [console.anthropic.com](https://console.anthropic.com/)
   - Sign up for an account (free trial available)
   - Navigate to API Keys section
   - Create a new API key

2. **Add to Game**:
   - Paste your key into the API key field at the top
   - Click "Save Key"
   - Your key is stored locally and never shared

3. **Security**:
   - Keys are stored in browser localStorage only
   - Never committed to GitHub or shared
   - Only sent to Anthropic's API for game functionality

## 📝 Character Sheet Format

### Upload JSON Format
```json
{
  "name": "Thorin Ironforge",
  "class": "Fighter",
  "race": "Dwarf",
  "level": 3,
  "background": "Soldier",
  "abilities": {
    "strength": 16,
    "dexterity": 12,
    "constitution": 15,
    "intelligence": 10,
    "wisdom": 13,
    "charisma": 8
  },
  "hitPoints": {"current": 28, "max": 28},
  "armorClass": 16,
  "speed": 25,
  "skills": ["Athletics", "Intimidation"],
  "equipment": ["Longsword", "Shield", "Chain Mail"]
}
```

### Upload Text Format
The game supports standard D&D character sheet text format:
```
Name
Borin Khardrum

Race
Hill Dwarf

Class
Ranger (Level 1)

Strength    14    +2
Dexterity   13    +1
Constitution 16   +3

HP: 13
AC: 15
Speed: 25 ft

Skills
Perception (Ranger)
Athletics (Soldier)

Equipment
Battleaxe
Longbow
Scale Mail
```

## 🎲 Dice Rolling

The game includes a comprehensive D&D dice system:

### Automatic Rolls
- AI requests rolls when needed (climbing, persuasion, combat, etc.)
- Visual dice animation with results
- Automatic success/failure vs Difficulty Class
- Critical success (natural 20) and critical failure (natural 1)

### Manual Rolling
Click the "🎲 Roll Dice" button to:
- Make ability checks
- Roll attack rolls
- Roll damage dice
- Create custom rolls (2d6+3, 1d20, etc.)

## 🛠️ Technologies Used

- **Frontend**: Pure HTML5, CSS3, JavaScript (ES6+)
- **AI**: Anthropic Claude API (Claude Sonnet 4)
- **Storage**: Browser localStorage for persistence
- **No Dependencies**: Self-contained single HTML file

## 📂 Project Structure

```
dnd-text-rpg/
├── text_rpg.html          # Main game file (self-contained)
├── README.md              # This file
└── examples/
    ├── character_sheet_sample.json
    └── character_sheet_sample.txt
```

## 🎨 Game Mechanics

### Stats & Leveling
- Health, Gold, Experience, Level tracking
- Level up at 100 XP per level
- Health restoration on level up

### D&D 5e Rules
- Ability scores (STR, DEX, CON, INT, WIS, CHA)
- Proficiency bonus based on level
- Advantage/disadvantage on appropriate checks
- Racial bonuses automatically applied

### Combat
- Attack rolls with ability modifiers
- Damage rolls with weapon dice
- Health tracking
- Enemy encounters generated by AI

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the MIT License - see below for details:

```
MIT License

Copyright (c) 2024 [Your Name]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 🐛 Known Issues

- Character sheet emoji parsing may vary by text editor
- API rate limits apply based on your Anthropic plan
- Large character sheets may need manual verification

## 🔮 Future Features

- [ ] Multiple save slots
- [ ] Party system for multiplayer
- [ ] Quest log and achievement tracking
- [ ] Custom campaign creation
- [ ] Image generation for scenes
- [ ] Voice narration option
- [ ] Mobile app version

## 📞 Support

If you encounter issues:
1. Check that your API key is valid and has credits
2. Ensure you're using a modern browser (Chrome, Firefox, Safari, Edge)
3. Open browser console (F12) to check for errors
4. Create an issue on GitHub with details

## 🙏 Acknowledgments

- **Anthropic** for the Claude AI API
- **D&D 5e** for game mechanics inspiration
- The amazing TTRPG community

## 🌟 Star History

If you find this project useful, please consider giving it a star on GitHub!

---

**Made with ⚔️ and 🤖 by [Your Name]**

[Play Now](https://yourusername.github.io/dnd-text-rpg/text_rpg.html) | [Report Bug](https://github.com/yourusername/dnd-text-rpg/issues) | [Request Feature](https://github.com/yourusername/dnd-text-rpg/issues)
