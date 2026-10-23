# HEADHEIGHT Synthetic Head–Foot Chronometry Corpus v2.0

This is the versioned source release for the **participant-visible** HEADHEIGHT dataset. The observations are original simulations, not measurements of people or optical clocks. The motivating scientific result is [Bothwell et al. (2022), as recorded by NIST](https://www.nist.gov/publications/resolving-gravitational-redshift-across-millimetre-scale-atomic-sample); none of that paper's data are included here.

## Download

Download the `headheight_public.zip` asset from [release v2.0.0](https://github.com/anjalikhatri019-hub/headheight-relativistic-chronometry-corpus/releases/tag/v2.0.0). The archive contains 1,600 float32 arrays of shape `(4096, 12)`, `manifest.csv`, `train_targets.csv`, `sample_submission.csv`, and `DATASET_CARD.md`. The 1,200 training targets are public. Targets for the 400 held-out scenes are intentionally absent.

The dataset archive is **318,334,784 bytes** with SHA-256:

```text
682f1caaf58ba1dbad40643d398835f00dada27476c7384e34aafc491ff8dc07
```

The corpus models the head-clock height above a stationary foot clock through eight hours of simulated posture changes, phase-wrapped optical links, drift, thermal response, sensor outages and motion proxies. Its target is a 128-point height trajectory plus integrated head-minus-foot proper-time lead in femtoseconds. The training scenes and labels are identical to v1.0. The 400 held-out scenes are newly generated and have different IDs, with motion-coupled complementary sensor outages and unknown optical phase re-lock offsets. They cannot be joined to the older unmasked test traces. Read [DATASET_CARD.md](DATASET_CARD.md) for channel meanings, the held-out regime, units, generation caveats, and target convention.

## License and provenance

The original synthetic dataset and documentation in this repository, including the release asset, are dedicated under **CC0 1.0 Universal**; see [LICENSE](LICENSE) and the [Creative Commons legal code](https://creativecommons.org/publicdomain/zero/1.0/). No external measured dataset was copied. This release is not affiliated with or endorsed by NIST.

Organizer-only answers, raw upload package, simulator source, grader, and challenge administration files are not part of this public dataset source release.
