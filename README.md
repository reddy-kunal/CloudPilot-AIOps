CloudPilot — AI Ops Agent for Cloud Cost & Performance Optimization

CloudPilot is an AI-powered FinOps and DevOps automation agent that analyzes cloud billing, metrics, and resource inventories to generate safe, explainable, and reversible optimization actions. It converts natural-language optimization goals into structured, auditable plans and enforces strict safety guardrails before executing any cloud changes. The system operates through a controlled Plan → Validate → Dry-Run → Execute → Audit → Rollback lifecycle.

Overview

CloudPilot unifies fragmented billing and performance data, identifies optimization opportunities, and ensures safe execution with full traceability. 

Problem Statement

Modern cloud environments suffer from fragmented visibility, high-risk manual optimizations, and hidden financial waste. Engineers must manually correlate billing, metrics, and inventory data across multiple dashboards, leading to inefficiency and overspending. CloudPilot addresses these challenges with an automated, auditable, and safe AI-based optimization engine.

#Use Cases

Automated cost optimization (idle detection, rightsizing, shutdown scheduling)

Safety-governed execution with no-prod rules, rollback guarantees, and downtime protection

Dry-run simulation of all recommended actions

Full audit and rollback history

Adaptive optimization behavior through user feedback

Solution Overview

CloudPilot integrates:

Natural-language goal interpretation

Unified billing/metrics/inventory ingestion via MCP tools

AI planning engine generating structured action plans

Policy validation through guardrails.yaml

Dry-run → execute workflow

Full audit logging and rollback support

Feedback loop for tuning optimization aggressiveness

High-Level Architecture

Core Data Contracts

PlanRequest – user goals, scope, constraints
ActionPlan – AI recommendations, savings, risk levels
Action – individual resource actions with rollback
DryRunReport – projected effects
ExecutionReport – actual applied changes
AuditRecord – full history for traceability

Technology Stack

Python 3.11
FastAPI
LangGraph
Pydantic / JSON Schema
Docker Compose
SQLite / Postgres
Pandas
OpenAI / Azure GPT

Project Phases

Phase 1: Architecture, schemas, data contracts, guardrails
Phase 2: Orchestrator, tools, API, dry-run/execute workflow
Phase 3: Evaluation scenarios, logs, CI/CD, demo polish
