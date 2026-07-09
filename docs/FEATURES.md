# SmartCent: Complete Features List

**Version**: 1.0  
**Last Updated**: July 2026  
**Status**: Feature Planning

---

## 📋 Overview

This document details every feature SmartCent will have, organized by:
- **Phase** (1: Learn & Practice, 2: Connected Simulation, 3: Ecosystem)
- **User Type** (Teenager, Parent, Educator)
- **Priority** (MVP, High, Medium, Low)
- **Complexity** (Simple, Medium, Complex)

---

## 🎮 PHASE 1: Learn & Practice (MVP - Q1 2026)

The foundation. Users learn financial concepts through interactive modules and gamified challenges.

### 1.1 User Authentication & Onboarding

#### Feature: User Sign-Up
- **Description**: Secure registration with email or phone number
- **User Type**: Teenager, Parent, Educator
- **Priority**: MVP
- **Complexity**: Medium
- **Requirements**:
  - Email or phone registration
  - Password strength validation (NIST guidelines)
  - Email/SMS verification
  - Age verification (confirm 13-16)
  - Parental consent for users under 16 (in some regions)
  - GDPR/POPIA compliant privacy acceptance

#### Feature: Social Sign-Up
- **Description**: Quick sign-up via Google or Apple ID
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - OAuth 2.0 integration
  - Auto-fill age from birthday
  - Link to existing account if available

#### Feature: Age-Based Onboarding
- **Description**: Different onboarding flows based on age
- **User Type**: Teenager
- **Priority**: MVP
- **Complexity**: Medium
- **Requirements**:
  - Quiz to determine if user is 13-14 vs 15-16
  - 13-14 path emphasizes budgeting and saving
  - 15-16 path emphasizes earning and investing
  - Content difficulty adjusts based on selection
  - User can update age preference later

#### Feature: Onboarding Questionnaire
- **Description**: Understand user's financial background and goals
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Simple
- **Requirements**:
  - "Do you receive an allowance?" (Yes/No)
  - "Do you have a part-time job?" (Yes/No)
  - "What's your biggest financial goal?" (Multiple choice)
  - "How much money do you typically spend per month?" (Estimate)
  - "Do you have a savings account?" (Yes/No)
  - Results inform initial module recommendations

#### Feature: Character Introduction
- **Description**: Meet the app's characters and their stories
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - Introduce 5 main characters with distinct personalities
  - Short video or animation for each character
  - Show character's financial journey teaser
  - Let user choose a "guide character" for personalized tips
  - Characters appear throughout app providing context

---

### 1.2 Dashboard & Navigation

#### Feature: Main Dashboard
- **Description**: Home screen showing user's progress and quick access to features
- **User Type**: Teenager
- **Priority**: MVP
- **Complexity**: Medium
- **Requirements**:
  - Display current level and progress to next level
  - Show active streak counter (days learning consecutively)
  - Quick links to today's challenge, active module, and rewards
  - Progress bar for current financial goal
  - Summary of recent achievements
  - Weekly learning summary (modules completed, quizzes passed)
  - Personalized recommendations based on progress

#### Feature: Bottom Navigation
- **Description**: Easy access to main sections
- **User Type**: Teenager
- **Priority**: MVP
- **Complexity**: Simple
- **Requirements**:
  - Home (Dashboard)
  - Learn (Modules & Lessons)
  - Practice (Simulations & Challenges)
  - Wallet (Financial Dashboard)
  - Profile (Settings & Progress)

#### Feature: Main Menu
- **Description**: Quick access to all major features
- **User Type**: Teenager
- **Priority**: MVP
- **Complexity**: Simple
- **Requirements**:
  - Modules
  - Challenges
  - Leaderboard
  - Achievements
  - Settings
  - Help & FAQ
  - Feedback

---

### 1.3 Virtual Wallet System

#### Feature: Virtual Wallet
- **Description**: User's virtual money account in the app
- **User Type**: Teenager
- **Priority**: MVP
- **Complexity**: Medium
- **Requirements**:
  - Display current balance in N$ (Namibian Dollar)
  - Real-time updates when money is earned or spent
  - Transaction history (last 30 transactions visible)
  - Clear, easy-to-read UI with large numbers
  - Monthly reset option (simulated new allowance)
  - Visual celebrations when balance increases

#### Feature: Initial Virtual Salary
- **Description**: Users start with virtual money to practice with
- **User Type**: Teenager
- **Priority**: MVP
- **Complexity**: Simple
- **Requirements**:
  - 13-14 year olds start with N$1,000
  - 15-16 year olds start with N$2,500
  - Can represent allowance or part-time job income
  - Monthly reset (simulates receiving new allowance)
  - User can customize monthly amount in settings

#### Feature: Transaction History
- **Description**: Detailed record of all money movements
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Simple
- **Requirements**:
  - Date, amount, category, description for each transaction
  - Filter by category or date range
  - Search transactions by keyword
  - Export as CSV (future feature)
  - Color-coded by type (earned, spent, invested, etc.)

#### Feature: Spending Categories
- **Description**: Organize spending into meaningful buckets
- **User Type**: Teenager
- **Priority**: MVP
- **Complexity**: Simple
- **Requirements**:
  - Needs (food, transport, school supplies)
  - Wants (games, social outings, entertainment)
  - Savings (goals, emergency fund)
  - Investments (stocks, ETFs)
  - Debt payments (if applicable)
  - Auto-categorization with user override

---

### 1.4 Learning Modules System

#### Feature: Module Library
- **Description**: Browse and access all learning modules
- **User Type**: Teenager
- **Priority**: MVP
- **Complexity**: Medium
- **Requirements**:
  - Display all available modules with progress
  - Each module shows: title, description, duration, difficulty, characters involved
  - Filter by topic, difficulty, or age recommendation
  - Search for specific modules
  - Lock/unlock system based on prerequisites
  - Recommended modules based on user profile

#### Feature: Module Structure
- **Description**: Standard structure for every learning module
- **User Type**: Teenager
- **Priority**: MVP
- **Complexity**: Medium
- **Requirements**:
  - Every module includes:
    1. **Introduction video** (30-60 seconds, engaging)
    2. **Story scenario** (relatable context, character involvement)
    3. **Interactive simulation** (hands-on learning)
    4. **Key terms** (glossary of concepts taught)
    5. **Quiz** (verify understanding)
    6. **Reward** (badge, points, unlock)
  - Estimated time per module: 10-15 minutes
  - Can be completed in one session or split across multiple sessions

