# What is Phylax

Phylax is a personal, data-sovereign health platform that runs in your browser. You build and maintain your medical profile as a living document: observations, lab values, supplements, open points and profile versions grow with you over years, encrypted with your master password, exclusively on your device.

## The core idea

Classical health apps manage you. Phylax does not. Phylax treats health as a process led by a person: you observe, you recognize patterns, you self-regulate, and you document what actually happened. Doctors, lab reports and therapies are part of the picture, but they are not the source of truth about your body, you are.

This idea is called "Living Health". Phylax is its app-shaped form.

## Why Phylax exists

People with chronic conditions, people caring for an elderly relative, people working through a long unresolved diagnostic process, all know the same problem: lab reports are scattered, self-observations get forgotten, and the next physician appointment lacks a thread connecting what came before. Tracker apps do not solve this because they aim at counting ("steps today") rather than understanding ("which pattern has been showing up for three months").

Phylax is an attempt to build a toolbox that supports understanding without handing your data to a third party.

## Who Phylax is for

- People living with chronic or unresolved conditions who want to keep a thread across years
- Family members maintaining a profile on someone else's behalf (parent, child)
- People who want to use AI as a structuring partner without sending their health data to a vendor cloud
- Anyone who wants software that belongs to them, not the other way around

## What makes Phylax different

Apple Health, Google Fit and the popular tracker apps store your data in the vendor's cloud. Phylax does not. There is no Phylax server. Your data does not leave your browser unless you actively export it. There is no telemetry, no analytics, no advertising tracker. Phylax is open source; the code is on GitHub for anyone to inspect.

AI is optional and bring-your-own-key: if you use it, you supply your own API key from OpenAI or Anthropic. Phylax acts only as a relay; your requests go directly from your browser to the provider you chose.

## What Phylax is NOT

- **Not a medical device.** Phylax does not diagnose and does not give therapy recommendations.
- **Not cloud-synced.** Data stays per device. Moving to another device goes through the encrypted `.phylax` backup, not automatic sync.
- **Not a physician portal.** Phylax is for you, not your doctor. They get a printout or a PDF export if you choose to share one.
- **Not auto-interpreting.** When you enter a lab value, Phylax does not tell you what it means. That conversation belongs with your physician.

## Read more

- [First Steps](first-steps.md) walks you from "app opened" to "first profile created".
- The thinking behind Phylax is in the "Living Health" article series: [Part 1: From Patient to Partner](https://asterios-raptis.medium.com/living-health-from-patient-to-partner-9fff311a8c45), [Part 2: Living Health in Practice](https://asterios-raptis.medium.com/living-health-in-practice-d53964053500). Parts 3 and 4 are translation in progress.
- Phylax is open source: [github.com/astrapi69/phylax](https://github.com/astrapi69/phylax).

Status: 2026-04-27 (Iteration 1, first content)
