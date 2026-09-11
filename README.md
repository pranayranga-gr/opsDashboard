# Ops Dashboard Prototype

This repository hosts the Ops Dashboard prototype for stakeholder and client review.

Prototype URL:

```text
https://pranayranga-gr.github.io/opsDashboard/
```

Access code:

```text
ops-review-2026
```

## Reviewer Flow

Send reviewers the prototype URL and access code. Ask each reviewer to enter their real name when prompted so their review session can be connected with their feedback.

Suggested message:

```text
Hi [Name],

Please review the Ops Dashboard prototype here:
https://pranayranga-gr.github.io/opsDashboard/

Access code:
ops-review-2026

When prompted, please enter your name so we can connect your comments with your review session.

As you go through the prototype, please try to use it naturally:
- What would you click first?
- What feels unclear?
- What information is missing?
- What would make this more useful for your workflow?

We are using session analytics to understand navigation patterns and improve the prototype.
```

## Using Microsoft Clarity

Microsoft Clarity is configured on the hosted prototype. Use it to understand how reviewers interact with the wireframe.

### Recordings

Start with session recordings. They show how a reviewer moved through the prototype, where they clicked, where they paused, and whether they tried to interact with something that was not clickable.

Use recordings to answer:

- Did the reviewer understand the dashboard quickly?
- Did they click elements that are not interactive?
- Did they hesitate around specific labels or controls?
- Did they miss important information?
- Did they follow the journey we expected?

### Heatmaps

Use heatmaps after several reviewers have visited the prototype. Heatmaps show where reviewers click most often.

Use heatmaps to identify:

- Buttons or areas reviewers expect to be clickable
- Sections that draw the most attention
- Important areas that are being ignored
- Confusing elements that attract repeated clicks

### Dashboard

Use the Clarity dashboard mainly to confirm visits and overall engagement. For prototype review, recordings and heatmaps usually provide the most useful evidence.

### Filtering By Reviewer

The access gate sends the reviewer name to Clarity with:

```js
clarity("identify", reviewerName)
```

In Clarity, use custom user ID or user filters to find sessions tied to a specific reviewer name.

## Turning Observations Into Product Improvements

Use this format to summarize findings:

| Observation | Evidence in Clarity | Product improvement |
| --- | --- | --- |
| Reviewer clicked a non-clickable status card | Repeated clicks in recording | Make the card clickable or reduce the visual affordance |
| Reviewer paused on routing labels | Long hesitation before next action | Rename labels or improve hierarchy |
| Reviewer ignored the task drawer | No clicks on task icon | Make the task count more prominent |

Clarity shows what happened, but it does not always explain why. Pair Clarity findings with written comments or a short follow-up conversation.

## Combining Clarity With Follow-Up Questions

Use Clarity as the evidence layer, then use a short follow-up to understand the reviewer's intent.

Recommended workflow:

1. Send the prototype link and access code to the reviewer.
2. Ask them to use the prototype naturally for 5-10 minutes.
3. Watch their Clarity recording.
4. Note 3-5 moments where something interesting happened, such as hesitation, repeated clicks, skipped sections, or clicks on non-clickable elements.
5. Send a short follow-up form or email asking about those moments.

Suggested follow-up questions:

```text
Thanks for reviewing the Ops Dashboard prototype.

A few quick follow-up questions:

1. What was the first thing you tried to understand or click?
2. Was anything unclear, missing, or misleading?
3. Were there any areas where you expected more detail or a next step?
4. Which part of the dashboard would be most useful in your actual workflow?
5. If you could change one thing before the next version, what would it be?
```

Use this format to connect behavior with intent:

| Clarity observation | Follow-up question | Product decision |
| --- | --- | --- |
| Reviewer clicked a non-clickable card | What were you expecting to happen there? | Make the card clickable or change the styling |
| Reviewer paused on a label | What did this label mean to you? | Rename the label or improve the hierarchy |
| Reviewer skipped a key section | Did this section feel useful? | Move it, simplify it, or remove it |
| Reviewer opened the same area repeatedly | What information were you looking for? | Add missing detail or improve navigation |

This keeps the review lightweight. Clarity shows the behavior, and the follow-up questions explain the reason behind it.

## File Ownership

`Concept Prototype Ops Dashboard.html` is the UI/UX-owned prototype export. Keep changes to that file minimal.

The only engineering-maintained block inside that file is clearly marked:

```html
<!-- BEGIN: Microsoft Clarity tracking - maintained by engineering wrapper setup -->
...
<!-- END: Microsoft Clarity tracking -->
```

Hosting, access gate behavior, reviewer identification, and wrapper-level analytics are maintained in `index.html`.
