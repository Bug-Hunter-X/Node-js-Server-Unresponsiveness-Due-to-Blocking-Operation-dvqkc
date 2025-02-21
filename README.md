# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js applications: server unresponsiveness due to blocking operations.  A long-running operation within the request handler prevents the event loop from processing other requests, causing the server to hang.

## Problem

The `server.js` file contains a simple HTTP server that simulates a long-running operation (a 5-second delay). During this time, the server becomes unresponsive to new requests.

## Solution

The `serverSolution.js` demonstrates how to address this using asynchronous operations.  By using asynchronous methods (such as `setTimeout` or promises), the event loop remains free to process other requests while the long-running operation completes in the background.