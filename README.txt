TD6 Tracking Transport Test v0.02

Purpose
- Fenced test app for the Google Tracking request/acknowledgement path.
- No STC Recorder code, GPS, timeout, abort, retry timer or queue replay.

Tests
1. GET: current Recorder-style request with JSON in the query string.
2. POST: same report sent in a text/plain request body.

Each test sends 10 records strictly one at a time.
The app waits for a valid Google JSON response before sending the next record.
It stops at the first unconfirmed response and can download a CSV diagnostic log.

Upload all files to the separate GitHub Pages test folder.
Run GET first and download its log, then run POST and download its log.
Both methods write clearly labelled test records to the existing Tracking and Tracking Debug sheets.
