# meetings
All meetings have 15m presentations, followed by an activity. We want to
wrap these up in a packaged format so we can publish them, get cred for the
club, and reuse them in future years.

Every folder at top-level is a meeting and is named for the meeting.

Every meeting folder contains the following:
* Markdown file formatted with a markdown header.
	* title: 
	* slides: \<link to slides hosted on Google Docs\>
	* link-to-assets-in-github:
		* Get access to this repository. 
		* Create a folder titled after the meeting you are boxing.
		* Add the files needed for this meeting. Try to avoid stuff in
		excess of 10mb (host it elsewhere).
	* list-of-topics: Summarize the slides into the major bullet points.
	Try to keep it to three.
	* Once you complete this file, send it to the
	website admin, currently @Flyrom / Trevor.

---

#### We want to package every meeting.
They'll come with the following:
 * Link to slides (hosted on Google Docs)
 * Meeting files

To package them, you must collect the following:
 * ~~Link to slides~~
 * ~~Files~~ (you already have these two)
 * Deploy instructions (how to run on your computer)
 * List of topics covered (eg printf vulnerabilities, Coppersmith's attack)
 * Goal (eg "get shell on remote computer")

#### Meetings come in one of five formats
Get all files from the presenter.

They'll have **additional** components depending on the meeting type.
 * pwn - libc.so.X (where X is a number, usu. 6), LD_PRELOAD command
 * reversing - nothing
 * crypto - 
 * web - Dockerfile

---

### Jekyll Details (don't read unless you're website admin)

* New packaged meetings (`meeting_name.md`) go into `_meetings` dir, copy
`EXAMPLE.md` and set jekyll front matter appropriately
* meeting formatting is handled by `_includes/single-meeting.html`
* Use `layout: meeting`. Meetings use a [jekyll layout](https://jekyllrb.com/docs/layouts/).
* meetings are a jekyll
"[collection](https://jekyllrb.com/docs/collections/)", if you need more
info about how they actually work / need to do design work.