#### Feature: Module Completion Tracking
- **Description**: Track progress through each module
- **User Type**: Teenager
- **Priority**: MVP
- **Complexity**: Simple
- **Requirements**:
  - Save user's position in module (if incomplete)
  - Record completion date
  - Store quiz score
  - Track time spent in module
  - Show completion percentage

---

### 1.5 Learning Modules (Content)

#### Module 1: Smart Budgeting (50/30/20 Rule)

**Module Level**: Beginner (13-14) & Intermediate (15-16)  
**Duration**: 12 minutes  
**Learning Objective**: Users understand how to categorize income and maintain a sustainable budget

**Content Breakdown**:

1. **Introduction Video** (1 min)
   - Character: Sarah, the spender
   - Scene: Sarah's avatar runs out of money mid-month
   - Question: "Why does this always happen to me?"
   - Hook: "By the end of this module, you'll never run out of money again"

2. **Story Scenario** (1 min)
   - Teen receives monthly allowance/salary: N$2,000
   - Goals: Buy new phone (N$3,000), pay for transport (N$300), save money
   - Problem: Can't do it all at once
   - Solution: Learn to categorize money

3. **Interactive Simulation: The Bucket Challenge** (6 min)
   - Drag-and-drop game with three digital buckets
   - N$2,000 "falls" from top of screen
   - User must tilt sliders to route money into buckets before timer (60 seconds):
     - 50% Needs bucket (transport, food, school)
     - 30% Wants bucket (games, outings, entertainment)
     - 20% Savings bucket (goals, emergency fund)
   - Timer creates engagement/gamification
   - Feedback: "Great job! You have N$1,000 for needs, N$600 for wants, N$400 to save"
   - Repeat 3 times with increasing difficulty
   - Show consequences: "If you keep spending 60% on wants, you'll never reach your N$3,000 goal"

4. **Key Terms Taught**:
   - Fixed Costs: Expenses that don't change (transport, school meals)
   - Disposable Income: Money left after essentials
   - The 50/30/20 Rule: Budget framework
   - Paying Yourself First: Saving before spending
   - Goals: Long-term financial targets

5. **Quiz** (2 min, 5 questions)
   - Q1: "If you earn N$1,000, how much should go to needs?" A: N$500 (50%)
   - Q2: "Sarah wants a N$2,000 laptop. She earns N$500/month and saves 20%. How long until she can afford it?" A: 20 months
   - Q3: "Which is a 'want'?" A: Gaming subscription
   - Q4: Scenario: "You have N$100 this month after paying for needs. What should you do?" A: Split between wants and savings
   - Q5: "What does 'paying yourself first' mean?" A: Save money before spending on wants

6. **Reward**:
   - Badge: "Budget Builder" (unlocked after passing quiz with 80%+)
   - 50 points added to user's total
   - Unlock next module: "Saving Goals"
   - Achievement notification: "You've mastered the 50/30/20 rule!"

**For 15-16 Year Olds** (Advanced Version):
- Scenario uses N$2,500 (part-time job income)
- Includes taxes: "After taxes, you actually take home N$2,100"
- Additional categories: Debt payments (if applicable)
- Real-world scenarios: "Your rent is N$1,200, food N$400, transport N$200..."
- More complex decision-making

---

#### Module 2: Saving Goals

**Module Level**: Beginner  
**Duration**: 13 minutes  
**Learning Objective**: Users understand how to set, track, and achieve financial goals

**Content Breakdown**:

1. **Introduction Video** (1 min)
   - Character: Daniel, the saver
   - Scene: Daniel counts money toward his goal
   - Question: "How do I actually save for something I want?"
   - Hook: "Goals + strategy = success"

2. **Story Scenario** (1 min)
   - Teen wants a new phone (N$3,000), gaming headset (N$1,500), or trip with friends (N$2,000)
   - Has N$200/month to allocate to savings
   - Problem: Which goal to prioritize? How to track progress?

3. **Interactive Simulation: Goal Setter** (6 min)
   - User inputs a goal, amount needed, and timeline
   - App calculates monthly savings needed
   - Visual progress bar shows journey to goal
   - Monthly breakdown: "Save N$X per month for Y months"
   - Fast-forward feature: Slide to see progress over time
   - Add multiple goals and compare
   - See consequences: "If you increase spending on wants, this goal takes X months longer"

4. **Key Terms Taught**:
   - Goal: Financial target
   - Short-term vs Long-term Goals
   - Savings Rate: Percentage of income saved
   - Goal Deadline: Target completion date
   - Trade-offs: Choosing between competing goals

5. **Quiz** (2 min, 5 questions)
   - Q1: "You want N$1,000 in 6 months. How much per month?" A: N$167
   - Q2: "Which is a long-term goal?" A: Saving for car
   - Q3: "True or False: You can have multiple goals at once?" A: True
   - Q4: Scenario: "Your goal timeline just got cut in half. What should you do?" A: Increase monthly savings
   - Q5: "What's a realistic first financial goal?" A: Multiple correct answers

6. **Reward**:
   - Badge: "Goal Setter"
   - 50 points
   - Unlock: "Long-Term Investing"

---

#### Module 3: Long-Term Investing

**Module Level**: Intermediate (15-16 recommended, available to advanced 14-year-olds)  
**Duration**: 15 minutes  
**Learning Objective**: Understand compound interest and how investments grow over time

**Content Breakdown**:

1. **Introduction Video** (1 min)
   - Character: Grace, the entrepreneur/investor
   - Scene: Grace's N$1,000 becomes N$50,000 over time
   - Question: "How did you turn a little money into so much?"
   - Hook: "The magic of compound interest"

2. **Story Scenario** (1 min)
   - Teen receives N$1,000 as a gift
   - Choice 1: Keep it in a piggy bank (under mattress)
   - Choice 2: Invest in an index fund
   - Problem: What happens to money over time?
   - Solution: Time Machine Simulator

