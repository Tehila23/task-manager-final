# Task Manager Pro - אפליקציית ניהול משימות 📝

אפליקציית מנהל משימות מתקדמת ומעוצבת שנבנתה כפרויקט מסכם בקורס React. האפליקציה מאפשרת למשתמשים לארגן את המשימות שלהם ביעילות, עם תמיכה בקטגוריות צבעוניות, תאריכי יעד וממשק משתמש מודרני ורספונסיבי.

## תכונות מרכזיות
* **ניהול משימות מלא:** הוספה, עריכה, מחיקה וסימון משימות כהושלמו.
* **קטגוריות דינמיות:** יצירת קטגוריות חדשות עם בחירת צבעים מתוך פלטה מעוצבת.
* **תאריכי יעד:** הגדרת דד-ליין למשימות באמצעות לוח שנה.
* **תצוגה גמישה:** מעבר בלחיצת כפתור בין "תצוגת רשימה" (List) ל"תצוגת כרטיסיות" (Grid).
* **סינון וחיפוש:** סינון משימות לפי סטטוס (הכל/לביצוע/הושלמו) וחיפוש חופשי בטקסט.
* **ממשק משתמש עשיר:** שימוש באנימציות, גרדיאנטים ועיצוב נקי (Glassmorphism).
* **שמירה אטומטית:** כל הנתונים נשמרים ב-LocalStorage של הדפדפן.

##  טכנולוגיות
הפרויקט נבנה באמצעות הכלים :
* **React 19**
* **Vite** (Build Tool)
* **Tailwind CSS v4** (Styling)
* **Lucide React** (Icons)
* **Radix UI** (Accessible Primitives)

## הוראות הרצה (Installation)

כדי להריץ את הפרויקט מקומית על המחשב:

1.  התקן את התלויות (Dependencies):
    ```bash
    npm install
    ```

2.  הרץ את שרת הפיתוח:
    ```bash
    npm run dev
    ```

3.  פתח את הדפדפן בכתובת שמופיעה בטרמינל (בדרך כלל `http://localhost:5173`).

##  רשימת קומפוננטות ואחריותן

האפליקציה מחולקת לקומפוננטות לוגיות להפרדת אחריות (Separation of Concerns):

1.  **`App`**: הקומפוננטה הראשית ("המוח"). מנהלת את ה-State של המשימות והקטגוריות, ומבצעת את השמירה והטעינה מול ה-LocalStorage.
2.  **`TaskForm`**: טופס להוספת משימות חדשות, הכולל גם דיאלוג ליצירת קטגוריות חדשות ובחירת צבעים.
3.  **`TaskList`**: אחראית על רינדור רשימת המשימות וניהול התצוגה (מעבר בין Grid לרשימה).
4.  **`TaskItem`**: מציגה משימה בודדת ומטפלת באינטראקציות שלה (עריכה, מחיקה, סימון כחשוב, שינוי סטטוס).
5.  **`FilterBar`**: רכיב Dropdown לסינון המשימות לפי הסטטוס שלהן (הכל, לביצוע, הושלמו).
6.  **`SearchBar`**: שורת חיפוש המאפשרת סינון חי של המשימות לפי טקסט חופשי.
7.  **`Footer`**: מציג סיכום סטטיסטי של המשימות וכפתור לניקוי משימות שהושלמו.

## ⚠️ מגבלות ידועות
* המידע נשמר ב-LocalStorage של הדפדפן בלבד (Client-Side) ולא מסתנכרן לענן או בין מכשירים שונים.