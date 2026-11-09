# QA report
Method: the game script was executed headlessly in Node with a stubbed DOM/canvas (no real browser or phone available here).
## Passed (automated)
- Script syntax check.
- Save: 2 full simulated runs persist (runs, coins, best); reload restores progress, upgrades and settings; corrupt primary falls back to backup; both corrupt -> clean defaults without crash; v1 save migrates with out-of-range values clamped; junk fields sanitised; unavailable storage does not crash; retry keeps coins.
- Generator: 80 consecutive sections, no immediate pattern repeats, 3 mechanic intros fired in order, ~32 decor items/section, 0 overlapping gameplay objects (<30 px), draw routine ran without exceptions across 3,800 m of course.
- Mechanics: boost pad sets speed to 800 px/s; fast hit smashes a scrap pile and the run continues; slow hit hops without ending the run; mega spring apex 878 px vs 415 px.
- 60 random simulated runs: median 820 m, 90th percentile 2,773 m, max 7,674 m; no invalid positions.
## NOT verified (needs a real device/browser)
- Visual appearance of any screen, pixel-art look, menu centring, 16:9 layout, rotate prompt, tap-target comfort.
- Real touch input, audio output, performance/memory on phones, service-worker install/offline, Add-to-Home-Screen, tab-hide auto-pause behaviour.
- Menu buttons/sliders were not clicked; only underlying functions were exercised.
## Limits before a real release
- Browser localStorage only (cleared with site data, no cross-device sync). Not a native app. No achievements/missions exist, so none are saved.
- Needs hands-on playtesting for feel/balance, and HTTPS hosting for install + offline.

## Final pass (headless Node simulation, stubbed DOM - no real browser)
Passed:
- Variation: 60 new runs -> 60 unique seeds and 60 unique obstacle layouts in the first 5,000 px; first obstacle appears 937-2965 px; start flat 750-1190 px; 17 distinct mechanic-unlock schedules across 40 runs.
- 4,089 generated objects across 40 runs: 0 overlaps (<30 px). Draw routine ran without errors at a 648 px wide canvas over the whole generated course.
- Same cannon setting (45 deg / 100%) x50 runs: 26 m to 2,010 m (median 605, IQR 340-809) - no single reliable result. Holding right in flight raised the median to 1,517 m, so skill clearly matters. Power matters (40%: median 363 m vs 100%: 605 m).
- Big Air bonus triggered in 27/30 full-power runs (avg 29.6 scrap). Air Control level 5 gave 455 vs 260 px/s sideways speed over 0.5 s.
- Garage: buy succeeds (100 -> 75 scrap), insufficient funds rejected with message, both tabs render without errors. Save: v2 save migrated to v3 and persisted across reload; earlier save tests (corrupt/backup/v1/storage-unavailable) were re-run in the previous pass and the save code is unchanged apart from the new 'a' upgrade.
- Responsive maths for 640x360, 800x360, 844x390, 932x430, 1024x768, 1920x1080, 2560x1080, 3440x1440 and portrait: canvas/stage aspect ratios match (no stretch).
Not verified (needs a real browser/phone): how any window looks or is sized on screen (the 72% panels, scrolling bodies, garage preview), tap comfort, touch controls, pause/resume and the new in-game confirm dialogs when clicked, audio, performance, rotation/resize behaviour, service worker. The designed 'feel' (pacing, fun) is not proven by simulation; please playtest.
Known notes: the run-length figures come from a bot that aims randomly, not a human. Integer pixel scaling is not enforced, so on some screens pixels can be slightly uneven.
