# אלוף בגמרא

משחק שאלות על מילים בארמית מהגמרא. האתר הוא קובץ אחד (`index.html`) עם אייקון.

## העלאה לאינטרנט

**GitHub Pages:** פותחים מאגר ציבורי בשם `aluf-bagemara`, מעלים אליו את כל הקבצים שבתיקייה, ואז Settings → Pages → Branch: `main` → Save. הקישור: `https://<שם-המשתמש>.github.io/aluf-bagemara`.

**Netlify (בלי חשבון GitHub):** נכנסים ל-https://app.netlify.com/drop וגוררים את התיקייה.

## טבלת אלופים משותפת ומשחק בכמה טלפונים

בלי Firebase המשחק הרגיל ופינג פונג עובדים, והשיאים נשמרים בכל מכשיר בנפרד.
כדי שהשיאים יהיו משותפים לכולם ושיעבוד "כל אחד בטלפון שלו":

1. ב-https://console.firebase.google.com פותחים פרויקט, ואז Build → Firestore Database → Create database.
2. בלשונית Rules מדביקים את התוכן של `firestore.rules` ולוחצים Publish.
3. בדף הפרויקט לוחצים על `</>`, רושמים אפליקציה, ומעתיקים את מה שבתוך `firebaseConfig = { ... }`.
4. ב-`index.html` מחליפים את `const FIREBASE_CONFIG = null;` ב-`const FIREBASE_CONFIG = { ... };` עם הפרטים.

## עריכת המילים

המילים נמצאות ב-`index.html` אחרי `const R=`, שורה לכל מילה: `מילה|פירוש|שלב|סוג`.
