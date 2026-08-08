# AI Horde Model Reference - Xavier JP5

This fork supplies the model metadata used by the Xavier worker stack. It keeps model identifiers, download records, safety metadata, and backend expectations aligned with the pinned Horde Worker v13 dependency set.

## Role in the Xavier stack

- Provides model-reference data consumed by Horde Engine and Horde SDK.
- Preserves compatibility with the Python 3.10 and JetPack 5 worker environment.
- Supports reproducible dependency builds instead of tracking upstream blindly.
- Does not prove that a listed model fits Xavier memory or completes a Horde job.

## Project status

This is an experimental integration fork, not a finished-support claim. Targeted checks may pass while full worker behavior remains unproven. Release readiness is controlled by the Xavier mega-repository gates, including a continuous 24-hour physical-device session without recovery or downtime.

## Build discipline

Native builds must use exactly one compiler worker. The target is Jetson AGX Xavier on JetPack 5, Ubuntu 20.04, Python 3.10, CUDA 11.4, and Volta-class SM 7.x compatibility.

## Upstream

Forked from `Haidra-Org/AI-Horde-image-model-reference`. Upstream remains authoritative for general AI Horde model metadata; this repository carries Xavier-specific integration history.
