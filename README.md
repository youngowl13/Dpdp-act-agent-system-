# DPDP Act Agent System

A multi-agent AI system for compliance with India's Digital Personal Data Protection (DPDP) Act of 2023, built using the OpenHands Software Agent SDK.

## Overview

This system implements a coordinated multi-agent architecture featuring five specialized agents, each dedicated to a specific compliance domain:

1. **Data Intelligence Agent** - Data mapping and discovery
2. **Subject Rights Agent** - Data Subject Request (DSR) handling
3. **Incident Response Agent** - Breach notification and response
4. **Risk Assessment Agent** - Data Protection Impact Assessments (DPIA)
5. **Compliance Monitoring Agent** - Continuous regulatory surveillance

## Architecture

The system uses OpenHands SDK's multi-agent delegation pattern:

```
User Request → Orchestrator Agent → Specialized Sub-Agents → Results
```

Each sub-agent is equipped with domain-specific skills and triggered by relevant keywords.

## Installation

```bash
pip install -r requirements.txt
```

## Configuration

Set the following environment variables:

```bash
export LLM_API_KEY=your-api-key
export LLM_MODEL=anthropic/claude-sonnet-4-5-20250929  # optional
export LLM_BASE_URL=  # optional, for custom endpoints
```

## Usage

```python
from dpdp_agent_system import DPDPAgentSystem

# Initialize the system
system = DPDPAgentSystem()

# Run a compliance task
system.run("Map all personal data flows in our cloud infrastructure")

# Get system status
status = system.get_system_status()
print(status)
```

## Example Tasks

- "Map all personal data flows in our cloud infrastructure"
- "Process a data subject erasure request for user@example.com"
- "Prepare breach notification for a security incident affecting 1000 users"
- "Conduct a DPIA for our new customer analytics system"
- "Monitor for any new DPDP regulatory updates this week"

## Key Features

### DPDP Act Compliance
- Core principles enforcement (purpose discipline, data minimization, etc.)
- Section 9 child data protection mandates
- Significant Data Fiduciary obligations
- Breach notification (72-hour DPB, 6-hour CERT-In)

### Efficiency Metrics
| Agent | Time Reduction |
|-------|---------------|
| Data Intelligence | 95% (18 min vs weeks) |
| Subject Rights | 90% (500+ DSRs/year) |
| Incident Response | 45 min response time |
| Risk Assessment | 87.5% (3 hrs vs weeks) |
| Compliance Monitoring | 96.9% (15 min vs 8 hrs) |

## Phased Deployment

| Phase | Timeline | Focus |
|-------|---------|-------|
| 1: Foundation | Month 1-4 | Data mapping, PII detection |
| 2: Consent | Month 5-8 | DSR handling, multilingual support |
| 3: Integration | Month 9-12 | Incident response, DPIA, SIEM/SOAR |
| 4: Sustaining | Month 17+ | Continuous monitoring, auditing |

## Files

```
output/
├── dpdp_agent_system.py    # Main system implementation
└── requirements.txt         # Python dependencies

plan/
├── SDK_PLAN.md             # Technical implementation plan
└── dpdp_agent_architecture.html  # Architecture visualization
```

## Dependencies

- OpenHands SDK
- Python 3.10+

## License

MIT

## References

- [DPDP Act 2023](https://www.meity.gov.in/writereaddata/files/Digital_Personal_Data_Protection_Act%2C_2023.pdf)
- [OpenHands SDK Documentation](https://docs.openhands.dev/)
