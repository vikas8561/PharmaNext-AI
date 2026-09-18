# Course Vocabulary
---

**Active ingredient** — The part of a medicine that actually does something. In a 500 mg paracetamol tablet, the paracetamol is the active ingredient. Everything else in the tablet holds it together and controls how fast it dissolves.

**ANDA** — Abbreviated New Drug Application. The paperwork a company files to get permission to sell a generic. It is called abbreviated because it does not have to prove the drug works — the original company already did that. It only has to prove the copy behaves the same in the body.

**Artificial intelligence** — The broadest of the AI words, and the least useful. It covers anything that makes a machine seem clever, from a 1990 chess program to ChatGPT. Being told that something "uses AI" tells you almost nothing about it.

**AUC** — Short for *area under the curve*. Take blood samples over several hours after a dose and plot how much drug is in the blood against time. AUC is the area underneath that line. In plain terms: how much drug the body was exposed to in total.

**Batch** — One production run. If a factory makes 100,000 tablets on Tuesday, that is one batch, and every tablet from it carries the same batch number so it can be traced afterwards.

**Bioactivity data** — Test results recording what compounds did to a target. Each line holds one compound, one test, and a number saying how strongly it worked.

**Bioequivalence** — Showing that a generic behaves in the body the same way as the original. Volunteers take both, blood samples from each are compared, and the generic passes if its Cmax and AUC land within 80 to 125 per cent of the original's.

**Cell** — One box inside a Colab notebook. A code cell holds instructions for the computer and has a play button beside it. A text cell just holds writing.

**Cheminformatics** — Treating molecules as data. Instead of drawing a structure on paper, you write it as a line of text, calculate numbers from it, and compare thousands of molecules at once.

**Clinical trial** — Testing a medicine on people. It runs in three phases, each larger than the one before, and all three must be passed before the medicine can be sold.

**Cmax** — The highest level a drug reaches in the blood after a dose. If blood samples show the concentration climbing, peaking after two hours, then falling away, that peak is Cmax.

**Colab** — A free website where you write and run code. Nothing gets installed on your laptop. The code runs on Google's computers and you see the result in your browser.

**Column** — In a table of data, one piece of information recorded for everything in the table. If each line is a compound, then weight is one column and oiliness is another.

**Dataset** — A whole table of data. "A dataset of 5,000 rows" means information on 5,000 things: 5,000 compounds, or 5,000 patients.

**Decision tree** — A model that works by asking yes-or-no questions in order. Is the weight above 500? If yes, predict not absorbed. If no, ask the next question. Keep going until you reach an answer.

**Deep learning** — Machine learning done using neural networks. The word *deep* only means the network has many layers stacked up. It is not automatically better than simpler methods.

**Dosage form** — The physical form a medicine comes in: tablet, capsule, syrup, injection, cream. The same drug is often sold in several of them.

**Feature** — One piece of information a model is allowed to use when making its guess. If you are predicting absorption from weight and oiliness, those two are the features.

**Formulation** — Everything that goes into making a medicine, not just the drug itself. Which binder, which coating, how hard the tablet is pressed, how quickly it dissolves.

**Generic** — A copy of a medicine, made by a different company once the original's patent runs out. Same drug, same strength, same form, and usually far cheaper.

**Gradient boosting** — A way of building many decision trees one after another, where each new tree concentrates on the cases the earlier trees got wrong. Usually more accurate than a single tree.

**Hit** — A molecule that shows some effect on a target when it is tested. It is not a drug. It is a starting point.

**Hit rate** — Out of all the molecules tested, the share that turn out to be hits. Around one in a hundred is normal, so testing 100,000 molecules might produce about 1,000 hits.

**Label** — The thing you want the model to work out. If you are predicting whether a compound is absorbed, then "absorbed: yes or no" is the label.

**Lead** — A hit that has been improved and is now worth taking seriously. Chemists make many versions of a hit to get there.

**Machine learning** — When a computer works out a rule by looking at examples, instead of being handed the rule by a person. Show it 5,000 compounds and what happened to each one, and it finds the pattern itself.

**Model** — The rule a computer worked out. It is not a program somebody wrote. It is a set of numbers that take information in and give an answer out.

**Natural language processing** — Getting a computer to read ordinary written English and pull out what matters. Used to read patient safety reports and research papers automatically.

**Neural network** — A kind of model built from thousands of tiny calculating units arranged in layers. Each unit on its own does something very simple. Put enough of them together and they can handle patterns far too tangled to write down as rules.

**Notebook** — A page in Colab, made up of cells. It saves to your Google Drive, and you can share it with someone as a link.

**Oiliness** — Whether a molecule dissolves better in oil or in water. It matters because a drug must first dissolve in the watery stomach, then pass through a cell wall made of fat. Too watery and it never gets through the wall; too oily and it never dissolves in the first place. Its proper name, LogP, arrives in Module 10.

**Pharmacovigilance** — Keeping watch on a medicine after it goes on sale. Reports of problems arrive, are assessed, and the serious ones must reach the regulator within 15 days.

**Phase 1** — The first time a drug is given to people. Usually 20 to 80 of them, normally healthy volunteers. The question being asked is whether it is safe, and how much can be given.

**Phase 2** — Up to about 300 patients who actually have the illness. The question being asked is whether the drug treats it.

**Phase 3** — Between 300 and 3,000 patients, with the new drug compared against either a dummy pill or the treatment already in use. The question being asked is whether it is better than what patients already have.

**Placebo** — A dummy treatment with no drug in it, given to one group in a trial. Without it you cannot tell whether patients improved because of the drug or would have improved anyway.

**Preclinical** — All the safety testing done before any person takes the drug. Cells in a dish first, then animals.

**Prediction** — The answer a trained model gives when you show it something new. Give it a compound nobody has ever tested and it tells you what it expects to happen.

**QA** — Quality Assurance. Checks that the right procedures were followed and properly recorded. If a batch was made correctly but nobody signed the paperwork, that is a QA problem. QA checks the process.

**QC** — Quality Control. Tests the actual product in a laboratory against its specification. Does this tablet really contain 500 mg, and does it dissolve in the required time? QC checks the product.

**Random forest** — Hundreds of decision trees, each built on a different slice of the same data. Every tree votes and the majority answer wins. More accurate than any single tree.

**Regulator** — The government body that decides whether a medicine may be sold. CDSCO in India, the FDA in the United States, the EMA in Europe.

**Reinforcement learning** — A computer learns by trying something, being given a score, and trying again. Used in research on designing new molecules. Not covered in this course.

**Row** — In a table of data, one line. One thing that was measured: one compound, one patient visit, one batch.

**Specification** — The limits a batch has to stay inside to pass its tests. If a tablet should contain 500 mg and the specification is 95 to 105 per cent, anything outside that range fails.

**Supervised learning** — Learning from examples where the right answer is already known and written down. Nearly all of this course is this kind.

**Target** — A protein in the body that a drug is meant to act on. Statins work by blocking an enzyme in the liver, and that enzyme is the target.

**Training** — How a model is made. It is shown an example, guesses, is told how wrong the guess was, and has its numbers nudged slightly. Repeat that thousands of times and the guesses get good.

**Tree-based methods** — Models built out of decision trees, such as random forests and gradient boosting. They work well on tables of data and do not need many rows to be useful.

**Unsupervised learning** — Looking for patterns in data where no answers are given at all. For example, sorting 10,000 untested compounds into groups of similar ones, without being told what the groups should be.
