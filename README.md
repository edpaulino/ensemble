# Ensemble

A verified, anonymous panel of people who work at frontier AI labs, answering questions from policymakers. Built for BlueDot's hackathon on AI tools for better decisions and coordination (San Francisco, September 2026), and still a work in progress.

Live page: https://edwardpaulino.com/ensemble/

## The problem

Policymakers writing rules for frontier AI hear mostly from the labs' government-affairs teams. The staff who build these systems know how things actually work, but have no low-risk way to weigh in.

## How it would work

1. **Ask.** Legislators' offices, agencies and AI safety nonprofits send the questions they most need answered.
2. **Answer.** Panelists get each question on Signal and answer anonymously in an encrypted CryptPad form. Questions are worded so answering never needs confidential information.
3. **Share.** We publish a short brief: how many people answered, from how many labs, and where views split. Nothing is reported from fewer than 10 answers.

Recruiters vouch for members with single-use codes; anyone else is verified in a short conversation.

## Status

A hackathon prototype. The site is live and the Signal account is set up. The panel isn't funded yet, and we're looking for recruiters, funders and advisers.

## This repo

The public site: one HTML page and a stylesheet, served by GitHub Pages as is, with no build step. It runs no scripts and sets no cookies, and a Content Security Policy blocks anything not from this site. The font, ET Book, is self-hosted in `fonts/` under its MIT license.

To check the live page matches this repo:

```bash
for f in index.html style.css; do cmp -s <(curl -s https://edwardpaulino.com/ensemble/$f) <(curl -s https://raw.githubusercontent.com/edpaulino/ensemble/main/$f) && echo "same $f" || echo "DIFFERENT $f"; done
```
