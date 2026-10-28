# Mentor Connect

A simple website that helps students get unstuck in their careers. A student describes a career problem, sees which mentors can help, and books a call.

**Live demo:** [add your Netlify URL]

## How it works

1. **Describe your problem.** The student writes a few sentences about what they're stuck on.
2. **See matching mentors.** The site shows mentors from the provided mentor list, best match first, with a short "Why" line explaining each match.
3. **Book a call.** The student picks a time slot, enters their name, email and topic, and confirms. The call itself happens on the student's own video link.

## Design choices

- **Only real mentor details.** The three mentors come from the provided Mentor_Sample_50 sheet. The page shows only fields that exist there (domain, seniority, sectors, roles, rating, past activity) and never makes anything up.
- **Transparent matching.** The student's text is matched against keywords tied to each mentor's listed experience. If nothing matches, the page says so and shows all mentors.
- **Handled edge cases.** Descriptions that are too short, problems with no clear match, double-booking the same slot, and invalid form input.
- **No dependencies.** One `index.html` file with no server and no build step.

## Run locally

Open `index.html` in a browser.

## Assumptions and limitations

- The mentor sheet has no availability data, so time slots are sample slots (10:00, 14:30 and 18:30 IST over the next five days).
- Bookings are saved only in the visitor's browser (localStorage). No emails are sent.
- Only 3 of the 50 mentors are included.

## Possible next steps

- Real mentor availability and calendar invites
- An AI intake assistant, with a check that rejects any mentor not on the list
- Post-call write-ups that the mentor confirms before the student sees them
