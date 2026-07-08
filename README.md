# SmartCent

**An interactive financial education platform where teenagers (13-16) safely learn how to manage money through realistic simulations, games, and challenges before they handle real money.**

---

## 📋 Project Overview

SmartCent is a gamified financial literacy app designed specifically for young teenagers in Namibia and beyond. It transforms financial education from passive reading into active learning through immersive simulations, engaging stories, and real-world challenges.

Instead of memorizing textbook definitions, users learn by doing—managing a virtual salary, making financial decisions, investing in simulated markets, and facing consequences in a safe environment.

### Why SmartCent?

- **13-year-olds** are transitioning to high school, receiving independent allowances, and facing peer pressure to spend
- **16-year-olds** are getting their first jobs, opening bank accounts, and need practical financial skills immediately
- **The Gap**: Current financial apps either feel too childish for 16-year-olds or too abstract for 13-year-olds
- **The Solution**: SmartCent segments content by age, evolving with the user from budgeting basics to investment management

---

## 🎯 Mission

Empower teenagers with practical financial literacy through engaging, gamified learning and safe real-world simulation—before they face real money.

---

## ✨ Core Features (Planned)

### Phase 1: Learn & Practice
- **Smart Budgeting Module** — Learn the 50/30/20 rule through interactive simulations
- **Investing Simulator** — Watch money grow through compound interest over virtual decades
- **Tax Decoder** — Understand net vs. gross pay through interactive pay slip analysis
- **Scam Detection Game** — Spot red flags in messages, emails, and fraudulent schemes
- **Quiz & Flashcard System** — Bite-sized learning with spaced repetition
- **Daily Challenges** — 5-minute missions to maintain engagement streaks

### Phase 2: Connected Simulation
- **Virtual Life** — Manage a monthly salary with bills, unexpected expenses, and life events
- **Character Stories** — Follow characters making different financial decisions
- **Levels & Progression** — Unlock features, avatar customization, and rewards
- **Progress Tracking** — Detailed analytics and learning insights

### Phase 3: Ecosystem
- **Parent Dashboard** — Monitor progress, set chores, link real allowances
- **Teacher Mode** — Create classes, assign modules, view class leaderboards
- **Multi-Country Support** — Localize for Namibia, South Africa, and beyond
- **AI Financial Coach** — Get instant answers about financial scenarios

---

## 👥 Target Audience

- **Primary**: Teenagers aged 13-16 in Namibia and Southern Africa
- **Secondary**: Schools (as supplementary life skills curriculum)
- **Tertiary**: Parents seeking to teach their teens about money

---

## 🛠 Technology Stack (Planned)

| Layer | Technology |
|-------|-----------|
| **Frontend** | Flutter (iOS + Android) |
| **Backend** | Node.js + Express/NestJS |
| **Database** | PostgreSQL |
| **Authentication** | Firebase Authentication / JWT |
| **Storage** | Firebase Storage / Cloud Storage |
| **Notifications** | Firebase Cloud Messaging |
| **Analytics** | Firebase Analytics |
| **Hosting** | Cloud Run / AWS / DigitalOcean |

---

## 📁 Repository Structure

```
SmartCent/
│
├── README.md                    # This file
├── LICENSE
├── .gitignore
│
├── docs/                        # Project documentation
│   ├── PROJECT_VISION.md        # Mission, goals, and context
│   ├── FEATURES.md              # Complete feature list
│   ├── ROADMAP.md               # Development timeline
│   ├── USER_STORIES.md          # User personas and stories
│   ├── SRS.md                   # Software Requirements Specification
│   ├── DATABASE_DESIGN.md       # Data models and schema
│   ├── API_DESIGN.md            # Backend API endpoints
│   └── UI_GUIDELINES.md         # Design standards and patterns
│
├── frontend/                    # Flutter mobile app
│   ├── lib/
│   │   ├── main.dart
│   │   ├── screens/
│   │   ├── widgets/
│   │   ├── models/
│   │   └── services/
│   ├── pubspec.yaml
│   └── README.md
│
├── backend/                     # Node.js API server
│   ├── src/
│   │   ├── index.ts
│   │   ├── routes/
│   │   ├── controllers/
│   │   ├── services/
│   │   ├── models/
│   │   └── middleware/
│   ├── package.json
│   ├── .env.example
│   └── README.md
│
├── database/                    # Database schemas and migrations
│   ├── migrations/
│   ├── seeds/
│   └── schema.sql
│
├── assets/                      # Design files, images, UI kits
│   ├── ui/
│   ├── characters/
│   ├── icons/
│   └── illustrations/
│
└── prototypes/                  # Figma designs and mockups
    └── README.md
```

