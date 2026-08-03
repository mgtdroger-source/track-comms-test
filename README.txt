TD6 Tracking Transport Test v0.04

Purpose
- Fenced diagnostic app only.
- Proves GET submission plus a read-only Report Key confirmation fallback.

Required Google update
- Rally Tracking Code.gs v0.16 must be deployed first.

Behaviour
1. Sends 10 full Tracking records, one at a time.
2. A clean trackingSubmit acknowledgement confirms the record.
3. If the submit acknowledgement fails, the report is NOT resent.
4. The app calls trackingConfirm using the exact Report Key.
5. Up to 3 small confirmation checks are made, 1.5 seconds apart.
6. Only after confirmation does the next record send.
7. Stops if storage cannot be confirmed.

No GPS, timeout, abort, background queue or STC Recorder code.