3. **Interactive Simulation: Time Machine** (7 min)
   - Visual dashboard with two paths:
     - **Piggy Bank**: Shows decreasing buying power (due to inflation)
     - **Index Fund**: Shows compounding growth
   - Slider lets user fast-forward 10, 20, 30 virtual years
   - Real-time graph updates as slider moves
   - **Key visuals**:
     - Starting amount: N$1,000
     - After 10 years: Piggy Bank N$700 (effective), Index Fund N$3,000+
     - After 20 years: Piggy Bank N$400 (effective), Index Fund N$12,000+
     - After 30 years: Piggy Bank N$0 (effective), Index Fund N$40,000+
   - Tooltip explains: "Inflation reduces buying power. Your piggy bank doesn't grow."
   - Tooltip explains: "Compound interest: Your investment earns money, that money earns more money, etc."
   - Assume 10% average annual return (conservative for diversified index fund)
   - Assume 3% annual inflation

4. **Key Terms Taught**:
   - Shares/Stocks: Ownership in companies
   - Index Fund: Investment in many companies
   - Diversification: Spreading risk across many investments
   - Inflation: Rising prices over time
   - Capital Growth: Money growing through investment
   - Compound Interest: Earning interest on interest
   - Bull/Bear Market: Rising/falling market conditions

5. **Quiz** (2 min, 5 questions)
   - Q1: "If you invest N$1,000 at 10% annual return, how much in 10 years?" A: ~N$2,594
   - Q2: "What does diversification mean?" A: Spreading money across different investments
   - Q3: "Why is inflation important?" A: It reduces the buying power of money
   - Q4: "When should you start investing?" A: As soon as possible
   - Q5: "True or False: Stock market is only for rich people?" A: False

6. **Reward**:
   - Badge: "Investment Rookie"
   - 75 points (higher points for intermediate module)
   - Unlock: "Demystifying Taxation"

---

#### Module 4: Demystifying Taxation

**Module Level**: Intermediate  
**Duration**: 14 minutes  
**Learning Objective**: Understand taxes, net vs gross pay, and why governments collect taxes

**Content Breakdown**:

1. **Introduction Video** (1 min)
   - Character: Aiden, confused about paycheck
   - Scene: Aiden's boss says "You earn N$150/hour" but paycheck is less
   - Question: "Wait, where did my money go?"
   - Hook: "Let's decode your paycheck"

2. **Story Scenario** (1 min)
   - Teen gets a contract for N$150/hour for weekend work
   - 20 hours of work = N$3,000 gross
   - But bank shows only N$2,340
   - Problem: Where did N$660 go?
   - Solution: Understand tax deductions

3. **Interactive Simulation: Pay Slip Decoder** (6 min)
   - Digital pay slip appears on screen
   - User sees breakdown:
     - **Gross Income**: N$3,000
     - **PAYE Tax (25%)**: -N$750
     - **Social Security (2.5%)**: -N$75
     - **Health Insurance (3%)**: -N$90
     - **Other deductions (1%)**: -N$30
     - **Net Income**: N$2,055
   - Tap on each deduction to see details:
     - **PAYE**: Government tax for public roads, schools, hospitals
     - **Social Security**: Retirement and unemployment insurance
     - **Health Insurance**: Healthcare contributions
   - Micro-animations show where money goes:
     - Roads being built
     - Hospitals being staffed
     - Schools being equipped
     - Elderly receiving pensions
   - Adjustable scenarios:
     - "What if you earned N$5,000?" (Shows PAYE is progressive)
     - "What if you had dependents?" (Shows tax credits/deductions)

4. **Key Terms Taught**:
   - Gross Income: Total before taxes
   - Net Income: Actual take-home pay
   - PAYE (Pay As You Earn): Income tax withheld at source
   - Tax Threshold: Amount before taxes apply
   - Tax Deduction: Reduction in taxable income
   - Tax Credit: Direct reduction in taxes owed
   - Statutory Deductions: Required contributions (social security, etc.)

5. **Quiz** (2 min, 5 questions)
   - Q1: "If gross is N$2,000 and PAYE is 20%, what's net?" A: N$1,600
   - Q2: "What is PAYE?" A: Income tax withheld by employer
   - Q3: "Where does your tax money go?" A: Public services (roads, schools, hospitals)
   - Q4: True/False: "Taxes are the same for everyone?" A: False (progressive system)
   - Q5: Scenario: "You get a raise from N$2,000 to N$2,500 gross. What else increased?" A: Your net income and taxes

6. **Reward**:
   - Badge: "Tax Expert"
   - 75 points
   - Unlock: "Spotting Scams"

---

#### Module 5: Spotting Scams

**Module Level**: Beginner-Intermediate  
**Duration**: 16 minutes  
**Learning Objective**: Identify financial fraud and protect personal data

**Content Breakdown**:

1. **Introduction Video** (1 min)
   - Character: Aiden, almost falls for a scam
   - Scene: Aiden receives message "Turn N$200 into N$2,000 in 48 hours!"
   - Question: "Is this real?"
   - Hook: "Learn to spot financial red flags before they catch you"

2. **Story Scenario** (1 min)
   - Inside app, teen gets a DM from account with luxury car avatar
   - Message: "Hey! I can help you make easy money. Turn N$200 into N$2,000 in just 2 days. Recruit 3 friends and get a N$5,000 bonus!"
   - Problem: Is this legitimate or a scam?
   - Solution: Use the Red Flag Detector

