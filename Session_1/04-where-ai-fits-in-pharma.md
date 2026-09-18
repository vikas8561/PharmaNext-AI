# Where AI Fits in Pharmaceutical Work

**PharmaNext AI · Session 1 Notes**

The nine stages from the earlier notes are still the same nine stages. Nothing about how a medicine gets made has changed. What has changed is who does certain parts of the work.

---

## 1. Choosing Which Molecules to Test

**Stages 2 and 3.** Screening for hits, and improving the leads.

### The work

You have a target and a collection of molecules. You need to know which ones do anything to it.

### How it was done

Every molecule gets tested in a laboratory. Robots made this faster, but each test still costs money and bench time, and the hit rate is around one per cent. Testing 100,000 molecules to find 1,000 hits means paying for 99,000 tests that found nothing.

### What changed

The molecules are filtered on a computer first.

Each molecule's properties are calculated — weight, oiliness, size, shape. A model trained on compounds already known to work against similar targets then estimates which of the untested ones are worth trying.

The laboratory receives a few hundred molecules instead of a hundred thousand. The tests that get run are the ones most likely to find something.

**In this course:** Module 10 for calculating molecular properties and building the model. Module 7 for the model itself.

---

## 2. Predicting What the Body Will Do to a Molecule

**Stage 4.** Preclinical testing.

### The work

Before a molecule can go near a person, you need to know whether it is absorbed, where it goes, how the liver breaks it down, how fast it leaves, and whether it causes damage.

### How it was done

Cell experiments, then animal studies. Slow, expensive, and only possible once the molecule physically exists.

### What changed

Much of it can now be estimated from the structure alone, before anybody synthesises anything.

You type in the molecule and get back estimates: is it likely to be absorbed, will it cross into the brain, which liver enzymes will act on it, does it carry a risk of damaging the heart or the liver.

These are estimates, not measurements. They do not replace the animal study. What they do is stop you spending six months making a molecule that was never going to survive stage 4.

Around 40 per cent of all clinical failures are caused by exactly these properties. Catching one of them at this stage instead of at Phase 3 is worth a very large amount of money.

**In this course:** Module 11.

---

## 3. Handling Trial Data

**Stages 5 to 7.** The human trials.

### The work

A trial produces a row for every patient at every visit, across dozens of measurements. Before anyone can analyse it, the data has to be cleaned: missing values found, impossible entries flagged, the same field written three different ways made consistent.

### How it was done

By hand, in spreadsheets. A person opens the file, scrolls, finds the problems, fixes them, and saves a new version.

Two things go wrong with that. It takes a long time, and there is no record of what was changed or why.

### What changed

The cleaning is written as code instead. The same file goes in, the same clean file comes out, and the instructions are written down in a form anyone can read and re-run.

When a regulator asks what was done to the data, the answer is a file rather than somebody's memory.

**In this course:** Modules 4 and 5.

---

## 4. Writing and Checking Documents

**Stage 8.** Regulatory submission.

### The work

An approval submission runs to thousands of pages. Every claim in it must be supported by evidence, and the evidence must be findable.

### How it was done

Written from scratch, by people, over months.

### What changed

The first draft is now often produced by a language model and then checked by a person. Searching the literature for evidence supporting a specific claim takes minutes instead of days.

The checking is not optional and is not a formality. A language model will produce a reference that looks entirely real and does not exist. In a regulatory document, an unverifiable citation is a finding against the company.

The work has not been removed. It has moved from writing to verifying, and verifying still requires someone who understands the subject.

**In this course:** Modules 1 and 2.

---

## 5. Reading Safety Reports

**Stage 9.** After the drug is on the market.

This is where the largest number of pharmacy graduates in India work, so it is worth being specific.

### The work

Somebody taking the medicine has a problem. A report arrives — from a doctor, a pharmacist, the patient, or a company representative. Most of it is a paragraph of ordinary written English describing what happened.

That paragraph has to be read, understood, converted into structured fields, coded to a standard vocabulary, entered into a database, and assessed for seriousness. If it is serious, it must reach the regulator within 15 days.

### How it was done

A trained person reads each report and fills in each field. Thirty to sixty minutes per report. A large company receives thousands every day.

### What changed

The machine now reads the paragraph and pulls out the drug name, the dose, the reaction, and the dates, filling in most of the fields before a person sees it. Published industry analyses report case processing times falling by 40 to 60 per cent.

The person's job shifts from typing to checking, and to the part a machine cannot do: deciding whether a pattern across many reports is a real safety signal or a coincidence.

**In this course:** Module 9.

---

## The Kind of Data Decides the Method

In the previous notes all the data was a table — rows of compounds, columns of properties. Pharmaceutical work produces four other shapes, and each needs a different approach.

| What the data is | What it looks like | What is used on it | Module |
|---|---|---|---|
| Measurements | A table of numbers | Statistics, tree-based models | 5, 7 |
| Written reports and papers | Paragraphs of ordinary language | Natural language processing | 9 |
| Molecules | A structure, written as a line of text | Cheminformatics | 10 |
| Images | Pixels | Neural networks | 8 |
| Records over time | A table with a date column | Statistics and trend analysis | 5, 6 |

You do not choose a method because it is fashionable. The shape of the data chooses it for you.

---

## This Is Not Theoretical

One example, with real numbers.

**Idiopathic pulmonary fibrosis** is a disease in which the lungs slowly become scarred. Breathing gets harder over time and there are very few treatments. Lung function is tracked by measuring **forced vital capacity** — how much air a person can blow out in one breath. In this disease the number falls year after year.

In 2021 a company called Insilico Medicine used an AI system to propose a protein called TNIK as a target for this disease. A second AI system designed a molecule to act on that protein.

The molecule reached its first human trial in under 30 months from the target being identified. The usual figure is closer to five years.

In June 2025 the Phase 2 results were published in *Nature Medicine*. On the 60 mg dose, patients' forced vital capacity **improved by 98.4 mL**. The placebo group **declined by 20.3 mL**. It entered Phase 3 trials in July 2026.

### What this does and does not show

It shows that a target chosen by a machine and a molecule designed by a machine can survive into a real trial and produce a real result. Five years ago that had not been demonstrated.

It does not show that the problem is solved. This is one drug. It is not approved. Phase 3 is the stage where most drugs fail, and it may yet fail there. And even with everything compressed, it still took from 2021 to 2026 to get this far.

---

## What an AI Project Actually Looks Like

Every project in this course, including the one you will build yourself, has the same six steps.

**1. The question.** What exactly are you trying to predict or find out? Stated precisely enough that you could tell whether you had answered it.

**2. The data.** Where will the rows come from, how many are there, and is the label column actually filled in?

**3. The model.** Choose one, train it.

**4. Checking it.** Test it on rows it has never seen. A model that gets every training row right and every new row wrong is a common and completely useless outcome.

**5. Using it.** Someone acts on its output.

**6. Watching it.** Does it still work six months later, on newer data than it was trained on?

### Where projects fail

Almost always at step 1 or step 6.

**Step 1** fails when the question is vague, or when the data needed to answer it does not exist. "Can we use AI to improve formulation" is not a question. "Can we predict tablet hardness from these seven process parameters, using the 400 batches we already have records for" is.

**Step 6** fails when nobody checks. A model trained on data from 2020 quietly stops being right, and because it still returns confident answers, nobody notices.

You will choose your own project in Session 20. It will have all six steps, and step 1 is the one to spend time on.
