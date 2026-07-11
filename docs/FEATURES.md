# SmartCent Features

> This document defines every planned feature for SmartCent, its purpose, priority, and implementation scope.

---

# Feature Classification

Features are grouped into four categories:

- 🔴 Core MVP (Required for Version 1)
- 🟡 Enhanced MVP (If time permits)
- 🔵 Future Release
- ⚪ Long-Term Vision

---

# 1. User Accounts

## Priority

🔴 Core MVP

## Purpose

Allow users to create and securely access their personal SmartCent account.

## User Benefits

- Personalized experience
- Secure progress storage
- Learning continuity across devices
- Individual achievements

## Success Criteria

Users can:

- Register
- Log in
- Log out
- Reset password
- Stay signed in securely

## Dependencies

- Authentication system
- User database

---

# 2. User Profile

## Priority

🔴 Core MVP

## Purpose

Store user information and learning statistics.

## Includes

- Username
- Avatar
- XP
- Current Level
- Learning Streak
- Achievements
- Financial Goals

## Success Criteria

Users can easily view their learning progress.

---

# 3. Dashboard

## Priority

🔴 Core MVP

## Purpose

Provide an overview of the user's learning journey.

## Displays

- XP
- Wallet Balance
- Active Challenges
- Current Lesson
- Budget Progress
- Daily Goal
- Learning Streak

---

# 4. Virtual Wallet

## Priority

🔴 Core MVP

## Purpose

Allow users to practice managing virtual money.

## Features

- Starting balance
- Earn virtual income
- Spend money
- Save money
- View transaction history

## Learning Outcome

Understanding how money flows.

---

# 5. Budget Planner

## Priority

🔴 Core MVP

## Purpose

Teach budgeting skills.

## Features

- Monthly income
- Monthly expenses
- Savings goal
- Budget categories
- Budget summary

## Learning Outcome

Responsible financial planning.

---

# 6. Lessons

## Priority

🔴 Core MVP

## Purpose

Teach financial concepts.

## Topics

- Saving
- Budgeting
- Banking
- Needs vs Wants
- Interest
- Goal Setting

Lessons should be:

- Interactive
- Short
- Easy to understand

---

# 7. Quiz Engine

## Priority

🔴 Core MVP

## Purpose

Reinforce learning.

## Features

- Multiple choice
- Instant feedback
- Score tracking
- XP rewards
- Difficulty levels

---

# 8. XP System

## Priority

🔴 Core MVP

## Purpose

Reward learning progress.

Users earn XP by:

- Completing lessons
- Passing quizzes
- Maintaining streaks
- Completing challenges

---

# 9. Achievement Badges

## Priority

🔴 Core MVP

Examples:

- First Lesson
- Quiz Master
- Budget Expert
- Saving Champion
- Seven-Day Streak

Purpose:

Increase motivation.

---

# 10. Progress Tracking

## Priority

🔴 Core MVP

Track:

- Lessons completed
- Quiz scores
- XP history
- Level progression
- Budget performance
- Learning streak

---

# 11. Daily Challenges

## Priority

🟡 Enhanced MVP

Examples

- Save 20 SmartCoins
- Finish one lesson
- Score 80% on a quiz

Purpose

Encourage daily engagement.

---

# 12. Financial Scenarios

## Priority

🟡 Enhanced MVP

Example

"You receive N$200 for your birthday."

How will you spend it?

Purpose

Teach decision making.

---

# 13. Notifications

## Priority

🟡 Enhanced MVP

Examples

- Daily reminder
- Challenge reminder
- New lesson available

---

# 14. Leaderboards

## Priority

🔵 Future Release

Allow users to compare progress with friends.

---

# 15. Parent Dashboard

## Priority

🔵 Future Release

Allow parents to monitor learning progress.

---

# 16. Teacher Dashboard

## Priority

🔵 Future Release

Allow teachers to assign lessons and monitor classroom progress.

---

# 17. AI Learning Assistant

## Priority

⚪ Long-Term Vision

Provide:

- Personalized explanations
- Learning recommendations
- Financial guidance
- Quiz assistance

---

# 18. Investing Simulator

## Priority

⚪ Long-Term Vision

Teach investing through simulated markets.

---

# 19. Entrepreneurship Module

## Priority

⚪ Long-Term Vision

Introduce:

- Business basics
- Profit
- Expenses
- Pricing
- Marketing

---

# 20. Multi-language Support

## Priority

⚪ Long-Term Vision

Support multiple languages to improve accessibility.

---

# Feature Dependencies

| Feature | Depends On |
|----------|------------|
| Dashboard | User Accounts |
| Wallet | User Accounts |
| Budget Planner | Wallet |
| Lessons | User Accounts |
| Quizzes | Lessons |
| XP | Lessons & Quizzes |
| Achievements | XP |
| Progress Tracking | All Core Features |

---

# MVP Summary

Version 1 includes:

- User Accounts
- User Profile
- Dashboard
- Virtual Wallet
- Budget Planner
- Lessons
- Quiz Engine
- XP System
- Achievement Badges
- Progress Tracking

Everything else is intentionally postponed to keep the MVP focused and achievable.

---

# Feature Evaluation Checklist

Before adding any new feature, ask:

- Does it support financial education?
- Does it improve practical learning?
- Is it appropriate for teenagers?
- Does it align with the SmartCent vision?
- Can it be maintained long-term?
- Does it belong in the current release?

If the answer is "no" to most of these questions, the feature should be reconsidered or postponed.