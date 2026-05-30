# 🏋️ GymGenius — AI-Powered Personal Fitness Planner

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Open Source](https://img.shields.io/badge/Open%20Source-Yes-green.svg)](https://github.com)

**GymGenius** is a free, open-source fitness planning website that generates fully personalized workout plans and diet plans using AI — built around the exact equipment available in your gym and your personal health goals.

> Built using: HTML · CSS · Vanilla JavaScript · Claude AI (Anthropic API)

---

## ✨ Features

- **BMI Calculator** — real-time BMI display with health category and visual indicator
- **Goal-Based Planning** — Weight Loss, Muscle Building, Endurance, Body Toning
- **Equipment-Aware Workouts** — plans use ONLY your gym's available machines
- **AI-Generated Plans** — full 7-day workout plan with sets, reps, rest times
- **Veg & Non-Veg Diet Plans** — 7-day meal plans with calorie targets and macros
- **Pre/Post Workout Nutrition** — timing guidance based on your goals
- **Print-Ready Output** — one-click print for both workout and diet plans
- **100% Open Source** — fork, customize, and deploy for free

---

## 🏗️ Equipment Available (Pre-Configured)

| Equipment | Brand | Type |
|-----------|-------|------|
| Treadmill | Life Fitness | Cardio |
| Spinning Bike | Life Fitness × ICG | Cardio |
| Recumbent Bike | Life Cycle | Cardio / Low Impact |
| Rowing Machine | HiRower | Full Body Cardio |
| Dumbbells 2.5–30kg | Ramp Up | Strength |
| Adjustable Bench | Life Fitness | Strength |
| Functional Trainer / Cable Machine | Life Fitness | Strength |
| Chest / Incline / Shoulder Press | Life Fitness | Upper Body |
| Lat Pulldown & Seated Row | Life Fitness | Back |
| Seated Leg Curl & Leg Extension | Life Fitness | Legs |
| Stability Ball | Swiss Ball | Core |
| Step Platform | Xpeed | HIIT / Cardio |
| Resistance Bands | Orange Bands | Strength / Mobility |
| Yoga / Exercise Mat | — | Core / Flexibility |
| Foam Rollers | — | Recovery |

---

## 🚀 Quick Start

### Option 1 — Run Locally (Zero Dependencies)

```bash
git clone https://github.com/YOUR_USERNAME/gymgenius.git
cd gymgenius
# Just open index.html in your browser!
open index.html
```

> **Note:** The AI plan generation requires an active internet connection to call the Anthropic API.

### Option 2 — Deploy on GitHub Pages (Free Hosting)

See the full [Step-by-Step GitHub Setup Guide](GITHUB_SETUP_GUIDE.md) below.

---

## ⚙️ Configuration

The website calls the Anthropic API automatically. The API key is handled by the Anthropic platform when running on claude.ai or as a configured deployment.

To use your own Anthropic API key in a self-hosted deployment, add it to your server environment:

```bash
# Never expose API keys in frontend code!
# Use a simple backend proxy instead (see docs/backend-proxy.md)
ANTHROPIC_API_KEY=your_key_here
```

---

## 🗂️ Project Structure

```
gymgenius/
├── index.html          # Main website (single file — all HTML/CSS/JS)
├── README.md           # This file
├── GITHUB_SETUP_GUIDE.md  # Step-by-step deployment guide
├── LICENSE             # MIT License
└── docs/
    └── backend-proxy.md   # Optional: how to add your own API key
```

---

## 📱 How to Customize

### Add or Remove Equipment
In `index.html`, find the `equipment` array in the `generatePlan()` function and edit accordingly:

```javascript
const equipment = [
  "Your Treadmill Model",
  "Your Dumbbell Range",
  // ... add or remove equipment here
];
```

### Change the Recipe Book
Update the `recipesInfo` variable in the `generatePlan()` function with your recipe book details.

### Change the Gym Name / Branding
Search and replace `GymGenius` with your gym's name throughout `index.html`.

---

## 📄 License

MIT License — free to use, modify, and distribute. See [LICENSE](LICENSE) for details.

---

## 🙏 Credits

- Workout planning powered by [Claude AI (Anthropic)](https://www.anthropic.com)
- Recipe book: "30 Healthy Bowl Recipes" by Hina
- Equipment: Life Fitness, Ramp Up, HiRower, Xpeed
- UI fonts: Barlow Condensed + DM Sans (Google Fonts)

---

## ⚠️ Disclaimer

GymGenius provides general fitness guidance only. Always consult a qualified healthcare professional or certified personal trainer before starting a new exercise program. This tool is not a substitute for professional medical advice.
