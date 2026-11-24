# Privacy information · Class Manager for Moodle™

This page describes the personal data that **Class Manager** (`local_efclassmanager`) stores. It mirrors what the
plugin declares through Moodle's Privacy API, so the same information appears in your own site under
*Site administration → Users → Privacy and policies → Plugin privacy registry*.

- **Everything stays in your Moodle site.** The plugin sends no data to eLearning Fácil or to any third party, and it
  loads no resources from external servers.
- **Data subject requests are supported.** The data is included in a user's data export and removed by a data
  deletion request, with the exception noted below for removal records, which keep the seat count of the course.

## What it stores

**Sign-ups** made by the class manager, one record per student and course:

- The student signed up (or the existing account linked) and the class manager who did it.
- The ID number entered at sign-up and the username generated or linked.
- The access period applied (start and end).
- The welcome email: mode, delivery status, attempts and when it was sent.
- The create-password link of the welcome email: only a SHA-256 hash of its single-use token (the token itself is
  never stored), when it expires and when it was used.

**Removals**: when a class manager removes a student from a course, a snapshot of who was removed (username, name,
email and groups at that moment), when, by whom and the reason entered, and whether the student was signed up again
later.

**User accounts**: sign-ups create user accounts in Moodle and write the ID number and the additional data entered
by the class manager to the user profile. When the welcome email includes a password, the account is asked to change
it on first login (Moodle's own `auth_forcepasswordchange` preference).

The settings of each course and group (seats, access periods, welcome texts, reply-to and support addresses) are
configuration entered by the site, not records about students.

## Data requests

- **Export**: a student receives their sign-ups and removals in full. A class manager receives only the fact and the
  dates of what they did; the students' personal data belongs to the students and is not included.
- **Deletion**: a student's sign-up records are deleted. Their removal records are **anonymised, never deleted**:
  name, username, email and reason are replaced, so the seat they used still counts towards the course's limit. For
  a class manager, only the reference to them is removed from the records they created.

## Logs

The actions of class managers (sign-ups, removals, readmissions, access period and email changes, welcome emails
sent or failed…) are recorded as events in Moodle's standard log and follow the site setting "Keep logs for".

---

Developed and maintained by eLearning Fácil (https://elearningfacil.com), an independent company that builds plugins
and themes for Moodle™, designed for training providers and companies. Not affiliated with Moodle Pty Ltd.
Moodle™ is a registered trademark of Moodle Pty Ltd.
