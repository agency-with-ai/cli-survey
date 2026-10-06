A. Benefits

A1. Speed: typing `mv *.log archive/` takes less time than dragging files in a GUI, and the gap grows with the number of files.
A2. Composability: small tools chained with pipes (`grep | sort | uniq -c`) answer questions that no single app was built to answer.
A3. Automation: any command you type can go into a script, a cron job, or a CI pipeline unchanged, so a task done once can be repeated without extra work.
A4. Reproducibility: shell history and scripts record exactly what ran. That makes work easier to audit, share, and debug than a series of clicks.
A5. Remote access: SSH gives full control of servers, containers, and headless machines over a low-bandwidth link.
A6. Low resource cost: a terminal uses very little memory and CPU, and it runs on old hardware and minimal systems.
A7. Precision and power: flags expose options that GUIs hide, and many tools (git, ffmpeg, package managers) work best or only from the command line.
A8. Stability: core Unix commands have behaved the same way for decades, so the skills last.
A9. Text everywhere: plain-text input and output are easy to search, diff, log, and pass to other programs, including AI agents.

B. Downsides

B1. Steep learning curve: you have to recall commands instead of recognizing them on screen, and a blank prompt gives no hint of what is possible.
B2. Unforgiving errors: `rm -rf` with a typo, an unquoted variable, or the wrong working directory can destroy data with no undo and no confirmation.
B3. Inconsistent interfaces: flags differ between tools (`-r` vs `-R`) and between GNU and BSD versions. Error messages are often unclear.
B4. Poor fit for visual work: image editing, layout, charts, and browsing large structured data are easier with a GUI.
B5. Discoverability: man pages are dense, and finding the right tool for a job often means searching the web.
B6. Portability gaps: scripts that work in bash can break in zsh, sh, or PowerShell, and they fail on Windows without extra layers.
B7. Security risks: pasting commands from the internet (`curl ... | sh`) runs code you have not read, and secrets can leak into shell history.
B8. Accessibility: novices and some users with disabilities may find a text-only interface harder to use than a well-designed GUI.
B9. Fragile parsing: pipelines that scrape human-readable output break when that output changes format.
