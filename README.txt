TD6 Tracking Transport Test v0.06

Purpose
- Fenced diagnostic app only.
- Proves the streamlined Code.gs end-to-end transport path.
- Prevents a poor Google acknowledgement from blocking the queue indefinitely.

Required Google update
- Rally Tracking Code.gs v0.17 must be deployed first.

Behaviour
1. Sends 10 full Tracking records, one at a time.
2. Waits up to 10 seconds for the normal trackingSubmit acknowledgement.
3. If the acknowledgement fails or times out, the report is NOT resent.
4. Calls trackingConfirm using the exact Report Key.
5. Makes up to 3 confirmation checks, 1.5 seconds apart.
6. Each confirmation request is limited to 8 seconds.
7. Only after confirmation does the next record send.
8. Stops and retains the unconfirmed test record if storage cannot be proved.

No GPS or STC Recorder code.


v0.06 queue rule: an unconfirmed report is retained for later retry; the batch continues so every queued report is attempted.
