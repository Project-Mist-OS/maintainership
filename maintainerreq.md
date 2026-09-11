# MistOS Official Maintainer Requirements
**Version 1.1** | Last Updated: 23/05/26

> **Maintainers are required to check this document regularly. If any rule or update is missed due to not reading this document, it is solely the maintainer's responsibility.**

---

## 📋 Requirements

Baseline criteria you must meet before applying for official maintainership.

### Requirement Levels

| Level | Meaning |
|-------|---------|
| 🔴 **R1 — Compulsory** | Mandatory, no exceptions |
| 🟠 **R2 — Needed** | Required, but exceptions can be made |
| 🟡 **R3 — Advised** | Recommended but not compulsory |

---

**1. Device Ownership** — 🔴 R1
You **MUST** own the device. Unified builds and devices with minimal hardware differences are permitted.

**2. Git Knowledge** — 🔴 R2
You must know basic Git operations (cherry-pick, squash, rebase, etc.) and keep your trees clean.

**3. Prior ROM Building Experience** — 🟠 R2
You should have a demonstrated history of building and maintaining ROMs, not just for this device. First-time builders with no prior experience are strongly discouraged from applying for official maintainership.

**4. Unofficial Build (1-Week Minimum)** — 🔴 R1
You **MUST** have a daily-drivable unofficial build publicly released for **at least 1 week** before applying.

**5. Open Source Trees** — 🔴 R1
**ALL** your trees (device, kernel, vendor) **MUST** be open source at the time of application and remain so.

**6. Meet All General Requirements** — 🔴 R1
You **MUST** meet all requirements listed in [requirements.md](requirements.md).

---

## 📏 Rules

Rules that apply throughout your maintainership. Violations carry consequences based on severity.

### Violation Levels

| Level | Consequence |
|-------|-------------|
| 🔴 **L1 — Critical** | Immediate removal with prior notice |
| 🟠 **L2 — Major** | 3 warnings then removal |
| 🟡 **L3 — Minor** | Not recommended; repeated violations may escalate |

---

### 🔧 Technical Rules

**1. SELinux Enforcing** — 🟠 L2
Builds **MUST** ship SELinux **Enforcing**. Exceptions may be granted for legacy devices — request approval before shipping.

**2. No Prebuilt Kernels** — 🟠 L2
Prebuilt kernels are only allowed if **no working kernel sources exist**. Shipping a prebuilt to save build time is not acceptable.

**3. No Personal/Unofficial Builds on Official Channels** — 🟠 L2
Maintainers **MUST NOT** release personal, test, or unofficial builds through the official device community channels. Official channels are strictly for MistOS official releases only.

**4. Trees Must Be Pushed to MistOS Devices Org** — 🔴 L1
Maintainers **MUST** push and maintain their trees on the **official MistOS devices organization on GitHub**. This is required for Jenkins to function correctly.

**5. Force Pushes** — 🟡 L3
Force-pushing or destructive history rewrites to trees are not recommended. If absolutely necessary, notify the team beforehand to avoid silently breaking Jenkins builds.

**6. OTA Commit Message Format** — 🟠 L2
All OTA commits must follow the format below strictly:

```
{codename}: DD/MM/YY Update -{build tag}(Optional)
```

> **Example:** `haydn: 23/05/26 Update v4.7-Aether`

Incorrect commit messages will be flagged and must be corrected before the build goes live.

**7. Changelog Requirement** — 🔴 L1
Every release **MUST** include a changelog. Known bugs must be documented and made accessible to users. Releasing without a changelog is not acceptable.

**8. Release Cadence** — 🟠 L2
Maintainers are expected to release builds at a reasonable and consistent frequency. If **2 consecutive updates are missed without any prior communication to the team**, the maintainer may be removed **without notice**.

**9. Community Reputation** — 🟠 L2
Maintainers must hold a good reputation in the community. Reports of blind building, misrepresenting build quality, or improper behavior will result in a warning and potential removal if repeated.

---

### 🗣️ Conduct Rules

**10. Respect Toward Core Team Members** — 🔴 L1
Maintainers **MUST** communicate politely and respectfully with all core team members at all times. The following are strictly prohibited:
- Racism or discriminatory language of any kind
- Spamming the same request repeatedly — a reminder after a reasonable time is acceptable, repeated spamming is not

**11. Respect Toward Fellow Maintainers** — 🟠 L2
All maintainers must treat each other with respect in the group. Personal matters, grudges, or disputes between individuals are **not** to be brought into the maintainers group.

**12. Language in Maintainers Group** — 🟠 L2
All conversations related to **device issues, source problems, or technical reports** must be in **English**. Off-topic conversations may be in any language.

**13. Respond to Announcements & Tags** — 🟠 L2
Maintainers are required to respond to announcements, polls, and direct tags in the maintainers group. A response is not expected immediately but should be provided **as soon as reasonably possible**.

**14. Inactive Maintainer Notice** — 🟠 L2
If a maintainer is going to be unavailable for an extended period, they **MUST** inform the team in advance. Going silent for **30+ days without any notice** will trigger a warning and potential removal.

**15. Personal Matters in Group** — 🟡 L3
Maintainers are advised not to discuss or disclose personal matters in the maintainers group. Keep the group focused and professional.

---

### 👥 Co-Maintainership

- A device may have a maximum of **2 co-maintainers**.
- Both co-maintainers share equal responsibility for the device — violations apply to both.
- One maintainer must be designated as the **primary contact** for the team.
- Co-maintainer requests must be approved by a core team member before being recognized officially.

---

### 🚪 Resignation

If a maintainer wishes to step down, they **MUST** inform any **Core Team member** directly before leaving. Silently abandoning a device without notice is not acceptable and may affect future applications. The team will then arrange handoff or mark the device as unmaintained.

---

## Enforcement

- **L1 violations** — Device is immediately unlisted. Maintainer is notified and may appeal within **14 days**.
- **L2 violations** — Strike 1: warning (7 days to fix) → Strike 2: formal warning (3 days, build may be unlisted) → Strike 3: removal. Strikes clear after **60 days** of clean maintainership.
- **L3 violations** — Advisory notice issued. Persistent negligence escalates to L2.

> Exceptions to any rule must be requested and approved **before** shipping the affected build.
