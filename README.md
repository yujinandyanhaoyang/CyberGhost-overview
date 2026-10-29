# CyberGhost

Task continuity across authorized hosts — toward real hardware.

English | [简体中文](README.zh-CN.md)

CyberGhost is an independent research prototype for carrying task goals, confirmed facts and progress from one execution host to another. The aim is to let a software agent resume work on an authorized device without losing track of what happened, what remains uncertain and what should happen next.

Consider an interrupted device task: the device may have acted even when the application received no result. Before retrying or handing the task to another host, the application needs to establish the original outcome and who is authorized to continue. This is the problem CyberGhost investigates.

**Status — October 30, 2026:** limited software and official ROS 2 mock experiments, plus read-only state reception on Linux and Windows, have passed project-internal reviews. Live execution across machines and physical hardware experiments have not yet been validated.

## What has been demonstrated

| Capability | Observed result | Scope |
|---|---|---|
| Recovery and handoff to a newly started receiver | Host A recovered persisted pending state after exiting at a fixed failure point, confirmed the original result and then started host B to continue | October 25; one VM, fixed mock controller, one failure location |
| Portable state reception | The same delivered code produced matching results for eight CLI cases on Linux and Windows. A 2,533-byte transfer preserved the original goal, memory and progress, and derived the next action | October 25; read-only reception, no device command or control authorization |
| Pending-result and owner checks | Earlier versions withheld handoff when results were unknown and rejected requests from the previous controller at a cooperating gateway | Separate experiments; not a combined guarantee for the latest version |

The implementation currently uses explicit protocols, structured state and hand-written policies. It does not train a model or provide general-purpose autonomous robot planning. Fixed-point A/B recovery was accepted in a separate October 27 same-VM mock version. The October 28 execution-adapter review also accepted three bounded normal/restart/unknown cases on one designated VM: two goal submissions and four result queries in total, with no resubmission after the tested client restart. These are separate versioned results, not a combined cross-machine guarantee.

The October 28 unknown-result case used historical predecessor state; it was not a new end-to-end A→B handoff. Server restart, cancellation, arbitrary crashes and physical actions were outside that experiment. The source and full records remain private; the result is suitable for an interface discussion, not a ready-to-install public release.

## Looking for a small hardware collaboration

We are looking for a **second execution node with permission to deploy an application, preserve state, restart the application and retrieve logs**, together with an agreed communication path between hosts.

Suitable starting points include an existing Linux/Python edge board, small computer or remotely accessible test node. Architecture and dependencies need review; we do not assume every board can run the full ROS stack. A loan, supervised remote session or interface review can be useful — donated hardware is not a prerequisite.

The next step is observable, low-energy input/output: for example, an onboard input and a display or indicator, followed by a supported actuator when appropriate. Sensing alone would be reported as sensing validation, not physical action continuity. Receiving a state file never grants control permission.

**A useful first response:** a public environment/SDK link, the permitted deployment and access model, and a technical contact. An asynchronous review or a roughly 30-minute discussion is enough to assess fit. After that, we can discuss a supervised session of up to half a day; preparation, scope and timing would be agreed separately.

In return, we propose a versioned interface behavior report, minimal reproductions where needed, a comparison against a native or single-host baseline, and a mutually agreed integration guide. Any savings in recovery effort or improvement in reliability must be measured, not assumed.

[Collaboration scope and resource checklist →](COOPERATION.md)

## From software evidence to physical results

The planned sequence is: confirm the second node and transport → verify state and authorization with outputs disabled → perform an approved physical output → compare normal execution with a bounded interruption/recovery case. Device findings go back into the software work; fixes are then retested on the same device.

No device or experiment slot is currently confirmed in our records. Mock behavior does not establish physical braking, stopping distance or safety. Device-specific permissions, supervision and an independent stop mechanism must be agreed before actuator tests. If an existing SDK or persistent task coordinator already solves the problem, that is a useful result too.

## Repository and evidence

This repository contains the public project overview and collaboration materials. It is **not an installable software release**. The research source and complete experimental records remain private; there is no public quick-start or independently reproducible release here yet.

Results above are scoped internal reviews, not third-party certification. Earlier failures remain recorded, and results from different versions are not combined into a single reliability claim. Detailed historical summaries are currently available in Chinese:

- [Software status and limitations (中文)](SOFTWARE_STATUS.md)
- [Version anchors and failed experiments (中文)](EVIDENCE_GUIDE.md)
- [Earlier experiment walkthrough (中文)](WALKTHROUGH.md)

Source publication, licensing and any partner deliverables would be agreed separately. No license to unpublished source is granted by this overview.

## Contact

**yujin / 余烬 — independent developer, Hangzhou, China (UTC+8)**

[vennai26@163.com](mailto:vennai26@163.com)

Open to remote collaboration internationally; available for in-person discussions or supervised sessions in Zhejiang and Shanghai, China. Please share public documentation rather than credentials, restricted logs or personal identification in public issues.
