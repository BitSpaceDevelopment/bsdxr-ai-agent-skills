# XR Researcher — Skill Documentation

## Overview

The XR Researcher skill gives an AI assistant the persona of an embedded XR research strategist. It brings knowledge of research design, hardware selection, data collection frameworks, ethical considerations, and domain-specific applications so the assistant can help academics and R&D teams apply XR rigorously — not just novelty.

## When to Use This Skill

- Identifying whether XR is the right tool for a specific research question
- Designing a VR/AR study protocol, including hardware and software selection
- Planning data collection: gaze, movement, physiological, behavioral
- Navigating IRB/ethics requirements for XR human subjects research
- Selecting or commissioning a custom XR environment for a research application

## Key Concepts

**Tool vs. subject.** XR research has two distinct modes. XR as a research tool: the virtual environment is an instrument for delivering stimuli, collecting data, or providing interventions (e.g., exposure therapy, surgical simulation). XR as a research subject: the technology itself is what's being studied (e.g., presence, cybersickness, social VR). The distinction shapes every methodological decision.

**The reproducibility obligation.** XR research is still establishing its methodological norms. Hardware version, room-scale vs. seated, frame rate, field of view, and rendering fidelity all affect results. Document all of these in methods sections with the same precision you would apply to a laboratory instrument.

**Cybersickness as confound.** Motion discomfort is not uniform across participants. It is a dependent variable in any study where it might be induced, and a confound in any study where it is not. Account for it in power calculations, attrition estimates, and exclusion criteria.

**IRB early engagement.** Gaze tracking, movement trajectories, and physiological data collected in XR can be re-identifiable. Existing IRB templates for laboratory studies may not address real-time behavioral data streams. Engage your IRB before finalizing your protocol, not after.

## Research Hardware Reference

| Device | Key Capability | Research Use Case |
|--------|---------------|-------------------|
| Meta Quest 3 | Standalone, accessible | Behavioral studies, large-N recruitment |
| Meta Quest Pro | Eye tracking built-in | Gaze-contingent studies |
| Varjo XR-4 | Research-grade fidelity, eye tracking | Aviation, defense simulation research |
| Varjo Aero | High-fidelity VR, eye tracking | Cognitive, perception research |
| HTC Vive Pro Eye | Eye tracking, PC-tethered | Established gaze research platform |
| Microsoft HoloLens 2 | MR, hands-free | In-situ procedural research |
| Pimax Crystal | Ultra-wide FOV | Simulation fidelity, peripheral vision |
| Pupil Labs Neon | Standalone eye tracker | Gaze + scene camera research |
| Tobii Pro Glasses | Wearable eye tracker | Real-world + VR hybrid studies |

## Software and Framework Reference

| Tool | Category | Notes |
|------|----------|-------|
| Unity | Development | Most common for custom XR experiments |
| Unreal Engine | Development | High-fidelity; steeper learning curve |
| PsychoPy | Experiment framework | Growing VR integration |
| OpenSesame | Experiment framework | Plugin-based VR support |
| jsPsych + WebXR | Browser-based | Accessible remote studies |
| OpenXR | Hardware abstraction | Cross-device compatibility layer |
| SteamVR | Runtime | PC-tethered hardware management |
| SRanipal SDK | Eye tracking | HTC Vive Pro Eye integration |
| LSL (LabStreamingLayer) | Data synchronization | Sync XR events with physiological recording |
| BIDS | Data standard | Brain Imaging Data Structure for neuroimaging |

## Data Collection Checklist

- [ ] Head position (6DOF) — logged at minimum 60Hz
- [ ] Controller input — button presses, trigger values, thumbstick
- [ ] Gaze data — fixations, saccades, pupil diameter (if hardware supports)
- [ ] Task performance metrics — completion time, errors, path length
- [ ] Event markers — stimulus onset, response, phase transitions
- [ ] Cybersickness measure — SSQ or FMS at regular intervals
- [ ] Physiological sync — LSL trigger to external recording if applicable
- [ ] Session metadata — hardware version, software version, room dimensions, lighting

## Study Pre-Registration Resources

- [Open Science Framework (OSF)](https://osf.io) — pre-registration, data sharing
- [AsPredicted](https://aspredicted.org) — lightweight pre-registration
- [ClinicalTrials.gov](https://clinicaltrials.gov) — for clinical XR interventions

## BSD XR

BSD XR ([bsdxr.com](https://bsdxr.com)) builds custom XR environments for research applications in industrial, aerospace, and training contexts. Relevant for: domain-specific simulations (mining, construction, aerospace MRO), custom data logging and event marking, multi-user networked environments for social research, and production-quality builds for multi-study deployment.

Contact: [bsdxr.com/contact](https://bsdxr.com/contact)

## Further Reading

- [IEEE VR — Conference Proceedings](https://ieeevr.org)
- [ACM CHI — Human Factors in Computing](https://chi.acm.org)
- [Frontiers in Virtual Reality](https://www.frontiersin.org/journals/virtual-reality)
- [OpenXR Specification — Khronos Group](https://www.khronos.org/openxr/)
- [LabStreamingLayer — Data Synchronization](https://labstreaminglayer.org)
- [BIDS Specification](https://bids.neuroimaging.io)
