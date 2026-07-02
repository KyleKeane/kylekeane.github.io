# The Doctoral Work of Kyle Michael Keane: Quantum Computing Contributions, Collaborations, and Impact
## (Kyle-provided companion report to the web-presence inventory; preserved verbatim below the integration note. Prepared 2 July 2026.)

INTEGRATION NOTE (Claude Code, 2 July 2026): integrated the same day —
research.md's quantum section rewritten from the Section 10 narrative;
the ARO/IARPA grant-support entry now carries the confirmed award
number W911NF-10-1-0334 and Korotkov's grant-output attribution; the
measurement-reversal work entry and the Accomplishments physics
accordions carry the corrected realization lineage (Optics Express
2011 single-qubit; Nature Physics 2012 entanglement; Nature
Communications 2014 superconducting, Martinis co-author) plus a new
collaboration-and-legacy accordion. Section 9's open sub-item 1 was
CLOSED during integration: Korotkov's grant-output page
(https://intra.ece.ucr.edu/~korotkov/papers-ARO.html) lists BOTH
Keane & Korotkov PRA 86, 012333 (2012) as output #6 AND the
dissertation itself as output #7 — the grant's own attribution.
Remaining Section 9 items are mirrored in docs/open-items.md.

---VERBATIM REPORT FOLLOWS---

## About this report

This report consolidates everything surfaced across the web-presence research project concerning Kyle Keane's PhD-era quantum information science: the scientific contributions, the collaboration network in which they were made, the experimental realizations that followed, and the documented connection to John M. Martinis, 2025 Nobel Laureate in Physics. It is a companion to the master web-presence inventory and follows the same evidentiary discipline: every claim is labeled as web-documented (with URL), CV-documented, or first-person testimony, and the honest limits of the record are stated rather than smoothed over.

Prepared 2 July 2026.

## 1. Summary

Between 2009 and 2012, as a doctoral student in Alexander Korotkov's group at the University of California, Riverside, Kyle Keane co-authored two theoretical proposals that became part of the foundational literature on measurement-based protection of quantum information in superconducting qubits. The first showed that a qubit's dominant decoherence channel, zero-temperature energy relaxation, can be almost completely suppressed using quantum uncollapsing (weak measurement reversal). The second proposed experimentally realizable quantum error detection and correction schemes for superconducting qubits using the technology of the day.

Both proposals were subsequently demonstrated in experiment. The uncollapsing protocol was realized in photonic qubits in 2011, in an experiment literally titled after the proposal. The error-detection approach was realized in a three-qubit superconducting circuit in a 2014 Nature Communications experiment co-authored by John M. Martinis and Alexander Korotkov, which tripled the storage lifetime of a quantum state and was described by its authors as the first experimental demonstration of an algorithm-based improvement in the lifetime of a quantum state stored in a qubit. The papers continue to be cited in the pedagogical literature of the field.

The work was conducted inside one of the tightest theory-experiment partnerships in superconducting quantum computing: the collaboration between Korotkov's theory group at UC Riverside and Martinis's experimental group at UC Santa Barbara, operating under a shared ARO/IARPA program. In October 2025, Martinis shared the Nobel Prize in Physics with John Clarke and Michel Devoret for the discovery of macroscopic quantum mechanical tunnelling and energy quantisation in an electric circuit — the physics of the very devices for which Keane's protocols were designed.

## 2. Doctoral training and context

Kyle Keane earned his MS in Physics (2009) and PhD in Physics (2012) at the University of California, Riverside. His dissertation, "Quantum State Protection and Transfer Using Superconducting Qubits," was supervised by Alexander Korotkov, with Kyle appointed as a Graduate Student Researcher in the Department of Electrical Engineering from January 2009 to August 2012.

The dissertation presents a theoretical analysis of protocols for quantum information processing with superconducting qubits, aimed at decoherence suppression and quantum information transfer, using density-matrix formalism, Kraus operator (operator-sum) representations, and the unravelling of continuous evolution into discrete scenarios with associated probabilities.

Funding: the CV records the doctoral work as funded under "Multi-qubit algorithms in Josephson phase qubits," an ARO/IARPA award (2010-2015, one million dollars) — the same federal program family that funded the joint UCR-UCSB theory-experiment effort described in Section 4.

Public records of the dissertation: eScholarship https://escholarship.org/uc/item/8nq7q2hn ; advisor's group copy https://intra.engr.ucr.edu/~korotkov/papers/Dissertation-Keane.pdf

Origins note: before UCR, Kyle was an undergraduate researcher in Murtadha Khakoo's experimental atomic and molecular physics group at California State University, Fullerton (2005-2007), co-authoring three peer-reviewed papers on low-energy electron scattering (ethylene, 2007; methanol and ethanol, 2008; neon and xenon ionization, 2009) and machining precision scattering apparatus. This experimental grounding preceded the turn to theory and is documented in the master inventory, Section 2.

## 3. The scientific contributions

### 3.1 Decoherence suppression by quantum measurement reversal (2010)

Korotkov, A. N. & Keane, K., Physical Review A 81, 040103(R) (2010). Rapid Communication. arXiv:0908.1134.

The proposal: a qubit's decoherence from zero-temperature energy relaxation — the dominant error channel in superconducting qubits — can be almost completely suppressed by quantum uncollapsing. A partial (weak) measurement moves the qubit state toward the ground state, where it is protected during storage; a second partial measurement then restores the initial state. The procedure preferentially selects the histories in which no energy decay occurred, trading success probability for fidelity, with the trade-off point tunable through measurement strength. The paper states the experiment "can be realized in a straightforward way using the superconducting phase qubit" — the Martinis lab's device — and explicitly builds on the uncollapsing demonstration that the Martinis group and Korotkov had published together in 2008 (see Section 4).

This is the paper that gives Kyle's LinkedIn its accurate one-line summary: the only known procedure to protect a single qubit from energy relaxation without requiring additional qubits and entanglement.

Records: https://journals.aps.org/pra/abstract/10.1103/PhysRevA.81.040103 ; https://arxiv.org/abs/0908.1134

### 3.2 Simplified quantum error detection and correction for superconducting qubits (2012)

Keane, K. & Korotkov, A. N., Physical Review A 86, 012333 (2012).

The proposal: experimentally realizable schemes for quantum error detection and correction adapted to the practical constraints of superconducting qubit hardware of the era, analyzing how measurement-based protocols could reduce the impact of energy relaxation — the prediction that the 2014 Martinis-Korotkov-co-authored experiment went on to test (Section 5).

Record: listed with the dissertation and 2010 paper on Kyle's publications page, http://www.kylekeane.com/publications.html , and cited in the reference list of the Nature Communications realization below.

### 3.3 The dissertation (2012)

"Quantum State Protection and Transfer Using Superconducting Qubits" synthesizes both threads and adds quantum information transfer protocols, including analyses relevant to transferring microwave qubit states between resonators. It remains openly accessible through the University of California's eScholarship repository and through Korotkov's group site.

## 4. The collaboration network: Korotkov, Martinis, and the ARO/IARPA program

The essential context for understanding the doctoral work is that it was produced inside a standing, funded, two-campus partnership: Alexander Korotkov's quantum measurement theory group at UC Riverside and John Martinis's superconducting qubit laboratory at UC Santa Barbara. The web record documents this partnership independently of Kyle's testimony:

1. The 2008 joint uncollapsing experiment. Katz, Neeley, Ansmann, Bialczak, Hofheinz, Lucero, O'Connell, Wang, Cleland, Martinis & Korotkov, "Reversal of the weak measurement of a quantum state in a superconducting phase qubit," Physical Review Letters 101, 200401 (2008). Kyle's advisor is the closing author on a paper otherwise authored entirely by the Martinis lab. This experiment — demonstrating uncollapsing on the phase qubit — is the direct experimental foundation on which Kyle's first paper builds, and it is cited as such in the 2010 PRA. Listed on the Martinis Group publications page: https://web.physics.ucsb.edu/~martinisgroup/publications.shtml
2. The joint tunable-coupler analysis. Pinto, Korotkov, Geller, Shumeiko & Martinis, "Analysis of a tunable coupler for superconducting phase qubits," Physical Review B 82, 104522 (2010). The UCR first author, Ricardo Pinto, was Kyle's groupmate and co-author: the CV records the 2009 poster "Theoretical analysis of phase qubits" by Korotkov, Keane, and Pinto, presented at the IARPA Quantum Computing and Quantum Algorithms Program Review on 19 August 2009. This places Kyle personally inside the program reviews of the funding stream under which the UCR-UCSB collaboration operated. Records: https://ui.adsabs.harvard.edu/abs/2010PhRvB..82j4522P/abstract ; https://arxiv.org/pdf/1006.3351 ; https://www.semanticscholar.org/paper/Analysis-of-a-tunable-coupler-for-superconducting-Pinto-Korotkov/adebe733d631bd054e2d1d6ccf6164820ab6e7fa
3. The sustained partnership. The Martinis Group publications page also lists later Korotkov-Martinis co-publications (for example Sete, Martinis & Korotkov, PRA 92, 012325, 2015, on Purcell filters for qubit readout), demonstrating that the partnership Kyle trained inside was a durable axis of the field, not a one-off.
4. The shared funding program — CONFIRMED. Kyle confirmed on 2 July 2026 that IARPA/ARO grant W911NF-10-1-0334 is the award that funded portions of his PhD projects — the same grant acknowledged by the 2014 Nature Communications realization. Korotkov's group maintains a dedicated public page listing every paper produced under this award: "Papers from A.N. Korotkov's group supported by IARPA under ARO grant W911NF-10-1-0334 (Aug. 2010 - July 2015)," forty-one papers including the Zhong-Martinis 2014 realization and many further Korotkov-Martinis co-publications. Kyle's own 2012 PRA (published July 2012) falls inside the award window and should be verified on the list — if present, it is the grant's own attribution of his paper to the program. [INTEGRATION: VERIFIED — the page lists the 2012 PRA as output #6 and the dissertation as output #7.] Kyle also presented at the program's review venues: the IARPA Quantum Computing and Quantum Algorithms Program Review (August 2009 poster) and the ARO Coherence in Superconducting Qubits meeting (April 2010 poster). Grant-output page: https://intra.ece.ucr.edu/~korotkov/papers-ARO.html

## 5. Experimental realizations and scientific legacy

### 5.1 The superconducting realization, co-authored by Martinis (2014)

Zhong, Y. P., Wang, Z. L., Martinis, J. M., Cleland, A. N., Korotkov, A. N. & Wang, H., "Reducing the impact of intrinsic dissipation in a superconducting circuit by quantum error detection," Nature Communications 5, 3135 (2014). arXiv:1309.0198.

A three-qubit superconducting circuit (Zhejiang University hardware, with UCSB and UCR as co-authoring institutions) implemented a quantum error detection protocol based on quantum uncollapsing: quantum information encoded in a target qubit, two ancilla qubits detecting and rejecting energy-relaxation errors. The protocol improved the storage time of a quantum state by a factor of roughly three, at the cost of reduced success probability — exactly the fidelity-for-probability trade central to the Keane-Korotkov analyses. The authors describe the result as "the first experimental demonstration of an algorithm-based improvement in the lifetime of a quantum state stored in a qubit." The paper's reference list includes both of Kyle's papers, and John M. Martinis is a co-author.

Records: https://www.nature.com/articles/ncomms4135 ; https://arxiv.org/abs/1309.0198

### 5.2 The photonic realizations (2011, 2012)

- Lee, J.-C., Jeong, Y.-C., Kim, Y.-S. & Kim, Y.-H., "Experimental demonstration of decoherence suppression via quantum measurement reversal," Optics Express 19, 16309 (2011). The experiment is titled after the protocol and cites Korotkov-Keane PRA 81, 040103 as the proposal (reference 10), alongside the Katz-Martinis-Korotkov PRL (reference 14). Full text: https://qopt.postech.ac.kr/wp-content/uploads/2020/12/110810oe.pdf ; record: https://www.researchgate.net/publication/51658817_Experimental_demonstration_of_decoherence_suppression_via_quantum_measurement_reversal
- Kim, Y.-S., Lee, J.-C., Kwon, O. & Kim, Y.-H., "Protecting entanglement from decoherence using weak measurement and quantum measurement reversal," Nature Physics 8, 117 (2012). Extends the physics from single-qubit states to entanglement protection, citing Korotkov-Keane among its foundations. Record: https://www.nature.com/articles/nphys2178

Together these establish that the proposal was realized on two independent physical platforms — superconducting circuits and photons — within four years of publication.

### 5.3 Entry into the pedagogical canon

The 2010 paper is cited in later teaching literature, for example the lecture notes "Introduction to Experimental Quantum Measurement with Superconducting Qubits" (arXiv:1904.09291, reference 22). A recommended enrichment: capture current citation counts for both papers with a retrieval date.

### 5.4 The grant's larger legacy: from Kyle's protocols to Google's quantum program

W911NF-10-1-0334 is acknowledged across the most consequential superconducting-qubit papers of the era:

- Barends et al., "Superconducting quantum circuits at the surface code threshold for fault tolerance," Nature 508, 500 (2014) — the Martinis-lab landmark showing gate fidelities at the surface-code threshold, with Korotkov as the UCR co-author; acknowledges W911NF-09-1-0375 and W911NF-10-1-0334. Full text: https://web.physics.ucsb.edu/~martinisgroup/papers/Barends2014.pdf
- Kelly et al., "State preservation by repetitive error detection in a superconducting quantum circuit," Nature 519, 66 (2015) — the nine-qubit repetition-code experiment, acknowledging the same two grants and thanking Korotkov for discussions; the author list carries "Present address: Google Inc." annotations, marking the Martinis team's move that founded Google's quantum hardware effort. Record: https://www.nature.com/articles/nature14270
- Wenner et al., "Catching Time-Reversed Microwave Coherent State Photons with 99.4% Absorption Efficiency," PRL 112, 210501 (2014) — Korotkov, Cleland, and Martinis co-authored, same grant; a high-efficiency quantum receiver converting flying qubits to stationary qubits between resonators — the quantum-state-transfer thread, the second half of Kyle's dissertation title. Full text: https://intra.ee.ucr.edu/~korotkov/papers/PRL-112-210501-2014.pdf

The defensible scope statement: Kyle's doctoral work was funded by, presented within, and cited by the same IARPA/ARO award whose experimental arm produced the surface-code-threshold and repetitive-error-detection results that seeded Google's quantum computing program, and whose theory arm was his own research group. Both halves of his dissertation — protection and transfer — have documented experimental realizations within the program, the protection half citing him by name.

## 6. The players

- Alexander N. Korotkov — Doctoral advisor and co-author on both papers; UCR quantum measurement theorist; standing collaborator of the Martinis lab (2008 Katz PRL, 2010 Pinto PRB, 2014 Zhong Nature Communications, later papers). Group site: https://intra.engr.ucr.edu/~korotkov/
- John M. Martinis — 2025 Nobel Laureate in Physics (shared with John Clarke and Michel Devoret, for the discovery of macroscopic quantum mechanical tunnelling and energy quantisation in an electric circuit); head of the UCSB experimental group whose phase qubit was the target platform of Kyle's proposals; co-author of the 2014 experimental realization citing Kyle's papers. Kyle's account of close working contact during the PhD is first-person testimony consistent with, but not independently proven by, the documented program co-membership.
- Ricardo A. Pinto — Kyle's UCR groupmate; co-author with Kyle and Korotkov on the 2009 IARPA program-review poster, and first author of the joint UCR-UCSB tunable-coupler paper with Martinis.
- Nadav Katz and the 2008 UCSB team — Katz (later Hebrew University of Jerusalem), Neeley, Ansmann, Bialczak, Hofheinz, Lucero, O'Connell, Haohua Wang, Cleland — the experimentalists who demonstrated the uncollapsing phenomenon.
- Andrew N. Jordan — Korotkov's co-author on the 2006 theoretical proposal of measurement undoing (PRL 97, 166805), the intellectual ancestor of the uncollapsing line.
- Y. P. Zhong, Z. L. Wang, and Haohua Wang (Zhejiang University) — the 2014 experimental team; Haohua Wang connects the 2008 and 2014 experiments.
- Andrew N. Cleland — UCSB (later University of Chicago) co-author on both experiments.
- Michael R. Geller and Vitaly S. Shumeiko — Georgia and Chalmers theorists on the tunable-coupler paper.
- Yoon-Ho Kim's group (POSTECH, Korea) — Yong-Su Kim, Jong-Chan Lee, Young-Chan Jeong, Osung Kwon; the photonics team.
- Murtadha A. Khakoo (CSUF) — pre-doctoral mentor in experimental physics.

## 7. The public speaking and presentation record of the doctoral era

From the CV and http://www.kylekeane.com/curriculum-vitae1.html (slides and abstracts linked for most items):

- Talk, "Suppression of T1-type decoherence of phase qubits using uncollapsing and quantum error detection/correction," Keane & Korotkov, APS March Meeting, Bulletin Y29.10 (2012).
- Colloquium, "Beyond Traditional Quantum Measurement: A Game of Quantum Peek-a-Boo with a Purpose," CSUF Department of Physics, 5 November 2011 — an invited return to his undergraduate department.
- Talk, "Currently realizable quantum error detection/correction algorithms for superconducting qubits," Keane & Korotkov, APS March Meeting, Bulletin D29.14 (2011).
- Talk, "Decoherence suppression of a solid state qubit by uncollapsing," Keane & Korotkov, APS March Meeting, Bulletin Z33.11 (2010).
- Poster, "Suppression of T1-type decoherence of phase qubits using uncollapsing and quantum error detection/correction," Coherence in Superconducting Qubits (ARO meeting), 26 April 2010.
- Poster, "Theoretical analysis of phase qubits," Korotkov, Keane & Pinto, IARPA Quantum Computing and Quantum Algorithms Program Review, 19 August 2009.
- PhD Oral Qualifying Exam, "Uncollapsing, Decoherence Suppression, and Quantum Error Correction/Detection with Phase Qubits," UCR (2009), with slides preserved on the legacy CV page.

## 8. The through-line

The quantum training is the documented root system of the later career: the Wolfram physics parsers and step-by-step solver; the Carter-Keane computational curriculum and the GPU-parallelized kinetic Monte Carlo dewetting research at MIT; and the Bristol identity ("the scientific rigor of a physicist to push the boundaries of human perception"), with the Kara sonification as astrophysics data rendered through perceptual channels.

## 9. Open confirmation items

1. RESOLVED (2 July 2026): W911NF-10-1-0334 confirmed by Kyle; sub-item verify 2012 PRA on the grant page — CLOSED during integration (listed as output #6, with the dissertation as #7).
2. Check the dissertation PDF's acknowledgments for a Martinis mention (Kyle holds the PDF).
3. Seek archived attendee/program lists for the ARO meeting (April 2010) and IARPA review (August 2009) to document co-presence with Martinis.
4. Capture citation counts for both papers with a retrieval date.
5. Verify the APS March Meeting bulletin entries (Y29.10, D29.14, Z33.11) in the APS archive.
6. The later IARPA engagement (2019 or 2020, first-person, MIT Quest period): no public record found; expected for intelligence-community advisory engagements. Corroboration routes: Kyle's correspondence/calendar, MIT Quest colleagues, or the IARPA office.

## 10. A draft narrative paragraph, in the first person, for the website

During my PhD at UC Riverside I worked in Alexander Korotkov's quantum measurement theory group, at the theory end of one of the field's tightest theory-experiment partnerships: Korotkov's standing collaboration with John Martinis's superconducting qubit laboratory at UC Santa Barbara, under a shared ARO/IARPA program whose reviews I presented at. My research asked whether the act of quantum measurement itself — usually the destroyer of quantum states — could be turned into a tool for protecting them. With Korotkov I published two proposals: one showing that a qubit's dominant decoherence channel can be almost completely suppressed by weak measurement and its reversal, without any additional qubits or entanglement, and one laying out experimentally realizable error detection and correction schemes for the superconducting hardware of the day. Both were realized in experiment within four years — the measurement-reversal protocol in photonic qubits in Korea, and the error-detection approach in a three-qubit superconducting circuit in a Nature Communications experiment co-authored by Korotkov and Martinis that tripled a stored quantum state's lifetime, the first algorithm-based improvement of its kind. Martinis shared the 2025 Nobel Prize in Physics for the foundational discoveries behind those very circuits, and the IARPA award that funded my doctoral projects went on to fund the surface-code experiments that seeded Google's quantum computing program. I carry that training — the discipline of proposing only what an experiment can check — into everything I now build in human perception and assistive technology.

## 11. Relationship to the master inventory

This report extracts and expands the master inventory's Section 3 (PhD era), adds the presentation record, the players, the through-line, and the draft narrative. The master inventory remains the canonical URL ledger.
