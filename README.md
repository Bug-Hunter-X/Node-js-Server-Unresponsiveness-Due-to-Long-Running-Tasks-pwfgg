# Node.js Server Unresponsiveness
This repository demonstrates a common issue in Node.js servers: unresponsiveness due to long-running tasks.  A simple HTTP server simulates a 5-second delay, causing it to become unresponsive during that period.  The solution shows how to prevent this using asynchronous operations and proper request handling.

## Bug
The `server.js` file contains a Node.js HTTP server that introduces a 5-second delay for each request.  This delay blocks the event loop and prevents other requests from being processed.

## Solution
The `serverSolution.js` file demonstrates the solution by using asynchronous operations to handle requests concurrently.  This prevents the event loop from being blocked, ensuring responsiveness even during long-running tasks.