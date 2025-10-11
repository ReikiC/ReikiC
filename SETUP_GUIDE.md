# GitHub Profile README Setup Guide

This document provides instructions for personalizing and configuring your GitHub profile README with all the integrated APIs and features.

## 📝 Quick Customization Checklist

### 1. Personal Information
Update the following placeholders in `README.md`:

- **Social Links** (Line ~130):
  - `YOUR_LINKEDIN` - Your LinkedIn username
  - `YOUR_TWITTER` - Your Twitter/X username
  - `YOUR_EMAIL@example.com` - Your contact email
  - `YOUR_WEBSITE.com` - Your personal website URL
  - `YOUR_DISCORD` - Your Discord server invite code

### 2. Spotify Integration
To display your currently playing song:

1. Go to [Spotify Account Overview](https://www.spotify.com/account/overview/)
2. Copy your Spotify User ID
3. In `README.md` (Line ~112), replace `YOUR_SPOTIFY_USER_ID` with your actual Spotify User ID

### 3. Blog Posts Integration
To automatically display your latest blog posts:

1. Open `.github/workflows/blog-post-workflow.yml`
2. Replace `YOUR_DEVTO_USERNAME` with your Dev.to username
3. Or use another RSS feed URL (Medium, Hashnode, etc.)

**Popular RSS feed formats:**
- Dev.to: `https://dev.to/feed/YOUR_USERNAME`
- Medium: `https://medium.com/feed/@YOUR_USERNAME`
- Hashnode: `https://YOUR_USERNAME.hashnode.dev/rss.xml`

### 4. Tech Stack Customization
The README includes badges for common technologies. To customize:

- **Add more badges:** Visit [shields.io](https://shields.io/) or [simpleicons.org](https://simpleicons.org/)
- **Remove unused technologies:** Delete the corresponding badge lines
- **Format:** `![Name](https://img.shields.io/badge/Name-Color?style=for-the-badge&logo=logoname&logoColor=white)`

### 5. About Me Section
Update the "About Me" section (Lines ~18-26) with:
- What you're currently working on
- What you're learning
- Your interests and goals
- Contact preferences
- Fun facts about yourself

## 🔧 Advanced Configuration

### GitHub Stats Customization

The README uses several GitHub stats APIs. You can customize them:

#### GitHub Stats Card
```markdown
![GitHub Stats](https://github-readme-stats.vercel.app/api?username=ReikiC&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true)
```

**Options:**
- `theme`: tokyonight, radical, merko, gruvbox, dark, default, etc.
- `show_icons`: true/false
- `hide_border`: true/false
- `count_private`: true/false (includes private repo stats)
- `include_all_commits`: true/false

#### Top Languages Card
```markdown
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=ReikiC&layout=compact&theme=tokyonight&hide_border=true&langs_count=8)
```

**Options:**
- `layout`: compact, normal
- `langs_count`: Number of languages to display (default: 5, max: 10)
- `hide`: Comma-separated list of languages to hide

#### Streak Stats
```markdown
![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=ReikiC&theme=tokyonight&hide_border=true)
```

**Available themes:** dark, radical, merko, gruvbox, tokyonight, onedark, cobalt, synthwave, highcontrast, dracula, and more.

### Profile View Counter

The profile view counter automatically tracks visitors:
```markdown
![Profile Views](https://komarev.com/ghpvc/?username=ReikiC&label=Profile%20Views&color=0e75b6&style=flat)
```

**Color options:** brightgreen, green, yellow, orange, red, blue, grey, lightgrey, blueviolet, ff69b4

## 🐍 Snake Animation Setup

The snake animation workflow is already configured in `.github/workflows/snake.yml`. It will:
- Run automatically every 24 hours
- Generate a snake eating your GitHub contributions
- Save the output to the `output` branch

**Note:** The first run might take a few minutes. After the workflow completes, the snake animation will appear in your README.

## 🎨 Theme Customization

All visual elements use the "tokyonight" theme by default. To change the theme globally:

1. Choose a theme:
   - dark
   - radical
   - merko
   - gruvbox
   - tokyonight
   - onedark
   - cobalt
   - synthwave
   - highcontrast
   - dracula

2. Replace `theme=tokyonight` with your chosen theme in all API URLs

## 📊 Adding More APIs

Here are some additional APIs you can integrate:

### WakaTime (Coding Activity)
Shows your coding time statistics:
```markdown
![WakaTime Stats](https://github-readme-stats.vercel.app/api/wakatime?username=YOUR_WAKATIME_USERNAME&theme=tokyonight)
```

### GitHub Metrics
Advanced metrics with more customization:
```markdown
![Metrics](https://metrics.lecoq.io/ReikiC?template=classic&config.timezone=Asia%2FShanghai)
```

### Coding Stats
Track your coding statistics:
```markdown
![Code Time](https://img.shields.io/endpoint?style=flat&url=https://codetime-api.datreks.com/badge/YOUR_CODETIME_ID)
```

## 🔒 Privacy Considerations

- **Private Repository Stats:** Set `count_private=true` only if you want to include them
- **Email Display:** Consider using a contact form instead of direct email
- **Personal Information:** Only share what you're comfortable being public

## 🚀 Testing Your README

Before committing:
1. Preview your README on GitHub (it renders automatically)
2. Check that all images load correctly
3. Verify all links work
4. Test on both light and dark GitHub themes
5. View on mobile to ensure responsive design

## 🆘 Troubleshooting

### Images Not Loading
- Check if the API service is down
- Verify your username is correct in all URLs
- Some APIs have rate limits; wait and try again

### Workflow Not Running
- Ensure GitHub Actions are enabled in repository settings
- Check workflow permissions in Settings > Actions > General
- Review workflow logs for error messages

### Permission Denied Error (403)
If the snake animation workflow fails with "Permission denied" or 403 error:
- The workflow file needs explicit `permissions: contents: write` in the YAML
- Go to Settings > Actions > General > Workflow permissions
- Ensure "Read and write permissions" is selected, or
- Use the `permissions` block in your workflow file (recommended)

### Stats Not Updating
- GitHub stats cache for ~4 hours
- Use `&cache_seconds=1800` to reduce cache time
- Force refresh by adding a query parameter like `&refresh=1`

## 📚 Resources

- [GitHub Profile README Guide](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme)
- [Awesome GitHub Profile README](https://github.com/abhisheknaiidu/awesome-github-profile-readme)
- [Shields.io Badges](https://shields.io/)
- [Simple Icons](https://simpleicons.org/)
- [GitHub Readme Stats](https://github.com/anuraghazra/github-readme-stats)

## 🤝 Contributing

Feel free to customize this README to match your personal style and preferences!

---

Made with ❤️ for the GitHub community
