# Plan: implementation order

The same 208 issues grouped by **when they have to be resolved**, expressed as milestones M0-M8 on the GitHub repo.
For the same issues grouped by subject area, see [plan.md](plan.md).

## Sequence at a glance

| Milestone | Issues | p0 | Depends on |
|---|---:|---:|---|
| [M0: Product, Scope & Legal Decisions](https://github.com/ahmdkaml/avoid-burnout/milestone/1) | 31 | 12 | - |
| [M1: Repo, Toolchain & Architecture Skeleton](https://github.com/ahmdkaml/avoid-burnout/milestone/2) | 45 | 5 | M0 |
| [M2: Core Domain Logic & Test Harness](https://github.com/ahmdkaml/avoid-burnout/milestone/3) | 19 | 2 | M1 |
| [M3: Settings, Data & Privacy](https://github.com/ahmdkaml/avoid-burnout/milestone/4) | 10 | 1 | M2 |
| [M4: Windows Activity Detection](https://github.com/ahmdkaml/avoid-burnout/milestone/5) | 21 | 2 | M2 |
| [M5: Reminder Surfaces (Tray, Overlay, Toast)](https://github.com/ahmdkaml/avoid-burnout/milestone/6) | 27 | 3 | M4 |
| [M6: UX (Onboarding, Settings & History)](https://github.com/ahmdkaml/avoid-burnout/milestone/7) | 26 | 0 | M5 |
| [M7: Hardening, QA & Release](https://github.com/ahmdkaml/avoid-burnout/milestone/8) | 24 | 0 | M6 |
| [M8: Deferred / Post-v1](https://github.com/ahmdkaml/avoid-burnout/milestone/9) | 5 | 0 | v1 shipped |

M2, M3 and M4 branch off the same point. M3 can be built in parallel with M4 by a second person; M2 cannot be skipped by either.

## Critical path

The chain that actually determines the calendar:

```
#6  name          -> #38 framework     -> #88 layer split
#207 v1 cut line  -> #91 IClock        -> #157/#158/#159 core tests
#45 what is activity -> #47 input is not enough -> #49/#50 classifier -> #63 sessionization
#119 suspend     -> #54 lock          -> #112 overlay focus -> #150 break surface
```

Two long-lead items do not appear in that chain but gate the calendar anyway: **#181 code signing** needs procurement lead time, and **#204 user research** needs people, not code. Start both during M0.

## M0: Product, Scope & Legal Decisions

Nothing gets built until these close. Every one is a written decision, not code. The product name, the health-claim boundary, the v1 cut line and the UI framework each change work that would otherwise be thrown away.

**Exit criteria:** Decisions recorded in the repo. #207 cut line agreed. UI framework and target framework chosen.

**Watch out:** Do not start scaffolding before #38 (UI framework) and #207 (v1 cut) close; both invalidate work. #47 is a premise flaw in the idle-only model and its answer shapes M2 and M4.

### p0-blocking (12)

- [#2](https://github.com/ahmdkaml/avoid-burnout/issues/2) **Decide public product vs personal tool** `p0-blocking` `product` `M0`
- [#6](https://github.com/ahmdkaml/avoid-burnout/issues/6) **Product name says burnout but the product is eye strain** `p0-blocking` `branding` `M0`
- [#19](https://github.com/ahmdkaml/avoid-burnout/issues/19) **Target framework undecided** `p0-blocking` `setup` `M0`
- [#38](https://github.com/ahmdkaml/avoid-burnout/issues/38) **UI framework decision not recorded** `p0-blocking` `framework` `M0`
- [#45](https://github.com/ahmdkaml/avoid-burnout/issues/45) **"Activity" is never defined** `p0-blocking` `activity` `M0`
- [#47](https://github.com/ahmdkaml/avoid-burnout/issues/47) **Any input resets idle, so games never get a break** `p0-blocking` `activity` `M0`
- [#71](https://github.com/ahmdkaml/avoid-burnout/issues/71) **Full-screen lockout breaks are considered a feature** `p0-blocking` `breakrules` `M0`
- [#126](https://github.com/ahmdkaml/avoid-burnout/issues/126) **Telemetry decision not made** `p0-blocking` `privacy` `M0`
- [#196](https://github.com/ahmdkaml/avoid-burnout/issues/196) **Blue light filtering must not be a feature** `p0-blocking` `product` `M0`
- [#204](https://github.com/ahmdkaml/avoid-burnout/issues/204) **No user research behind the core mechanic** `p0-blocking` `product` `M0`
- [#206](https://github.com/ahmdkaml/avoid-burnout/issues/206) **No definition of success** `p0-blocking` `product` `M0`
- [#207](https://github.com/ahmdkaml/avoid-burnout/issues/207) **No MVP cut line** `p0-blocking` `product` `M0`

### p1-high (12)

- [#5](https://github.com/ahmdkaml/avoid-burnout/issues/5) **Name implies prevention of a medical condition** `p1-high` `branding` `M0`
- [#15](https://github.com/ahmdkaml/avoid-burnout/issues/15) **Health-claim copy needs review** `p1-high` `branding` `M0`
- [#42](https://github.com/ahmdkaml/avoid-burnout/issues/42) **Cross-platform has no cheap activity detection** `p1-high` `framework` `M0`
- [#43](https://github.com/ahmdkaml/avoid-burnout/issues/43) **Packaged vs unpackaged affects startup and privileges** `p1-high` `framework` `M0`
- [#44](https://github.com/ahmdkaml/avoid-burnout/issues/44) **Framework choice determines headless testability** `p1-high` `framework` `M0`
- [#61](https://github.com/ahmdkaml/avoid-burnout/issues/61) **Blink detection / real eye tracking scope is undefined** `p1-high` `product` `M0`
- [#82](https://github.com/ahmdkaml/avoid-burnout/issues/82) **Reporting is not scoped into or out of v1** `p1-high` `product` `M0`
- [#187](https://github.com/ahmdkaml/avoid-burnout/issues/187) **Health claims need a defined boundary** `p1-high` `branding` `M0`
- [#188](https://github.com/ahmdkaml/avoid-burnout/issues/188) **No medical disclaimer** `p1-high` `legal` `M0`
- [#193](https://github.com/ahmdkaml/avoid-burnout/issues/193) **Blink-rate and eye tracking is out of scope but unstated** `p1-high` `product` `M0`
- [#197](https://github.com/ahmdkaml/avoid-burnout/issues/197) **Adjacent wellness features are scope creep** `p1-high` `product` `M0`
- [#205](https://github.com/ahmdkaml/avoid-burnout/issues/205) **No competitor analysis** `p1-high` `product` `M0`

### p2-medium (6)

- [#40](https://github.com/ahmdkaml/avoid-burnout/issues/40) **WPF is the lowest-friction option for a Windows tray utility** `p2-medium` `framework` `M0`
- [#41](https://github.com/ahmdkaml/avoid-burnout/issues/41) **WinUI 3 adds bootstrapper and MSIX identity friction** `p2-medium` `framework` `M0`
- [#85](https://github.com/ahmdkaml/avoid-burnout/issues/85) **Gamification is unspecified** `p2-medium` `product` `M0`
- [#110](https://github.com/ahmdkaml/avoid-burnout/issues/110) **Resident tray process vs scheduled task** `p2-medium` `winapi` `M0`
- [#198](https://github.com/ahmdkaml/avoid-burnout/issues/198) **Mobile companion app is a second product** `p2-medium` `product` `M0`
- [#199](https://github.com/ahmdkaml/avoid-burnout/issues/199) **Team or employer dashboard has surveillance implications** `p2-medium` `product` `M0`

### p3-low (1)

- [#201](https://github.com/ahmdkaml/avoid-burnout/issues/201) **Theming and skinning is low value here** `p3-low` `product` `M0`

## M1: Repo, Toolchain & Architecture Skeleton

Make the repo buildable, testable and CI-enforced, and lay down the layer boundaries that keep the core headless-testable.

**Exit criteria:** dotnet build and dotnet test green in CI from a clean clone. Settings store atomic and versioned. Single instance enforced.

**Watch out:** #91 (IClock) and #104 (settings schema version) are the two that get more expensive every week they are deferred. Lock the NuGet restore in CI from day one (#184).

### p0-blocking (5)

- [#17](https://github.com/ahmdkaml/avoid-burnout/issues/17) **No global.json, so builds are not reproducible** `p0-blocking` `setup` `M1`
- [#20](https://github.com/ahmdkaml/avoid-burnout/issues/20) **No solution or project structure** `p0-blocking` `setup` `M1`
- [#24](https://github.com/ahmdkaml/avoid-burnout/issues/24) **No CI pipeline** `p0-blocking` `setup` `M1`
- [#88](https://github.com/ahmdkaml/avoid-burnout/issues/88) **No solution structure separating domain from platform from UI** `p0-blocking` `arch` `M1`
- [#91](https://github.com/ahmdkaml/avoid-burnout/issues/91) **No IClock abstraction** `p0-blocking` `arch` `M1`

### p1-high (26)

- [#22](https://github.com/ahmdkaml/avoid-burnout/issues/22) **No Directory.Build.props** `p1-high` `setup` `M1`
- [#23](https://github.com/ahmdkaml/avoid-burnout/issues/23) **No Directory.Packages.props for central package management** `p1-high` `setup` `M1`
- [#26](https://github.com/ahmdkaml/avoid-burnout/issues/26) **Test framework not chosen** `p1-high` `setup` `M1`
- [#29](https://github.com/ahmdkaml/avoid-burnout/issues/29) **README is a single heading** `p1-high` `setup` `M1`
- [#30](https://github.com/ahmdkaml/avoid-burnout/issues/30) **No LICENSE file** `p1-high` `legal` `M1`
- [#31](https://github.com/ahmdkaml/avoid-burnout/issues/31) **No .gitignore** `p1-high` `setup` `M1`
- [#37](https://github.com/ahmdkaml/avoid-burnout/issues/37) **No packaging or publishing pipeline** `p1-high` `setup` `M1`
- [#39](https://github.com/ahmdkaml/avoid-burnout/issues/39) **No smoke test for a missing or corrupt config** `p1-high` `setup` `M1`
- [#89](https://github.com/ahmdkaml/avoid-burnout/issues/89) **Core must not reference UI or Win32 types** `p1-high` `arch` `M1`
- [#90](https://github.com/ahmdkaml/avoid-burnout/issues/90) **Key abstractions not defined** `p1-high` `arch` `M1`
- [#92](https://github.com/ahmdkaml/avoid-burnout/issues/92) **Timer design undecided** `p1-high` `arch` `M1`
- [#93](https://github.com/ahmdkaml/avoid-burnout/issues/93) **No rule banning async void** `p1-high` `arch` `M1`
- [#94](https://github.com/ahmdkaml/avoid-burnout/issues/94) **No global cancellation token for shutdown** `p1-high` `arch` `M1`
- [#95](https://github.com/ahmdkaml/avoid-burnout/issues/95) **No single-instance enforcement** `p1-high` `arch` `M1`
- [#96](https://github.com/ahmdkaml/avoid-burnout/issues/96) **No top-level crash handler** `p1-high` `arch` `M1`
- [#97](https://github.com/ahmdkaml/avoid-burnout/issues/97) **Logging approach not chosen** `p1-high` `arch` `M1`
- [#98](https://github.com/ahmdkaml/avoid-burnout/issues/98) **Log file location, rotation and size cap undefined** `p1-high` `arch` `M1`
- [#99](https://github.com/ahmdkaml/avoid-burnout/issues/99) **Logs will contain window titles, which is PII** `p1-high` `arch` `M1`
- [#100](https://github.com/ahmdkaml/avoid-burnout/issues/100) **Settings persistence mechanism not chosen** `p1-high` `arch` `M1`
- [#101](https://github.com/ahmdkaml/avoid-burnout/issues/101) **Settings writes are not atomic** `p1-high` `arch` `M1`
- [#103](https://github.com/ahmdkaml/avoid-burnout/issues/103) **No options pattern with startup validation** `p1-high` `arch` `M1`
- [#104](https://github.com/ahmdkaml/avoid-burnout/issues/104) **No settings schema versioning or migration** `p1-high` `arch` `M1`
- [#108](https://github.com/ahmdkaml/avoid-burnout/issues/108) **Autostart registration method not chosen** `p1-high` `winapi` `M1`
- [#109](https://github.com/ahmdkaml/avoid-burnout/issues/109) **Autostart must be opt-in, never pre-enabled** `p1-high` `winapi` `M1`
- [#175](https://github.com/ahmdkaml/avoid-burnout/issues/175) **Distribution format not chosen: single-file publish or framework-dependent** `p1-high` `setup` `M1`
- [#184](https://github.com/ahmdkaml/avoid-burnout/issues/184) **Dependency supply chain not pinned** `p1-high` `setup` `M1`

### p2-medium (13)

- [#21](https://github.com/ahmdkaml/avoid-burnout/issues/21) **No .editorconfig analyzer baseline** `p2-medium` `setup` `M1`
- [#25](https://github.com/ahmdkaml/avoid-burnout/issues/25) **No code coverage collection** `p2-medium` `setup` `M1`
- [#27](https://github.com/ahmdkaml/avoid-burnout/issues/27) **No formatting gate in CI** `p2-medium` `setup` `M1`
- [#32](https://github.com/ahmdkaml/avoid-burnout/issues/32) **No defined policy for where these issues live** `p2-medium` `product` `M1`
- [#33](https://github.com/ahmdkaml/avoid-burnout/issues/33) **No dependency update automation** `p2-medium` `setup` `M1`
- [#34](https://github.com/ahmdkaml/avoid-burnout/issues/34) **No CHANGELOG convention** `p2-medium` `setup` `M1`
- [#35](https://github.com/ahmdkaml/avoid-burnout/issues/35) **No check that the app runs without elevation** `p2-medium` `setup` `M1`
- [#36](https://github.com/ahmdkaml/avoid-burnout/issues/36) **No deterministic build or version stamping** `p2-medium` `setup` `M1`
- [#102](https://github.com/ahmdkaml/avoid-burnout/issues/102) **No DI container decision** `p2-medium` `arch` `M1`
- [#105](https://github.com/ahmdkaml/avoid-burnout/issues/105) **Extensibility is unconsidered** `p2-medium` `arch` `M1`
- [#106](https://github.com/ahmdkaml/avoid-burnout/issues/106) **No localization plan, and strings are likely hardcoded** `p2-medium` `arch` `M1`
- [#107](https://github.com/ahmdkaml/avoid-burnout/issues/107) **Settings scope ambiguity: per user or per machine** `p2-medium` `arch` `M1`
- [#176](https://github.com/ahmdkaml/avoid-burnout/issues/176) **No build architecture matrix** `p2-medium` `setup` `M1`

### p3-low (1)

- [#28](https://github.com/ahmdkaml/avoid-burnout/issues/28) **No CONTRIBUTING.md** `p3-low` `setup` `M1`

## M2: Core Domain Logic & Test Harness

The pure part: interval and sessionization rules, break state machine, scoring, DST/timezone handling. No UI, no Win32, driven by a FakeClock.

**Exit criteria:** Core has no UI or Win32 reference (enforced by a test). 20-20-20 attribution documented. Intervals use a monotonic clock that survives suspend.

**Watch out:** Write #157/#158/#159 tables before the algorithm, not after. #79 and #81 are the timezone/suspend traps; a naive DateTime.Now interval will fail both.

### p0-blocking (2)

- [#157](https://github.com/ahmdkaml/avoid-burnout/issues/157) **No unit tests for the strain or interval algorithm** `p0-blocking` `breakrules` `M2`
- [#162](https://github.com/ahmdkaml/avoid-burnout/issues/162) **No fake clock means no testable time logic** `p0-blocking` `arch` `M2`

### p1-high (12)

- [#63](https://github.com/ahmdkaml/avoid-burnout/issues/63) **Continuous work block / sessionization not defined** `p1-high` `activity` `M2`
- [#65](https://github.com/ahmdkaml/avoid-burnout/issues/65) **Activity log has no growth or retention strategy** `p1-high` `activity` `M2`
- [#66](https://github.com/ahmdkaml/avoid-burnout/issues/66) **Default break interval is arbitrary and hardcoded by assumption** `p1-high` `breakrules` `M2`
- [#67](https://github.com/ahmdkaml/avoid-burnout/issues/67) **Default break duration is likewise arbitrary** `p1-high` `breakrules` `M2`
- [#69](https://github.com/ahmdkaml/avoid-burnout/issues/69) **Escalation after ignored breaks is undefined** `p1-high` `breakrules` `M2`
- [#72](https://github.com/ahmdkaml/avoid-burnout/issues/72) **No cap on back-to-back breaks** `p1-high` `breakrules` `M2`
- [#73](https://github.com/ahmdkaml/avoid-burnout/issues/73) **Does the timer pause during the break itself?** `p1-high` `breakrules` `M2`
- [#79](https://github.com/ahmdkaml/avoid-burnout/issues/79) **No timezone or DST handling in daily logic** `p1-high` `breakrules` `M2`
- [#80](https://github.com/ahmdkaml/avoid-burnout/issues/80) **No strain scoring formula** `p1-high` `reporting` `M2`
- [#81](https://github.com/ahmdkaml/avoid-burnout/issues/81) **System clock change mid-session is unhandled** `p1-high` `breakrules` `M2`
- [#158](https://github.com/ahmdkaml/avoid-burnout/issues/158) **No unit tests for sessionization and the gap threshold** `p1-high` `activity` `M2`
- [#159](https://github.com/ahmdkaml/avoid-burnout/issues/159) **No unit tests for the activity classifier** `p1-high` `activity` `M2`

### p2-medium (5)

- [#62](https://github.com/ahmdkaml/avoid-burnout/issues/62) **No continuity model when the app is not running** `p2-medium` `activity` `M2`
- [#70](https://github.com/ahmdkaml/avoid-burnout/issues/70) **Snooze semantics not defined** `p2-medium` `breakrules` `M2`
- [#74](https://github.com/ahmdkaml/avoid-burnout/issues/74) **No cumulative strain model** `p2-medium` `breakrules` `M2`
- [#75](https://github.com/ahmdkaml/avoid-burnout/issues/75) **No daily cap on break count** `p2-medium` `breakrules` `M2`
- [#76](https://github.com/ahmdkaml/avoid-burnout/issues/76) **No per-activity rule differentiation** `p2-medium` `breakrules` `M2`

## M3: Settings, Data & Privacy

Consent, local-only history, export and delete, validation, and the explicit no-telemetry / no-screenshots posture.

**Exit criteria:** Consent shown before first collection. JSON/CSV export and delete-all work. Settings validated and treated as untrusted input.

**Watch out:** The export shape is a public contract once released - version it. If #126 stays 'none', say so in the UI, not just in a privacy page.

### p0-blocking (1)

- [#125](https://github.com/ahmdkaml/avoid-burnout/issues/125) **No consent screen for activity tracking** `p0-blocking` `privacy` `M3`

### p1-high (7)

- [#83](https://github.com/ahmdkaml/avoid-burnout/issues/83) **No export format for history** `p1-high` `reporting` `M3`
- [#129](https://github.com/ahmdkaml/avoid-burnout/issues/129) **No data export, deletion, or forget-me path** `p1-high` `legal` `M3`
- [#130](https://github.com/ahmdkaml/avoid-burnout/issues/130) **No in-app statement that screen content is never captured** `p1-high` `ux` `M3`
- [#160](https://github.com/ahmdkaml/avoid-burnout/issues/160) **No tests for settings migration** `p1-high` `arch` `M3`
- [#161](https://github.com/ahmdkaml/avoid-burnout/issues/161) **No test for concurrent settings access** `p1-high` `arch` `M3`
- [#179](https://github.com/ahmdkaml/avoid-burnout/issues/179) **Settings values are not validated** `p1-high` `breakrules` `M3`
- [#180](https://github.com/ahmdkaml/avoid-burnout/issues/180) **Settings and classification files are untrusted input** `p1-high` `arch` `M3`

### p2-medium (2)

- [#127](https://github.com/ahmdkaml/avoid-burnout/issues/127) **If telemetry is on, the PII surface is undefined** `p2-medium` `privacy` `M3`
- [#128](https://github.com/ahmdkaml/avoid-burnout/issues/128) **No decision on encryption at rest for history** `p2-medium` `privacy` `M3`

## M4: Windows Activity Detection

GetLastInputInfo idle, foreground process classification, lock/unlock and suspend/resume handling, fullscreen disambiguation, multi-monitor.

**Exit criteria:** No reminder burst after suspend or lock. High-engagement activities detected. Unknown processes fall back to a defined default.

**Watch out:** #54 (lock) and #119 (suspend) are the two paths that only get discovered in real use. #55/#57 is the classic false-positive pair: a borderless-fullscreen video player is nearly indistinguishable from a borderless game.

### p0-blocking (2)

- [#54](https://github.com/ahmdkaml/avoid-burnout/issues/54) **Lock and screen-saver events not handled** `p0-blocking` `activity` `M4`
- [#119](https://github.com/ahmdkaml/avoid-burnout/issues/119) **Power events (suspend and resume) not handled** `p0-blocking` `winapi` `M4`

### p1-high (9)

- [#46](https://github.com/ahmdkaml/avoid-burnout/issues/46) **Idle detection needs GetLastInputInfo, with ~1s granularity** `p1-high` `activity` `M4`
- [#48](https://github.com/ahmdkaml/avoid-burnout/issues/48) **Foreground process detection not designed** `p1-high` `activity` `M4`
- [#49](https://github.com/ahmdkaml/avoid-burnout/issues/49) **Process-to-category mapping has no maintainable home** `p1-high` `arch` `M4`
- [#50](https://github.com/ahmdkaml/avoid-burnout/issues/50) **Activity categories not enumerated** `p1-high` `activity` `M4`
- [#51](https://github.com/ahmdkaml/avoid-burnout/issues/51) **Default behaviour for the unknown category is undefined** `p1-high` `activity` `M4`
- [#58](https://github.com/ahmdkaml/avoid-burnout/issues/58) **Multi-monitor handling undefined** `p1-high` `activity` `M4`
- [#122](https://github.com/ahmdkaml/avoid-burnout/issues/122) **Session lock and unlock event ordering not handled** `p1-high` `winapi` `M4`
- [#163](https://github.com/ahmdkaml/avoid-burnout/issues/163) **No integration test for suspend and resume** `p1-high` `winapi` `M4`
- [#170](https://github.com/ahmdkaml/avoid-burnout/issues/170) **No negative tests for locked session and fullscreen** `p1-high` `winapi` `M4`

### p2-medium (7)

- [#52](https://github.com/ahmdkaml/avoid-burnout/issues/52) **Meeting detection needs a documented approach** `p2-medium` `activity` `M4`
- [#53](https://github.com/ahmdkaml/avoid-burnout/issues/53) **Video playback detection via window titles is fragile** `p2-medium` `activity` `M4`
- [#55](https://github.com/ahmdkaml/avoid-burnout/issues/55) **Exclusive fullscreen (games) detection has no public API** `p2-medium` `activity` `M4`
- [#57](https://github.com/ahmdkaml/avoid-burnout/issues/57) **Borderless fullscreen video must not be treated as a game** `p2-medium` `activity` `M4`
- [#64](https://github.com/ahmdkaml/avoid-burnout/issues/64) **Idle-detection accuracy is undocumented** `p2-medium` `activity` `M4`
- [#123](https://github.com/ahmdkaml/avoid-burnout/issues/123) **No policy for power-saving mode** `p2-medium` `winapi` `M4`
- [#203](https://github.com/ahmdkaml/avoid-burnout/issues/203) **Idle-time-as-game-time heuristic will be wrong** `p2-medium` `product` `M4`

### p3-low (3)

- [#56](https://github.com/ahmdkaml/avoid-burnout/issues/56) **RDP sessions change the meaning of idle** `p3-low` `activity` `M4`
- [#59](https://github.com/ahmdkaml/avoid-burnout/issues/59) **Multi-user and fast-user-switching not considered** `p3-low` `activity` `M4`
- [#60](https://github.com/ahmdkaml/avoid-burnout/issues/60) **Virtual machines blur input attribution** `p3-low` `activity` `M4`

## M5: Reminder Surfaces (Tray, Overlay, Toast)

Tray icon and menu, non-activating overlay, toasts with a registered AUMID, global hotkeys, quick-hide, quiet hours, DPI and display topology.

**Exit criteria:** Overlay never steals focus. Reminder never blocks input. Hidden tray icon is recoverable. Test notification works.

**Watch out:** Design the overlay against the worst case (exclusive fullscreen game, live call, screen share), not the best. #112 and #150 are non-negotiable: an overlay that steals focus gets the app uninstalled.

### p0-blocking (3)

- [#135](https://github.com/ahmdkaml/avoid-burnout/issues/135) **Pause control is not discoverable** `p0-blocking` `ux` `M5`
- [#150](https://github.com/ahmdkaml/avoid-burnout/issues/150) **Break surface can interrupt work that cannot be paused** `p0-blocking` `winapi` `M5`
- [#151](https://github.com/ahmdkaml/avoid-burnout/issues/151) **Reminders must be non-blocking by default** `p0-blocking` `notify` `M5`

### p1-high (15)

- [#3](https://github.com/ahmdkaml/avoid-burnout/issues/3) **No logo or app mark** `p1-high` `branding` `M5`
- [#78](https://github.com/ahmdkaml/avoid-burnout/issues/78) **Quiet hours and Focus Assist not integrated** `p1-high` `breakrules` `M5`
- [#111](https://github.com/ahmdkaml/avoid-burnout/issues/111) **DPI awareness not set** `p1-high` `winapi` `M5`
- [#112](https://github.com/ahmdkaml/avoid-burnout/issues/112) **Overlay window will steal focus unless carefully created** `p1-high` `winapi` `M5`
- [#113](https://github.com/ahmdkaml/avoid-burnout/issues/113) **Overlay over exclusive fullscreen may be impossible** `p1-high` `breakrules` `M5`
- [#114](https://github.com/ahmdkaml/avoid-burnout/issues/114) **Toast notifications from an unpackaged app need a registered AUMID** `p1-high` `winapi` `M5`
- [#117](https://github.com/ahmdkaml/avoid-burnout/issues/117) **No plan for the user hiding the tray icon** `p1-high` `winapi` `M5`
- [#118](https://github.com/ahmdkaml/avoid-burnout/issues/118) **Tray balloon notifications are unreliable on Windows 11** `p1-high` `winapi` `M5`
- [#120](https://github.com/ahmdkaml/avoid-burnout/issues/120) **Display topology changes while the overlay is showing** `p1-high` `winapi` `M5`
- [#124](https://github.com/ahmdkaml/avoid-burnout/issues/124) **Startup race with the shell at boot** `p1-high` `winapi` `M5`
- [#145](https://github.com/ahmdkaml/avoid-burnout/issues/145) **Tray menu contents not specified** `p1-high` `notify` `M5`
- [#152](https://github.com/ahmdkaml/avoid-burnout/issues/152) **No design against alert fatigue** `p1-high` `breakrules` `M5`
- [#153](https://github.com/ahmdkaml/avoid-burnout/issues/153) **Suppressed-by-DND breaks have no defined status** `p1-high` `notify` `M5`
- [#154](https://github.com/ahmdkaml/avoid-burnout/issues/154) **Notification copy does not state the action** `p1-high` `notify` `M5`
- [#202](https://github.com/ahmdkaml/avoid-burnout/issues/202) **No quick-hide affordance** `p1-high` `product` `M5`

### p2-medium (8)

- [#7](https://github.com/ahmdkaml/avoid-burnout/issues/7) **Icon variants and themes not specified** `p2-medium` `branding` `M5`
- [#10](https://github.com/ahmdkaml/avoid-burnout/issues/10) **Tray icon needs multiple visual states** `p2-medium` `branding` `M5`
- [#115](https://github.com/ahmdkaml/avoid-burnout/issues/115) **Notification click-through has no defined behaviour** `p2-medium` `winapi` `M5`
- [#116](https://github.com/ahmdkaml/avoid-burnout/issues/116) **Global hotkey handling not designed** `p2-medium` `winapi` `M5`
- [#121](https://github.com/ahmdkaml/avoid-burnout/issues/121) **DPI change while running not handled** `p2-medium` `winapi` `M5`
- [#155](https://github.com/ahmdkaml/avoid-burnout/issues/155) **Notification text is not localized** `p2-medium` `notify` `M5`
- [#156](https://github.com/ahmdkaml/avoid-burnout/issues/156) **No notification priority or channel decision** `p2-medium` `notify` `M5`
- [#178](https://github.com/ahmdkaml/avoid-burnout/issues/178) **No performance budget for the overlay render** `p2-medium` `ux` `M5`

### p3-low (1)

- [#12](https://github.com/ahmdkaml/avoid-burnout/issues/12) **Notification branding undecided** `p3-low` `branding` `M5`

## M6: UX (Onboarding, Settings & History)

First run, consent copy, the pause control, settings scope, screen-reader and keyboard support, empty/error states, .resx extraction.

**Exit criteria:** A new user understands what will interrupt them and how to stop it. Overlay is keyboard-operable and readable by Narrator.

**Watch out:** Keep the settings surface small - every knob is a decision the user has to maintain. #141 (test notification) is a two-line fix that prevents a whole class of support noise.

### p1-high (12)

- [#16](https://github.com/ahmdkaml/avoid-burnout/issues/16) **Contrast ratios unspecified for the break overlay** `p1-high` `branding` `M6`
- [#18](https://github.com/ahmdkaml/avoid-burnout/issues/18) **Overlay animation must respect reduced-motion** `p1-high` `branding` `M6`
- [#133](https://github.com/ahmdkaml/avoid-burnout/issues/133) **No first-run onboarding** `p1-high` `ux` `M6`
- [#134](https://github.com/ahmdkaml/avoid-burnout/issues/134) **Onboarding does not disclose what data is collected** `p1-high` `ux` `M6`
- [#137](https://github.com/ahmdkaml/avoid-burnout/issues/137) **The break screen does not say what to actually do** `p1-high` `breakrules` `M6`
- [#138](https://github.com/ahmdkaml/avoid-burnout/issues/138) **Eye exercise animations carry real risk** `p1-high` `branding` `M6`
- [#141](https://github.com/ahmdkaml/avoid-burnout/issues/141) **No test-notification button in settings** `p1-high` `notify` `M6`
- [#142](https://github.com/ahmdkaml/avoid-burnout/issues/142) **No screen reader support for the overlay** `p1-high` `ux` `M6`
- [#143](https://github.com/ahmdkaml/avoid-burnout/issues/143) **Overlay is not designed for keyboard-only operation** `p1-high` `ux` `M6`
- [#144](https://github.com/ahmdkaml/avoid-burnout/issues/144) **No quiet mode for calls and presentations** `p1-high` `activity` `M6`
- [#168](https://github.com/ahmdkaml/avoid-burnout/issues/168) **No DPI matrix test** `p1-high` `ux` `M6`
- [#208](https://github.com/ahmdkaml/avoid-burnout/issues/208) **Onboarding cannot assume the user wants interruptions** `p1-high` `product` `M6`

### p2-medium (13)

- [#8](https://github.com/ahmdkaml/avoid-burnout/issues/8) **Three different surfaces need one visual language** `p2-medium` `branding` `M6`
- [#11](https://github.com/ahmdkaml/avoid-burnout/issues/11) **No colour palette defined** `p2-medium` `branding` `M6`
- [#14](https://github.com/ahmdkaml/avoid-burnout/issues/14) **No sound design decision** `p2-medium` `branding` `M6`
- [#77](https://github.com/ahmdkaml/avoid-burnout/issues/77) **System accessibility settings not respected** `p2-medium` `breakrules` `M6`
- [#87](https://github.com/ahmdkaml/avoid-burnout/issues/87) **No empty or calibration state for new users** `p2-medium` `ux` `M6`
- [#136](https://github.com/ahmdkaml/avoid-burnout/issues/136) **Pause duration options not defined** `p2-medium` `ux` `M6`
- [#140](https://github.com/ahmdkaml/avoid-burnout/issues/140) **Settings surface has no scope limit** `p2-medium` `ux` `M6`
- [#146](https://github.com/ahmdkaml/avoid-burnout/issues/146) **Interval setting has no explanation** `p2-medium` `ux` `M6`
- [#147](https://github.com/ahmdkaml/avoid-burnout/issues/147) **Onboarding does not preview the break screen** `p2-medium` `ux` `M6`
- [#148](https://github.com/ahmdkaml/avoid-burnout/issues/148) **Time to first break is long** `p2-medium` `ux` `M6`
- [#149](https://github.com/ahmdkaml/avoid-burnout/issues/149) **Empty and error states are not listed anywhere** `p2-medium` `ux` `M6`
- [#164](https://github.com/ahmdkaml/avoid-burnout/issues/164) **No UI automation test for the overlay** `p2-medium` `ux` `M6`
- [#200](https://github.com/ahmdkaml/avoid-burnout/issues/200) **Multi-language support doubles the string work** `p2-medium` `product` `M6`

### p3-low (1)

- [#9](https://github.com/ahmdkaml/avoid-burnout/issues/9) **No type scale or spacing tokens** `p3-low` `branding` `M6`

## M7: Hardening, QA & Release

Test matrices, soak and leak checks, perf targets, code signing, packaging, privacy policy, changelog, store copy.

**Exit criteria:** Signed build installs without SmartScreen warnings. All p0-blocking closed. Soak shows flat memory across simulated breaks.

**Watch out:** Every matrix run is expensive; batch them. #181 (signing) needs budget and procurement lead time, so start it during M0 even though it closes here.

### p1-high (7)

- [#68](https://github.com/ahmdkaml/avoid-burnout/issues/68) **No provenance or citation for the 20-20-20 rule** `p1-high` `legal` `M7`
- [#132](https://github.com/ahmdkaml/avoid-burnout/issues/132) **Unsigned binary will be quarantined by SmartScreen** `p1-high` `privacy` `M7`
- [#166](https://github.com/ahmdkaml/avoid-burnout/issues/166) **No memory leak check on the break path** `p1-high` `testing` `M7`
- [#167](https://github.com/ahmdkaml/avoid-burnout/issues/167) **No Windows version test matrix** `p1-high` `winapi` `M7`
- [#181](https://github.com/ahmdkaml/avoid-burnout/issues/181) **No code signing** `p1-high` `security` `M7`
- [#182](https://github.com/ahmdkaml/avoid-burnout/issues/182) **No auto-update mechanism defined** `p1-high` `setup` `M7`
- [#189](https://github.com/ahmdkaml/avoid-burnout/issues/189) **No terms of privacy or EULA** `p1-high` `legal` `M7`

### p2-medium (11)

- [#4](https://github.com/ahmdkaml/avoid-burnout/issues/4) **Trademark search not done** `p2-medium` `branding` `M7`
- [#131](https://github.com/ahmdkaml/avoid-burnout/issues/131) **No privacy declaration for a store submission** `p2-medium` `legal` `M7`
- [#165](https://github.com/ahmdkaml/avoid-burnout/issues/165) **No soak test** `p2-medium` `testing` `M7`
- [#169](https://github.com/ahmdkaml/avoid-burnout/issues/169) **No multi-monitor overlay placement test** `p2-medium` `winapi` `M7`
- [#171](https://github.com/ahmdkaml/avoid-burnout/issues/171) **No idle memory target** `p2-medium` `perf` `M7`
- [#172](https://github.com/ahmdkaml/avoid-burnout/issues/172) **No CPU-when-idle target** `p2-medium` `perf` `M7`
- [#173](https://github.com/ahmdkaml/avoid-burnout/issues/173) **Poll interval versus battery life tradeoff is undocumented** `p2-medium` `perf` `M7`
- [#183](https://github.com/ahmdkaml/avoid-burnout/issues/183) **Update check requires a hosting endpoint** `p2-medium` `setup` `M7`
- [#185](https://github.com/ahmdkaml/avoid-burnout/issues/185) **Single-instance IPC is unencrypted and world-visible** `p2-medium` `arch` `M7`
- [#190](https://github.com/ahmdkaml/avoid-burnout/issues/190) **20-20-20 rule attribution not documented** `p2-medium` `legal` `M7`
- [#191](https://github.com/ahmdkaml/avoid-burnout/issues/191) **No accessibility compliance target** `p2-medium` `legal` `M7`

### p3-low (6)

- [#1](https://github.com/ahmdkaml/avoid-burnout/issues/1) **Domain name availability unchecked** `p3-low` `branding` `M7`
- [#13](https://github.com/ahmdkaml/avoid-burnout/issues/13) **No store listing copy** `p3-low` `branding` `M7`
- [#174](https://github.com/ahmdkaml/avoid-burnout/issues/174) **No startup time target** `p3-low` `perf` `M7`
- [#177](https://github.com/ahmdkaml/avoid-burnout/issues/177) **No crash dump and symbol story** `p3-low` `setup` `M7`
- [#186](https://github.com/ahmdkaml/avoid-burnout/issues/186) **No obfuscation decision** `p3-low` `security` `M7`
- [#192](https://github.com/ahmdkaml/avoid-burnout/issues/192) **No age rating or not-for-under-13 statement** `p3-low` `legal` `M7`

## M8: Deferred / Post-v1

Explicitly outside the v1 cut. Recorded so scope is not re-litigated mid-build.

**Exit criteria:** Re-triage after v1 against the success metric from #206.

**Watch out:** Do not pull anything forward without re-checking it against the M0 cut line. Reports and streaks are the most likely items to be pulled forward, and #84 pulls a charting dependency in with them.

### p2-medium (3)

- [#86](https://github.com/ahmdkaml/avoid-burnout/issues/86) **Streak rules across timezone and DST are undefined** `p2-medium` `reporting` `M8`
- [#194](https://github.com/ahmdkaml/avoid-burnout/issues/194) **Screen brightness control to reduce glare is undecided** `p2-medium` `product` `M8`
- [#195](https://github.com/ahmdkaml/avoid-burnout/issues/195) **Ambient light sensor access is undecided** `p2-medium` `product` `M8`

### p3-low (2)

- [#84](https://github.com/ahmdkaml/avoid-burnout/issues/84) **Charting library decision not made** `p3-low` `reporting` `M8`
- [#139](https://github.com/ahmdkaml/avoid-burnout/issues/139) **Snooze and streak interaction is undefined** `p3-low` `ux` `M8`

## Rules of the road

1. **No scaffolding before M0 closes.** #38 and #207 both invalidate work started early.
2. **No Core reference to UI or Win32, enforced by a test (#89).** A comment will not hold.
3. **Every timing rule goes through IClock (#91).** No Thread.Sleep, no DateTime.Now for intervals.
4. **Tests before the algorithm** for anything in M2 (#157, #158, #159).
5. **The overlay never takes focus and never blocks input** (#112, #150, #151). This is the single behaviour that decides whether the app survives contact with users.
6. **Nothing is collected before consent** (#125) and no screenshots, ever (#130).
7. **Out-of-scope stays out of scope.** M8 is not a backlog to be raided when a milestone runs late.

## Commands

```
gh issue list --milestone 'M2: Core Domain Logic & Test Harness' --state open
gh issue list --milestone 'M2: Core Domain Logic & Test Harness' --state open --label p0-blocking
gh issue list --label area:activity --state open
```
