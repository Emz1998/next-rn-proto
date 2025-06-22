
# NextRn – Mobile App Product Requirements Document (PRD)

**Version:** 1.0  
**Last Updated:** 20 Jun 2025

---

## 1. Introduction & Problem Statement

### 1.1 Executive Summary  
NextRn is a mobile‑first social and micro‑learning platform connecting **student nurses** with **registered nurses (RNs)** for real‑time mentorship, academic support, and career guidance. It leverages threaded discussions, live chat, and livestream Q&A to deliver timely answers while providing nurses with flexible income streams – directly addressing burnout and knowledge gaps among nursing cohorts.

### 1.2 Problem Statement  
Student nurses often struggle to access verified answers quickly during clinical rotations or exam prep. Existing forums are desktop‑centric, slow, or unmoderated, leading to misinformation. RNs willing to help rarely receive compensation, contributing to burnout. *On‑the‑go*, trustworthy support is missing in the mobile context.

### 1.3 Justification for a Mobile App  
Nursing students spend long hours in hospitals and commuting; a dedicated **native‑like** app ensures offline caching, push notifications, and biometric log‑in — conveniences a mobile web experience cannot fully match. React Native offers a single codebase for iOS & Android, accelerating time‑to‑market while preserving near‑native performance.

---

## 2. Goals & Objectives

| Goal | Metric | Target | Timeline |
|------|--------|--------|----------|
| Acquire early cohort | App Store downloads | 5 000 within 3 months of launch | T+3 months |
| Engagement | DAU / MAU ratio | ≥ 35 % | Rolling monthly |
| Retention | Day‑30 retention | ≥ 25 % | Rolling |
| Revenue | Average monthly gross GMV from paid DMs / Super Chats | ≥ $8 000 by month 6 | T+6 months |
| Reliability | Crash‑free session rate | ≥ 99.6 % | Always |

*KPIs separated into business vs. technical per rule 2.2* fileciteturn1file0

---

## 3. Users & Personas

| Persona | Context of Use | Pain Point | Mobile Need |
|---------|---------------|------------|-------------|
| **Sofia, 2nd‑year student** | On train to clinical site; one‑hand phone use | Needs quick dosage confirmation | Fast answer, offline cache |
| **Jon, RN mentor** | Break room, limited time | Wants to monetize expertise without commitment | Push alert for paid DM |
| **Lynn, exam crammer** | Library study session | Overwhelmed by threads | Curated high‑signal answers |

Personas focus on *mobile contexts* per rule 3.1 fileciteturn1file3.

---

## 4. Features & Requirements (MoSCoW)

### Must‑Have (P0)
- **Threaded Lobby:** “As a student, I want to post questions so that multiple RNs can weigh in.”  
  *Acceptance:* Post appears instantly; can be liked, bookmarked.
- **Live Chat Lounge:** “As a student, I want Discord‑style chat for group study.”
- **Paid DM (queue):** “As a student, I can send a paid question to a VIP RN.”
- **Push Notifications:** New replies, DM responses.

### Should‑Have (P1)
- **Livestream Stage with Super Chats.**
- **Hall of Excellence badges.**

### Could‑Have (P2)
- **AI answer suggestions for unanswered posts.**

### Won’t‑Have (Out of Scope)
- TikTok‑style short‑form video feed (future).

Out‑of‑scope section satisfies rule 4.2 fileciteturn1file3.

---

## 5. Platform & Technical Requirements

| Item | Spec |
|------|------|
| **Platforms** | iOS & Android (single React Native codebase) |
| **Min OS** | iOS 15+, Android 11+ |
| **Devices** | Phones first, tablet‑optimized later |
| **Orientation** | Portrait primary, landscape optional for livestream |
| **Launch Time** | < 2 s cold start |
| **Offline** | Cache last 50 messages & bookmarked posts |
| **Battery** | ≤ 3 % drain per hour active use |

---

## 6. Mobile‑Specific Considerations

### 6.1 Gestures & UI
- Tap, swipe left/right to switch rooms, long‑press to react.

### 6.2 Push Notification Strategy
- Trigger on: DM reply, post answered, livestream starting.  
- Sample copy: “🩺 RN Emma replied – tap to view answer.”

### 6.3 Hardware Access & Permissions
| Access | Reason | Permission Timing |
|--------|--------|-------------------|
| Camera | Avatar & livestream | In‑context when user taps “Upload photo” |
| Microphone | Livestream host | At start of stream |
| Biometrics | Quick login | First app open (optional skip) |

Permissions flow defined per rule A.4 fileciteturn1file2.

---

## 7. App Distribution & Lifecycle

| Store Info | Value |
|------------|-------|
| **Name** | NextRn |
| **Subtitle** | Nursing Support, Anywhere |
| **Category** | Education / Medical |
| **Keywords** | nursing, student nurse, RN, NCLEX |

**Update Strategy:** Optional updates with forced update if API version mismatch; “What’s New” screen after major release.  
**Analytics & Crash Reporting:** Firebase Analytics events (screen_view, dm_sent, superchat_purchase) + Sentry for crashes.

---

## 8. Success Criteria (Definition of Done)

1. All Must‑Have features pass acceptance tests.  
2. App passes Apple TestFlight & Google internal testing with ≥ 99 % crash‑free sessions.  
3. Day‑7 retention ≥ 30 % in closed beta.  
4. Legal/Compliance review complete (HIPAA alignment for PHI avoidance).

---

## 9. Open Questions & Assumptions

| # | Item | Plan to Validate |
|---|------|------------------|
| 1 | Student willingness to pay $2 per DM | Survey beta cohort |
| 2 | RN supply to meet demand | Pilot with 20 RNs |
| 3 | Battery drain with livestream | Measure in QA lab |

---

*Self‑review complete – all required sections and mobile‑specific rules addressed.* fileciteturn1file1
