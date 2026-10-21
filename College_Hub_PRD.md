# College Hub — Product Requirements Document

Ali · October 21, 2026

## Overview

College Hub is a mobile app that gives college students one place for three things: finding and sharing study files, looking up information about their college, and reading official news and decisions. Students search and upload course materials. Staff publish announcements to a news board at the top of the home screen. It is a student-run practice project for a single college, with no budget and no official sponsorship.

## Problem statement

Study material and college information are scattered, and students miss official decisions. Today:

- Lecture notes, past exams and summaries move through WhatsApp and Telegram groups, where they get buried and are hard to search.
- New students struggle to find basic facts: departments, schedules, contacts, locations and procedures.
- College decisions (exam dates, holidays, rule changes) are posted on paper boards or social pages, so many students hear about them late or never.

College Hub replaces these channels with one trusted, searchable source.

## Goals and non-goals

**Goals**

1. Let students find a study file for their course in under 30 seconds.
2. Make college decisions reach every active user on the day they are published.
3. Give new students a complete, up-to-date guide to the college.
4. Build a shared library of study files that grows through student uploads.

**Non-goals (first release)**

- Grades, attendance or registration (these belong to the college's student information system).
- Live classes, video lectures or a full learning management system.
- Chat or social feeds between students.
- Paid ads, paid content or a marketplace for selling notes.

## Target users

The app serves three roles. Each one has different permissions.

| Role | Who | Main needs | Can do |
| --- | --- | --- | --- |
| Student | Undergraduates, all years | Find study files, read news, learn about the college | Search, download, upload files, save favorites, rate files, report content |
| Moderator | A team of 5 trusted students covering all departments | Keep the file library clean | Approve or reject uploads, remove reported files |
| College admin | The student team, reposting official college news and decisions | Reach all students with official information | Publish news and decisions, pin announcements, edit college info, manage users |

## Core features

The app has four main areas, reached from a bottom navigation bar: Home, Study Files, College and Profile.

**1. News and decisions board (Home)**

- A banner block at the top of Home rotates through pinned announcements, like an ad slot, but it carries no paid ads.
- Below it sits a feed of news and official decisions, newest first, each tagged by type: Decision, News, Event or Exam.
- Each post has a title, body, optional image or PDF attachment, publish date and the issuing office.
- Urgent decisions trigger a push notification.

**2. Study files**

- Files are organized by Department → Stage (year) → Course → Type (lecture, summary, past exam, assignment).
- Search by keyword, with filters for department, stage, course, file type and semester.
- Upload PDF, Word, PowerPoint or image files, with the course and type filled in on upload.
- New uploads wait for moderator approval before they appear.
- Students can download, save to favorites, rate and report files.

**3. College information**

- About the college, departments and their heads, and staff contact details.
- Academic calendar and exam schedules.
- Campus map and building locations.
- Common procedures and FAQs (registration, transfers, document requests).

**4. Profile**

- Sign up with the student's college email, confirmed with a one-time code.
- Department and stage, used to personalize files and news.
- My uploads, favorites, downloads and notification settings.

## User stories

- As a **student**, I want to search past exams for my course so I can prepare for finals.
- As a **student**, I want to upload my lecture summary so classmates can use it.
- As a **student**, I want a notification when the college posts an exam schedule so I don't miss it.
- As a **new student**, I want to find my department's location and head of department so I know where to go.
- As a **moderator**, I want a queue of pending uploads so I can approve good files quickly.
- As a **college admin**, I want to pin an urgent decision to the top banner so every student sees it first.
- As a **college admin**, I want to attach the official decision PDF to a post so students see the original document.

## Functional requirements

P0 items make up the MVP. P1 and P2 follow in later phases.

| ID | Area | Requirement | Priority |
| --- | --- | --- | --- |
| FR-1 | Accounts | Sign up and log in with a verified college email; role set to Student, Moderator or Admin | P0 Must |
| FR-2 | News | Admins create, edit, pin and delete posts with type tag and attachment | P0 Must |
| FR-3 | News | Home shows a rotating banner of pinned posts above a newest-first feed | P0 Must |
| FR-4 | News | Push notification for posts marked urgent | P0 Must |
| FR-5 | Files | Browse files by department, stage, course and type | P0 Must |
| FR-6 | Files | Keyword search with filters; results in under 2 seconds | P0 Must |
| FR-7 | Files | Upload files up to 25 MB (PDF, DOCX, PPTX, JPG, PNG) into a moderation queue | P0 Must |
| FR-8 | Files | Moderators approve, reject or remove files; uploader is notified | P1 Should |
| FR-9 | College info | Admin-editable pages for departments, staff, calendar, map and FAQs | P1 Should |
| FR-10 | Files | Favorites, ratings and reporting | P1 Should |
| FR-11 | Personalization | Feed and file suggestions filtered by the student's department and stage | P1 Should |
| FR-12 | Files | Offline access to saved files | P2 Could |
| FR-13 | News | Comments or reactions on news posts | P2 Could |
| FR-14 | Platform | Support for multiple colleges in one app | P2 Could |

## Non-functional requirements

| Area | Requirement |
| --- | --- |
| Platforms | Android and iOS from one codebase (for example Flutter or React Native); admin panel on the web |
| Language | Arabic and English, with full right-to-left layout for Arabic |
| Performance | App opens in under 3 seconds; search returns in under 2 seconds on 4G |
| Scale | Handles 10,000 registered students and 1,000 people online at once |
| Security | Encrypted connections (HTTPS); role-based permissions; only verified students can upload |
| Storage | Files virus-scanned on upload; duplicate files detected |
| Accessibility | Readable font sizes, screen reader labels, sufficient color contrast |
| Availability | 99.5% uptime, with extra capacity during exam periods |

## Success metrics

These targets are measured 6 months after launch. They are starting proposals to adjust with the college.

| Metric | Target |
| --- | --- |
| Registered students | 50% of enrolled students |
| Weekly active users | 40% of registered students |
| Approved study files in the library | 2,000 |
| Searches that end in a download | 60% |
| Students who open an urgent decision within 24 hours | 70% |
| Upload approval time | Under 48 hours |
| App store rating | 4.3 or higher |

## Release plan

| Phase | Scope | Includes | Gate to next phase |
| --- | --- | --- | --- |
| Phase 1 · MVP | P0 · FR-1 to FR-7 | Sign-up and roles; news board, banner, alerts; browse, search, upload files; uploads approved by admins | Pilot with 1 department |
| Phase 2 · Growth | P1 · FR-8 to FR-11 | Moderator role and tools; college information pages; favorites, ratings, reports; personalized feed and files | All departments live |
| Phase 3 · Expansion | P2 · FR-12 to FR-14 | Offline saved files; comments and reactions; multiple colleges | Ongoing, driven by feedback |

Phase 1 alone is enough to launch, since it covers both the news board and the study file library. With no budget, every phase runs on free tools and hosting tiers, and the team's own schedule sets the dates.

## Risks and decisions

**Risks**

| Risk | Mitigation |
| --- | --- |
| Copyrighted textbooks get uploaded | Moderation queue, report button, clear upload rules, fast takedown |
| Too few files at launch, so students don't return | Seed the library with moderators and class representatives before launch |
| Official news is missed because the college is not a partner | Student admins repost each decision with the original document attached; posting takes under 2 minutes |
| Fake or unofficial "decisions" spread | Only verified admin accounts can post; every post shows the issuing office |
| Storage costs grow with uploads | Free hosting tiers, 25 MB file limit, duplicate detection, compression |

**Decisions**

- **Sponsorship:** student-run. The college is not an official sponsor.
- **Verification:** college email only, confirmed with a one-time code.
- **Banner:** college announcements only, with no paid ads.
- **Moderators:** 5 students, covering all departments.
- **Budget:** none. This is a practice project, so it uses free tools and free hosting tiers.
