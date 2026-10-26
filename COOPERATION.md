# A small collaboration to test task continuity on hardware

English | [简体中文](COOPERATION.zh-CN.md)

Updated October 27, 2026 · [Project overview](README.md)

## The question we want to test

When a device may have completed an action but the application has no confirmed result, can the application recover the original outcome and safely determine whether another authorized host may continue?

CyberGhost has limited evidence from official ROS 2 mock controllers, persisted task recovery within one VM, and read-only state reception on Linux and Windows. Real device behavior, live execution across machines and practical benefits remain unvalidated.

## The smallest useful starting point

A public environment/SDK link or an asynchronous interface review is enough to start. We can also discuss the fit in a roughly 30-minute conversation.

Our immediate priority is a second execution node: a Linux/Python edge board, small computer or remote test node where deployment, persistent task storage, application restart and log export are permitted. We need to check CPU architecture, Python version, dependencies and the authorized communication path; full ROS compatibility is not assumed.

An onboard input and a display or indicator can support an initial bounded experiment. An actuator with task identity, result queries, cancellation and observable state is a later option. Script-upload-only platforms are useful for full continuity testing only if their state retention, export and invocation permissions fit the experiment; otherwise their role would be limited to interface evaluation.

Existing equipment, loans and supervised remote time are welcome. Shipping a complete robot is not required. No resource or time slot is currently committed in our records.

## What we would contribute

| Proposed deliverable | Purpose |
|---|---|
| A versioned interface behavior table | Document submission, completion, queries, cancellation, loss of connection and controller changes, including unknowns |
| Minimal reproductions and sanitized evidence | Help reproduce integration issues; report correct behavior just as clearly |
| A bounded comparison on the same device | Compare the native/single-host baseline with handoff: duplicate actions, false completion, unknown outcomes and manual recovery |
| An agreed integration note or demonstration | Give developers a reusable account of what worked and what did not |

We would prepare the adaptation and report the results. The partner would provide an interface contact, authorized access and, for physical tests, an operator and stop procedure. Scope, preparation effort and delivery dates are agreed after the environment is understood. We make no advance claim of reduced costs, improved reliability or audience reach.

If an existing SDK or single persistent coordinator is sufficient, we will document that finding rather than force an additional layer.

## Information that helps assess fit

Please answer what is readily available or send public documentation; unknowns can remain open.

| Topic | Useful details |
|---|---|
| Execution environment | Board/computer, CPU architecture, OS, Python, SDK/driver versions and official example |
| Deployment and communication | Allowed application location, persistent storage, process restart, log export, transport and authentication |
| Task outcome | Stable task ID, query interface, result retention, behavior on repeated submission of the same ID |
| Authorization | Granting/revoking control, concurrent clients, read-only or output-disabled mode |
| Device behavior | Cancellation versus final outcome, observable state and timestamps, behavior after client exit or disconnection |
| Physical access | Remote or on-site supervision, independent stop mechanism and allowed operating limits |
| Terms | Availability, fees/deposit, data retention, publication and ownership requirements |

## A bounded first experiment

After an interface review, we propose discussing a supervised session of up to half a day, including checks and cleanup. Preparation time is separate. Confirm the second node and transport first, then read-only/output-disabled behavior, then an approved physical output.

Before actuator testing, jointly agree the device, software version, parameters, observations, samples, stop conditions and responsible operator. If permissions, supervision or the stop mechanism are unclear, the deliverable stays an interface gap report. The initial scope excludes destructive faults, power-cut tests, collisions and unattended motion.

Observe cancellation acknowledgement, controller outcome and actual stopping separately. Mock position retention is not evidence of physical stopping. Compare the same task and configuration against a native/single-host baseline; do not claim a benefit without comparable measurements.

A software fix is not the end of a hardware finding: retest on the same device and record the outcome. Failures remain in the report. Fees, liability, publication rights and source delivery require separate agreement; this page accepts none of those terms on either party's behalf.

## Contact and next step

Email **[vennai26@163.com](mailto:vennai26@163.com)** with a public environment/interface link and the access model you could consider. No credentials or restricted logs are needed.

**yujin / 余烬**, independent developer, Hangzhou, China (UTC+8). Remote collaboration is welcome internationally; in-person availability is in Zhejiang and Shanghai. We can start asynchronously to accommodate time zones.

[English project overview](README.md) · [中文项目介绍](README.zh-CN.md)