3. **Interactive Simulation: Red Flag Detector** (8 min)
   - User sees series of 6 chat messages, emails, SMS texts
   - Each message contains 3-5 red flags
   - User clicks on red flags with a "magnifying glass" tool
   - When flag is clicked, tooltip explains:
     - **Urgent language** ("Act now!", "Limited time!", "Last chance!")
     - **Guaranteed returns** ("Risk-free returns!", "Double your money!")
     - **Request for sensitive info** (PIN, password, banking details)
     - **Anonymous links** ("Click here for more info")
     - **Too good to be true** (unusually high returns, easy money)
     - **Unknown sender** (no verified account, generic username)
     - **Pressure to recruit** (Ponzi/pyramid scheme signs)

   **Example Messages**:
   
   *Message 1 (SMS)*:
   ```
   "Congratulations! You've won N$50,000! Claim now: bit.ly/claimnow 
   Enter your PIN to verify. Hurry, expires in 2 hours!"
   ```
   Red flags: Urgent language, request for sensitive info, anonymous link, unverified source
   
   *Message 2 (Email)*:
   ```
   "From: Bank of Namibia <security@nam-bank-official.com>
   Your account has suspicious activity. Confirm your password: ___
   Click here to verify: bankofnamibia-verify.site"
   ```
   Red flags: Email address slightly off, request for password, fake link
   
   *Message 3 (App DM)*:
   ```
   "I turned my N$500 into N$50,000 in 3 weeks. No experience needed.
   Join my group for just N$100 membership fee. Guaranteed profits!"
   ```
   Red flags: Guaranteed returns, unusually high profits, membership fee, pressure to join
   
   *Message 4 (Phone Call Transcript)*:
   ```
   "We're from your bank. Your account is frozen due to fraud.
   Give us your account number and PIN to reactivate it. Immediately!"
   ```
   Red flags: Pressure, request for sensitive info, threat (frozen account)
   
   *Message 5 (Social Media DM)*:
   ```
   "I found a way to earn passive income. Invest N$1,000, get N$5,000 back.
   Invite 5 friends, each gets N$2,000 commission.
   Limited spots available!"
   ```
   Red flags: Guaranteed returns, pyramid scheme structure, scarcity language
   
   *Message 6 (Chat App)*:
   ```
   "Hey, it's your cousin. I'm stuck and need N$500 for emergency.
   Send via mobile money to: 081234567"
   ```
   Red flags: Unexpected urgent request, suspicious request method, verify sender first

   - User gets 1 point per flag correctly identified
   - At end: "You spotted X/18 flags. Great job protecting yourself!"

4. **Consequence Scenario** (2 min)
   - If user clicks "Accept Deal" or "Claim Prize" without spotting flags:
     - Virtual wallet drained of N$200-500
     - Message: "Oh no! You fell for a scam. This is why the red flags matter!"
     - Money restored immediately (consequence-free learning)
     - Analysis: "Here's what you missed..."

5. **Key Terms Taught**:
   - Phishing: Fake websites/emails stealing information
   - Ponzi/Pyramid Scheme: Unsustainable investment scam
   - Identity Theft: Criminal use of someone's personal data
   - Two-Factor Authentication (2FA): Extra security layer
   - Verification: Confirming sender identity before sharing info
   - Spoofing: Faking sender identity

6. **Quiz** (2 min, 5 questions)
   - Q1: "Which is NOT a red flag?" A: "I offer 15% annual return with market risk"
   - Q2: "What is phishing?" A: Fake emails/sites stealing information
   - Q3: "Your bank will never ask for..." A: Your password or PIN via email
   - Q4: "True/False: Guaranteed returns exist?" A: False
   - Q5: Scenario: "You get a job offer: N$100/hour, no experience needed, work from home. Red flag?" A: Yes

7. **Reward**:
   - Badge: "Scam Detective"
   - 100 points
   - Unlock: Advanced modules
   - Achievement: "Congratulations, you can spot most common scams!"

---

### 1.6 Quiz & Assessment System

#### Feature: Interactive Quizzes
- **Description**: Embedded quizzes at end of each module
- **User Type**: Teenager
- **Priority**: MVP
- **Complexity**: Medium
- **Requirements**:
  - 5-10 questions per module
  - Multiple question types: multiple choice, true/false, scenario-based
  - Immediate feedback (correct/incorrect with explanation)
  - Score calculation (percentage, points awarded)
  - Passing requirement: 70-80% to unlock reward
  - Randomized question order
  - Ability to retake quiz (score history saved)
  - Hint system (1-2 hints per quiz)

#### Feature: Glossary & Definitions
- **Description**: In-app dictionary of financial terms
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Simple
- **Requirements**:
  - Every module links to glossary
  - Search by term or browse by category
  - Definition, example, and related terms
  - Pronunciation guide for difficult terms
  - Audio pronunciation button
  - Add to "My Terms" for flashcard creation

#### Feature: Flashcard System
- **Description**: Spaced repetition learning
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - Auto-generated from module content
  - User can create custom cards
  - Spaced repetition algorithm (shows harder cards more often)
  - Flip animation for front/back
  - Mark as "easy", "medium", "hard"
  - Daily quiz from flashcards
  - Track mastery percentage

---

### 1.7 Daily Challenges

#### Feature: Challenge System
- **Description**: Daily 5-minute missions to maintain engagement
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - New challenge every day (24 hours)
  - Takes 5-10 minutes to complete
  - Three difficulty levels: Easy, Medium, Hard
  - User selects difficulty for bonus points
  - Challenges reset daily (opportunity to rebuild streak)

#### Feature: Challenge Types
- **Description**: Variety of daily challenges
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - **Budget Challenge**: Allocate N$X into categories
  - **Calculation Challenge**: Quick financial math (compound interest, tax calculation, etc.)
  - **Scam Spotting**: Identify red flags in a message
  - **Decision Scenario**: Choose best financial action
  - **Quiz Challenge**: Random questions from modules
  - **Goal Progress**: Check progress toward personal goals
  - **Terminology**: Match terms to definitions

#### Feature: Streak System
- **Description**: Reward consistency and daily engagement
- **User Type**: Teenager
- **Priority**: MVP
- **Complexity**: Simple
- **Requirements**:
  - Counter shows consecutive days of using app
  - Visual celebration at day 7, 14, 30, 60, 100, 365
  - Streak bonuses: 1.5x points after 7-day streak, 2x after 30-day
  - Lose streak if miss a day (after 24 hours of last activity)
  - "Streak Saver" power-up: Save streak once per month if missed day
  - Public display of current streak

#### Feature: Daily Reward
- **Description**: Bonus points for daily engagement
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Simple
- **Requirements**:
  - Base reward: 10 points per completed challenge
  - Streak bonus: +5 points per day of active streak
  - Difficulty bonus: Easy +10, Medium +20, Hard +50
  - First-time bonus: +50 for first challenge of the day
  - Encourage app opening by awarding points for visit

---

### 1.8 Rewards & Progression

#### Feature: Points System
- **Description**: Earn points for learning activities
- **User Type**: Teenager
- **Priority**: MVP
- **Complexity**: Medium
- **Requirements**:
  - Complete module: 50 points
  - Pass quiz (70%+): 50 points
  - Daily challenge completed: 10-50 points based on difficulty
  - Streak milestone (7, 14, 30, 60, 100 days): 100-500 points
  - Achievement unlocked: 50-200 points
  - Leaderboard reward: Top 3 get bonus points weekly
  - Visible point counter on dashboard
  - Points do NOT purchase real items (cosmetic only)

