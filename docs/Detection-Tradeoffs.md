# Detection Tradeoffs

## Overview
Detection engineering requires balancing visibility, accuracy, and operational noise. No detection is perfect-every rule represents a tradeoff between catching malicious behavior and minimizing false positives.

This document outlines key tradeoffs considered throughout the detection engineering process in this case study.

---

## Signal vs Noise

One of the primary challenges in detection engineering is balancing signal strength with noise reduction.

- **High sensitivity detections**
  - Increase visibility into potential threats
  - Often generate more false positives
  - Require additional tuning and context enrichment

- **High precision detections**
  - Reduce alert fatigue
  - May miss subtle or evolving attacker behavior
  - Risk creating blind spots in coverage

Effective detection engineering aims to find an optimal balance between the two.

---

## Broad vs Specific Logic

Detection rules can be designed to be either broad or highly specific.

- **Broad detections**
  - Capture a wider range of attacker behavior
  - Useful for early-stage detection
  - Can introduce noise in production environments

- **Specific detections**
  - Target known techniques or patterns precisely
  - Lower false positive rate
  - May fail against adapted or novel attacker behavior

---

## Coverage vs Precision

Improving detection coverage often comes at the cost of precision.

- Expanding coverage improves visibility across the attack surface
- Increasing precision improves confidence in alerts
- SOC environments must prioritize based on operational capacity and risk tolerance

---

## Telemetry Limitations

Detection quality is constrained by available telemetry sources.

Common limitations include:
- Incomplete endpoint logging
- Encrypted network traffic
- Cloud and CDN obfuscation
- Lack of process-level visibility in some environments

These constraints must be considered when designing detection logic.

---

## False Positives as a Design Factor

False positives are an expected outcome in early detection development.

Rather than being treated as failure, they are used to:
- Identify weaknesses in detection logic
- Improve filtering and enrichment
- Refine behavioral assumptions
- Strengthen rule accuracy over time

---

## Operational Considerations

In real SOC environments, detections must consider:
- Analyst workload capacity
- Alert prioritization
- Incident response impact
- Business risk tolerance

Detection engineering extends beyond technical implementation into operational decision-making and organizational priorities within a SOC environment.

---

## Summary

Detection engineering is fundamentally a balancing exercise between competing priorities such as coverage, precision, and operational usability. Effective detections are the result of iterative tuning, informed assumptions, and continuous refinement based on real-world feedback.
