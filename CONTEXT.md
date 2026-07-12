# HighView

This context defines the language for the current student-engagement platform spanning staff operations and student progress.

## Language

**Student**:
A learner whose profile, participation, enrollment, and progress are represented in HighView.
_Avoid_: Cohort row without an identity, staff user

**Staff Member**:
An authorized operator who manages cohort programs, sessions, courses, opportunities, and engagement interventions.
_Avoid_: Student with elevated UI state

**Cohort**:
A managed group of Students evaluated over a shared program or academic period.
_Avoid_: Course roster, filtered table only

**Engagement Record**:
The persisted evidence used to calculate attendance, pillar progress, and at-risk signals for a Student.
_Avoid_: Hardcoded chart value, browser preference

**Program Session**:
A scheduled event with attendance rules and optional grade-level requirements.
_Avoid_: Authentication session, course

**Attendance Requirement**:
A rule describing which Students must attend a Program Session.
_Avoid_: Registration, observed attendance

**Course**:
A learning offering with schedule, capacity, and completion state.
_Avoid_: Program Session, static catalog card

**Enrollment**:
The persisted relationship between a Student and a Course.
_Avoid_: Clicking Register without backend confirmation

**Opportunity**:
A staff-managed internship, job-shadow, event, or experiential-learning listing available to eligible Students.
_Avoid_: Course, notification

**Student Profile**:
The Student-owned academic and professional identity used across progress and opportunity workflows.
_Avoid_: Authentication metadata alone

**Pillar Progress**:
An evidence-backed measure for AI Learning, Experiential Learning, or Session Attendance.
_Avoid_: Manually displayed percentage without an Engagement Record

**Prototype-Local State**:
Any remaining localStorage-backed auth, settings, registration, or profile behavior. It is migration debt and must not be described as multi-device persistence or production truth.
_Avoid_: Supabase record, production system of record
