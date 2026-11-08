# CyberGhost

A migrating agent that learns to use each authorized host while carrying its goals, memory and task progress.

English | [简体中文](README.zh-CN.md)

Updated November 8, 2026.

## Research objective

CyberGhost investigates a common process for discovering a host’s existing skills, interpreting its interfaces, verifying capability mappings, planning with those capabilities, and continuing a task after moving to another host. Host frameworks, drivers and control skills supply the available body and actions.

The research has two linked requirements.

- **Continuity** preserves goals, relevant memory, confirmed progress and execution ownership.
- **Host adaptation** acquires reliable knowledge of a new host and uses that knowledge to choose valid actions.

Protocol adapters and device-specific knowledge remain explicit parts of the integration. We intend to measure how much the agent can obtain or generate, and how much human work is required.

## Current evidence

The internally reviewed CG73R1 baseline covers three fixed cases involving changes to a declared communication graph, explicit rejection before authorization, and an unknown receipt. Skills run in controlled isolated software processes. CG74 additionally passed two fixed direct-link-loss cases with an authoritative ledger still reachable, covering confirmed revocation, alternate routing and rejection of late activation. Earlier ROS 2 mock and Linux/Windows results have their own versions and scopes.

CG75R2 reused RAX’s lightweight client and passed four fixed Context protocol cases over local Unix sockets, covering success, JSON-RPC errors, tool errors and response-ID mismatch. This is a bounded client compatibility result.

New-host capability learning, physical migration, generalization to arbitrary robots, external adoption and economic benefit remain open validation items. [Software evidence and limits](SOFTWARE_STATUS.md)

RAX is a closely related research direction. Our source review identified host-interface descriptions, handoff memory and cross-session skill storage, and informed the client reuse above. The value of combining host adaptation with our continuity mechanism needs direct comparison. [RAX](https://arxiv.org/abs/2610.22496) · [Robot adaptation guide](https://github.com/robot-agent-exploration/rax/blob/main/docs/REAL_ROBOT_ADAPTATION.md)

## What we want to test with a partner

Start with one bounded, observable physical task using an existing skill and a documented interface. Progress toward a second host with a different interface or capability set. Freeze the agent core before exposing the held-out host, and record every host-specific adaptation.

Useful inputs include SDK or skill documentation, units and frames, preconditions, completion/query/stop behavior, permitted deployment and communication, and a named technical reviewer. A documented integration or interruption problem and the current workaround would help choose a meaningful comparison.

Compare task outcomes, capability understanding, invalid calls, human modifications and adaptation time. Continuity comparisons should include a persistent coordinator with the same task information. Proposed physical tests require a device-specific scope and authorization.

[Collaboration details](COOPERATION.md) · [Historical evidence guide](EVIDENCE_GUIDE.md) · [Historical walkthrough](WALKTHROUGH.md)

## Contact

yujin / 余烬, independent developer in Hangzhou. Local collaboration in Zhejiang/Shanghai or supervised remote access may be suitable.

[vennai26@163.com](mailto:vennai26@163.com)

This repository publishes project summaries and collaboration information. Private implementation and raw experiment records are retained separately. Access, fees, responsibilities, data use and publication terms are agreed for each collaboration.
