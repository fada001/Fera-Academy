# Fera Language Academy website

Files
- index.html          the whole website (English + Dari)
- vercel.json         security headers for Vercel
- favicon.png, robots.txt
- backend/Code.gs     the secure registration backend (runs free in YOUR Google account)

## 1. Connect the registration system (5 minutes)
1. Create a new Google Sheet (name it "Fera Students").
2. Extensions > Apps Script. Delete the sample code, paste all of backend/Code.gs, Save.
3. Deploy > New deployment > gear icon > Web app.
   Execute as: Me. Who has access: Anyone. Deploy and approve the permissions
   (Google shows "not verified" because it is your own script: Advanced > continue).
4. Copy the link that ends in /exec.
5. Open index.html, find `endpoint: ''` near the top and paste the link between the quotes.
   Also fill telegramChannel / telegramContact / instagram / facebook if you have them.

## 2. Put it online with Vercel (free)
Option A (easiest): upload this folder to a new GitHub repository, then in Vercel choose
"Add New > Project", import the repository and press Deploy. No settings are needed.
Option B: install Node.js, open a terminal in this folder and run `npx vercel`, then `npx vercel --prod`.
You receive a free address like fera-academy.vercel.app. Share https://YOUR-ADDRESS/?lang=fa
to open the Dari version directly.

## 3. Test before announcing
Submit one test application yourself. You should get two emails (the application and the
result) in the academy inbox and see rows in the sheet tabs "Applications" and "Results".
If you change the Apps Script code later: Deploy > Manage deployments > edit > New version.

## Changing prices, lengths, contacts
Everything is in the settings block at the top of index.html (monthly fee and months for every course).
The email address that receives results is ADMIN_EMAIL at the top of backend/Code.gs.
Test questions: the question text is in index.html, the correct answers only in backend/Code.gs.
Change both together.
