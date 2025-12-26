# 🚀 Setup Checklist for Your Digital Garden

Complete these steps to fully personalize your digital garden.

## ✅ Phase 1: Essential Configuration (Do First)

### 1. Site Configuration
- [ ] Open `_config.yml`
- [ ] Update `title` (currently "Sanjan's Codex")
- [ ] Update `description`
- [ ] Update `author` name
- [ ] Update `url` with your actual domain
- [ ] Save file

### 2. About Page
- [ ] Open `_pages/about.md`
- [ ] Replace placeholder contact info:
  - [ ] Email address (appears 3 times)
  - [ ] GitHub username
  - [ ] Twitter handle
- [ ] Update bio and description
- [ ] Save file

### 3. Social Links (Multiple Files)
Update these placeholder values in the following files:

#### `_pages/subscribe.md`
- [ ] Newsletter form action URL (if using newsletter service)
- [ ] Email address
- [ ] Twitter handle
- [ ] GitHub username
- [ ] LinkedIn profile

#### `_pages/network.md`
- [ ] Email address
- [ ] GitHub repository URL/username

#### `_pages/start.md`
- [ ] Email address
- [ ] Twitter handle
- [ ] GitHub username

#### `_pages/roadmap.md`
- [ ] Email address
- [ ] Twitter handle
- [ ] GitHub repository URL

#### `_pages/reference.md`
- [ ] Email address
- [ ] Twitter handle
- [ ] All site URL placeholders

#### `_includes/head.html`
- [ ] Twitter handle (meta tag: `@yourhandle`)

#### `_includes/footer.html`
- [ ] GitHub repository URL

### 4. README.md
- [ ] Replace all `[Your Name]` placeholders
- [ ] Update `[Your URL Here]` with actual site URL
- [ ] Update repository URLs
- [ ] Replace email addresses
- [ ] Update copyright year

## ✅ Phase 2: Optional Enhancements

### 5. Newsletter Integration (If Using)
- [ ] Sign up for newsletter service (e.g., Buttondown, Substack, Mailchimp)
- [ ] Get form action URL
- [ ] Update `_pages/subscribe.md` with actual form endpoint
- [ ] Test subscription flow

### 6. Analytics (Optional)
- [ ] Choose analytics provider (Plausible, Simple Analytics, or Google Analytics)
- [ ] Add tracking code to `_includes/head.html`
- [ ] Test analytics tracking

### 7. Custom Domain (If Using)
- [ ] Purchase domain
- [ ] Update `url` in `_config.yml`
- [ ] Configure DNS settings
- [ ] Update Netlify domain settings
- [ ] Enable HTTPS

### 8. Favicon
- [ ] Create your favicon (16x16, 32x32, etc.)
- [ ] Add to `assets/` folder
- [ ] Update `_includes/head.html` favicon link

## ✅ Phase 3: Content Personalization

### 9. Clean Up Template Content
- [ ] Review all notes in `_notes/` folder
- [ ] Keep, edit, or delete template examples:
  - [ ] `accents.md`
  - [ ] `adaptive-patterns.md`
  - [ ] `career-development.md`
  - [ ] `conceptual-frameworks.md`
  - [ ] `conceptual-migration.md`
  - [ ] `consistency.md`
  - [ ] `current-investigations.md`
  - [ ] `move your body every day.md`
  - [ ] `paradox-of-boundaries.md`
  - [ ] `programming-concepts.md`
  - [ ] `welcome-to-my-garden.md`
  - [ ] `your-first-note.md` (already updated to "How This Garden Works")
  - [ ] `안녕하세요.md`
  - [ ] `animals/cats.md`
  - [ ] `animals/tigers.md`

### 10. Add Your First Real Notes
- [ ] Create 3-5 notes in your own voice
- [ ] Add tags to each note
- [ ] Create connections between notes
- [ ] Update index pages with your notes

### 11. Customize Index Pages
Review and update:
- [ ] `_notes/index-programming.md`
- [ ] `_notes/index-systems-thinking.md`
- [ ] `_notes/index-personal-development.md`

## ✅ Phase 4: Deployment

### 12. GitHub Repository
- [ ] Create new GitHub repository
- [ ] Initialize git in your project folder
- [ ] Add remote origin
- [ ] Push code to GitHub

```bash
git init
git add .
git commit -m "Initial commit of digital garden"
git remote add origin https://github.com/yourusername/your-repo.git
git branch -M main
git push -u origin main
```

### 13. Netlify Deployment
- [ ] Sign up for Netlify account
- [ ] Connect GitHub repository
- [ ] Configure build settings:
  - Build command: `jekyll build`
  - Publish directory: `_site`
- [ ] Deploy site
- [ ] Test deployed site

### 14. Post-Deployment
- [ ] Update `_config.yml` with actual deployed URL
- [ ] Rebuild and redeploy
- [ ] Test all links and features
- [ ] Verify RSS feed works
- [ ] Test dark mode toggle
- [ ] Try search functionality
- [ ] Check mobile responsiveness

## ✅ Phase 5: Dependencies & Local Setup

### 15. Install Dependencies
- [ ] Ensure Ruby 3.x is installed
- [ ] Run `bundle install`
- [ ] Install the new RSS feed gem: `bundle install`
- [ ] Test local build: `bundle exec jekyll serve`
- [ ] Verify site works at `localhost:4000`

### 16. Test All Features Locally
- [ ] Bidirectional links work
- [ ] Graph visualization loads
- [ ] Search returns results
- [ ] Tag pages display correctly
- [ ] Dark mode toggles properly
- [ ] RSS feed generates
- [ ] All navigation links work

## 🎯 Quick Find & Replace

Use your code editor's find/replace function for these common placeholders:

| Find | Replace With |
|------|--------------|
| `your.email@example.com` | Your actual email |
| `@yourhandle` | Your Twitter handle |
| `@yourusername` | Your GitHub username |
| `your-site-url.com` | Your actual domain |
| `https://your-site-url.com` | Your full URL |
| `yourusername/repo` | Your GitHub repo path |

## 📝 Notes

- **Don't skip social links**: Even if you don't use all platforms, update or remove the placeholders
- **Test before deploying**: Always run `bundle exec jekyll serve` locally first
- **Backup your work**: Commit to git frequently
- **Start small**: Don't feel pressured to fill everything immediately

## ✅ Final Checklist

Before announcing your garden to the world:

- [ ] All placeholder text replaced
- [ ] All links tested and working
- [ ] RSS feed validates (use https://validator.w3.org/feed/)
- [ ] Mobile experience tested
- [ ] Dark mode works correctly
- [ ] Search returns accurate results
- [ ] At least 5 personal notes published
- [ ] About page reflects your voice
- [ ] README updated with your info

## 🎉 Launch!

Once everything is checked:

- [ ] Share on Twitter/social media
- [ ] Add to digital garden directories
- [ ] Connect with other gardeners
- [ ] Start writing regularly!

---

**Need Help?** Refer to the main README.md for detailed instructions.

**Questions?** Check the [Jekyll documentation](https://jekyllrb.com/docs/) or [digital gardening resources](https://github.com/MaggieAppleton/digital-gardeners).
