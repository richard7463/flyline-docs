# Reproducible experiment

**Status: Experimental**

## Question

Under the same predator-approach scenario, does retaining the declared LC4/LPLC2 connectivity relationship make GF escape more likely to trigger early enough before a committed lunge than shuffling that connectivity?

## Setup

- **Seed:** `1337`
- **Paired trials:** `200`
- **Each trial:** one predator committed lunge
- **Independent variable:** real connectivity versus shuffled connectivity
- **Metrics:** escape success and mean trigger lead time, measured from GF trigger to committed-lunge impact

Lead time is not survival duration, jump count, or egg production. It describes the timing margin in one committed attack.

## Published baseline

| Configuration | Escape rate | Mean trigger lead |
| --- | ---: | ---: |
| Real connectivity | 100% | 0.202 s |
| Shuffled connectivity | 68% | 0.183 s |

These are the only published experiment figures for this phase: seed `1337`, `200` paired trials, real `100% / 0.202s`, and shuffled `68% / 0.183s`.

## Rerun procedure

Run the project's documented simulation command from its project root:

```bash
node --input-type=module -e "import('./js/sim.js').then(m => console.log(m.runExperiment(1337)))"
```

The experiment is designed to run without the DOM or Phaser. A rerun should record the seed, paired-trial count, configuration names, metric definitions, and output. Do not replace a changed result with the published baseline without investigating the cause.

## Limitations

This is a small, paired comparison in a simplified model. It tests one seed, one trial design, one predator event, and one metric definition. It does not establish animal behavior, generalize to all seeds, prove a causal biological claim, or compare every possible shuffle. Changes to GF, the predator trajectory, RNG consumption, or the metric require a new declared experiment rather than an informal number update.
