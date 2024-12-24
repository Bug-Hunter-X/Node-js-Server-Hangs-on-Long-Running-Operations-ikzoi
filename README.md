# Node.js Server Hangs on Long-Running Operations

This repository demonstrates a common issue in Node.js where long-running operations in request handlers can cause the server to hang and become unresponsive.  The example showcases a server that simulates a 5-second delay, blocking the event loop and preventing it from handling subsequent requests.

The solution provides a method to address this issue using asynchronous operations or worker threads, ensuring the server remains responsive even during lengthy processing tasks.

## Bug
The `server.js` file contains the buggy code.  The `while` loop simulates a long-running operation, blocking the event loop, resulting in a non-responsive server. 

## Solution
The `serverSolution.js` file provides a solution using asynchronous operations, preventing the event loop from being blocked.