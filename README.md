# Food Diary

A simple web app for logging your child's daily food intake. Built with Supabase for data storage.

## Features

- 📝 Log meals (breakfast, lunch, dinner, snacks)
- 📅 Date-based entries
- 💭 Add notes (allergies, reactions, etc.)
- 📋 View recent entries
- 🗑️ Delete entries
- 📱 Mobile-friendly design

## Setup

### 1. Create Supabase Project
1. Go to [supabase.com](https://supabase.com) and create a free account
2. Create a new project
3. Run this SQL in the Supabase SQL editor:
```sql
create table food_entries (
  id bigint primary key generated always as identity,
  created_at timestamp default now(),
  date date not null,
  meal_type text,
  food_items text,
  notes text
);
```

### 2. Add Credentials
1. Copy your Supabase Project URL (Settings → API)
2. Copy your Anon Public Key (Settings → API)
3. Open `index.html` and replace:
```javascript
const SUPABASE_URL = 'YOUR_SUPABASE_URL';
const SUPABASE_KEY = 'YOUR_SUPABASE_KEY';
```

### 3. Run Locally
Just open `index.html` in your browser. That's it!

## Deploy to GitHub Pages

1. Create a new repository on GitHub named `food-diary`
2. Clone it locally
3. Copy `index.html` to your repo
4. Push to GitHub:
```bash
git add .
git commit -m "Initial commit"
git push
```
5. In GitHub settings, enable GitHub Pages (main branch)
6. Your app will be live at: `https://yourusername.github.io/food-diary/`

## License

MIT