#### Feature: Badge/Achievement System
- **Description**: Unlock achievements for milestones
- **User Type**: Teenager
- **Priority**: MVP
- **Complexity**: Medium
- **Requirements**:
  - 50+ total badges to unlock
  - Categories: Learning (module completion), Engagement (streaks), Mastery (perfect scores), Milestones (account age)
  - Each badge has: name, description, icon, unlock condition, notification
  - Badge showcase in profile
  - Share achievements (screenshot or link)
  - Some rare badges (hidden until earned)

  **Example Badges**:
  - "Budget Builder" — Complete Smart Budgeting module
  - "Goal Setter" — Complete Saving Goals module
  - "Investment Rookie" — Complete Investing module
  - "Scam Detective" — Complete Spotting Scams module
  - "Week Warrior" — Maintain 7-day streak
  - "Month Master" — Maintain 30-day streak
  - "Perfect Score" — Pass quiz with 100%
  - "Speed Learner" — Complete module in <8 minutes
  - "Curious Mind" — Unlock 10+ badges
  - "Financial Whiz" — Complete all Phase 1 modules

#### Feature: Levels & Experience (XP)
- **Description**: Progression system showing overall advancement
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - 20 total levels (1-20)
  - XP earned from all activities (modules, quizzes, challenges, achievements)
  - XP requirements increase per level (exponential curve)
  - Level 1: 0 XP (starting point)
  - Level 5: ~1,000 XP
  - Level 10: ~10,000 XP
  - Level 20: ~100,000 XP
  - Visual level progression bar
  - Level-based unlocks (some features/modules require certain level)
  - Estimated time to reach milestones displayed

#### Feature: Avatar Customization
- **Description**: Personalize character appearance
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - Choose from 10 base avatars (diverse representation)
  - Cosmetic unlocks earned through badges/level:
    - Clothing options (10+)
    - Hairstyles (15+)
    - Accessories (20+)
    - Skin tones (8+)
    - Background themes (15+)
  - Avatar shown on profile and leaderboard
  - Share avatar with friends
  - No premium cosmetics (all earned through play)

---

### 1.9 Profile & User Settings

#### Feature: User Profile
- **Description**: Personal profile page
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Simple
- **Requirements**:
  - Display name (customizable)
  - Avatar
  - Level and XP progress
  - Total points earned
  - Badges earned (showcase top 8)
  - Current streak
  - Join date
  - Total modules completed
  - Personal bio/quote (optional)
  - Preferred guide character

#### Feature: Progress Analytics
- **Description**: Detailed breakdown of user's learning
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - Modules completed with dates and scores
  - Total learning time
  - Average quiz score
  - Most challenging modules
  - Learning streaks over time (calendar heatmap)
  - Weekly/monthly activity chart
  - Comparison to app average (anonymously)
  - Export learning report (PDF)

#### Feature: Settings & Preferences
- **Description**: Customize app experience
- **User Type**: Teenager, Parent, Educator
- **Priority**: MVP
- **Complexity**: Simple
- **Requirements**:
  - Notification settings (push, email, SMS)
  - Daily challenge time preference
  - Difficulty level (Easy, Medium, Hard, Auto)
  - Age group (13-14 vs 15-16)
  - Language (English, future: local languages)
  - Currency (N$ default, future: ZAR, BWP, etc.)
  - Parental controls (if applicable)
  - Data & privacy settings
  - Account security (2FA, password change)
  - Help & support

#### Feature: Privacy & Data Management
- **Description**: User control over personal data
- **User Type**: All
- **Priority**: MVP
- **Complexity**: Medium
- **Requirements**:
  - Clear privacy policy (POPIA compliant)
  - Data download (GDPR/POPIA right)
  - Data deletion request
  - Opt-out of analytics
  - Restrict data sharing
  - Cookie preferences
  - Third-party integrations visible
  - Account deletion option

---

### 1.10 Notifications & Engagement

#### Feature: Push Notifications
- **Description**: Timely reminders and updates
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - Daily challenge reminder (customizable time)
  - Streak milestone celebrations ("7-day streak! 🔥")
  - Module recommendations ("Ready to try investing?")
  - New features/content ("New module available!")
  - Achievement unlocked alerts
  - Leaderboard updates ("You're #2 this week!")
  - Opt-in/out controls
  - Frequency capping (max 2-3 per day)
  - Quiet hours (no notifications 9pm-9am by default)

#### Feature: Email Digest
- **Description**: Weekly summary of progress
- **User Type**: Teenager
- **Priority**: Medium
- **Complexity**: Simple
- **Requirements**:
  - Weekly email with:
    - Modules completed
    - Points earned
    - Achievements unlocked
    - Streak status
    - Leaderboard ranking
    - Recommended next steps
  - Frequency: Weekly on Sunday (customizable)
  - Plain text and HTML versions
  - Unsubscribe option

---

### 1.11 Leaderboard

#### Feature: Global Leaderboard
- **Description**: Compare progress with other users
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - Rank by total XP (global, regional, age group)
  - Top 100 displayed
  - Search for specific user
  - Show current rank and nearby users (±10)
  - Weekly leaderboard (resets every Sunday)
  - Monthly leaderboard (resets every month)
  - Seasonal leaderboard (3-month cycle)
  - Rewards for top 3 weekly (bonus points)
  - Filter by age group (13-14 vs 15-16)
  - Anonymous or real name display (user choice)

#### Feature: Friends Leaderboard
- **Description**: Compare with friends (future feature)
- **User Type**: Teenager
- **Priority**: Medium
- **Complexity**: Medium
- **Requirements**:
  - Add friends by username or invite link
  - Private leaderboard with only friends
  - Challenge friends to duels or competitions
  - See friend's achievements
  - Leave supportive comments on friend's progress

---

### 1.12 Help & Support

#### Feature: In-App FAQ
- **Description**: Quick answers to common questions
- **User Type**: All
- **Priority**: High
- **Complexity**: Simple
- **Requirements**:
  - Searchable FAQ (50+ common questions)
  - Organized by category
  - Video tutorials for complex features
  - Contact support button
  - Feedback form

#### Feature: Support Ticketing
- **Description**: Direct contact with support team
- **User Type**: All
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - Submit support tickets in-app
  - Category selection (bug, feature request, technical issue, billing)
  - Expected response time displayed
  - Ticket history visible
  - Email notification of responses
  - Real-time chat with support (future)

---

