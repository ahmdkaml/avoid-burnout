# Plan: issue backlog by category

All 208 issues from the v0 backlog, grouped by what they are about.
For the same issues grouped by **the order they must be built in**, see [plan-implementation-order.md](plan-implementation-order.md).

Issue numbers were assigned during a batch upload and are **not** in category order. Sort by the priority or milestone tag, not by number.

Tags on every line: `priority` · `primary area` · `milestone`.

Most issues are **cross-cutting**: 109 of the 208 carry more than one area label. Each is filed once, under its subject (see [Cross-cutting concerns](#cross-cutting-concerns)), so the category counts below are the primary subject of the issue, not the total number of issues that touch that topic.

## Summary

| Category | Issues | p0 | p1 | p2 | p3 | Milestones |
|---|---:|---:|---:|---:|---:|---|
| Product & Scope | 21 | 5 | 7 | 8 | 1 | M0, M1, M4, M5, M6, M8 |
| Branding & Visual Identity | 18 | 1 | 7 | 6 | 4 | M0, M5, M6, M7 |
| Legal, Claims & Compliance | 9 | 0 | 5 | 3 | 1 | M0, M1, M3, M7 |
| UI Framework & Packaging | 6 | 1 | 3 | 2 | 0 | M0 |
| Repo, Toolchain & CI | 25 | 4 | 10 | 9 | 2 | M0, M1, M7 |
| Architecture & Design Patterns | 26 | 3 | 18 | 5 | 0 | M1, M2, M3, M4, M7 |
| Activity & Idle Detection | 22 | 3 | 10 | 6 | 3 | M0, M2, M4, M6 |
| Break Rules & Scheduling | 19 | 2 | 12 | 5 | 0 | M0, M2, M3, M5, M6 |
| Windows Platform Integration | 21 | 2 | 13 | 6 | 0 | M0, M1, M4, M5, M7 |
| Notifications, Tray & Reminders | 7 | 1 | 4 | 2 | 0 | M5, M6 |
| UX & Accessibility | 17 | 1 | 6 | 9 | 1 | M3, M5, M6, M8 |
| Scoring, History & Reports | 4 | 0 | 2 | 1 | 1 | M2, M3, M8 |
| Privacy & Data Handling | 5 | 2 | 1 | 2 | 0 | M0, M3, M7 |
| Testing & QA | 2 | 0 | 1 | 1 | 0 | M7 |
| Performance & Distribution | 4 | 0 | 0 | 3 | 1 | M7 |
| Security & Supply Chain | 2 | 0 | 1 | 0 | 1 | M7 |
| **Total** | **208** | **25** | **100** | **68** | **15** | M0-M8 |

## Categories

### 1. Product & Scope (21)

What this is, who it is for, and what it explicitly refuses to do. Nothing in the backlog survives contact with an unfocused scope.

- [#2](https://github.com/ahmdkaml/avoid-burnout/issues/2) **Decide public product vs personal tool** `p0-blocking` `product` `M0`
- [#196](https://github.com/ahmdkaml/avoid-burnout/issues/196) **Blue light filtering must not be a feature** `p0-blocking` `product` `M0`
- [#204](https://github.com/ahmdkaml/avoid-burnout/issues/204) **No user research behind the core mechanic** `p0-blocking` `product` `M0`
- [#206](https://github.com/ahmdkaml/avoid-burnout/issues/206) **No definition of success** `p0-blocking` `product` `M0`
- [#207](https://github.com/ahmdkaml/avoid-burnout/issues/207) **No MVP cut line** `p0-blocking` `product` `M0`
- [#61](https://github.com/ahmdkaml/avoid-burnout/issues/61) **Blink detection / real eye tracking scope is undefined** `p1-high` `product` `M0`
- [#82](https://github.com/ahmdkaml/avoid-burnout/issues/82) **Reporting is not scoped into or out of v1** `p1-high` `product` `M0`
- [#193](https://github.com/ahmdkaml/avoid-burnout/issues/193) **Blink-rate and eye tracking is out of scope but unstated** `p1-high` `product` `M0`
- [#197](https://github.com/ahmdkaml/avoid-burnout/issues/197) **Adjacent wellness features are scope creep** `p1-high` `product` `M0`
- [#202](https://github.com/ahmdkaml/avoid-burnout/issues/202) **No quick-hide affordance** `p1-high` `product` `M5`
- [#205](https://github.com/ahmdkaml/avoid-burnout/issues/205) **No competitor analysis** `p1-high` `product` `M0`
- [#208](https://github.com/ahmdkaml/avoid-burnout/issues/208) **Onboarding cannot assume the user wants interruptions** `p1-high` `product` `M6`
- [#32](https://github.com/ahmdkaml/avoid-burnout/issues/32) **No defined policy for where these issues live** `p2-medium` `product` `M1`
- [#85](https://github.com/ahmdkaml/avoid-burnout/issues/85) **Gamification is unspecified** `p2-medium` `product` `M0`
- [#194](https://github.com/ahmdkaml/avoid-burnout/issues/194) **Screen brightness control to reduce glare is undecided** `p2-medium` `product` `M8`
- [#195](https://github.com/ahmdkaml/avoid-burnout/issues/195) **Ambient light sensor access is undecided** `p2-medium` `product` `M8`
- [#198](https://github.com/ahmdkaml/avoid-burnout/issues/198) **Mobile companion app is a second product** `p2-medium` `product` `M0`
- [#199](https://github.com/ahmdkaml/avoid-burnout/issues/199) **Team or employer dashboard has surveillance implications** `p2-medium` `product` `M0`
- [#200](https://github.com/ahmdkaml/avoid-burnout/issues/200) **Multi-language support doubles the string work** `p2-medium` `product` `M6`
- [#203](https://github.com/ahmdkaml/avoid-burnout/issues/203) **Idle-time-as-game-time heuristic will be wrong** `p2-medium` `product` `M4`
- [#201](https://github.com/ahmdkaml/avoid-burnout/issues/201) **Theming and skinning is low value here** `p3-low` `product` `M0`

### 2. Branding & Visual Identity (18)

Name, mark, tray icon states and visual language. Cheap now, expensive once there is a shipped install base.

- [#6](https://github.com/ahmdkaml/avoid-burnout/issues/6) **Product name says burnout but the product is eye strain** `p0-blocking` `branding` `M0`
- [#3](https://github.com/ahmdkaml/avoid-burnout/issues/3) **No logo or app mark** `p1-high` `branding` `M5`
- [#5](https://github.com/ahmdkaml/avoid-burnout/issues/5) **Name implies prevention of a medical condition** `p1-high` `branding` `M0`
- [#15](https://github.com/ahmdkaml/avoid-burnout/issues/15) **Health-claim copy needs review** `p1-high` `branding` `M0`
- [#16](https://github.com/ahmdkaml/avoid-burnout/issues/16) **Contrast ratios unspecified for the break overlay** `p1-high` `branding` `M6`
- [#18](https://github.com/ahmdkaml/avoid-burnout/issues/18) **Overlay animation must respect reduced-motion** `p1-high` `branding` `M6`
- [#138](https://github.com/ahmdkaml/avoid-burnout/issues/138) **Eye exercise animations carry real risk** `p1-high` `branding` `M6`
- [#187](https://github.com/ahmdkaml/avoid-burnout/issues/187) **Health claims need a defined boundary** `p1-high` `branding` `M0`
- [#4](https://github.com/ahmdkaml/avoid-burnout/issues/4) **Trademark search not done** `p2-medium` `branding` `M7`
- [#7](https://github.com/ahmdkaml/avoid-burnout/issues/7) **Icon variants and themes not specified** `p2-medium` `branding` `M5`
- [#8](https://github.com/ahmdkaml/avoid-burnout/issues/8) **Three different surfaces need one visual language** `p2-medium` `branding` `M6`
- [#10](https://github.com/ahmdkaml/avoid-burnout/issues/10) **Tray icon needs multiple visual states** `p2-medium` `branding` `M5`
- [#11](https://github.com/ahmdkaml/avoid-burnout/issues/11) **No colour palette defined** `p2-medium` `branding` `M6`
- [#14](https://github.com/ahmdkaml/avoid-burnout/issues/14) **No sound design decision** `p2-medium` `branding` `M6`
- [#1](https://github.com/ahmdkaml/avoid-burnout/issues/1) **Domain name availability unchecked** `p3-low` `branding` `M7`
- [#9](https://github.com/ahmdkaml/avoid-burnout/issues/9) **No type scale or spacing tokens** `p3-low` `branding` `M6`
- [#12](https://github.com/ahmdkaml/avoid-burnout/issues/12) **Notification branding undecided** `p3-low` `branding` `M5`
- [#13](https://github.com/ahmdkaml/avoid-burnout/issues/13) **No store listing copy** `p3-low` `branding` `M7`

### 3. Legal, Claims & Compliance (9)

The boundary between "relieves eye strain" and a medical claim, plus the documents that follow from wherever that boundary lands.

- [#30](https://github.com/ahmdkaml/avoid-burnout/issues/30) **No LICENSE file** `p1-high` `legal` `M1`
- [#68](https://github.com/ahmdkaml/avoid-burnout/issues/68) **No provenance or citation for the 20-20-20 rule** `p1-high` `legal` `M7`
- [#129](https://github.com/ahmdkaml/avoid-burnout/issues/129) **No data export, deletion, or forget-me path** `p1-high` `legal` `M3`
- [#188](https://github.com/ahmdkaml/avoid-burnout/issues/188) **No medical disclaimer** `p1-high` `legal` `M0`
- [#189](https://github.com/ahmdkaml/avoid-burnout/issues/189) **No terms of privacy or EULA** `p1-high` `legal` `M7`
- [#131](https://github.com/ahmdkaml/avoid-burnout/issues/131) **No privacy declaration for a store submission** `p2-medium` `legal` `M7`
- [#190](https://github.com/ahmdkaml/avoid-burnout/issues/190) **20-20-20 rule attribution not documented** `p2-medium` `legal` `M7`
- [#191](https://github.com/ahmdkaml/avoid-burnout/issues/191) **No accessibility compliance target** `p2-medium` `legal` `M7`
- [#192](https://github.com/ahmdkaml/avoid-burnout/issues/192) **No age rating or not-for-under-13 statement** `p3-low` `legal` `M7`

### 4. UI Framework & Packaging (6)

The choice that determines tray support, overlay behaviour, packaging, distribution size and whether the core can be tested headless.

- [#38](https://github.com/ahmdkaml/avoid-burnout/issues/38) **UI framework decision not recorded** `p0-blocking` `framework` `M0`
- [#42](https://github.com/ahmdkaml/avoid-burnout/issues/42) **Cross-platform has no cheap activity detection** `p1-high` `framework` `M0`
- [#43](https://github.com/ahmdkaml/avoid-burnout/issues/43) **Packaged vs unpackaged affects startup and privileges** `p1-high` `framework` `M0`
- [#44](https://github.com/ahmdkaml/avoid-burnout/issues/44) **Framework choice determines headless testability** `p1-high` `framework` `M0`
- [#40](https://github.com/ahmdkaml/avoid-burnout/issues/40) **WPF is the lowest-friction option for a Windows tray utility** `p2-medium` `framework` `M0`
- [#41](https://github.com/ahmdkaml/avoid-burnout/issues/41) **WinUI 3 adds bootstrapper and MSIX identity friction** `p2-medium` `framework` `M0`

### 5. Repo, Toolchain & CI (25)

Everything needed for a stranger to clone, build, test and trust the repo.

- [#17](https://github.com/ahmdkaml/avoid-burnout/issues/17) **No global.json, so builds are not reproducible** `p0-blocking` `setup` `M1`
- [#19](https://github.com/ahmdkaml/avoid-burnout/issues/19) **Target framework undecided** `p0-blocking` `setup` `M0`
- [#20](https://github.com/ahmdkaml/avoid-burnout/issues/20) **No solution or project structure** `p0-blocking` `setup` `M1`
- [#24](https://github.com/ahmdkaml/avoid-burnout/issues/24) **No CI pipeline** `p0-blocking` `setup` `M1`
- [#22](https://github.com/ahmdkaml/avoid-burnout/issues/22) **No Directory.Build.props** `p1-high` `setup` `M1`
- [#23](https://github.com/ahmdkaml/avoid-burnout/issues/23) **No Directory.Packages.props for central package management** `p1-high` `setup` `M1`
- [#26](https://github.com/ahmdkaml/avoid-burnout/issues/26) **Test framework not chosen** `p1-high` `setup` `M1`
- [#29](https://github.com/ahmdkaml/avoid-burnout/issues/29) **README is a single heading** `p1-high` `setup` `M1`
- [#31](https://github.com/ahmdkaml/avoid-burnout/issues/31) **No .gitignore** `p1-high` `setup` `M1`
- [#37](https://github.com/ahmdkaml/avoid-burnout/issues/37) **No packaging or publishing pipeline** `p1-high` `setup` `M1`
- [#39](https://github.com/ahmdkaml/avoid-burnout/issues/39) **No smoke test for a missing or corrupt config** `p1-high` `setup` `M1`
- [#175](https://github.com/ahmdkaml/avoid-burnout/issues/175) **Distribution format not chosen: single-file publish or framework-dependent** `p1-high` `setup` `M1`
- [#182](https://github.com/ahmdkaml/avoid-burnout/issues/182) **No auto-update mechanism defined** `p1-high` `setup` `M7`
- [#184](https://github.com/ahmdkaml/avoid-burnout/issues/184) **Dependency supply chain not pinned** `p1-high` `setup` `M1`
- [#21](https://github.com/ahmdkaml/avoid-burnout/issues/21) **No .editorconfig analyzer baseline** `p2-medium` `setup` `M1`
- [#25](https://github.com/ahmdkaml/avoid-burnout/issues/25) **No code coverage collection** `p2-medium` `setup` `M1`
- [#27](https://github.com/ahmdkaml/avoid-burnout/issues/27) **No formatting gate in CI** `p2-medium` `setup` `M1`
- [#33](https://github.com/ahmdkaml/avoid-burnout/issues/33) **No dependency update automation** `p2-medium` `setup` `M1`
- [#34](https://github.com/ahmdkaml/avoid-burnout/issues/34) **No CHANGELOG convention** `p2-medium` `setup` `M1`
- [#35](https://github.com/ahmdkaml/avoid-burnout/issues/35) **No check that the app runs without elevation** `p2-medium` `setup` `M1`
- [#36](https://github.com/ahmdkaml/avoid-burnout/issues/36) **No deterministic build or version stamping** `p2-medium` `setup` `M1`
- [#176](https://github.com/ahmdkaml/avoid-burnout/issues/176) **No build architecture matrix** `p2-medium` `setup` `M1`
- [#183](https://github.com/ahmdkaml/avoid-burnout/issues/183) **Update check requires a hosting endpoint** `p2-medium` `setup` `M7`
- [#28](https://github.com/ahmdkaml/avoid-burnout/issues/28) **No CONTRIBUTING.md** `p3-low` `setup` `M1`
- [#177](https://github.com/ahmdkaml/avoid-burnout/issues/177) **No crash dump and symbol story** `p3-low` `setup` `M7`

### 6. Architecture & Design Patterns (26)

Layer boundaries, abstractions and the decisions that make the core testable and the background loop safe.

- [#88](https://github.com/ahmdkaml/avoid-burnout/issues/88) **No solution structure separating domain from platform from UI** `p0-blocking` `arch` `M1`
- [#91](https://github.com/ahmdkaml/avoid-burnout/issues/91) **No IClock abstraction** `p0-blocking` `arch` `M1`
- [#162](https://github.com/ahmdkaml/avoid-burnout/issues/162) **No fake clock means no testable time logic** `p0-blocking` `arch` `M2`
- [#49](https://github.com/ahmdkaml/avoid-burnout/issues/49) **Process-to-category mapping has no maintainable home** `p1-high` `arch` `M4`
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
- [#160](https://github.com/ahmdkaml/avoid-burnout/issues/160) **No tests for settings migration** `p1-high` `arch` `M3`
- [#161](https://github.com/ahmdkaml/avoid-burnout/issues/161) **No test for concurrent settings access** `p1-high` `arch` `M3`
- [#180](https://github.com/ahmdkaml/avoid-burnout/issues/180) **Settings and classification files are untrusted input** `p1-high` `arch` `M3`
- [#102](https://github.com/ahmdkaml/avoid-burnout/issues/102) **No DI container decision** `p2-medium` `arch` `M1`
- [#105](https://github.com/ahmdkaml/avoid-burnout/issues/105) **Extensibility is unconsidered** `p2-medium` `arch` `M1`
- [#106](https://github.com/ahmdkaml/avoid-burnout/issues/106) **No localization plan, and strings are likely hardcoded** `p2-medium` `arch` `M1`
- [#107](https://github.com/ahmdkaml/avoid-burnout/issues/107) **Settings scope ambiguity: per user or per machine** `p2-medium` `arch` `M1`
- [#185](https://github.com/ahmdkaml/avoid-burnout/issues/185) **Single-instance IPC is unencrypted and world-visible** `p2-medium` `arch` `M7`

### 7. Activity & Idle Detection (22)

The premise of the product: deciding what the user is doing, and what counts as strain.

- [#45](https://github.com/ahmdkaml/avoid-burnout/issues/45) **"Activity" is never defined** `p0-blocking` `activity` `M0`
- [#47](https://github.com/ahmdkaml/avoid-burnout/issues/47) **Any input resets idle, so games never get a break** `p0-blocking` `activity` `M0`
- [#54](https://github.com/ahmdkaml/avoid-burnout/issues/54) **Lock and screen-saver events not handled** `p0-blocking` `activity` `M4`
- [#46](https://github.com/ahmdkaml/avoid-burnout/issues/46) **Idle detection needs GetLastInputInfo, with ~1s granularity** `p1-high` `activity` `M4`
- [#48](https://github.com/ahmdkaml/avoid-burnout/issues/48) **Foreground process detection not designed** `p1-high` `activity` `M4`
- [#50](https://github.com/ahmdkaml/avoid-burnout/issues/50) **Activity categories not enumerated** `p1-high` `activity` `M4`
- [#51](https://github.com/ahmdkaml/avoid-burnout/issues/51) **Default behaviour for the unknown category is undefined** `p1-high` `activity` `M4`
- [#58](https://github.com/ahmdkaml/avoid-burnout/issues/58) **Multi-monitor handling undefined** `p1-high` `activity` `M4`
- [#63](https://github.com/ahmdkaml/avoid-burnout/issues/63) **Continuous work block / sessionization not defined** `p1-high` `activity` `M2`
- [#65](https://github.com/ahmdkaml/avoid-burnout/issues/65) **Activity log has no growth or retention strategy** `p1-high` `activity` `M2`
- [#144](https://github.com/ahmdkaml/avoid-burnout/issues/144) **No quiet mode for calls and presentations** `p1-high` `activity` `M6`
- [#158](https://github.com/ahmdkaml/avoid-burnout/issues/158) **No unit tests for sessionization and the gap threshold** `p1-high` `activity` `M2`
- [#159](https://github.com/ahmdkaml/avoid-burnout/issues/159) **No unit tests for the activity classifier** `p1-high` `activity` `M2`
- [#52](https://github.com/ahmdkaml/avoid-burnout/issues/52) **Meeting detection needs a documented approach** `p2-medium` `activity` `M4`
- [#53](https://github.com/ahmdkaml/avoid-burnout/issues/53) **Video playback detection via window titles is fragile** `p2-medium` `activity` `M4`
- [#55](https://github.com/ahmdkaml/avoid-burnout/issues/55) **Exclusive fullscreen (games) detection has no public API** `p2-medium` `activity` `M4`
- [#57](https://github.com/ahmdkaml/avoid-burnout/issues/57) **Borderless fullscreen video must not be treated as a game** `p2-medium` `activity` `M4`
- [#62](https://github.com/ahmdkaml/avoid-burnout/issues/62) **No continuity model when the app is not running** `p2-medium` `activity` `M2`
- [#64](https://github.com/ahmdkaml/avoid-burnout/issues/64) **Idle-detection accuracy is undocumented** `p2-medium` `activity` `M4`
- [#56](https://github.com/ahmdkaml/avoid-burnout/issues/56) **RDP sessions change the meaning of idle** `p3-low` `activity` `M4`
- [#59](https://github.com/ahmdkaml/avoid-burnout/issues/59) **Multi-user and fast-user-switching not considered** `p3-low` `activity` `M4`
- [#60](https://github.com/ahmdkaml/avoid-burnout/issues/60) **Virtual machines blur input attribution** `p3-low` `activity` `M4`

### 8. Break Rules & Scheduling (19)

Interval and duration policy, sessionization, snooze, escalation, and the state machine around a break.

- [#71](https://github.com/ahmdkaml/avoid-burnout/issues/71) **Full-screen lockout breaks are considered a feature** `p0-blocking` `breakrules` `M0`
- [#157](https://github.com/ahmdkaml/avoid-burnout/issues/157) **No unit tests for the strain or interval algorithm** `p0-blocking` `breakrules` `M2`
- [#66](https://github.com/ahmdkaml/avoid-burnout/issues/66) **Default break interval is arbitrary and hardcoded by assumption** `p1-high` `breakrules` `M2`
- [#67](https://github.com/ahmdkaml/avoid-burnout/issues/67) **Default break duration is likewise arbitrary** `p1-high` `breakrules` `M2`
- [#69](https://github.com/ahmdkaml/avoid-burnout/issues/69) **Escalation after ignored breaks is undefined** `p1-high` `breakrules` `M2`
- [#72](https://github.com/ahmdkaml/avoid-burnout/issues/72) **No cap on back-to-back breaks** `p1-high` `breakrules` `M2`
- [#73](https://github.com/ahmdkaml/avoid-burnout/issues/73) **Does the timer pause during the break itself?** `p1-high` `breakrules` `M2`
- [#78](https://github.com/ahmdkaml/avoid-burnout/issues/78) **Quiet hours and Focus Assist not integrated** `p1-high` `breakrules` `M5`
- [#79](https://github.com/ahmdkaml/avoid-burnout/issues/79) **No timezone or DST handling in daily logic** `p1-high` `breakrules` `M2`
- [#81](https://github.com/ahmdkaml/avoid-burnout/issues/81) **System clock change mid-session is unhandled** `p1-high` `breakrules` `M2`
- [#113](https://github.com/ahmdkaml/avoid-burnout/issues/113) **Overlay over exclusive fullscreen may be impossible** `p1-high` `breakrules` `M5`
- [#137](https://github.com/ahmdkaml/avoid-burnout/issues/137) **The break screen does not say what to actually do** `p1-high` `breakrules` `M6`
- [#152](https://github.com/ahmdkaml/avoid-burnout/issues/152) **No design against alert fatigue** `p1-high` `breakrules` `M5`
- [#179](https://github.com/ahmdkaml/avoid-burnout/issues/179) **Settings values are not validated** `p1-high` `breakrules` `M3`
- [#70](https://github.com/ahmdkaml/avoid-burnout/issues/70) **Snooze semantics not defined** `p2-medium` `breakrules` `M2`
- [#74](https://github.com/ahmdkaml/avoid-burnout/issues/74) **No cumulative strain model** `p2-medium` `breakrules` `M2`
- [#75](https://github.com/ahmdkaml/avoid-burnout/issues/75) **No daily cap on break count** `p2-medium` `breakrules` `M2`
- [#76](https://github.com/ahmdkaml/avoid-burnout/issues/76) **No per-activity rule differentiation** `p2-medium` `breakrules` `M2`
- [#77](https://github.com/ahmdkaml/avoid-burnout/issues/77) **System accessibility settings not respected** `p2-medium` `breakrules` `M6`

### 9. Windows Platform Integration (21)

Tray, overlay, DPI, power and session events, autostart, hotkeys, single instance.

- [#119](https://github.com/ahmdkaml/avoid-burnout/issues/119) **Power events (suspend and resume) not handled** `p0-blocking` `winapi` `M4`
- [#150](https://github.com/ahmdkaml/avoid-burnout/issues/150) **Break surface can interrupt work that cannot be paused** `p0-blocking` `winapi` `M5`
- [#108](https://github.com/ahmdkaml/avoid-burnout/issues/108) **Autostart registration method not chosen** `p1-high` `winapi` `M1`
- [#109](https://github.com/ahmdkaml/avoid-burnout/issues/109) **Autostart must be opt-in, never pre-enabled** `p1-high` `winapi` `M1`
- [#111](https://github.com/ahmdkaml/avoid-burnout/issues/111) **DPI awareness not set** `p1-high` `winapi` `M5`
- [#112](https://github.com/ahmdkaml/avoid-burnout/issues/112) **Overlay window will steal focus unless carefully created** `p1-high` `winapi` `M5`
- [#114](https://github.com/ahmdkaml/avoid-burnout/issues/114) **Toast notifications from an unpackaged app need a registered AUMID** `p1-high` `winapi` `M5`
- [#117](https://github.com/ahmdkaml/avoid-burnout/issues/117) **No plan for the user hiding the tray icon** `p1-high` `winapi` `M5`
- [#118](https://github.com/ahmdkaml/avoid-burnout/issues/118) **Tray balloon notifications are unreliable on Windows 11** `p1-high` `winapi` `M5`
- [#120](https://github.com/ahmdkaml/avoid-burnout/issues/120) **Display topology changes while the overlay is showing** `p1-high` `winapi` `M5`
- [#122](https://github.com/ahmdkaml/avoid-burnout/issues/122) **Session lock and unlock event ordering not handled** `p1-high` `winapi` `M4`
- [#124](https://github.com/ahmdkaml/avoid-burnout/issues/124) **Startup race with the shell at boot** `p1-high` `winapi` `M5`
- [#163](https://github.com/ahmdkaml/avoid-burnout/issues/163) **No integration test for suspend and resume** `p1-high` `winapi` `M4`
- [#167](https://github.com/ahmdkaml/avoid-burnout/issues/167) **No Windows version test matrix** `p1-high` `winapi` `M7`
- [#170](https://github.com/ahmdkaml/avoid-burnout/issues/170) **No negative tests for locked session and fullscreen** `p1-high` `winapi` `M4`
- [#110](https://github.com/ahmdkaml/avoid-burnout/issues/110) **Resident tray process vs scheduled task** `p2-medium` `winapi` `M0`
- [#115](https://github.com/ahmdkaml/avoid-burnout/issues/115) **Notification click-through has no defined behaviour** `p2-medium` `winapi` `M5`
- [#116](https://github.com/ahmdkaml/avoid-burnout/issues/116) **Global hotkey handling not designed** `p2-medium` `winapi` `M5`
- [#121](https://github.com/ahmdkaml/avoid-burnout/issues/121) **DPI change while running not handled** `p2-medium` `winapi` `M5`
- [#123](https://github.com/ahmdkaml/avoid-burnout/issues/123) **No policy for power-saving mode** `p2-medium` `winapi` `M4`
- [#169](https://github.com/ahmdkaml/avoid-burnout/issues/169) **No multi-monitor overlay placement test** `p2-medium` `winapi` `M7`

### 10. Notifications, Tray & Reminders (7)

How a reminder reaches the user, how loud it is, and how to get it to stop.

- [#151](https://github.com/ahmdkaml/avoid-burnout/issues/151) **Reminders must be non-blocking by default** `p0-blocking` `notify` `M5`
- [#141](https://github.com/ahmdkaml/avoid-burnout/issues/141) **No test-notification button in settings** `p1-high` `notify` `M6`
- [#145](https://github.com/ahmdkaml/avoid-burnout/issues/145) **Tray menu contents not specified** `p1-high` `notify` `M5`
- [#153](https://github.com/ahmdkaml/avoid-burnout/issues/153) **Suppressed-by-DND breaks have no defined status** `p1-high` `notify` `M5`
- [#154](https://github.com/ahmdkaml/avoid-burnout/issues/154) **Notification copy does not state the action** `p1-high` `notify` `M5`
- [#155](https://github.com/ahmdkaml/avoid-burnout/issues/155) **Notification text is not localized** `p2-medium` `notify` `M5`
- [#156](https://github.com/ahmdkaml/avoid-burnout/issues/156) **No notification priority or channel decision** `p2-medium` `notify` `M5`

### 11. UX & Accessibility (17)

First run, the pause control, accessibility, and every empty/error state.

- [#135](https://github.com/ahmdkaml/avoid-burnout/issues/135) **Pause control is not discoverable** `p0-blocking` `ux` `M5`
- [#130](https://github.com/ahmdkaml/avoid-burnout/issues/130) **No in-app statement that screen content is never captured** `p1-high` `ux` `M3`
- [#133](https://github.com/ahmdkaml/avoid-burnout/issues/133) **No first-run onboarding** `p1-high` `ux` `M6`
- [#134](https://github.com/ahmdkaml/avoid-burnout/issues/134) **Onboarding does not disclose what data is collected** `p1-high` `ux` `M6`
- [#142](https://github.com/ahmdkaml/avoid-burnout/issues/142) **No screen reader support for the overlay** `p1-high` `ux` `M6`
- [#143](https://github.com/ahmdkaml/avoid-burnout/issues/143) **Overlay is not designed for keyboard-only operation** `p1-high` `ux` `M6`
- [#168](https://github.com/ahmdkaml/avoid-burnout/issues/168) **No DPI matrix test** `p1-high` `ux` `M6`
- [#87](https://github.com/ahmdkaml/avoid-burnout/issues/87) **No empty or calibration state for new users** `p2-medium` `ux` `M6`
- [#136](https://github.com/ahmdkaml/avoid-burnout/issues/136) **Pause duration options not defined** `p2-medium` `ux` `M6`
- [#140](https://github.com/ahmdkaml/avoid-burnout/issues/140) **Settings surface has no scope limit** `p2-medium` `ux` `M6`
- [#146](https://github.com/ahmdkaml/avoid-burnout/issues/146) **Interval setting has no explanation** `p2-medium` `ux` `M6`
- [#147](https://github.com/ahmdkaml/avoid-burnout/issues/147) **Onboarding does not preview the break screen** `p2-medium` `ux` `M6`
- [#148](https://github.com/ahmdkaml/avoid-burnout/issues/148) **Time to first break is long** `p2-medium` `ux` `M6`
- [#149](https://github.com/ahmdkaml/avoid-burnout/issues/149) **Empty and error states are not listed anywhere** `p2-medium` `ux` `M6`
- [#164](https://github.com/ahmdkaml/avoid-burnout/issues/164) **No UI automation test for the overlay** `p2-medium` `ux` `M6`
- [#178](https://github.com/ahmdkaml/avoid-burnout/issues/178) **No performance budget for the overlay render** `p2-medium` `ux` `M5`
- [#139](https://github.com/ahmdkaml/avoid-burnout/issues/139) **Snooze and streak interaction is undefined** `p3-low` `ux` `M8`

### 12. Scoring, History & Reports (4)

Data model, scoring, export, and whether reporting is in v1 at all.

- [#80](https://github.com/ahmdkaml/avoid-burnout/issues/80) **No strain scoring formula** `p1-high` `reporting` `M2`
- [#83](https://github.com/ahmdkaml/avoid-burnout/issues/83) **No export format for history** `p1-high` `reporting` `M3`
- [#86](https://github.com/ahmdkaml/avoid-burnout/issues/86) **Streak rules across timezone and DST are undefined** `p2-medium` `reporting` `M8`
- [#84](https://github.com/ahmdkaml/avoid-burnout/issues/84) **Charting library decision not made** `p3-low` `reporting` `M8`

### 13. Privacy & Data Handling (5)

What is collected, where it lives, how long it is kept, and how to delete it.

- [#125](https://github.com/ahmdkaml/avoid-burnout/issues/125) **No consent screen for activity tracking** `p0-blocking` `privacy` `M3`
- [#126](https://github.com/ahmdkaml/avoid-burnout/issues/126) **Telemetry decision not made** `p0-blocking` `privacy` `M0`
- [#132](https://github.com/ahmdkaml/avoid-burnout/issues/132) **Unsigned binary will be quarantined by SmartScreen** `p1-high` `privacy` `M7`
- [#127](https://github.com/ahmdkaml/avoid-burnout/issues/127) **If telemetry is on, the PII surface is undefined** `p2-medium` `privacy` `M3`
- [#128](https://github.com/ahmdkaml/avoid-burnout/issues/128) **No decision on encryption at rest for history** `p2-medium` `privacy` `M3`

### 14. Testing & QA (2)

What is proven versus what is hoped, across the matrices that actually break this class of app.

- [#166](https://github.com/ahmdkaml/avoid-burnout/issues/166) **No memory leak check on the break path** `p1-high` `testing` `M7`
- [#165](https://github.com/ahmdkaml/avoid-burnout/issues/165) **No soak test** `p2-medium` `testing` `M7`

### 15. Performance & Distribution (4)

Memory, CPU, startup time and distribution size targets for a process that runs all day.

- [#171](https://github.com/ahmdkaml/avoid-burnout/issues/171) **No idle memory target** `p2-medium` `perf` `M7`
- [#172](https://github.com/ahmdkaml/avoid-burnout/issues/172) **No CPU-when-idle target** `p2-medium` `perf` `M7`
- [#173](https://github.com/ahmdkaml/avoid-burnout/issues/173) **Poll interval versus battery life tradeoff is undocumented** `p2-medium` `perf` `M7`
- [#174](https://github.com/ahmdkaml/avoid-burnout/issues/174) **No startup time target** `p3-low` `perf` `M7`

### 16. Security & Supply Chain (2)

Input validation, signing, updates and the dependency chain for a resident background app.

- [#181](https://github.com/ahmdkaml/avoid-burnout/issues/181) **No code signing** `p1-high` `security` `M7`
- [#186](https://github.com/ahmdkaml/avoid-burnout/issues/186) **No obfuscation decision** `p3-low` `security` `M7`

## The blocking path

25 issues are `p0-blocking`. They are not equally blocking - these are the ones that gate other work:

| Issue | Why it gates |
|---|---|
| #6 | name the product correctly, before the identity is baked into an exe, an AUMID and a signing identity |
| #207 | agree the v1 cut line, so M1-M6 are not built against a moving target |
| #38 | choose the UI framework, since it decides packaging, overlay behaviour and testability |
| #45 | define what "activity" means; every rule in M2 and every detector in M4 depends on it |
| #47 | fix the premise that input alone can drive breaks, or games never get one |
| #88 | split domain from platform from UI, before detection code exists and the boundary gets expensive |
| #91 | introduce `IClock`, before any timing code is written without it |
| #119 | handle suspend/resume, or the first user to close their laptop gets a burst of reminders |
| #125 | consent before collection, not after |
| #126 | telemetry decision, which constrains the privacy posture and the store declaration |
| #135 | make pause reachable from the tray, or users uninstall instead of pausing |
| #150 | design the break surface so it cannot interrupt unpausable work |
| #151 | non-blocking reminders by default |
| #162 | a `FakeClock`, without which none of the timing tests are writable |
| #196 | ban blue-light filtering; the claim is false and it is a legal problem |
| #157 | table-driven tests for the interval algorithm |

## Cross-cutting concerns

An issue is filed under one primary area but can carry several. This table gives the full membership of every area label, so the subject categories above never hide work.

| Area label | Tagged | Primary here | Also cross-cutting | Milestones |
|---|---:|---:|---:|---|
| `area:product` | 21 | 21 | 0 | M0, M1, M4, M5, M6, M8 |
| `area:branding` | 18 | 18 | 0 | M0, M5, M6, M7 |
| `area:legal` | 15 | 9 | 6 | M0, M1, M3, M7 |
| `area:framework` | 6 | 6 | 0 | M0 |
| `area:setup` | 27 | 25 | 2 | M0, M1, M7 |
| `area:arch` | 27 | 26 | 1 | M0, M1, M2, M3, M4, M7 |
| `area:activity` | 26 | 22 | 4 | M0, M2, M4, M6 |
| `area:breakrules` | 23 | 19 | 4 | M0, M2, M3, M5, M6, M7 |
| `area:winapi` | 29 | 21 | 8 | M0, M1, M4, M5, M7, M8 |
| `area:notify` | 17 | 7 | 10 | M0, M2, M5, M6 |
| `area:ux` | 38 | 17 | 21 | M0, M1, M2, M3, M5, M6, M7, M8 |
| `area:reporting` | 12 | 4 | 8 | M0, M2, M3, M6, M8 |
| `area:privacy` | 12 | 5 | 7 | M0, M1, M3, M6, M7 |
| `area:testing` | 21 | 2 | 19 | M0, M1, M2, M3, M4, M6, M7 |
| `area:perf` | 16 | 4 | 12 | M0, M1, M4, M5, M7, M8 |
| `area:security` | 10 | 2 | 8 | M1, M3, M7 |

### `area:testing` - all 21 tagged

- [#91](https://github.com/ahmdkaml/avoid-burnout/issues/91) **No IClock abstraction** `p0-blocking` `M1` _(filed under arch)_
- [#157](https://github.com/ahmdkaml/avoid-burnout/issues/157) **No unit tests for the strain or interval algorithm** `p0-blocking` `M2` _(filed under breakrules)_
- [#162](https://github.com/ahmdkaml/avoid-burnout/issues/162) **No fake clock means no testable time logic** `p0-blocking` `M2` _(filed under arch)_
- [#26](https://github.com/ahmdkaml/avoid-burnout/issues/26) **Test framework not chosen** `p1-high` `M1` _(filed under setup)_
- [#39](https://github.com/ahmdkaml/avoid-burnout/issues/39) **No smoke test for a missing or corrupt config** `p1-high` `M1` _(filed under setup)_
- [#44](https://github.com/ahmdkaml/avoid-burnout/issues/44) **Framework choice determines headless testability** `p1-high` `M0` _(filed under framework)_
- [#89](https://github.com/ahmdkaml/avoid-burnout/issues/89) **Core must not reference UI or Win32 types** `p1-high` `M1` _(filed under arch)_
- [#142](https://github.com/ahmdkaml/avoid-burnout/issues/142) **No screen reader support for the overlay** `p1-high` `M6` _(filed under ux)_
- [#158](https://github.com/ahmdkaml/avoid-burnout/issues/158) **No unit tests for sessionization and the gap threshold** `p1-high` `M2` _(filed under activity)_
- [#159](https://github.com/ahmdkaml/avoid-burnout/issues/159) **No unit tests for the activity classifier** `p1-high` `M2` _(filed under activity)_
- [#160](https://github.com/ahmdkaml/avoid-burnout/issues/160) **No tests for settings migration** `p1-high` `M3` _(filed under arch)_
- [#161](https://github.com/ahmdkaml/avoid-burnout/issues/161) **No test for concurrent settings access** `p1-high` `M3` _(filed under arch)_
- [#163](https://github.com/ahmdkaml/avoid-burnout/issues/163) **No integration test for suspend and resume** `p1-high` `M4` _(filed under winapi)_
- [#166](https://github.com/ahmdkaml/avoid-burnout/issues/166) **No memory leak check on the break path** `p1-high` `M7`
- [#167](https://github.com/ahmdkaml/avoid-burnout/issues/167) **No Windows version test matrix** `p1-high` `M7` _(filed under winapi)_
- [#168](https://github.com/ahmdkaml/avoid-burnout/issues/168) **No DPI matrix test** `p1-high` `M6` _(filed under ux)_
- [#170](https://github.com/ahmdkaml/avoid-burnout/issues/170) **No negative tests for locked session and fullscreen** `p1-high` `M4` _(filed under winapi)_
- [#25](https://github.com/ahmdkaml/avoid-burnout/issues/25) **No code coverage collection** `p2-medium` `M1` _(filed under setup)_
- [#164](https://github.com/ahmdkaml/avoid-burnout/issues/164) **No UI automation test for the overlay** `p2-medium` `M6` _(filed under ux)_
- [#165](https://github.com/ahmdkaml/avoid-burnout/issues/165) **No soak test** `p2-medium` `M7`
- [#169](https://github.com/ahmdkaml/avoid-burnout/issues/169) **No multi-monitor overlay placement test** `p2-medium` `M7` _(filed under winapi)_

### `area:perf` - all 16 tagged

- [#37](https://github.com/ahmdkaml/avoid-burnout/issues/37) **No packaging or publishing pipeline** `p1-high` `M1` _(filed under setup)_
- [#98](https://github.com/ahmdkaml/avoid-burnout/issues/98) **Log file location, rotation and size cap undefined** `p1-high` `M1` _(filed under arch)_
- [#166](https://github.com/ahmdkaml/avoid-burnout/issues/166) **No memory leak check on the break path** `p1-high` `M7` _(filed under testing)_
- [#175](https://github.com/ahmdkaml/avoid-burnout/issues/175) **Distribution format not chosen: single-file publish or framework-dependent** `p1-high` `M1` _(filed under setup)_
- [#36](https://github.com/ahmdkaml/avoid-burnout/issues/36) **No deterministic build or version stamping** `p2-medium` `M1` _(filed under setup)_
- [#110](https://github.com/ahmdkaml/avoid-burnout/issues/110) **Resident tray process vs scheduled task** `p2-medium` `M0` _(filed under winapi)_
- [#123](https://github.com/ahmdkaml/avoid-burnout/issues/123) **No policy for power-saving mode** `p2-medium` `M4` _(filed under winapi)_
- [#165](https://github.com/ahmdkaml/avoid-burnout/issues/165) **No soak test** `p2-medium` `M7` _(filed under testing)_
- [#171](https://github.com/ahmdkaml/avoid-burnout/issues/171) **No idle memory target** `p2-medium` `M7`
- [#172](https://github.com/ahmdkaml/avoid-burnout/issues/172) **No CPU-when-idle target** `p2-medium` `M7`
- [#173](https://github.com/ahmdkaml/avoid-burnout/issues/173) **Poll interval versus battery life tradeoff is undocumented** `p2-medium` `M7`
- [#176](https://github.com/ahmdkaml/avoid-burnout/issues/176) **No build architecture matrix** `p2-medium` `M1` _(filed under setup)_
- [#178](https://github.com/ahmdkaml/avoid-burnout/issues/178) **No performance budget for the overlay render** `p2-medium` `M5` _(filed under ux)_
- [#84](https://github.com/ahmdkaml/avoid-burnout/issues/84) **Charting library decision not made** `p3-low` `M8` _(filed under reporting)_
- [#174](https://github.com/ahmdkaml/avoid-burnout/issues/174) **No startup time target** `p3-low` `M7`
- [#177](https://github.com/ahmdkaml/avoid-burnout/issues/177) **No crash dump and symbol story** `p3-low` `M7` _(filed under setup)_

### `area:security` - all 10 tagged

- [#132](https://github.com/ahmdkaml/avoid-burnout/issues/132) **Unsigned binary will be quarantined by SmartScreen** `p1-high` `M7` _(filed under privacy)_
- [#179](https://github.com/ahmdkaml/avoid-burnout/issues/179) **Settings values are not validated** `p1-high` `M3` _(filed under breakrules)_
- [#180](https://github.com/ahmdkaml/avoid-burnout/issues/180) **Settings and classification files are untrusted input** `p1-high` `M3` _(filed under arch)_
- [#181](https://github.com/ahmdkaml/avoid-burnout/issues/181) **No code signing** `p1-high` `M7`
- [#182](https://github.com/ahmdkaml/avoid-burnout/issues/182) **No auto-update mechanism defined** `p1-high` `M7` _(filed under setup)_
- [#184](https://github.com/ahmdkaml/avoid-burnout/issues/184) **Dependency supply chain not pinned** `p1-high` `M1` _(filed under setup)_
- [#33](https://github.com/ahmdkaml/avoid-burnout/issues/33) **No dependency update automation** `p2-medium` `M1` _(filed under setup)_
- [#183](https://github.com/ahmdkaml/avoid-burnout/issues/183) **Update check requires a hosting endpoint** `p2-medium` `M7` _(filed under setup)_
- [#185](https://github.com/ahmdkaml/avoid-burnout/issues/185) **Single-instance IPC is unencrypted and world-visible** `p2-medium` `M7` _(filed under arch)_
- [#186](https://github.com/ahmdkaml/avoid-burnout/issues/186) **No obfuscation decision** `p3-low` `M7`

### `area:privacy` - all 12 tagged

- [#125](https://github.com/ahmdkaml/avoid-burnout/issues/125) **No consent screen for activity tracking** `p0-blocking` `M3`
- [#126](https://github.com/ahmdkaml/avoid-burnout/issues/126) **Telemetry decision not made** `p0-blocking` `M0`
- [#83](https://github.com/ahmdkaml/avoid-burnout/issues/83) **No export format for history** `p1-high` `M3` _(filed under reporting)_
- [#99](https://github.com/ahmdkaml/avoid-burnout/issues/99) **Logs will contain window titles, which is PII** `p1-high` `M1` _(filed under arch)_
- [#129](https://github.com/ahmdkaml/avoid-burnout/issues/129) **No data export, deletion, or forget-me path** `p1-high` `M3` _(filed under legal)_
- [#130](https://github.com/ahmdkaml/avoid-burnout/issues/130) **No in-app statement that screen content is never captured** `p1-high` `M3` _(filed under ux)_
- [#132](https://github.com/ahmdkaml/avoid-burnout/issues/132) **Unsigned binary will be quarantined by SmartScreen** `p1-high` `M7`
- [#134](https://github.com/ahmdkaml/avoid-burnout/issues/134) **Onboarding does not disclose what data is collected** `p1-high` `M6` _(filed under ux)_
- [#107](https://github.com/ahmdkaml/avoid-burnout/issues/107) **Settings scope ambiguity: per user or per machine** `p2-medium` `M1` _(filed under arch)_
- [#127](https://github.com/ahmdkaml/avoid-burnout/issues/127) **If telemetry is on, the PII surface is undefined** `p2-medium` `M3`
- [#128](https://github.com/ahmdkaml/avoid-burnout/issues/128) **No decision on encryption at rest for history** `p2-medium` `M3`
- [#131](https://github.com/ahmdkaml/avoid-burnout/issues/131) **No privacy declaration for a store submission** `p2-medium` `M7` _(filed under legal)_

### `area:legal` - all 15 tagged

- [#196](https://github.com/ahmdkaml/avoid-burnout/issues/196) **Blue light filtering must not be a feature** `p0-blocking` `M0` _(filed under product)_
- [#5](https://github.com/ahmdkaml/avoid-burnout/issues/5) **Name implies prevention of a medical condition** `p1-high` `M0` _(filed under branding)_
- [#15](https://github.com/ahmdkaml/avoid-burnout/issues/15) **Health-claim copy needs review** `p1-high` `M0` _(filed under branding)_
- [#30](https://github.com/ahmdkaml/avoid-burnout/issues/30) **No LICENSE file** `p1-high` `M1`
- [#68](https://github.com/ahmdkaml/avoid-burnout/issues/68) **No provenance or citation for the 20-20-20 rule** `p1-high` `M7`
- [#129](https://github.com/ahmdkaml/avoid-burnout/issues/129) **No data export, deletion, or forget-me path** `p1-high` `M3`
- [#187](https://github.com/ahmdkaml/avoid-burnout/issues/187) **Health claims need a defined boundary** `p1-high` `M0` _(filed under branding)_
- [#188](https://github.com/ahmdkaml/avoid-burnout/issues/188) **No medical disclaimer** `p1-high` `M0`
- [#189](https://github.com/ahmdkaml/avoid-burnout/issues/189) **No terms of privacy or EULA** `p1-high` `M7`
- [#4](https://github.com/ahmdkaml/avoid-burnout/issues/4) **Trademark search not done** `p2-medium` `M7` _(filed under branding)_
- [#131](https://github.com/ahmdkaml/avoid-burnout/issues/131) **No privacy declaration for a store submission** `p2-medium` `M7`
- [#190](https://github.com/ahmdkaml/avoid-burnout/issues/190) **20-20-20 rule attribution not documented** `p2-medium` `M7`
- [#191](https://github.com/ahmdkaml/avoid-burnout/issues/191) **No accessibility compliance target** `p2-medium` `M7`
- [#199](https://github.com/ahmdkaml/avoid-burnout/issues/199) **Team or employer dashboard has surveillance implications** `p2-medium` `M0` _(filed under product)_
- [#192](https://github.com/ahmdkaml/avoid-burnout/issues/192) **No age rating or not-for-under-13 statement** `p3-low` `M7`

## Where to start

Close M0 first. It contains no code, it is the cheapest thing in the repo to finish, and two of its issues (#38, #207) invalidate work started before they close.

```
gh issue list --milestone 'M0: Product, Scope & Legal Decisions' --state open
gh issue list --label p0-blocking --state open
```
