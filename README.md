```mermaid
gantt
    title Cron windows vs. a late-available submission
    dateFormat HH:mm
    axisFormat %H:%M

    section Cron runs (query last 15 min)
    Run @10:10  → covers 09:55–10:10   :w1, 09:55, 10:10
    Run @10:20  → covers 10:05–10:20   :w2, 10:05, 10:20
    Run @10:30  → covers 10:15–10:30   :w3, 10:15, 10:30

    section Submission (stamped 10:01)
    Stamped 10:01                       :milestone, s1, 10:01, 0m
    Not yet returned by Fillout API     :crit, gap, 10:01, 16m
    Becomes visible 10:17               :milestone, s2, 10:17, 0m
```
