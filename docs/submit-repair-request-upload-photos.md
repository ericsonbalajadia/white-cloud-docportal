## White Cloud  
**Target:** AB.010.001

---

#### Site Map
[Project Homepage](project-homepage.md) > [Online Request Submission](online-request-submission.md) > **Upload Photos**

---
## Submit Repair Request – Submit Form – Upload Photo/s
The requester uploads photo attachments for the repair request.

#### Actors
- Requester

#### Preconditions
- Repair form is open

#### Postconditions
- Photo(s) are attached to the form

---

#### Basic Flows

| Actor Action | System Response |
|-------------|-----------------|
| 1. Requester clicks Upload Photos. | 1.1 System displays the file selection window. |
| 2. Requester selects and confirms the photos. | 2.1 System uploads and attaches the photos to the request. |

---

#### Database Schema Reference

#### Attachment Table
```
- attachment_id (PK)
- request_id (FK)
- feedback_id (FK, nullable)
- file_name
- file_path
- file_size
- file_type
- uploaded_by
```

---

© 2026 TRAQ
