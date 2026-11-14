# holdpays-timer

Calls https://holdpays-clone.vercel.app/api/tick every minute with GitHub Actions. That drives Hold's payouts and the payouts of every coin launched on its launchpad.

- `.github/workflows/tick.yml`: starts every 5 minutes, and each run calls the URL once a minute for 15 minutes. A new run replaces the old one.
- `.github/workflows/keepalive.yml`: makes a commit on the 1st of each month, so GitHub doesn't pause the schedule.

This repo is public so the Actions minutes are free. It contains only the public site URL.

To stop the timer, open **Actions → tick → ⋯ → Disable workflow**.
