TD6 Tracking Transport Timing Test v0.10

Purpose
- Fenced diagnostic app only.
- Sends 30 full Tracking reports one at a time.
- Shows phone send time, Google received time, phone acknowledgement time, phone-to-Google time, acknowledgement delay and total duration live.
- Uses the proven bounded submit and trackingConfirm recovery logic.
- Exports the complete timing table to CSV.

Server
- Rally Tracking Code.gs v0.19.

Unchanged
- STC Recorder is not included or modified.

Changed in v0.10
- Test count increased from 20 to 30.
- Internal/export version corrected to 0.10.
- On-screen submit limit wording corrected to 5 seconds.
- Service-worker cache name advanced so GitHub/PWA installs receive the full updated set.
