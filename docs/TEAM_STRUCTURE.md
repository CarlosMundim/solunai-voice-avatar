# TEAM STRUCTURE - SOLUNAI VOICE AVATAR

## Organization: Octopus Model

```
                    ┌─────────────────┐
                    │   PAPAI (PO)    │
                    │ Product Owner   │
                    │ Vision & Goals  │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │   TIGER (PM)    │
                    │ Project Manager │
                    │ Octopus Head    │
                    │ Supervision     │
                    └────────┬────────┘
                             │
        ┌────────────────────┼────────────────────┐
        │                    │                    │
        ▼                    ▼                    ▼
   ┌─────────┐         ┌─────────┐         ┌─────────┐
   │  ARM 1  │         │  ARM 2  │         │  ARM 3  │
   │Research │         │  Dev    │         │  Test   │
   │ Agent   │         │ Agent   │         │ Agent   │
   └─────────┘         └─────────┘         └─────────┘
        │                    │                    │
        ▼                    ▼                    ▼
   ┌─────────┐         ┌─────────┐         ┌─────────┐
   │  ARM 4  │         │  ARM 5  │         │  ARM 6  │
   │  Asset  │         │  Docs   │         │ Deploy  │
   │ Agent   │         │ Agent   │         │ Agent   │
   └─────────┘         └─────────┘         └─────────┘
        │                    │                    │
        ▼                    ▼                    ▼
   ┌─────────┐         ┌─────────┐
   │  ARM 7  │         │  ARM 8  │
   │Japanese │         │  QA     │
   │ Agent   │         │ Agent   │
   └─────────┘         └─────────┘
```

---

## ROLES & RESPONSIBILITIES

### Product Owner (PO) - PAPAI
- Define product vision
- Prioritize features
- Accept/reject deliverables
- Client communication (Japan Steel, Jeanette)
- Budget approval (>¥50,000)

### Project Manager (PM) - TIGER
- Sprint planning
- Agent coordination
- Progress tracking
- Risk management
- Quality oversight
- Technical decisions

---

## OCTOPUS ARMS (Agents)

### ARM 1: Research Agent
**Mission:** Find information, analyze options, compare solutions
**Tasks:**
- Find Live2D tiger models
- Research TTS voice options
- Compare API pricing
- Benchmark performance

**Spawn Command:**
```
Task(subagent_type="Explore", prompt="Research [topic]...")
```

---

### ARM 2: Development Agent
**Mission:** Write code, implement features, fix bugs
**Tasks:**
- Configure Open-LLM-VTuber
- Integrate APIs
- Build custom modules
- Optimize performance

**Spawn Command:**
```
Task(subagent_type="general-purpose", prompt="Implement [feature]...")
```

---

### ARM 3: Test Agent
**Mission:** Test functionality, find bugs, verify quality
**Tasks:**
- Test voice pipelines
- Test avatar responses
- Load testing
- User acceptance testing

---

### ARM 4: Asset Agent
**Mission:** Find/create visual and audio assets
**Tasks:**
- Source Live2D models
- Find voice samples
- Create demo content
- Optimize assets

---

### ARM 5: Documentation Agent
**Mission:** Write docs, update tracking, maintain records
**Tasks:**
- Update PROGRESS.md weekly
- Write setup guides
- API documentation
- User guides

---

### ARM 6: Deployment Agent
**Mission:** Deploy, configure servers, monitor
**Tasks:**
- Docker configuration
- Cloud deployment
- SSL/HTTPS setup
- Monitoring setup

---

### ARM 7: Japanese Agent
**Mission:** Japanese language quality
**Tasks:**
- Test Japanese TTS quality
- Write Japanese prompts
- Verify cultural appropriateness
- Translate documentation

---

### ARM 8: QA Agent
**Mission:** Quality assurance, final verification
**Tasks:**
- End-to-end testing
- Performance benchmarks
- Security review
- Final sign-off

---

## AGENT COMMUNICATION

### Handoff Protocol
1. PM spawns agent with clear mission
2. Agent executes and reports back
3. PM reviews output
4. PM updates tracking
5. PM reports to PO if needed

### Status Codes
- `SPAWNED` - Agent started
- `WORKING` - Agent in progress
- `BLOCKED` - Agent needs help
- `DONE` - Agent completed
- `FAILED` - Agent failed, needs review

---

## SPRINT STRUCTURE

**Sprint Duration:** 1 week (Sunday to Saturday)

### Sunday (Sprint Planning)
- PO prioritizes backlog
- PM assigns tasks to arms
- PM spawns agents

### Monday-Friday (Execution)
- Agents work on tasks
- PM monitors progress
- PM handles blockers

### Saturday (Sprint Review)
- PM collects agent outputs
- PM updates PROGRESS.md
- PM presents to PO

---

## ESCALATION PATH

```
Agent → PM (Tiger) → PO (Papai)
```

**Escalate when:**
- Budget impact >¥50,000
- Timeline risk >3 days
- Technical blocker requiring human decision
- Client communication needed

---

*Octopus Model - One brain, many arms, infinite productivity!*
*Last Updated: December 14, 2025*
