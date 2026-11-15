# SMAI Discord AI Bot

בוט דיסקורד חכם מבוסס Gemini שרץ 24/7 בענן ושומר על פרטיות מלאה (ללא חשיפת שם או גיל).

## שלב 1: יצירת בוט בדיסקורד
1. היכנסו אל [Discord Developer Portal](https://discord.com/developers/applications) ולחצו **New Application**.
2. עברו ללשונית **Bot** בצד שמאל:
   - לחצו **Reset Token** והעתיקו את ה-Token.
   - גללו למטה ל-**Privileged Gateway Intents** והפעילו את **Message Content Intent**.
3. עברו ללשונית **OAuth2 -> URL Generator**:
   - סמנו `bot`
   - ב-Bot Permissions סמנו: `Send Messages`, `Read Message History`, `View Channels`.
   - פתחו את הקישור שנוצר והוסיפו את הבוט לשרת שלכם (או שידברו איתו ישירות ב-DM).

## שלב 2: העלאה לענן (רץ גם כשהמחשב כבוי)
### אפשרות מומלצת: Railway / Render
1. העלו את התיקייה ל-GitHub (או חברו ישירות ל-Railway).
2. הגדירו שני משתני סביבה (Environment Variables):
   - `DISCORD_BOT_TOKEN` — הטוקן של הבוט מ-Discord.
   - `GEMINI_API_KEY` — מפתח ה-API שלכם מ-Google AI Studio.
3. הפעילו את השירות כ-**Worker** (`python bot.py` — מוגדר כבר ב-`Procfile`).
