# 🚀 שערי שמיעה - מערכת Jekyll למאגר תורני

**תאריך:** 27 בינואר 2025  
**גרסה:** 1.0.0

---

## 📖 אודות הפרויקט

"שערי שמיעה" הוא מאגר תורני מקיף העוסק בדיני **"כעונה שומע"** - העיקרון ההלכתי הקובע ששמיעת דבר מחייבת משפטית כאילו נאמר על ידי השומע.

המאגר נבנה באמצעות **Jekyll** - מחולל אתרים סטטי המאפשר ניהול קל של תוכן Markdown והצגתו באתר אינטרנט מודרני.

---

## 🏗️ מבנה הפרויקט

```
.
├── _config.yml              # הגדרות Jekyll
├── Gemfile                  # תלויות Ruby
├── _layouts/                # תבניות HTML
│   ├── default.html         # תבנית בסיסית
│   └── article.html         # תבנית למאמרים
├── _articles/               # מאמרי Markdown
│   ├── shaarei-shemia-dini-ke-ona-shomea.md
│   ├── halacha-vedikdukei-shemia.md
│   └── shaar-hakol-vehadibur-haeloki.md
├── index.html               # עמוד הבית
├── articles.html            # עמוד כל המאמרים
├── about.html               # עמוד אודות
└── README.md                # קובץ זה
```

---

## ⚙️ התקנה והפעלה

### דרישות מערכת

- Ruby 3.0+
- Bundler
- Git

### התקנה מהירה

```bash
# 1. שכפול הפרויקט
git clone https://github.com/anlominus/shaarei-shemia.git
cd shaarei-shemia

# 2. התקנת תלויות
bundle install

# 3. הפעלת שרת פיתוח
bundle exec jekyll serve

# 4. פתיחת הדפדפן
# האתר יהיה זמין ב: http://localhost:4000
```

### פקודות נוספות

```bash
# בניית האתר
bundle exec jekyll build

# ניקוי ופיתוח מחדש
bundle exec jekyll clean && bundle exec jekyll serve

# בדיקת האתר
bundle exec jekyll doctor
```

---

## 📝 הוספת מאמרים חדשים

### שיטה 1: יצירת קובץ חדש ב-`_articles/`

```markdown
---
title: "כותרת המאמר"
date: 2025-01-27
author: "שם המחבר"
category: "קטגוריה"
tags: ["תגית1", "תגית2"]
excerpt: "תיאור קצר של המאמר"
---

# כותרת המאמר

תוכן המאמר ב-Markdown...
```

### שיטה 2: העתקת קובץ Markdown קיים

פשוט העתקו קובץ `.md` קיים לתיקיית `_articles/` והוסיפו את ה-Front Matter הנדרש.

---

## 🎨 התאמה אישית

### עיצוב

- עריכת `_layouts/default.html` לשינוי מבנה האתר
- עריכת `_layouts/article.html` לשינוי תצוגת המאמרים
- הוספת קבצי CSS ב-`assets/css/`

### הגדרות

- עריכת `_config.yml` לשינוי הגדרות כלליות
- הוספת Collections חדשות
- שינוי ברירות מחדל

### תוכן

- עריכת `index.html` לשינוי עמוד הבית
- עריכת `about.html` לשינוי עמוד האודות
- הוספת עמודים חדשים

---

## ☁️ פריסה (Deploy)

### GitHub Pages (מומלץ)

1. העלו את הפרויקט ל-GitHub תחת המשתמש AnLoMinus
2. ב-Settings → Pages בחרו "Build from a branch"
3. בחרו את הענף `main` או `gh-pages`
4. האתר יהיה זמין ב: `https://anlominus.github.io/shaarei-shemia`

### GitHub Actions (לשליטה מלאה)

```yaml
# .github/workflows/jekyll.yml
name: Build & Deploy Jekyll
on:
  push:
    branches: [ main ]
permissions:
  contents: write
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: ruby/setup-ruby@v1
        with: { ruby-version: '3.2', bundler-cache: true }
      - run: bundle install
      - run: bundle exec jekyll build -d _site
      - uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: _site
          publish_branch: gh-pages
```

---

## 🔧 תכונות מתקדמות

### חיפוש וסינון

- חיפוש לפי כותרת המאמר
- סינון לפי קטגוריה
- סינון לפי תגיות

### SEO

- תמיכה ב-Jekyll SEO Tag
- מפת אתר אוטומטית
- Feed RSS

### נגישות

- תמיכה בעברית (RTL)
- עיצוב רספונסיבי
- תמיכה בקוראי מסך

---

## 📚 משאבים נוספים

- [תיעוד Jekyll](https://jekyllrb.com/docs/)
- [GitHub Pages](https://pages.github.com/)
- [Markdown Guide](https://www.markdownguide.org/)
- [Liquid Template Language](https://shopify.github.io/liquid/)

---

## 🤝 תרומה לפרויקט

אנחנו מעודדים תרומות לפרויקט!

### איך לתרום

1. Fork את הפרויקט
2. צרו ענף חדש (`git checkout -b feature/amazing-feature`)
3. Commit את השינויים (`git commit -m 'Add amazing feature'`)
4. Push לענף (`git push origin feature/amazing-feature`)
5. פתחו Pull Request

---

## 📄 רישיון

פרויקט זה מופץ תחת רישיון MIT. ראה קובץ `LICENSE` לפרטים נוספים.

---

## 📞 צור קשר

- 📧 אימייל: [contact@shaarei-shemia.org](mailto:contact@shaarei-shemia.org)
- 🐙 GitHub: [github.com/anlominus](https://github.com/anlominus)

---

## 🙏 תודות

תודה לכל התורמים והמשתמשים של הפרויקט, ולכל מי שתרם לשמירה והעברה של המסורת התורנית.

---

**"שמע ישראל ה' אלוקינו ה' אחד"** (דברים ו:ד)
