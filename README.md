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
!pip install qrcode[pil]```
⚙️ התאמת סביבת העבודה להרצה – קונפיגורציה
לפני השימוש במערכת, יש לבצע את ההכנות הבאות:

העלאת כל קבצי המערכת ל-Colab, כולל:

קובץ המודל movie_success_model.joblib

קובץ הנתונים adi_halel1.csv

קבצי המקודדים *.pkl (לשחקנים, שפות, ז'אנרים, במאים וכו')

יצירת תיקיות דרושות:
```!mkdir -p templates
!mkdir -p models```
הגדרת טוקן של Ngrok לצורך הפעלת השרת:
```from pyngrok import ngrok
ngrok.set_auth_token("2v0a9ia4ml7K2VFmRpaY8UJ9kJ2_7zXk9LvhX2jdRFLgrV9q2")```
לאחר הרצת הקוד, תתקבל כתובת Ngrok זמנית – זו הכתובת של האתר שלך.
בנוסף יווצר קובץ QR בתוך האתר המוביל לאותה כתובת,  בשביל ניידים וכדומה.
📌 הערה: הממשק אינו פעיל תמיד – בכל פתיחה מחדש של המחברת יש להעלות את הקבצים ולהריץ שוב את הקוד.