## 🎮 PHASE 2: Connected Simulation (Q2-Q3 2026)

The metagame. All learning connects to a persistent financial simulation.

### 2.1 Virtual Life Simulation

#### Feature: Monthly Salary & Income
- **Description**: Simulated income system
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - Receive monthly salary (simulates allowance or part-time job)
  - 13-14 year olds: N$1,000-2,000 monthly
  - 15-16 year olds: N$2,000-3,500 monthly
  - Income variations: Bonus for good decisions, penalty for poor ones
  - Seasonal income (e.g., higher in December)
  - Job/income source customizable by user

#### Feature: Monthly Expenses & Bills
- **Description**: Recurring costs that reduce available money
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - Essential expenses:
    - Transport: N$150-300/month
    - Phone data: N$50-100/month
    - School supplies: N$50-150/month
  - Optional expenses:
    - Gaming subscription: N$20-50
    - Entertainment: N$100-200
    - Social outings: N$150-300
  - Random expenses (simulating real life):
    - Phone needs repair (N$200-500)
    - New shoes needed (N$300-800)
    - Trip with friends (N$500-1,000)
  - User must cover bills or face consequences
  - Visual countdown to bill due date

#### Feature: Life Events
- **Description**: Unexpected financial challenges
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: High
- **Requirements**:
  - Random monthly events that test financial decisions:
    - **Positive Events**:
      - Bonus from employer (N$500)
      - Birthday gift (N$200-1,000)
      - Unexpected income opportunity (N$100-500)
      - Tax refund (N$300-800)
    - **Negative Events**:
      - Medical expense (N$400-1,000)
      - Phone stolen (N$800-2,000)
      - Transport fare increase
      - Data costs spike
      - Car/bike needs repair
      - Teacher fee required
    - **Decision Events**:
      - Friend asks to borrow money (lend or decline?)
      - Opportunity to buy something expensive (buy now or save?)
      - Chance to earn extra money (side gig, time trade-off)
      - Investment opportunity (real or scam?)

  - Events have probability based on user's financial decisions
  - Good budgeters get fewer emergencies (rewarding good behavior)
  - Scam susceptibility increases if user ignores warnings
  - Event resolution shows consequences

#### Feature: Consequences & Feedback
- **Description**: Immediate feedback on financial decisions
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - Real-time impact on virtual life:
    - Happiness (0-100%)
    - Stress level (0-100%)
    - Financial health (0-100%)
    - Savings progress
  - Visual indicators:
    - Avatar expression changes based on happiness
    - Metrics dashboard shows current state
    - Color-coded warnings (red = trouble, green = healthy)
  - Consequence explanations:
    - "Your spending is too high. You'll run out of money by month end."
    - "You've saved N$1,000! On track for your goal."
    - "You handled that emergency well. Your financial stress is lower."
  - Recovery paths shown (how to improve situation)

---

### 2.2 Character Stories & Decision-Making

#### Feature: Character Story Campaign
- **Description**: Follow 5 characters through financial journeys
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: High
- **Requirements**:
  - **5 Main Characters**:
    1. **Sarah** — The Spender
       - Learns about budgeting after money runs out mid-month
       - Story arc: Realizes she needs to prioritize
       - Modules: Smart Budgeting, Identifying Wants vs Needs
    2. **Daniel** — The Saver
       - Saves patiently for goals
       - Story arc: Realizes saving alone isn't enough, needs investing
       - Modules: Saving Goals, Long-Term Investing
    3. **Grace** — The Entrepreneur
       - Starts side business, learns about income and taxes
       - Story arc: Growing business, managing employees, paying taxes
       - Modules: Entrepreneurship, Taxation, Income Management
    4. **Aiden** — The Cautious One
       - Almost falls for scams, learns online safety
       - Story arc: Gets wiser about financial decisions
       - Modules: Spotting Scams, Two-Factor Authentication
    5. **Zoe** — The Goal-Oriented
       - Sets specific financial targets, achieves them
       - Story arc: Reaching goals, setting new challenges
       - Modules: Goal Setting, Investing for Future

  - Each character has 10-15 short story segments (2-3 min each)
  - User makes decisions on character's behalf
  - Your decisions affect character's outcome
  - Multiple endings based on cumulative choices
  - Character interactions (Sarah learns from Daniel, etc.)

#### Feature: Interactive Decision Points
- **Description**: Choose character's financial actions
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: High
- **Requirements**:
  - At key moments, user chooses character's action
  - 2-3 options per decision point
  - Consequences shown immediately and long-term
  - Some decisions create diverging story paths
  - Users can replay to see different outcomes
  - Decision analytics: See what % of users chose each option
  - Moral dimension: Sometimes choosing "harder" path teaches lesson
  - Example decision:
    ```
    Sarah: "I got N$1,000 bonus. Should I:
    A) Buy the new phone I've wanted (N$1,200)
    B) Invest it and save for bigger goal
    C) Spend half, save half?"
    ```
  - Consequences vary:
    - A: Short-term happiness, long-term regret (no money for emergency)
    - B: No immediate satisfaction, long-term wealth (N$1,000 grows)
    - C: Balanced approach (happiness + progress)

#### Feature: Character Insights & Tips
- **Description**: Characters provide personalized financial advice
- **User Type**: Teenager
- **Priority**: Medium
- **Complexity**: Medium
- **Requirements**:
  - Characters offer tips based on user's decisions
  - Sarah: "I used to spend everything... try the 50/30/20 rule like I did"
  - Daniel: "Start with small savings goals. I saved N$50/month for 10 months"
  - Grace: "Track your income carefully. Taxes are complicated but important"
  - Aiden: "Always verify before clicking. I almost lost my money!"
  - Zoe: "Set SMART goals. Mine worked because I was specific."
  - Tips appear at relevant moments
  - User can request character's advice on demand
  - Character wisdom evolves as user progresses

---

### 2.3 Levels & Unlocks

#### Feature: Progression Levels (Expanded)
- **Description**: Major milestones unlock new features
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - **Level 5: "Money Explorer"** — Unlock Investing Module
  - **Level 10: "Financial Analyst"** — Unlock Tax Module
  - **Level 15: "Investment Strategist"** — Unlock Advanced Investing
  - **Level 20: "Financial Master"** — Unlock all premium features
  - Visual ceremony for level-ups
  - "You've unlocked a new module!" notifications
  - Level-up gift (bonus points or cosmetics)

