# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation blocks the event loop, making the server unresponsive to new requests.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides a solution using asynchronous operations.

## Problem

Node.js is single-threaded, relying on the event loop to handle asynchronous operations efficiently.  When a synchronous operation takes a long time to complete, it blocks the event loop, preventing any other tasks from executing. This can lead to an unresponsive server and a poor user experience.

## Solution

The solution involves replacing the synchronous operation with an asynchronous equivalent, allowing the event loop to continue processing other requests while the long-running task is performed in the background.