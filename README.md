# Research Hub v1.1

Research Hub keeps the tasks and reports for all your research projects in one place, on your computer and your phone.

It doesn't have its own server or account. Everything is saved as plain files in **your own Dropbox**, and the apps simply read and write those files. Nothing is sent anywhere else.

**Website:** [hpellegrina.github.io/research-hub](https://hpellegrina.github.io/research-hub/). Download it for your computer there, and open the phone app at [hpellegrina.github.io/research-hub/app](https://hpellegrina.github.io/research-hub/app/).

---

## What you can do

- **Tasks per project:** add tasks, tick them off, archive or delete them.
- **Reports per project:** see every PDF for a project, newest first, and open one with a click or tap.
- **Read or unread:** mark reports as read. Each project shows how many tasks are open and how many reports are unread.
- **Archive:** move tasks and reports you're finished with out of the way, and restore them any time.
- **Recent PDFs (phone):** the newest reports from all projects in one list, with search and an "Unread" filter.
- **Manage projects (computer):** add, rename, renumber and remove projects.
- **Shared folders stay as they are:** your reports stay in the folders you already use, such as folders shared with coauthors. The hub only shows them; it never moves, copies or changes them.
- **Private:** your tasks, read marks and archive are saved in *your* `research_hub` folder, which nobody else sees.

---

## How it works

```
Dropbox/
├── research_hub/                  ← your hub (private to you)
│   ├── tracker/                   the app for your computer
│   ├── projects/
│   │   └── 1. Example project/
│   │       ├── TASKS.md           tasks: To do, Completed, Archived
│   │       ├── REPORTS.txt        first line: where this project's PDFs are
│   │       ├── READ_REPORTS.txt   reports you've marked as read
│   │       └── ARCHIVED_REPORTS.txt
│   ├── removed_projects/          projects you removed (nothing is deleted)
│   └── README.md                  this guide
│
└── some_shared_folder/
    └── reports/                   ← the PDFs, wherever they already are
```

- **Projects:** each folder in `research_hub/projects` is a project.
- **Reports:** a project's PDFs are in the Dropbox folder named on the first line of its `REPORTS.txt`, for example `some_shared_folder/reports`. If there's no `REPORTS.txt`, the hub uses a `reports` folder inside the project instead.
- **Plain text:** all the files are plain text, so you can also read or edit them in the Dropbox app.
- **Sync:** because everything is in Dropbox, the computer and phone apps stay in sync automatically.

---

## Setting up on your computer (about 5 minutes)

1. **Download** the zip from [hpellegrina.github.io/research-hub](https://hpellegrina.github.io/research-hub/) (the **Download for Mac or Windows** button) and double-click it to unzip. You get a folder called `research_hub`.
2. **Move it to the top level of your Dropbox**, so it's `Dropbox/research_hub`. The phone app looks for it exactly there.
3. **Open the hub:**
   - **Mac:** open `research_hub/tracker` and double-click **Research Hub**. You can drag it to your Dock for one-click access.
     The first time, your Mac may say it can't check the app. Open **System Settings › Privacy & Security**, scroll down and click **Open Anyway**.
   - **Windows:** double-click `Open Research Hub (Windows).bat` in the same folder.
4. **Your browser opens the hub.** You're done. The hub runs quietly in the background and stops by itself a few minutes after you close the page.

**You need Python 3.** A Mac offers to install it the first time it's needed; say yes. On Windows, install it from [python.org](https://www.python.org/downloads/) and tick **"Add Python to PATH"**.

---

## Setting up on your phone (about 5 minutes)

1. **Open the app:** on your phone, go to [hpellegrina.github.io/research-hub/app](https://hpellegrina.github.io/research-hub/app/). You can also open [the website](https://hpellegrina.github.io/research-hub/) and tap **Open the phone app**.
2. **Add it to your home screen:**
   - **iPhone:** in **Safari**, tap Share › **Add to Home Screen**.
   - **Android:** in **Chrome**, tap ⋮ › **Add to Home screen**.
3. **Open it from the icon:** open Research Hub **from the new home-screen icon**, not from the browser. On iPhone the icon keeps its own login, so the next step must happen there.
4. **Connect Dropbox:**
   1. Paste a Dropbox app key (see below) and tap **Continue**.
   2. Tap **Open Dropbox** and allow access.
   3. Dropbox shows a code. Copy it, go back to the app, paste it, and tap **Finish**.

You stay connected after this.

### Getting a Dropbox app key

The key lets the phone app open *your* Dropbox after you sign in. It doesn't give anyone else access to your files. There are two ways to get one:

- **Easiest:** ask the person who shared Research Hub with you for their key.
- **Or make your own** (on a computer):
  1. Go to [dropbox.com/developers/apps](https://www.dropbox.com/developers/apps) and click **Create app**.
  2. Choose **Scoped access** and **Full Dropbox**. Name it anything unique, for example `research-hub-yourname`.
  3. On the **Permissions** tab, tick `files.metadata.read`, `files.content.read` and `files.content.write`, then click **Submit**.
  4. On the **Settings** tab, copy the **App key**. Leave "Allow public clients" set to Allow. You don't need a redirect URI.

---

## Everyday use

### On your computer

| To… | Do this |
|---|---|
| Add a project | Click **+ Add project** in the sidebar. Type a name and click **Choose folder…** to pick the Dropbox folder with its PDFs. You can leave the folder empty to use the project's own `reports` folder. |
| Rename a project | Click **Rename** next to the project's title. |
| Fix the numbering | If your projects are numbered (1., 2., 3.…) and there are gaps, click **Renumber 1, 2, 3…** in the sidebar. It shows the changes before doing anything. |
| Remove a project | Click **Remove project…** at the bottom of its page. Nothing is deleted: it moves to `research_hub/removed_projects`. To bring it back, move its folder back into `projects`. |
| Add a task | Type it in the box at the top of the project and press Enter. |
| Finish a task | Click the circle next to it. It moves to **Completed** with today's date. |
| Archive or delete a task | Hover over the task and click the box icon (archive) or **×** (delete). |
| Read a report | Click its name. It opens in a new browser tab. |
| Mark as read | Click **Mark read** next to the report. It changes to **✓ Read**; click again to undo. Use **Mark all as read** to clear a project in one go. |
| Archive a report | Click the box icon next to it. The PDF itself isn't touched. |
| See or restore archived items | Open **Archive** at the bottom of the project and click **Restore**. |

### On your phone

- **Projects:** each project shows its open tasks and unread reports. Tap one to see its tasks and reports.
- **Recent PDFs:** the newest reports from all projects, with a search box. Tap **Unread** to see only what you haven't read.
- **Reading:** tap a report to read it. On iPhone it opens on top of the app; tap **Done** to come back.
- **Editing:** tasks, read marks and archive work just like on the computer, and changes show up there too.
- **Refreshing:** tap the ↻ button at the top to reload from Dropbox.

To add, rename or remove projects, use the computer.

---

## Working with coauthors

- **Everyone has their own hub.** Your coauthor installs Research Hub in their own Dropbox and gets their own projects, tasks and read marks. You don't see each other's.
- **You can point to the same shared folder.** If you both have access to a shared Dropbox folder with the project's PDFs, each of you can add a project that points to it. You'll both see the same reports, each with your own read marks and tasks.
- **The folder path may differ.** A shared folder can sit in a different place in each person's Dropbox. Always use **Choose folder…** on your own computer rather than copying someone else's `REPORTS.txt`.
- **Shared folders are never modified.** Research Hub only writes inside your own `research_hub` folder.

---

## Troubleshooting

**A project shows no reports.**
Its `REPORTS.txt` probably points to a folder that doesn't exist, for example `.../reports` when the folder is actually called `.../reports_hub`. On your computer, open `research_hub/projects/<project>/REPORTS.txt` and correct the first line: it's the folder's path inside Dropbox. Or remove the project and add it again with **Choose folder…**.

**The Mac keeps blocking the app.**
Open Terminal and run `xattr -dr com.apple.quarantine ~/Dropbox/research_hub`, then try again. This only removes the "downloaded from the internet" flag from this folder.

**A Terminal window stays open on the Mac.**
This is harmless, and you can close it. To have it close by itself, go to Terminal › Settings › Profiles › Shell › "When the shell exits" and choose *Close if the shell exited cleanly*.

**The hub page says "The tracker isn't running".**
It stops by itself a few minutes after you close the page. Double-click **Research Hub** again.

**The phone says the code didn't work.**
Tap **Open Dropbox** again and paste the *new* code it shows. Each code can be used only once.

**The phone says something "was changed on another device".**
You edited the same list on your computer and phone at nearly the same time. The app reloads the latest version; just make your change again. Nothing is overwritten.

**A report opens as a download instead of in the viewer.**
Open it from your phone's Downloads, or tell whoever shared the app with you.

---

## Versions

- **v1.1** (September 2026): rename projects; renumber projects when numbers have gaps.
- **v1.0** (September 2026): first release. Tasks, reports, read marks and archive on computer and phone; add and remove projects from the computer app.