---

## 🚀 Project Status

**Current Phase**: Planning & Design

- [x] Project concept and vision
- [x] Feature planning
- [ ] Software Requirements Specification (SRS)
- [ ] Database design
- [ ] UI/UX wireframes and prototypes
- [ ] Frontend setup (Flutter)
- [ ] Backend setup (Node.js)
- [ ] Core authentication
- [ ] Virtual wallet system
- [ ] Budgeting module
- [ ] Quiz system
- [ ] Investing simulator
- [ ] And more...

---

## 📈 Development Roadmap

### Q1: Foundation
- User authentication and onboarding
- Age-based content segmentation
- Virtual wallet and dashboard
- Basic quiz system

### Q2: Core Learning
- Smart Budgeting module
- Investing Simulator
- Tax Decoder
- Daily Challenges system

### Q3: Advanced Features
- Connected virtual life simulation
- Character stories and decision-making
- Reward and progression system
- Scam Detection game

### Q4: Ecosystem
- Parent dashboard
- Teacher/School mode
- Analytics and reporting
- Performance optimization

### 2026+: Growth
- Multi-country localization
- AI Financial Coach
- Community features
- Real-world partnerships

---

## 🎓 Learning Modules (Overview)

Each module is designed for self-contained learning but contributes to a larger connected simulation:

1. **Smart Budgeting (50/30/20 Rule)** — Categorize income into needs, wants, and savings
2. **Long-Term Investing** — Visualize compound interest and diversification over decades
3. **Demystifying Taxation** — Understand net pay, tax deductions, and civic spending
4. **Spotting Scams** — Identify red flags in common fraud schemes
5. **Banking Basics** — Accounts, deposits, withdrawals, and transfers
6. **Credit Scores** — How credit works and why it matters
7. **Entrepreneurship** — Starting small businesses and managing income
8. **Salary Negotiation** — Earning more through negotiation skills
9. **And many more...**

---

## 🌍 Namibian Localization

SmartCent is built from the ground up for Namibian teenagers and will include:

- **Currency**: Namibian Dollar (N$) as the default
- **Examples**: Transport costs, data bundles, school expenses, taxi fares
- **Banking**: Reference to local banks and financial institutions
- **Jobs**: Typical teenage jobs in Namibia
- **Education**: Context relevant to Namibian schools

Future versions will support other countries with localized examples and currencies.

---

## 🤝 Contributing

This project is under active development. If you're interested in contributing:

1. Check the [ROADMAP.md](docs/ROADMAP.md) for current priorities
2. Review the [FEATURES.md](docs/FEATURES.md) for planned functionality
3. Open an issue or pull request with your ideas
4. Follow the code style guide in [UI_GUIDELINES.md](docs/UI_GUIDELINES.md)

---

## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

## 📞 Contact & Support

- **Project Lead**: [Your Name/GitHub]
- **Questions**: Open an issue on GitHub
- **Feedback**: We'd love to hear from you!

---

## 🎯 Next Steps

1. Review the [PROJECT_VISION.md](docs/PROJECT_VISION.md) for detailed goals
2. Explore [ROADMAP.md](docs/ROADMAP.md) for development timeline
3. Check [SRS.md](docs/SRS.md) for technical specifications
4. View UI designs in [Figma](#) (to be added)

---

**Let's build something that helps millions of teenagers make smarter financial decisions! 🚀**
