# 🚀 הפעלה מהירה - שערי שמיעה

## התקנה מהירה (5 דקות)

### 1. התקנת Ruby ו-Bundler

```bash
# macOS (עם Homebrew)
brew install ruby bundler

# Ubuntu/Debian
sudo apt update
sudo apt install ruby-full bundler

# Windows (עם Chocolatey)
choco install ruby
gem install bundler
```

### 2. שכפול והתקנה

```bash
# שכפול הפרויקט
git clone https://github.com/anlominus/shaarei-shemia.git
cd shaarei-shemia

# התקנת תלויות
bundle install

# הפעלת שרת פיתוח
bundle exec jekyll serve
```

### 3. פתיחת האתר

פתחו את הדפדפן וגשו ל: **<http://localhost:4000>**

---

## הוספת מאמר חדש

### שיטה מהירה

1. צרו קובץ חדש בתיקיית `_articles/`
2. הוסיפו את ה-Front Matter הבא:

```markdown
---
title: "כותרת המאמר"
date: 2025-01-27
author: "שם המחבר"
category: "קטגוריה"
tags: ["תגית1", "תגית2"]
excerpt: "תיאור קצר"
---

# תוכן המאמר
```

3. שמרו את הקובץ
4. המאמר יופיע אוטומטית באתר!

---

## פריסה ל-GitHub Pages

### אוטומטי (מומלץ)

1. העלו את הקוד ל-GitHub תחת המשתמש AnLoMinus
2. ב-Settings → Pages בחרו "GitHub Actions"
3. האתר יהיה זמין ב: `https://anlominus.github.io/shaarei-shemia`

### ידני

```bash
# בניית האתר
bundle exec jekyll build

# העלאת תיקיית _site ל-GitHub Pages
```

---

## פתרון בעיות נפוצות

### שגיאת Ruby

```bash
# עדכון Ruby
rbenv install 3.2.0
rbenv global 3.2.0
```

### שגיאת Bundler

```bash
# ניקוי והתקנה מחדש
bundle clean --force
bundle install
```

### שגיאת Jekyll

```bash
# ניקוי cache
bundle exec jekyll clean
bundle exec jekyll serve
```

---

## תכונות מיוחדות

✅ **עברית מלאה** - תמיכה מלאה בעברית ו-RTL  
✅ **חיפוש דינמי** - חיפוש וסינון במאמרים  
✅ **עיצוב רספונסיבי** - עובד על כל המכשירים  
✅ **SEO מובנה** - אופטימיזציה למנועי חיפוש  
✅ **GitHub Pages** - פריסה אוטומטית  

---

## צור קשר

📧 **<support@shaarei-shemia.org>**  
🐙 **GitHub Issues** - לדיווח על באגים: [github.com/anlominus/shaarei-shemia/issues](https://github.com/anlominus/shaarei-shemia/issues)  
📖 **Wiki** - לתיעוד מפורט  

---

**"שמע ישראל ה' אלוקינו ה' אחד"** (דברים ו:ד)
