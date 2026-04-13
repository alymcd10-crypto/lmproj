# Daily Habits — Setup Guide

## What You're Deploying
A shared daily habit tracker that syncs in real time across all family devices.

**Features:** Real-time Firebase sync, 70+ habit suggestions across 9 categories, customizable habits/members/rotation, streaks, points, confetti, 7 PM reminders, parent dashboard (today/history/points), scales from 2-25+ members.

---

## Files

| File | What it does |
|------|-------------|
| `family-tasks.html` | Deployable app with Firebase sync |
| `daily-tasks-premium.jsx` | Preview artifact (runs in Claude) |
| `firebase-rules.json` | Security rules for Firebase |
| `SETUP-GUIDE.md` | This document |
| `ONBOARDING-SCRIPT.md` | How to introduce it to your family |
| `PRODUCT-ROADMAP.md` | Plan for turning it into a product |

---

## Step 1: Firebase Backend (5 min)

1. [console.firebase.google.com](https://console.firebase.google.com) → Create project → disable Analytics
2. Build → Realtime Database → Create Database → Start in test mode
3. Gear icon → Project Settings → Your apps → Web (</>) → Register → keep config visible

## Step 2: Deploy (3 min)

1. Create folder `daily-habits`, put `family-tasks.html` inside, rename to `index.html`
2. Go to [app.netlify.com/drop](https://app.netlify.com/drop), drag folder
3. Site settings → Change site name

## Step 3: Connect

1. Open your URL → paste Firebase config → make up a Family ID (same on all devices) → Connect
2. Setup wizard: add members → review/customize habits → Let's go
3. Pick your name

## Step 4: Everyone else

Same URL, same config, same Family ID. Add to Home Screen. Allow notifications.

## Step 5: Lock down

Firebase → Realtime Database → Rules → paste `firebase-rules.json` contents.

---

## Troubleshooting

- **No sync:** Check Family ID matches exactly (case-sensitive)
- **No notifications:** Allow in browser + add to home screen
- **Change habits:** Parent dashboard → Edit tab
- **Reset device:** Parent dashboard → Edit → Reset connection
