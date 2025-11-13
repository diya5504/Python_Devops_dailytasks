# Python_Devops_dailytasks
# Automation & Scripting

Purpose
- Central place for small automation and scripting tasks used to automate repetitive DevOps tasks (log rotation/cleanup, backups, deployments, health checks, etc.).

Getting started
1. Choose an environment (Linux/macOS/containers). These scripts target a POSIX-compatible environment by default.
2. Install Python 3.8+ if not already present.
3. (Optional) create a virtual environment:
   python -m venv .venv
   source .venv/bin/activate
4. Install dependencies:
   pip install -r requirements.txt

Examples
- Cleanup old log files:
  python scripts/log_cleanup.py --path /var/log/myapp --days 30 --action compress

Script conventions
- All scripts accept `--dry-run` so you can preview changes without modifying files.
- Logging is written to stdout and includes timestamps.
- Scripts favor safe defaults (no destructive actions without explicit flags).

Contributing
- Add new scripts into the `scripts/` folder.
- Include tests where practical and add simple usage examples in the README or script docstrings.
- Open a PR against `main` or the repo's default branch.

If you'd like, I can add GitHub Actions to run linters and tests on submit.