#### Feature: Module Prerequisites
- **Description**: Some modules unlock after completing others
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Simple
- **Requirements**:
  - Smart Budgeting → Saving Goals → Investing
  - Spotting Scams → Online Banking Safety
  - Taxation → Income Management
  - Prerequisites prevent overwhelm
  - Visual path shows module dependencies
  - Can skip prerequisites at higher levels

---

### 2.4 Enhanced Rewards System

#### Feature: Cosmetic Unlocks
- **Description**: Earn appearance customizations
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - Avatar clothing (50+ outfits)
  - Hairstyles (30+ options)
  - Accessories (50+ items)
  - Background themes (20+ themes)
  - Wallet skins (15+ designs)
  - Bank card designs (10+ styles)
  - House/room customization (10+ themes)
  - Pet companions (10+ virtual pets)
  - Emoji packs (5+ themed packs)
  - Title badges (30+ titles like "Budget Master", "Scam Detective")

#### Feature: Redemption Marketplace
- **Description**: Spend earned points on cosmetics
- **User Type**: Teenager
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - Browse cosmetic items with point costs
  - 1,000-10,000 points per item (scaled by rarity)
  - Daily rotation of featured items
  - Rare seasonal items (limited availability)
  - Wishlists (save items to buy later)
  - Preview before purchase
  - No real money transactions
  - Purchased items shown immediately

#### Feature: Seasonal Rewards
- **Description**: Time-limited exclusive rewards
- **User Type**: Teenager
- **Priority**: Medium
- **Complexity**: Medium
- **Requirements**:
  - Monthly themes (January = New Year Goals, December = Giving)
  - Holiday-specific rewards (Christmas, independence day, etc.)
  - Event-based challenges (Financial Literacy Month = special badges)
  - Limited-time cosmetics (30 days availability)
  - FOMO without exploitation (rewards stay cosmetic-only)
  - Can re-unlock items in future seasons

---

## 🏫 PHASE 3: Ecosystem (Q4 2026+)

Connect teenagers, parents, and educators into one integrated platform.

### 3.1 Parent Dashboard

#### Feature: Parent Account Setup
- **Description**: Parents create linked accounts
- **User Type**: Parent
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - Email-based registration
  - Link to one or more child accounts (with consent)
  - Child privacy by design (parents see progress, not chat/messages)
  - Multiple children support
  - Customizable access levels per child
  - Account security (2FA recommended)

#### Feature: Child Progress Monitoring
- **Description**: See child's learning and financial progress
- **User Type**: Parent
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - Dashboard showing:
    - Modules completed
    - Current level and XP progress
    - Weekly activity summary
    - Quiz scores
    - Achievements unlocked
    - Time spent learning
    - Streaks maintained
  - Visual progress bars and charts
  - Alerts for milestones ("Son just completed Investing module!")
  - Weekly email digest

#### Feature: Allowance & Chores Integration
- **Description**: Link app to real-world allowance
- **User Type**: Parent
- **Priority**: High
- **Complexity**: High
- **Requirements**:
  - Set monthly allowance amount (N$)
  - Create chore list (e.g., "Do laundry" = N$50)
  - Child completes chore, marks it in app
  - Parent approves completion and payment
  - Money credited to child's real account or virtual wallet
  - Track chore completion over time
  - Reports on reliability
  - Link to real banking app (future integration)

#### Feature: Conversation Starters
- **Description**: Prompts for parent-child money conversations
- **User Type**: Parent
- **Priority**: Medium
- **Complexity**: Simple
- **Requirements**:
  - Weekly suggested topics to discuss:
    - "Ask your child about the budgeting challenge they did"
    - "Discuss: How would you handle this unexpected expense?"
    - "Role-play: Negotiating a raise"
  - Talking points and conversation guides
  - Fun activities to do together
  - Links to relevant modules

#### Feature: Goal Collaboration
- **Description**: Set family financial goals
- **User Type**: Parent & Teenager
- **Priority**: Medium
- **Complexity**: Medium
- **Requirements**:
  - Family goal creation ("Save N$5,000 for family trip")
  - Contribution tracking (who saved how much)
  - Progress visualization
  - Celebrate family milestones
  - Teach collaborative saving

---

### 3.2 Teacher / School Dashboard

#### Feature: Teacher Account Setup
- **Description**: Educators create school-linked accounts
- **User Type**: Educator
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - Registration with school email
  - School verification (admin approval)
  - Create multiple classes
  - Invite students to join specific class
  - Link to curriculum standards (NCEA, local)

#### Feature: Class Management
- **Description**: Manage student cohorts
- **User Type**: Educator
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - View all students in class
  - See individual and class-wide progress
  - Assign specific modules
  - Set module deadlines
  - Create custom challenges
  - Monitor completion rates

#### Feature: Assignment Tracking
- **Description**: Assign modules with deadlines
- **User Type**: Educator
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - Create assignments (e.g., "Complete Smart Budgeting by Friday")
  - Set due dates
  - Track completion status
  - See quiz scores for grading
  - Mark assignments as complete/incomplete
  - Integration with grade books (future)

#### Feature: Class Leaderboard & Competitions
- **Description**: In-class rankings and friendly competition
- **User Type**: Educator & Teenager
- **Priority**: High
- **Complexity**: Medium
- **Requirements**:
  - Class-only leaderboard (weekly/monthly)
  - Top 3 get bonus points
  - Optional: Classroom-wide competitions (e.g., "Budget Challenge")
  - Rewards for top performers
  - Public display in classroom (screen or printout)
  - Motivates healthy competition

#### Feature: Assessment Reports
- **Description**: Detailed class-wide analytics
- **User Type**: Educator
- **Priority**: High
- **Complexity**: High
- **Requirements**:
  - Module completion rates
  - Average quiz scores
  - Engagement metrics (time spent, sessions)
  - Identify struggling students
  - Identify high performers
  - Learning outcomes analysis
  - Export reports (PDF, CSV)
  - Disaggregated data (by age, gender, socioeconomic - anonymous)

#### Feature: Professional Development
- **Description**: Support for educators using SmartCent
- **User Type**: Educator
- **Priority**: Medium
- **Complexity**: Medium
- **Requirements**:
  - Training modules for teachers
  - Lesson plans aligned to modules
  - Classroom activity guides
  - Discussion guides
  - Assessment rubrics
  - Webinars and workshops
  - Peer community (teacher forums)

