# Node.js HTTP Response Encoding Bug

This repository demonstrates a subtle bug in Node.js HTTP responses where the character encoding may be unexpected if the charset is not explicitly specified in the `Content-Type` header.

## Bug Description

When sending an HTTP response using Node.js's `http` module, omitting the charset in the `Content-Type` header can lead to inconsistent encoding.  Browsers might interpret the response using a default encoding, potentially leading to incorrect display or unexpected behavior.

## Bug Reproduction

1. Clone this repository.
2. Run `node bug.js`.
3. Open `http://localhost:3000/` in your browser. Observe the potential encoding issues.

## Solution

Always specify the charset in the `Content-Type` header to ensure consistent encoding across different browsers and systems.  The solution file (`bugSolution.js`) demonstrates the corrected code.