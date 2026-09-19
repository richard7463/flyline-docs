# Connectome-inspired model

**Status: Implemented as a simplified model; Experimental for connectivity comparison**

## How biology becomes rules

Flyline does not run a complete brain network. It translates a small set of research-informed relationships into parameters that a player can observe:

| Biological idea | Observable game result |
| --- | --- |
| Motion vision | Threat evidence as the predator approaches |
| LC4 input | Weight associated with speed/angle change |
| LPLC2 input | Weight associated with looming size change |
| GF output | READY window, jump, cooldown, and cost |
| Body state | Energy, speed, perception range, and exposure |

The translation keeps three useful constraints: inputs are incomplete, responses are fast, and actions have costs. It does not preserve every biological variable.

## Research anchors

The public anchors used by the project are approximately 2,442 synapses for LC4 and 1,366 for LPLC2, with Ache et al. (2019) and MaleCNS v1.0 cited as source anchors. These figures are not evidence that Flyline reconstructed the complete connectome.

## Extension test

A proposed circuit should answer three questions:

1. Does it change a signal the player can observe?
2. Does it change an action or an action cost?
3. Can it be tested under a fixed seed with declared metrics?

If not, it remains a research or design note rather than a claimed gameplay feature.
