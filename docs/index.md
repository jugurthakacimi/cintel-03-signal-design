# Continuous Intelligence

This site provides documentation for this project.
Use the navigation to explore module-specific materials.

## How-To Guide

Many instructions are common to all our projects.

See
[⭐ **Workflow: Apply Example**](https://denisecase.github.io/pro-analytics-02/workflow-b-apply-example-project/)
to get these projects running on your machine.

## Project Documentation Pages (docs/)

- **Home** - this documentation landing page
- **Project Instructions** - instructions specific to this module
- **Your Files** - how to copy the example and create your version
- **Glossary** - project terms and concepts

## Additional Resources

- [Suggested Datasets](https://denisecase.github.io/pro-analytics-02/reference/datasets/cintel/)
-

## Custom Project

### Dataset
Metrics recorded over time, containing raw counts of requests handled,
errors encountered, and total response time in milliseconds.

### Signals
- `error_rate`: ratio of failed requests to total requests.
- `avg_latency_ms`: average response time per request.
- `throughput`: number of requests handled per observation.
- `latency_spike`: boolean flag that marks observations where average latency exceeded 30ms.

### Experiments
Added a latency spike detection signal with a threshold of 30ms. The threshold is stored
as a named constant for easy adjustment.

### Results
Each observation is now labeled with a True/False spike flag, making it straightforward
to filter and isolate high-latency periods without manually scanning numeric columns.

### Interpretation
The pipeline can now distinguish normal operation from degraded performance automatically.
