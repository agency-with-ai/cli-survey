**A. Benefits**

- A1. **Speed for repeated tasks.** One line like `rename 's/\.jpeg$/.jpg/' *.jpeg` or `rg TODO -l` does work that takes dozens of clicks in a GUI, and shell history lets you rerun or edit past commands.
- A2. **Composition.** Small tools pipe into each other (`cat log | grep ERROR | sort | uniq -c | sort -rn | head`). You can solve a new problem by combining tools you already know, with no new program needed.
- A3. **Automation and repeatability.** A command you typed once can go into a script, a cron job, a Makefile, or CI. A sequence of GUI clicks rarely can.
- A4. **Exact and recordable.** A command says exactly what will happen. You can paste it into docs, a ticket, or a chat, and someone else can run the same thing and get the same result.
- A5. **Remote and low-bandwidth work.** Over SSH you can run a headless server, a container, or a Raspberry Pi with almost no network overhead. Many servers have no GUI at all.
- A6. **Low resource use.** A terminal starts almost instantly, uses little memory, and keeps working on old or overloaded machines.
- A7. **Access to everything.** Many tools and options exist only on the CLI (git internals, ffmpeg flags, package managers, cloud SDKs). GUIs often wrap only a subset.
- A8. **Stability over time.** Core Unix commands (`ls`, `grep`, `find`, `ssh`) have worked the same way for decades, so what you learn keeps paying off.
- A9. **Works well with AI agents and tools.** Text in and text out is easy for scripts and LLM agents to read, generate, and check.

**B. Downsides**

- B1. **Steep learning curve.** Nothing on screen shows you what is possible. You have to already know that `find`, `awk`, or `xargs` exist and how to use their flags.
- B2. **Inconsistent syntax.** Flags differ between tools (`-r` vs `-R` vs `--recursive`), and GNU and BSD/macOS versions disagree (`sed -i`, `date`). Quoting and escaping rules trip up even experienced users.
- B3. **Unforgiving mistakes.** `rm -rf` on the wrong path, a misplaced `>` that truncates a file, or a bad glob can destroy data with no confirmation prompt and no trash can.
- B4. **Poor discoverability and feedback.** Many commands print nothing on success. Error messages can be cryptic, and man pages are written as references, not tutorials.
- B5. **Weak for visual or spatial tasks.** Image editing, layout, browsing unfamiliar data, and comparing rich documents are slower and clumsier in text.
- B6. **Fragile text parsing.** Pipelines that parse human-formatted output break when filenames contain spaces or newlines, or when a tool changes its output format.
- B7. **Platform differences.** Shell scripts written for bash on Linux often fail on macOS zsh, Windows PowerShell, or minimal containers.
- B8. **Security footguns.** Copying `curl ... | sh` from the web, leaving secrets in shell history, or shell injection through unquoted variables are easy mistakes.
- B9. **Accessibility and inclusion.** Beginners and non-developers often find it intimidating, which can shut them out of workflows the team builds only around the CLI.

**Bottom line:** the command line works best for repeatable, scriptable, remote, and text-based work. A GUI works better for visual tasks, one-off exploration, and newcomers. Most experienced users switch between the two depending on the task.
