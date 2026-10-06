**A. Benefits**

A1. **Composable.** Small tools chain through pipes, so `grep ERROR app.log | sort | uniq -c | sort -rn` builds a frequency report from four tools that know nothing about each other.

A2. **Scriptable and repeatable.** Any command you type can go in a script, a cron job or a CI pipeline. The steps can be rerun, put under version control and reviewed, which GUI clicks can't.

A3. **Fast for people who know it.** Keyboard only, tab completion, history search (Ctrl-R), globbing like `mv *.jpg photos/`, and one command that acts on thousands of files.

A4. **Light on resources.** It works over SSH on slow links, on headless servers and inside containers, and needs almost no memory or display.

A5. **Precise and visible.** The command is the exact record of what happened. You can paste it into a doc, a ticket or a chat, and someone else can run the same thing.

A6. **Stable over time.** Core tools (`ls`, `grep`, `awk`, `ssh`) have behaved much the same for decades, so the skills last while GUIs get redesigned.

A7. **Reaches everything.** Many tools, flags and config options exist only as commands: package managers, git plumbing, cloud CLIs, `ffmpeg`.

A8. **Easy to automate, including by AI agents.** Text in and text out is the easiest interface for another program, or an LLM, to drive and check.

**B. Downsides**

B1. **Steep learning curve, little to discover.** A blank prompt gives no hint of what's possible. You have to already know the command name and its flags, or go read `man` pages.

B2. **Unforgiving.** There is often no undo and no "are you sure?" prompt: `rm -rf`, `>` overwriting a file, `dd` to the wrong disk. One typo can do real damage.

B3. **Inconsistent.** Flags differ between tools (`-v` means verbose in one and version in another). GNU and BSD versions differ (`sed -i` on Linux vs macOS). Shells differ too (bash vs zsh vs fish vs PowerShell).

B4. **Fragile text parsing.** Pipelines that scrape human-readable output break on spaces in filenames, on locale changes, or when the output format changes. Quoting and escaping rules confuse people.

B5. **Poor fit for visual or spatial work.** Image editing, layout, and browsing or comparing rich data are slower or impossible as text.

B6. **Hard to remember.** Rarely used incantations (`tar`, `find -exec`, `awk`) send people back to search engines or cheat sheets.

B7. **Security risks.** `curl | sh` installs, secrets left in shell history, and commands pasted from untrusted sources all run with your full permissions.

B8. **Barrier to access and adoption.** Non-technical users find it intimidating, and screen readers handle dense or colored terminal output unevenly.

**Bottom line:** the command line pays off for repeated, automated, remote or bulk work. It costs the most for occasional users and for visual tasks. Many people use both: a GUI to explore and the CLI to repeat and automate.
