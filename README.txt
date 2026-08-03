TD6 Tracking Transport Test v0.01

Purpose
- Isolates the phone-to-Google Tracking request and acknowledgement path.
- Sends exactly 10 synthetic Tracking records.
- Sends one record at a time.
- Waits for and records the complete Google response before sending the next.
- Stops at the first unconfirmed response.

Deliberately excluded
- STC Recorder logic
- GPS collection
- offline queue
- retry timers
- AbortController
- forced request timeout
- Event End
- Submit

Test
1. Upload all five files to a separate GitHub Pages test folder/repository.
2. Open the page on the phone while online.
3. Press “Send 10 Test Records”.
4. Watch each record move through sending and confirmed.
5. Download the test log after completion or failure.
6. Compare the same records in the Tracking Debug sheet.

Expected
- 10 confirmed records.
- Each record should show HTTP 200 and JSON containing ok:true.
- The next record starts only after the prior response is received.
