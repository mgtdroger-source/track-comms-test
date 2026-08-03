TD6 Tracking Transport Test v0.03

Purpose
- Fenced diagnostic app only.
- Tests GET acknowledgements without touching the STC Recorder.

Tests
1. Full GET: 10 records using the current full Tracking payload.
2. Lean GET: 10 records using only eventId, senderId, sequence, gpsTime, latitude, longitude, accuracy, speedKph and eventType.

Behaviour
- Sends strictly one record at a time.
- Waits for Google acknowledgement before sending the next.
- Stops on the first unconfirmed response.
- No GPS, timeout, abort, retry loop or Recorder logic.
- Download each run log before starting the other test.
