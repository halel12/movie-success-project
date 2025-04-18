# 🎬 Movie Success Predictor – מודל לסיווג הצלחת סרטים

פרויקט זה כולל ממשק אינטרנטי שפותח באמצעות Flask ב־Google Colab, לצורך חיזוי רמת ההצלחה של סרטים על פי פרמטרים כמו שחקנים, במאים, ז'אנרים, שפה, פופולריות ועוד.

---

## 🛠️ מדריך התקנה

לפני הפעלת המערכת, יש להתקין את כל חבילות התוכנה (ספריות פייתון) הדרושות.  
יש להריץ את הפקודות הבאות בתחילת הקוד במחברת Google Colab:

```python
!pip install Flask
!pip install flask-ngrok
!pip install pyngrok
!pip install joblib
!pip install pandas
!pip install numpy
!pip install qrcode[pil]
```

---

## ⚙️ התאמת סביבת העבודה להרצה – קונפיגורציה

לפני השימוש במערכת, יש לבצע את ההכנות הבאות:

### 1. העלאת קבצי המערכת

מכיוון ש־GitHub לא תומך בקבצים מעל 25MB, יש להוריד את הקבצים הבאים מ־Google Drive ולהעלות אותם ל־Colab:

- 📄 [לחצי כאן להורדת קובץ הנתונים (adi_halel1.csv)](https://drive.google.com/file/d/1zfkW52oCCVC8TuC51i695-cz-CWPZctJ/view?usp=sharing)
- 🧠 [לחצי כאן להורדת המודל המאומן (movie_success_model.joblib)](https://drive.google.com/file/d/1fFErmme9JxUnoFeT1V4hNMOlpPOPB7Of/view?usp=sharing)

כמו כן, יש להעלות את כל קבצי המקודדים בפורמט `.pkl`.

---

### 2. יצירת תיקיות דרושות

```python
!mkdir -p templates
!mkdir -p models
```

---

### 3. הגדרת טוקן של Ngrok לצורך הפעלת השרת

```python
from pyngrok import ngrok
ngrok.set_auth_token("2v0a9ia4ml7K2VFmRpaY8UJ9kJ2_7zXk9LvhX2jdRFLgrV9q2")
```

---

### 4. תוצאה לאחר הרצה

לאחר הרצת הקוד, תתקבל כתובת זמנית של Ngrok – זו תהיה הכתובת של האתר שלך.  
בנוסף, יווצר קובץ QR שיוצג באתר ומאפשר סריקה וגישה נוחה דרך מכשירים ניידים.

---

📌 **הערה:**  
הממשק אינו פעיל תמיד – בכל פתיחה מחדש של המחברת יש להעלות את הקבצים ולהריץ מחדש את הקוד.

