INTRODUCTION TO OPEN SOURCE  |  WEEK 3, CLASS 2
Pull Request Practice Lab
Student Handout
Name	 azizzbek
GitHub username	 
Exercise number	 
Class repository URL	 
My review partner (exercise number + 1)	 

Objective
Today you will join the workflow of a real software team. You will make a small, safe contribution to a shared repository and go through the same steps that professional developers and open-source contributors use every day:
Fork → Clone → Branch → Edit → Commit → Push → Pull Request → Review → Merge
By the end you will have opened a Pull Request with a professional description, reviewed a classmate's Pull Request, and responded to feedback. You do not need advanced programming: your contribution is a documentation improvement.
Prerequisites
•	Git installed and working (test with git --version).
•	A GitHub account, and Git able to push to it (you did this in Week 2). Authentication must already work; if you are unsure, tell your professor now.
•	A text editor (VS Code, Notepad++, or any editor you like). Turn off 'format on save' for today so it does not change unrelated lines.
•	A terminal (Git Bash, Terminal, or your IDE's terminal).
•	Your exercise number from your professor. Wherever you see NN in this handout, replace it with your number (for example 07).
Time plan (30 minutes for the lab)
By minute 30: forked and cloned.   By minute 40: edited, committed, and pushed.   By minute 50: Pull Request open with a good description.   By minute 55: PR link posted in the class channel, ready to review.
 
The big picture
Git tracks my work. GitHub helps people collaborate around that work. Today you use both: Git on your computer, GitHub in your browser.
#	Step	Where	What it does
1	Fork	GitHub (browser)	Makes your own copy of the class repository under your account.
2	Clone	Your computer	Downloads YOUR fork so you can work on it.
3	Branch	Your computer	Creates a separate line of work for your change.
4	Edit	Your computer	You improve one documentation file.
5	Commit	Your computer	Saves a snapshot with a clear message.
6	Push	Your computer to GitHub	Sends your branch to your fork.
7	Pull Request	GitHub (browser)	Asks the maintainers to review and consider your change.
8	Review	GitHub (browser)	A classmate reads your PR and comments; you review theirs.
9	Merge / close	GitHub (browser)	A maintainer decides. Today that is your professor.

Three repositories, one name
Name	What it is	Address looks like
Upstream (the class repo)	The original, owned by the course. You cannot push to it.	github.com/COURSE/week3-pr-lab
Origin (your fork)	Your own copy on GitHub. You CAN push here.	github.com/YOUR-USERNAME/week3-pr-lab
Your local clone	The copy on your computer, cloned from your fork.	A folder named week3-pr-lab

Safe habits
Run git status whenever you are unsure. It tells you the branch and what changed.
Add files by name (git add docs/lab/exercise-NN.md), never git add . today.
Never use git push --force or git reset --hard. If something looks wrong, ask for help.
Never edit or commit on main. Always work on your branch.
 
Part A: Make your contribution
Step 1: Open the class repository
1.	Go to the class repository URL (on the board and in the class channel).
2.	Read the README and CONTRIBUTING.md. Two minutes is enough.
3.	Open docs/lab/ and find your file: exercise-NN.md. Read it and notice what could be improved.
Step 2: Fork the repository
1.	Click Fork (top right of the repository page).
2.	Owner: your account. Repository name: keep the default.
3.	Click Create fork.
Check
The address bar now shows YOUR-USERNAME/week3-pr-lab, and under the title it says 'forked from COURSE/week3-pr-lab'.
Step 3: Clone YOUR fork
1.	On your fork, click the green Code button, choose HTTPS, and copy the URL.
2.	In your terminal, move to the folder where you keep projects, then run:
git clone https://github.com/YOUR-USERNAME/week3-pr-lab.git
cd week3-pr-lab
git remote -v
Check
git remote -v shows origin with YOUR username in the URL (both fetch and push). If you see the course name, you cloned the original. Delete the folder and clone again from your fork.
Step 4: Create a branch
git switch -c docs/improve-ex-NN
git status
The -c means 'create'. If your Git is older and git switch is not recognized, the equivalent is git checkout -b docs/improve-ex-NN.
Check
git status says: On branch docs/improve-ex-NN. If it says main, stop and run the switch command again.
Step 5: Make ONE useful documentation improvement
Open docs/lab/exercise-NN.md in your editor. Choose one of these (or several, if they belong together in one small change):
•	Fix a typo (there are at least two).
•	Fix the broken documentation link.
•	Fix a formatting slip (for example a heading missing a space).
•	Add a short useful example, such as this under Step 3:
    git config --global user.name "Your Name"
    git config --global user.email "you@example.com"
Save the file, then check exactly what you changed:
git diff
Check
git diff shows only the lines you meant to change, in only one file.
Step 6: Commit the change
git add docs/lab/exercise-NN.md
git status
git commit -m "Fix typos in exercise NN"
A good commit message is verb + what + where. Examples: 'Fix broken link in exercise NN', 'Add git config example to exercise NN'. Avoid 'update', 'fix', or 'asdf'.
Step 7: Push your branch
git push -u origin docs/improve-ex-NN
Check
The terminal shows your branch being created on the remote. On GitHub (your fork) you see a yellow banner: 'Compare & pull request'.
Step 8: Open a Pull Request
1.	On your fork, click Compare & pull request.
2.	Check the direction (this is the most misread part of the screen): base repository = the CLASS repo, base = main. head repository = YOUR fork, compare = your branch.
3.	Write a clear title, for example: Docs: fix typos in exercise NN.
Watch out
If the base repository is your own fork, you are about to open a PR to yourself. Click the 'base repository' dropdown and choose the class repository.
Step 9: Write a professional description
Fill in the template that GitHub pre-loads. Be specific and honest. 'N/A' is fine for screenshots if there is nothing to show.
Template heading	What to write	Example
What did you change?	One or two sentences.	Fixed two typos and a broken link in the setup steps of exercise 07.
Why did you change it?	What problem does it fix?	The typo 'instal' made the command hard to copy, and the link led to a 404 page.
How did you test it?	How do you know it works?	Previewed the Markdown on GitHub and clicked the corrected link.
Screenshots (if applicable)	Before and after, if useful.	N/A (text-only change).

Click Create pull request. Copy the link from your address bar and post it in the class channel.
Copy-and-fill template
## What did you change?
 
## Why did you change it?
 
## How did you test it?
 
## Screenshots (if applicable)
 
Part B: Review a classmate's Pull Request
Your partner is the student with the next exercise number after yours (the last student reviews the first). Find their link in the class channel, or open the class repository's Pull requests tab.
How to leave a review
1.	Open your partner's Pull Request.
2.	Click the Files changed tab.
3.	Hover over a line you want to comment on and click the blue +.
4.	Write a kind, specific comment and click Start a review.
5.	Click Review changes (top right), choose Comment, Approve, or Request changes, and click Submit review.
Peer review checklist
	Question	Notes
☐	Is the PR title clear?	
☐	Is the description understandable (what, why, how tested)?	
☐	Is the change focused (one purpose, one file)?	
☐	Is the change useful and correct?	
☐	Is anything unclear?	
☐	Is there anything that should be improved?	
☐	Is the contributor respectful and professional?	

Write comments that help
Instead of	Try
"Looks good."	"Nice catch on the broken link. The corrected URL works for me."
"Wrong."	"Could we double-check this spelling? I think it should be 'account'."
"Why did you do this?"	"I'm not sure I follow the reason for this change. Could you explain it in the description?"
"Too small to matter."	"Thanks for keeping this focused. Could you also add a short example under Step 3?"

Your review comment (write it here, then post it on GitHub)
 
 
 

Requirement: leave at least ONE constructive comment (specific, kind, and actionable) and submit the review. Critique the work, not the person.
Part C: Respond to feedback
1.	Read every comment on your PR. Breathe: feedback is normal, and helpful.
2.	Reply to each comment. 'Thanks, done!' is a fine reply. If you disagree, ask politely and give your reason.
3.	Make the change in your editor, then:
git add docs/lab/exercise-NN.md
git commit -m "Address review: clarify step 2"
git push
1.	Refresh the PR. The new commit appears automatically. Do not open a new PR.
2.	Click Resolve conversation on comments you have addressed.
If your reviewer only left praise, improve one small thing (for example the PR description) and reply with what you changed.
What can happen to a Pull Request
Outcome	What it means	What you do
Merged (purple badge)	The maintainer accepted your change; it is now part of the project.	Celebrate. Then update your fork's main if you want to continue.
Changes requested	A good idea, but something needs to change first.	Fix it on the same branch and push. The PR updates.
Closed without merging	Not accepted (duplicate, out of scope, or not now). Not a personal failure.	Read the maintainer's reason; learn; try again or pick another issue.
 
Command cheat sheet
Command	What it does
git clone <url>	Download a repository (use YOUR fork's URL).
git remote -v	Show which repository origin points to.
git switch -c <branch>	Create a new branch and switch to it (older: git checkout -b).
git status	Show the current branch and what changed.
git diff	Show exactly what you changed.
git add <file>	Stage a specific file for commit.
git commit -m "message"	Save a snapshot with a message.
git push -u origin <branch>	Send your branch to your fork (first time).
git push	Send new commits on the same branch.
git pull	Bring remote changes to your computer.
git branch	List your branches; the current one has an asterisk.

Troubleshooting
Every fix below is safe. If it does not work, ask for help before trying anything else.
"Permission denied" or 403
What it usually means: GitHub does not recognize you, or you do not have write access to that repository.
•	Run git remote -v. Is your username in the URL? If not, you are pushing to the original: re-clone your fork.
•	If it IS your fork, the problem is login (see 'GitHub authentication problem').
"Repository not found"
What it usually means: The URL is wrong, the repository is private to someone else, or you are logged in as the wrong account.
•	Copy the URL again from the green Code button of YOUR fork.
•	Check the spelling of your username and repository name.
•	Confirm you finished forking (your fork appears under your own profile).
Wrong remote
What it usually means: origin points to the class repository or to a classmate's fork.
•	git remote -v to inspect.
•	git remote set-url origin https://github.com/YOUR-USERNAME/week3-pr-lab.git to correct it (safe).
•	Or delete the folder and clone your fork again if nothing important was done.
Wrong branch
What it usually means: You are on main, or you edited before switching.
•	git branch shows the current branch with an asterisk.
•	Not committed yet: git switch -c docs/your-branch keeps your edits.
•	Already committed on main: stop and ask your instructor; do not use reset --hard.
Push rejected
What it usually means: The remote has commits you do not have, or the branch has no upstream yet.
•	'no upstream branch': git push -u origin your-branch.
•	'fetch first' or 'non-fast-forward': git pull, resolve anything Git reports, then git push.
•	Do not use --force.
Merge conflict
What it usually means: Two changes touched the same lines and Git needs a human decision.
•	git status lists the conflicted files.
•	Open the file. Find <<<<<<<, =======, >>>>>>> markers. Keep the text that is right and delete the markers.
•	git add the file, then git commit. To back out safely: git merge --abort.
GitHub authentication problem
What it usually means: GitHub no longer accepts your account password for Git over HTTPS.
•	Use one of: GitHub CLI (gh auth login), Git Credential Manager, a personal access token as the password, or an SSH key you added to GitHub.
•	Fallback for the lab: edit on GitHub in the browser (pencil icon on your fork), choose 'Create a new branch', and open the PR from there.
PR shows unexpected files
What it usually means: Unrelated files were committed, or the PR compares the wrong branches.
•	Open the Files changed tab and list what should not be there.
•	Locally: git status and git log --oneline to see what you committed.
•	An extra file: git rm --cached <file>, commit, push. The PR updates automatically. Ask for help if unsure.
Branch not appearing on GitHub
What it usually means: You committed locally but did not push, or you are looking at the wrong repository.
•	git push -u origin your-branch.
•	On GitHub, make sure you are on YOUR fork (username in the address), then open the branch dropdown.
•	git branch -a lists local and remote branches.
 
Submission requirements
Submit the following through the course page (or as your professor directs) by the deadline:
	Item	Done?
1	Link to YOUR Pull Request in the class repository.	☐
2	A screenshot of the PR page showing the title, description, and Files changed count.	☐
3	The link to (or text of) your review comment on your partner's PR.	☐
4	Evidence that you responded to feedback (a reply or a pushed commit), if you received any.	☐
5	Your reflection (below).	☐

How this lab is graded
Criterion	Excellent (4)	Developing (2 to 3)	Needs improvement (0 to 1)
Branch	Created a correctly named, purpose-built branch and never committed to main.	Used a branch but the name is vague, or one commit landed on main.	Worked directly on main or no separate branch.
Commit	One or more small commits with clear messages (verb + what + where).	Commit works but the message is vague (for example 'update docs').	No commit, or messages like 'asdf'.
PR description	Template fully completed: what, why, how tested; specific and honest.	Template partly completed; some parts vague.	Empty, missing, or 'fixed stuff'.
Change quality	Small, focused, correct, useful documentation improvement with no unrelated files.	Change is valid but trivial, slightly unfocused, or has a small side effect.	Incorrect, unrelated files included, or no real improvement.
Code review	At least one specific, kind, actionable comment that references the checklist; submitted as a review.	A comment exists but it is generic ('looks good') or lacks a suggestion.	No review, or the comment is dismissive.
Professional communication	Polite, clear, responds to feedback with thanks and a pushed update or a reasoned reply.	Polite but does not respond fully to feedback.	Rude, defensive, or ignores feedback.
Total: 24 points. Grading is about process and professionalism, not perfection.
Reflection
In 3 to 5 sentences: What did you learn about contributing to a project that you didn't create? What surprised you? What will you do differently next time?
 
 
 
 

Before you leave
Your PR link is posted. You left a review comment. You know what happened to your PR (open, merged, changes requested, or closed). You know your homework.


