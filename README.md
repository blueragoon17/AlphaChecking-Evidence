# AlpaSim evidence: follow-up to NVlabs/alpasim #192

This repository hosts only the curated evidence package for my
[follow-up to NVlabs/alpasim #192](https://github.com/NVlabs/alpasim/issues/192).
It is not the private AlphaChecking code repository.

## Downloads

- [Complete prepared evidence ZIP](https://github.com/blueragoon17/AlphaChecking-Evidence/releases/download/alpasim-4m-20260928/AlpaSim_MultiCase_Evidence_4m_Audited_20260928.zip)
- [Release with individual MP4 downloads and SHA256 checksums](https://github.com/blueragoon17/AlphaChecking-Evidence/releases/tag/alpasim-4m-20260928)
- [Actual metric extracts and standard-library offline auditor](https://gist.github.com/blueragoon17/ad595259dc53719f5d7d6fee500e8ff4)

The ZIP includes **nine executions, six review videos, 27 captures, nine original
metric Parquet files, audit results, configurations, hashes and source-time
mappings**. The six videos represent four runs; two videos are alternative views.
The five historical cases have original metrics and individual captures, not full
videos. No full ASL, complete multiview sequences, source USDZ, model weights or
replacement PLY assets are included. This is the complete prepared triage package,
not a complete simulator installation or all raw experimental data.

## Interpretation first

- 4m is a distance-from-recorded-path evaluation cutoff, not a driving goal.
- No crossing means recorded distances stayed below 4m, not absent data.
- Seven post-handover contact executions become six after the reference filters;
  this does **not** mean six confirmed model defects.
- Original 1.5 (A01): contact at 9.1s is outside the window ending at 4.1s.
- v4 1.5 (B01): contact at 10.5s is retained, but visual assets were modified.
  The contact is behind ego geometrically; there is no direct rear-view camera.
- Historical C01-C05: one source scene with parameter variations, not independent
  scenes. Warmup, timing, input-history and replay-traffic qualifications remain.
  C05's target contact disappeared in a later official-synchronization rerun.

These are NuRec-rendered driver inputs, not original dashcam footage. The files
were not retouched or re-encoded for upload. The existing contact-window MP4s have
contact at **3.0s playback**. A01 maps that to 9.1s after handover; B01 to 10.5s.
Super clips show only late review windows. See `CASE_INDEX.md`, `MANIFEST.json`
and `support/HANDOFF_CONTEXT_en.md` in the ZIP before interpreting the media.

The source scene is `clipgt-01d503d4-449b-46fc-8d78-9085e70d3554` from
`nvidia/PhysicalAI-Autonomous-Vehicles-NuRec` at revision
`ebbb8d5b433bcf072451a55e3d8b86c5ed7a9396`.
The audit reference is AlpaSim commit
`affc2eab209fa43bdfa2f26c0f8d437922d78a68`.

This is diagnostic feedback, not a benchmark ranking, fault assignment or a
claim of rendering validity. CARLA C07 is separate. Dataset and model rights
remain with their respective owners; this evidence package does not grant a
general redistribution license. No new GPU resources were started for publication.
