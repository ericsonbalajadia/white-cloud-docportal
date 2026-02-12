## White Cloud  
**Target:** AB.010.001

---

### Site Map
[Project Homepage](project-homepage.md) > [Online Request Submission](online-request-submission.md) > **Submit Form**

---

# Submit Repair Request – Submit Form

## Summary
The requester fills out and submits the repair request form.

## Actors
- Requester

## Preconditions
- Requester is logged in

## Postconditions
- Repair schedule is recorded in the system

---

## Basic Flows

| Actor Action | System Response |
|-------------|-----------------|
| 1. Requester fills out the form. | 1.1 System displays the entered details. |
| 2. Requester clicks Submit. | 2.1 System saves the request and shows confirmation. |

---

## Form Fields

Based on the ERD, the request form should include:

### Required Fields
- **Title:** Brief description of the issue
- **Description:** Detailed explanation of the repair/service needed
- **Category:** Type of request (HVAC, Plumbing, Electrical, etc.)
- **Priority:** Emergency, High, Normal, Low
- **Location:** Building name, room number, campus zone

### Optional Fields
- **Photos:** Attachments showing the issue
- **Comments:** Additional notes or context

---

## Exceptions
- **Missing fields:** System displays validation error indicating required fields
- **Invalid format:** System displays error for incorrectly formatted data

---

## Related Use Cases

- [Upload Photos](submit-repair-request-upload-photos.md) - Add photo attachments
- [Validate Request](submit-repair-request-validate-request.md) - Form validation process
- [Track Request](request-tracking.md) - View submitted request status

---

## Database Interactions

**Tables Affected:**
- `Request` - New record created with requester_id, title, description, location_id, category_id, priority_id
- `Status` - Default status set to "Pending"
- `Notification` - Trigger notification to clerk for new request

---

© 2026 TRAQ
