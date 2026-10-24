# Love Style Quiz

A 5 Love Languages quiz for individuals and couples. It's a single static page with no build step, no backend and no dependencies apart from Google Fonts.

## Features

- 110 "I feel most loved when my partner…" questions plus 10 "how I give love" questions. There's also a quick 40-question mode.
- Scores the five love languages (Words of Affirmation, Quality Time, Receiving Gifts, Acts of Service, Physical Touch) plus the specific "dialects" within each.
- Love report with 12 sections: primary and secondary styles, giving vs receiving, compatibility, tips, least comfortable styles, friends and family, self-love, workplace, personality, finances and parenting.
- Couples can take turns on one device, or compare results with a share code.
- Partner compatibility score, how each partner can love the other best, and potential love blockers.
- 28-day personal-growth challenge and 28-day relationship challenge, with progress saved in the browser.
- Roadmap for strengthening all your relationships.
- "See a sample report" button on the home screen.
- Light and dark mode, mobile friendly.

## Privacy

Everything runs in the browser. Answers and progress are stored in `localStorage` on the user's device, and nothing is sent to a server. Partner codes are the user's scores encoded in the code itself.

## Run locally

Open `index.html` in a browser. To run it on a local web server instead:

```bash
npx serve .
```

## Deploy to Vercel

1. Push this folder to a GitHub repository.
2. In Vercel, choose **Add New → Project**, then import the repository.
3. Framework preset: **Other**. Leave the build command and output directory empty.
4. Click **Deploy**.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole app: markup, styles, quiz data, scoring and report |
| `favicon.svg` | Browser tab icon |
| `vercel.json` | Clean URLs and basic security headers |

## How scoring works

- **Receiving styles:** for each language, *times chosen ÷ times offered*. Only questions that compare two different languages count. The five rates are then scaled to add up to 100%.
- **Giving styles:** 10 questions, one for each pair of languages.
- **Compatibility:** 40% × overlap of receiving styles + 30% × how well A's giving matches B's receiving + 30% × the reverse.

The model is based on Gary Chapman's *The 5 Love Languages* (1992). The quiz is for self-reflection, not a clinical assessment.
