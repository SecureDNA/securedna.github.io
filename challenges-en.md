---
layout: default
title: SecureDNA
--- 
{% include_relative header-en.md %}

<br />

## Challenge: Enabling Legitimate Research
---
Many hazardous sequences added to the databases are likely subjects of study by legitimate scientists who may or may not realize the potential for misuse. This type of benevolent research could continue without obstruction if large commercial providers have access to DNA synthesizers that accept a whitelist. Each laboratory would send the provider a certificate corresponding to the genomes of organisms for which they have approval from their biosafety committee or other governing body. The restricted-access synthesizers will accept the certificate, compare the sequences from the order to the whitelist, and refrain from screening any that match.

→ *Legitimate researchers can request DNA from ‘whitelist-capable’ commercial synthesizers*
> showcase remove: Legitimate researchers can request DNA from ‘whitelist-capable’

> showcase remove: Legitimate researchers can request DNA from ‘whitelist-capable’

<br /><br />

## Challenge: State-Level Actors
---
Any state-level actor will have sufficient resources to construct their own unlocked DNA synthesizers and assemblers. There is little that can be done to prevent such actors from making any biological agents that they are aware of. By enabling future scientists to privately disclose newly identified potential bioweapons to authorized experts who can add them to the database, the Secure DNA Project would minimize the number of credible bioweapons available to rogue states.

→ *The project assumes that state-level actors will have access to unlocked synthesizers*

→ *Enabling secure screening may reduce the severity of agents known to state-level actors*
<br /><br />

## Challenge: Ensuring Attacks Learn Nothing Useful
---
Whitelists will be especially important because some sequences in the database will be ‘decoys’ from autonomous agents that could plausibly pose a threat, but are not actually of concern. Including decoys is necessary because an obvious first attack by an adversary would seek to determine which known viruses are in the database; decoys will ensure that they learn little of consequence. Any researcher who might discover that the virus they study is blocked and must submit a whitelist will only learn that it is considered a potential risk worthy of caution, not that it necessarily poses a severe threat. 

→ *Some database entries will be decoys: plausible-seeming but not actual threats*
<br /><br />

## Challenge: Estimating Required Database Size
---
The database must be constructed to allow for future advances permitting the construction of harmful autonomous agents. How many such agents exist and what sorts of sequences may be involved are by definition unknown at this time. One way to estimate the size of the database required is to evaluate the number of natural autonomous agents that currently exist.

As of May 2019, there were 4,257,881,634 base-pairs of DNA sequences in the Reference Viral Database, most of which comprise human viruses. There are less than a billion unique 42-mers sequences in this database (h/t Andrew Liu, whose code is [here](https://github.com/abliu/viral-genomes)); excluding HIV and influenza, which have notably high diversity and are overrepresented, there are 486,339,373. Similarly, there are 101,537,029 unique 19-amino-acid peptides in the associated [database of proteins](https://rvdb-prot.pasteur.fr/files/U-RVDBv15.1-prot.fasta.bz2). Hence, 10<sup>9</sup> sequences appears a reasonable guideline for the potential number of future autonomous threats if saturation coverage without variants was required.

With random adversarial threshold screening, the number of variants per agent depends on the conservation of genome sequences, the extent to which different agents share them, and how many variants preserve the function of the agent. The latter will require experimental analysis, but we can conservatively assume that 10<sup>7</sup>functional variants for all of the randomly chosen fragments of a given agent. Since known hazardous agents need not be counted because pre-screening can ensure that orders do not include matching sequences, we may assume that no more than 100 private agents must be guarded against at any time.

→ *Analysis of currently known viral genomes suggests a database size of ~10<sup>9</sup> should suffice*
<br /><br />

## Challenge: Permutations
---
Exact-match screening might be evaded by switching the reagents in the synthesizer and permuting the desired sequence order to match. For example, swapping “T” with “A” would render the sequence unrecognizable, but as long as the synthesizer is agnostic to the identity of the reagent, a physical exchange would produce the desired sequence. Permutation can be defeated by including all 4! variants of each hazard in the database. However, combining this inclusion with the reverse strand inflates the number of sequences by a factor of 48. Because reagent-swapping would be difficult to accomplish at major commercial suppliers, these firms could in principle screen using databases without such permutations. Benchtop synthesizers would certainly require databases with permutations, but given that much less DNA is anticipated to be synthesized on such machines, they may produce fewer false positives overall.

→ *Switching reagents and sequence orders could evade screening*

→ *Including all 4! permutations and blocks this but inflates the database size for benchtops*

→ *The reduced amount of DNA synthesized on benchtops should cancel out the increased size*
<br /><br />

## Challenge: Interrogation
---
The finite set of sequences for each window length renders the hazard databases theoretically susceptible to *exfiltration*, or interrogation of the database to determine its contents, given a sufficiently large number of queries. This can be prevented by limiting the number of queries permitted for each synthesizer. Throttling the total number of queries to little more than the total number required for global DNA synthesis makes extracting more than a tiny fraction of sequences from the database quite difficult: the set of possible sequences is over nine orders of magnitude larger than the number of queries submitted by anticipated global DNA synthesis a decade from now. In other words, even if total global synthesis capacity were devoted to interrogation for the next decade, it could not discover more than the tiniest fraction of sequences designated as hazardous.

→ *Limiting the number of queries per synthesizer precludes interrogation of the database because the total queries per year is far smaller than the set of possible sequences*
<br /><br />

## Challenge: DDoS Attacks and Synthesizer Types
---
Structuring the independent parties to ensure that they cannot be compromised while permitting efficient querying by large-scale commercial providers and future benchtop synthesis machines, which currently comprise the great majority of global synthesis, will be a key challenge. Ideally, the independent parties would not be connected to the internet and would only communicate by direct fiber line with the major synthesis cores. However, benchtop synthesizers will presumably need to communicate with the parties via standard internet protocols. This is a failure point for the screening system, which could be taken down by an attack directed at the parties or potentially the database server. Global DNA synthesis cannot afford to be halted entirely by such an attack. Ensuring that large-scale commercial suppliers have their own dedicated fiber lines would render the majority of the system robust to such interference. To minimize the cost, servers representing the independent parties might be located in vaults near the major synthesis centers that are only accessible through the coordination of outside organizations.

→ *The structure of the system should minimize the risk of DDoS and covert interrogation*
<br /><br />

## Challenge: DNA For Information Storage
---
The estimate of 10<sup>15</sup> base-pairs synthesized globally in a decade assumes annual doubling, which is likely reasonable for the biotechnology industry. However, there is considerable interest in adopting DNA for medium- and long-term information storage. If this occurs, and especially if synthesizers proliferate to match, global DNA synthesis could greatly exceed the capacity of the screening system. Ideally, DNA synthesis for information storage would use synthesizers with hardware locks that render them incapable of making biologically relevant sequences. A naive implementation might require the inclusion of stop codons in all frames, or the use of synthesis error rates that would be unacceptable in biology but tolerable for data storage; many more are possible. One of the best might involve the mandatory inclusion of xenobases not found in nature, which would also increase information storage density and provide a market advantage. 

→ *If DNA synthesis for information storage becomes widespread, synthesizers used for that purpose must be incapable of making biologically relevant sequences*
