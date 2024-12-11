# Express.js 500 Error: Sending Objects Directly in Response

This repository demonstrates a common error in Express.js applications where sending an object directly in the response without stringifying it can lead to a 500 Internal Server Error. The issue stems from the mismatch between the expected response type (usually JSON) and the actual response type (an object).

## Bug Description
The `bug.js` file contains an Express.js route handler that fetches user data and sends it as a response. However, it fails to stringify the `userData` object, resulting in a server error when trying to send the raw object.

## Bug Solution
The `bugSolution.js` file provides the corrected version.  The `res.send()` method is modified to include `JSON.stringify(userData)` to ensure that the response is a valid JSON string.