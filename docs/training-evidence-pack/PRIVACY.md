# Privacy information · Training Evidence Pack for Moodle™

This page describes the personal data each plugin of the Training Evidence Pack stores. It mirrors what every plugin
declares through Moodle's Privacy API, so the same information appears in your own site under
*Site administration → Users → Privacy and policies → Plugin privacy registry*.

Common to all the plugins:

- **Everything stays in your Moodle site.** No plugin sends data to eLearning Fácil or to any third party, and none
  loads resources from external servers.
- **Data subject requests are supported.** The plugins that store personal data implement Moodle's Privacy API:
  the data is included in a user's data export and removed by a data deletion request, with the exceptions noted
  below for records that are course evidence.

## local_efreport

**Training Evidence: Time, Activity & Evaluation Report** stores:

- Active time spent by each user on each course activity, and the same time by quarter-hour.
- The estimated time of a student before the clock was enabled, calculated from the logs.
- The work schedule each student follows in a group.
- Supporting evidence attached to a student record (the files are kept in Moodle's file storage) and the audit trail
  of its uploads and deletions.
- Manual certifications of attendance at BigBlueButton™ sessions.
- Downloads of certificates from "My certificates", as proof of delivery.
- Marks set by the time-based completion engine (an activity held incomplete below the required minutes, or
  completed by time). The completion itself is recorded in Moodle's activity completion.
- Bulk message batches sent from the report (sender, text and filter) and their delivery queue. The messages
  themselves are delivered through Moodle messaging.
- Two user preferences of the report interface.

Retention: the setting *Data retention (days)* deletes sessions older than the number of days you choose; 0 keeps
them indefinitely. The report access log lives in Moodle's standard log and follows the site setting "Keep logs for".

## local_efcomms

**Training Evidence: Communications Report** reads forum posts and messages that Moodle already holds; it does not
copy their content. It stores:

- A log of who viewed communication content (who, what and when; never the content).
- Off-platform communications: PDFs attached to a student's record by managers or teachers (kept in Moodle's file
  storage), and the audit trail of their uploads and deletions.
- The audit trail of changes to sensitive settings.
- Export jobs requested by users.
- Bulk message batches sent from the report and their delivery queue. The messages themselves are delivered
  through Moodle messaging.

## local_efdossier

**Training Evidence: Group Dossier** stores:

- The dossiers requested: who asked for them and with which filters.
- The audit trail of who generated and who downloaded each dossier.
- The dossier ZIP files, in Moodle's file storage. A dossier contains the time, communications (full content),
  grades, activity log and supporting evidence records of every student in the course, and is kept as evidence of
  the training.

## local_efalerts

**Training Evidence: Automatic Alerts** stores:

- The alerts issued to each student, as engagement evidence.
- The queue of alert messages pending delivery.
- The per-course configuration of the alerts.

The notices are delivered as Moodle messages from the tutor to the student.

## local_efready

**Training Evidence: Course Ready Check** stores who ticked each manual checklist item in a course, and when. The
tick itself is course configuration: deleting a user's personal data removes who ticked the item; the tick stays.

## availability_eftime

**Training Evidence: Time Restriction** does not store any personal data. It only reads the time already tracked by
the Time, Activity & Evaluation Report (`local_efreport`).

## availability_efreq

**Training Evidence: Requirements Restriction** does not store any personal data. It only reads the data already
held by the Time, Activity & Evaluation Report (`local_efreport`).

## block_efprogress

**Training Evidence: My Progress** only displays existing data: Moodle's own activity completion and, when it is
installed, the time measured by `local_efreport`. It does not store any personal data.

## block_eflinks

**Training Evidence: Report Links** only displays links. It does not store any personal data.

---

Developed and maintained by eLearning Fácil (https://elearningfacil.com), an independent company that builds plugins
and themes for Moodle™, designed for training providers and companies. Not affiliated with Moodle Pty Ltd.
Moodle™ is a registered trademark of Moodle Pty Ltd. BigBlueButton™ is a trademark of BigBlueButton Inc.
