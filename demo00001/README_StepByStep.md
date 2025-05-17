step by step guide to create my first angular app and connect it to git. i need angular 10.0.5. Please make sure not to commit any git files that are not necessary (git ignore) please assume i already have empty repostiry on git i cloned the empty repository i need to install everything for my angular i want that that same git repository will have many angular demo applications give me step by step tuturial assuming i an new to git and angular to install whatever i need for angular co create the project build run commit everything push in the end







Step-by-Step Guide (Using Angular 10.0.5) + Git Integration
🎯 Goal:
	• Use Angular 10.0.5
	• Avoid committing unnecessary files (like node_modules)
	• Push to a cloned empty Git repository
	• Support multiple Angular apps (e.g., demo1, demo2, etc.)

🔧 1. Install Node.js v12.22.12
Go to: https://nodejs.org
Download and install the LTS version (v14 recommended for Angular 10).
Check:
node -v
npm -v

📦 2. Install Angular CLI v10.0.5 (Globally)

npm install -g @angular/cli@10.0.5
Verify:

ng version
It should show Angular CLI 10.0.5

📁 3. Navigate to Your Cloned Git Repo

cd path/to/your/cloned/repo  
Example:

cd C:/Projects/angular-demos   (c:\Data\Repos\00004_LearnAngular)

🆕 4. Create Angular 10 App in a Subfolder
This ensures you can add more apps later (e.g., demo1, demo2):

ng new demo00001 --directory=demo00001
Choose:
	• ❌ No routing (unless needed)
	• ✅ CSS (or your preferred style)
Angular CLI will generate a .gitignore in demo1 that ignores node_modules, dist, etc.

✅ 5. Ensure .gitignore is Present and Correct
Check demo1/.gitignore includes:


/node_modules
/dist
/tmp
*.log
This ensures you won’t accidentally commit unnecessary files.

⚙️ 6. Build and Run the App

bash
cd demo00001
ng build
ng serve
Then open: http://localhost:4200

🧹 7. Prepare for Git Commit (on branch main)
Go back to repo root:

cd ..  (to the repo folder)

Check what will be committed:

git status
Make sure you don’t see node_modules or dist.
If all looks good:


git add .
Git status                     (see branch is main)
git commit -m " demo00001: creating Angular app (10.5.5)"
Git log --oneline
git push
Git status

Login to git -> open the repo -> see the commit on main branch

➕ 8. Add More Angular 10 Apps Later
You can repeat:

bash
ng new demo2 --directory=demo2
cd demo2
ng build
cd ..
git add .
git commit -m "Add demo2 Angular 10.0.5 app"
git push

note: 
to generate comonnet          cd to the directory and run: ng generate component <name>
