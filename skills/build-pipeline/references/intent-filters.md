# Intent filters and copy

One intent filter per saved search, so each campaign speaks to one reason for reaching out.
Replace the `{{placeholders}}` with your own words before the campaign goes live.

## Lead signals

Sales Navigator lead search, groups **Buyer intent** and **Recent updates**. Ask `build_sn_search_from_prompt` for the ICP people plus the signal in plain words.

### Following your company

- **What it means:** They follow your company page on LinkedIn.
- **Why it works:** They already know you exist, so your email is not a cold one.
- **Opener:** You follow {{yourCompany}} on LinkedIn, so you have probably seen what we do with {{yourTopic}}.
- **Follow-up:** Since you follow our updates, I thought the {{caseStudy}} result would be relevant: {{oneLineResult}}.

### Viewed your profile recently

- **What it means:** They looked at your own LinkedIn profile recently.
- **Why it works:** They were curious about you first. Answering that curiosity feels natural.
- **Opener:** Saw you checked my profile, so I'll keep this short.
- **Follow-up:** Was it {{yourTopic}} that caught your eye? Happy to share how {{similarCompany}} handles it.

### Changed jobs

- **What it means:** They started a new role in the last 90 days.
- **Why it works:** New leaders review their tools and budgets in their first 90 days.
- **Opener:** Congrats on the new role at {{companyName}}. The first 90 days are when most {{jobTitle}}s rethink {{yourTopic}}.
- **Follow-up:** When {{similarPerson}} joined {{similarCompany}}, the first thing they fixed was {{problem}}. Worth a look?

### Posted on LinkedIn

- **What it means:** They published a post in the last 30 days.
- **Why it works:** Active posters read their notifications and answer people who engage with their ideas.
- **Opener:** Your recent post on {{postTopic}} made me think of a problem we solve for {{jobTitle}}s.
- **Follow-up:** Following up on {{postTopic}}: here is the one-page version of how {{similarCompany}} approached it.

## Account signals

Hiring, leadership changes, funding and headcount growth belong to the company, so they need an account list that is refreshed every week. This plugin does not set them up: point the user to https://github.com/evaboot-labs/unlimited-leads-system, which ships the refresh script.
