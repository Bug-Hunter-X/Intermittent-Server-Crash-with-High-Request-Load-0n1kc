# Node.js Server Crash Under Load

This repository demonstrates a bug where a Node.js HTTP server crashes intermittently when handling a high volume of requests.  The crash is non-deterministic and doesn't provide readily identifiable error messages.

## Bug Description

A simple HTTP server is set up. When subjected to a significant number of concurrent requests, the server unexpectedly crashes without clear error indications in the console or logs.

## Reproduction Steps
1. Clone this repository.
2. Run `node server.js`.
3. Use a load testing tool (e.g., k6, Apache Bench) to simulate a large number of concurrent requests to `http://localhost:8080`.
4. Observe the server's behavior. It is likely to crash after some time under sufficient load.

## Solution
The solution involves using techniques to handle high concurrency and prevent resource exhaustion.