---

### 3.3 AI Financial Coach (Future)

#### Feature: Natural Language Q&A
- **Description**: Ask AI financial questions
- **User Type**: Teenager, Parent
- **Priority**: Medium (Post-MVP)
- **Complexity**: High
- **Requirements**:
  - Natural language input (text or voice)
  - Questions about financial scenarios
  - Example: "What if I save N$200/month for 5 years?"
  - AI responds with calculation and explanation
  - Personalized to user's financial profile
  - Learning opportunity (not just answer, but teach)

#### Feature: Scenario Modeling
- **Description**: "What if" analysis for financial decisions
- **User Type**: Teenager, Parent
- **Priority**: Medium (Post-MVP)
- **Complexity**: High
- **Requirements**:
  - "If I get a N$500 raise, how much faster will I reach my goal?"
  - "What if I start investing at 15 instead of 16?"
  - "How much would I have in 30 years if I save N$200/month?"
  - AI generates graphs and projections
  - Multiple scenarios compared side-by-side

#### Feature: Personalized Recommendations
- **Description**: Suggest next steps based on learning
- **User Type**: Teenager
- **Priority**: Medium (Post-MVP)
- **Complexity**: High
- **Requirements**:
  - Analyze user's behavior and knowledge level
  - Recommend modules to complete next
  - Suggest challenges suited to current level
  - Point out knowledge gaps
  - Encourage spaced repetition of difficult concepts
  - Celebrate progress

---

### 3.4 Community Features

#### Feature: Social Sharing
- **Description**: Share achievements with others
- **User Type**: Teenager
- **Priority**: Medium
- **Complexity**: Medium
- **Requirements**:
  - Share badges and achievements
  - Share level-up milestones
  - Share goal progress
  - Share tips learned ("Just realized I can save N$X per month!")
  - Shareable links/screenshots
  - Share to social media (Instagram, TikTok, WhatsApp)
  - Privacy controls (who can see)

#### Feature: Peer Communities (Future)
- **Description**: Connect with other users
- **User Type**: Teenager
- **Priority**: Low
- **Complexity**: High
- **Requirements**:
  - Forums by topic (Budgeting, Investing, Scam Alerts)
  - Moderated by community managers
  - Q&A sections (teens help teens)
  - Success stories
  - Safety by design (no personal data sharing)

#### Feature: Parent Community (Future)
- **Description**: Connect parents for advice
- **User Type**: Parent
- **Priority**: Low
- **Complexity**: Medium
- **Requirements**:
  - Private parent forums
  - Share strategies for teaching money
  - Ask questions from other parents
  - Moderated discussions

---

### 3.5 Real-World Integrations (Future)

#### Feature: Banking Integration
- **Description**: Connect to real bank accounts (optional)
- **User Type**: Teenager (16+), Parent
- **Priority**: Low (Post-MVP, requires partnerships)
- **Complexity**: Very High
- **Requirements**:
  - Secure API integration with banks
  - View real account balance in app
  - See real transactions
  - Compare spending to budgets
  - Bridge simulation to reality
  - Parental controls for spending
  - Age-appropriate account features

#### Feature: Micro-Task Marketplace (Future)
- **Description**: Earn real money through tasks
- **User Type**: Teenager (16+)
- **Priority**: Low (Post-MVP)
- **Complexity**: High
- **Requirements**:
  - Age-appropriate tasks (surveys, categorization)
  - Earn real money (not app currency)
  - Payments via mobile money or real bank account
  - Parental approval for under 18
  - Fair compensation (market rates)
  - Transparency on earnings

#### Feature: Investment Platform Link (Future)
- **Description**: Move from simulation to real investing
- **User Type**: Teenager (16+)
- **Priority**: Low (Post-MVP, requires partnerships)
- **Complexity**: Very High
- **Requirements**:
  - Partner with brokerage or investment app
  - Open real investment account
  - Move from simulated investments to real
  - Educational support for real investing
  - Regulatory compliance (FCA, etc.)
  - Parental approval required

---

## 📊 Feature Priority Matrix

### MVP (Phase 1, Q1 2026) - Must Have

- User authentication and onboarding
- Dashboard and navigation
- Virtual wallet system
- Module library and core modules (5+)
- Quiz system
- Badge/achievement system
- Points system
- Daily challenges
- Streak system
- Profile and settings
- Leaderboard

**Estimated Development Time**: 12-16 weeks

### High Priority (Phase 1-2, Q1-Q2)

- Age-based segmentation
- Character introduction
- Flashcard system
- Progress analytics
- Story campaign (character stories)
- Levels and progression
- Cosmetic unlocks
- Notifications and engagement

**Estimated Development Time**: 8-12 weeks

### Medium Priority (Phase 2-3, Q2-Q4)

- Life events and simulation
- Parent dashboard (basic)
- Teacher dashboard (basic)
- Seasonal rewards
- Social sharing
- Support ticketing

**Estimated Development Time**: 12-16 weeks

### Low Priority (Post-Launch, 2027+)

- AI Financial Coach
- Banking integration
- Micro-task marketplace
- Investment platform link
- Advanced community features

**Estimated Development Time**: 20+ weeks per feature

---

## 🎯 Feature Dependencies

```
Authentication → Onboarding → Dashboard
                                   ├→ Wallet
                                   ├→ Modules (Learning)
                                   ├→ Challenges (Daily)
                                   ├→ Profile
                                   └→ Leaderboard

Modules → Quizzes → Achievements
           ↓
        Points System → Rewards
                           ├→ Badges
                           ├→ Levels
                           └→ Cosmetics

Modules → Character Stories → Decision System → Life Simulation

Teacher/Parent Features (requires teen features first)
AI Features (requires rich user behavior data first)
Integration Features (requires stable core platform)
```

---

## 📱 Success Metrics per Feature

Every feature will be measured on:
- **Adoption**: % of users engaging with this feature
- **Engagement**: Average time spent, frequency of use
- **Learning Impact**: Does this feature improve financial knowledge?
- **Retention**: Do users who use this feature stay longer?
- **Satisfaction**: NPS score for this specific feature

---

## 📝 Document Status

- **Draft**: ✅ Complete
- **Review**: Awaiting feedback
- **Approval**: Pending team consensus
- **Implementation**: Ready for development

**Next Steps**: Create USER_STORIES.md to define detailed user scenarios and requirements.

