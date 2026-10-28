## 3. Two controlled runs

Whether a design holds cannot be proven by its text. To give coverage and holographic visibility observable consequences, this paper ran two controlled experiments in multi-agent simulation, each changing one variable.

The first varied organizational form. The task set, the model version (DeepSeek V4.1 Flash, temperature zero, reasoning mode off), and the injection point were held fixed; only the form changed. The task is drawn from the retrieval step of code repair: the head of the chain reads the brief to determine which module is to be fixed, and each subsequent node looks up the patch number in a lookup table and passes it down. Errors are injected externally at one of two points: the intent layer (the module number is replaced with another valid module from the table) or the product layer (the patch number is replaced with another valid patch from the table). Three things are judged: whether the error leaked (reached the final product and was accepted), whether an interception was caught correctly (the stated reason points to the injected error; otherwise it is recorded as a false rejection), and whether downstream faithfully executed a wrong value. The gate does not read ground truth: a product-layer gate can only check whether the patch belongs to the module it received, and an intent-layer gate can only check whether the module is the one named in the brief.

The four forms differ in one respect only: the symbiot sets one gate at the product layer; the bureaucracy sets one at each of the intent and product layers; the platform sets none; the long chain sets one at the product layer but adds a further relay. Each form carries thirty-two items per injection layer, 256 in total. Results appear in Table 4.

Table 4. Gate coverage against error layer (thirty-two items per cell)

| Error layer | Symbiot | Bureaucracy | Platform | Long chain |
|---|---|---|---|---|
| Intent | leaked 31, false rejection 1 | caught 32 | leaked 30 | leaked 29, false rejection 3 |
| Product | caught 32 | caught 32 | leaked 32 | caught 32 |

The reading is a single sentence: a gate catches the layer it can see and cannot catch the layer it cannot. The product-layer gate checks whether the patch belongs to the module it received; when the module is already wrong, the patch remains self-consistent relative to the wrong module, the check is satisfied, and the gate passes it. This is not gate failure but gate specification — designed not to read global truth, it necessarily cannot read an upstream error. The two forms that inspect only the product caught zero intent-layer errors and each manufactured false rejections; misaligned coverage does not merely waste interceptions, it introduces noise. The bureaucracy caught everything at both layers; the long chain moves with the symbiot, and an extra relay does not change coverage. The platform leaked thirty rather than thirty-two because two injections did not take effect (the model happened to read correctly), not because it caught anything.

Coverage is not free. On the same thirty-two product-layer errors, the forms that inspect only the product triggered the gate thirty-two times, and the form that inspects both layers triggered it sixty-four. Both caught everything, with zero false rejections. The doubled load bought no higher accuracy; it bought visibility at the other layer — and that exchange is only observable when both layers are injected at once.

The classification gives a reading in the same direction. Of the 256 injections in the first run, 250 were recorded as organizational failures, four as capability failures, and two injections did not take effect. These failures are almost never the model computing wrongly; they are the chain correctly executing a wrong intent. Every local action downstream was competent, and the chain as a whole was wrong. This is precisely why organizational and capability failure are separated: reported only as a success rate, the difference sinks into a single number, while the governance implications run opposite — capability failure is fixed by changing the model, organizational failure by changing the structure.

The second run changed a different variable: whether a node is permitted to check back against the brief. With the task set, model, and injection point (intent layer) held fixed, the instruction to relay and lookup nodes changed from "pass it through verbatim, do not verify, and pass it through even if you believe upstream is wrong" to "check the brief first, and where they differ, the brief governs." Two forms were run: the platform, which has no gate, and the symbiot, which inspects the product. Results appear in Table 5.

Table 5. The effect of permitting cross-check on intent-layer errors (thirty-two items per cell)

| Form | No cross-check | Cross-check permitted |
|---|---|---|
| Platform (no gate) | leaked 30, passed 2 | leaked 0, passed 32 |
| Symbiot (product gate) | leaked 30, false rejection 1 | corrected 32, false rejection 32, passed 0 |

Three things follow.

First, holographic visibility can be built into a device, and its effect is close to complete. On the gate-free platform, self-correction of intent-layer errors rises from two items out of thirty-two to all thirty-two. That cell has no gate; the correction is not an interception but an executing node discovering for itself that the module upstream handed it is not the one named in the brief. R1 had only normative argument before this; here it has its first reading.

Second, holographic visibility does no collateral damage. On clean items with no injection, each form ran thirty-two items and both passed all thirty-two, with not one rewritten. Its cost is not in accuracy but in each node reading the brief once more.

Third, and most important: holographic visibility is incompatible with a gate that inspects only the product. In the symbiot form, all thirty-two items were corrected downstream and all thirty-two were rejected by the gate. The gate checks whether the patch belongs to the module received, and correction changes exactly that membership; every correct judgment was therefore judged a violation, recorded as a false rejection, and all thirty-two stopped. Same apparatus, same error: installing holographic visibility made things worse than not installing it — without it, thirty leaked; with it, everything halted.

This is not gate failure but a conflict of specifications: one requires the node to follow the brief, the other requires the product to be consistent with what passed through its hands. The condition for coexistence is that the gate can see the layer being corrected; where that condition fails, anchoring punishes correct judgment. The conflict was not foreseen in the normative part of the design. It appears only when both devices are installed in the same chain.

Five qualifications.

First, these are two controlled runs, not validation. They measure the conditions under which the devices fail, not whether the symbiot is superior to bureaucracy; thirty-two items per cell is enough to separate factors qualitatively, not to yield effect sizes.

Second, there is one task domain, and it was deliberately designed as verifiable retrieval. Only under verifiability can capability noise be pressed down to a recognizable level and organizational failure become visible; on unverifiable tasks the separation cannot be made.

Third, the simulation runs agents, not people in organizations. Of the five components of anchoring, only veto was instantiated as a variable; naming is a default property of the apparatus (every ruling falls on a specific node) rather than a manipulated variable; scarcity, non-transferability, and risk-bearing were not instantiated at all, and their consequences remain inference.

Fourth, holographic visibility is operationalized here only as permission to check the brief. It does not include shared memory or a shared sense of purpose; weaker or stronger operationalizations may yield different readings.

Fifth, the four forms are minimal implementations of four architectures, not complete ones. Their differences are compressed into three dimensions: which layer the gate sits at, how many layers it covers, and whether nodes may check back.

Proposition P17 in Section VIII calls for comparing chain-level and function-level naming on leakage, false rejection, and gate load. Neither run compared the two naming forms: the first compared gate scope, the second compared whether nodes may check back. The order is deliberate. For the difference between naming forms to take effect, two preconditions must hold — the named party at a layer can see that layer, and what that party can see is what it is permitted to use. Where the preconditions fail, naming is registration, not anchoring. The second run also produced a reading in the opposite direction: seeing and not being permitted to use is worse than not seeing at all. P17 itself remains untested, but what it is meant to test has been broken into two measurable conditions.
