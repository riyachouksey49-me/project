# project
# API-Sentry: REST API Health & Latency Auditor

## Problem Statement

Modern web and mobile applications depend heavily on REST APIs for communication between different software systems. The availability, reliability, and response time of these APIs directly affect the performance and user experience of an application.

Developers often need to manually test API endpoints to determine whether they are available, responding correctly, or taking too long to respond. Manual checking becomes time-consuming when multiple APIs need to be monitored repeatedly. It can also make it difficult to consistently identify connection failures, timeout errors, HTTP status-code errors, and slow response times.

To address this problem, **API-Sentry** is proposed as a lightweight REST API Health & Latency Auditor. The system will accept an API endpoint, send an HTTP request, measure its response time, analyze the HTTP status code, and detect common network or connection failures.

Based on these results, API-Sentry will classify the API endpoint into one of three health states:

* HEALTHY – The API is reachable and responding normally.
* DEGRADED – The API is reachable but its response time or status indicates a potential performance problem.
* DOWN – The API cannot be reached, times out, or encounters a major failure.

The system will then generate an easy-to-understand health report containing the API URL, HTTP status code, response latency, availability status, and overall health classification.

## Objectives

1. Check the availability of REST API endpoints.
2. Measure API response latency.
3. Analyze HTTP status codes.
4. Handle network and timeout errors.
5. Classify API health as HEALTHY, DEGRADED, or DOWN.
6. Generate a clear API health report.
7. Provide a simple and reusable tool for basic API monitoring.

## Scope

The initial version of API-Sentry will focus on manually provided REST API endpoints and basic health and latency analysis. The project will use Python and the `requests` library for sending HTTP requests.

Future versions could include multiple API monitoring, scheduled checks, historical performance data, graphical dashboards, and automated alerts.
