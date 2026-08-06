# DBETA Bones

A governed, logic-first platform for building structured, scalable and machine-legible digital systems.

![Platform](https://img.shields.io/badge/Platform-Bones%209-purple)
![Architecture](https://img.shields.io/badge/Architecture-Modular%20Monolith-blue)
![Framework](https://img.shields.io/badge/Framework-Laravel-red)
![Status](https://img.shields.io/badge/Status-In%20Development-orange)

## Overview

DBETA Bones is a Laravel-based platform for creating governed digital systems around structured business data.

Its central capability is a user-definable data model. Administrators can create their own entity types—such as Projects, Cases, Services, Assets or People—then add fields, relationships and validation rules without requiring a developer to create a new database-backed feature for every business object.

The same governed records can then power:

- administration interfaces
- publishing workflows
- public websites
- APIs and integrations
- structured JSON-LD
- audit and compliance evidence
- data export

Bones is designed to keep these outputs connected to one controlled source of truth.

## Who Bones Is For

Bones is intended for organisations whose websites and digital services depend on structured, interconnected business information.

Typical users include:

- **Content and operations teams** managing records through the Admin interface
- **Digital teams** defining business entities, fields, relationships and publishing workflows
- **Developers and implementation partners** building modules, integrations and presentation layers
- **Governance and compliance teams** reviewing permissions, changes, publishing decisions and audit evidence
- **Organisations preparing for AI-driven discovery** that need reliable, traceable machine-readable information

Bones is particularly suited to organisations managing interconnected information such as services, projects, cases, people, locations, assets or publications across one or more digital channels.

It is not primarily a page builder or a conventional website CMS. It is a governed data and publishing platform for organisations that need their business information to remain structured, reusable and verifiable.

## Problems Bones Solves

Many digital platforms begin as collections of pages and gradually accumulate separate content types, databases, integrations and structured-data scripts.

This creates recurring problems:

- **Rigid data models** — every new business object or relationship requires custom development
- **Duplicated information** — the same facts are maintained separately across pages, systems and integrations
- **Disconnected outputs** — websites, APIs and structured data can present conflicting information
- **Uncontrolled publishing** — stored changes may become public without clear review, approval or revision boundaries
- **Weak traceability** — organisations cannot reliably determine who changed, approved or published information
- **Semantic drift** — machine-readable output becomes outdated or diverges from the underlying records
- **Presentation lock-in** — important business information becomes trapped inside templates or page-builder structures
- **Unsafe extension** — plugins and integrations can bypass permissions, validation or data ownership rules
- **Poor portability** — organisations struggle to export complete records and relationships in a usable form
- **Scaling through duplication** — new sites, services and channels create additional disconnected systems

Bones addresses these problems by placing governed entity definitions and records at the centre of the platform.

Web pages, administration interfaces, APIs, exports and AIDI outputs are produced from the same controlled source. Publishing, authorisation, provenance, validation and audit rules remain attached to the underlying information rather than being recreated separately for every output.

## The Product Model

```text
┌──────────────────────────────────────┐
│              Admin UX                │
│ Define entities, fields and rules    │
└──────────────────┬───────────────────┘
                   │
┌──────────────────▼───────────────────┐
│       User-Defined Data Model        │
│ Types, fields and relationships      │
└──────────────────┬───────────────────┘
                   │
┌──────────────────▼───────────────────┐
│          Governed Records            │
│ Validation, revisions and history    │
└──────────────────┬───────────────────┘
                   │
┌──────────────────▼───────────────────┐
│       Publishing and Workflow        │
│ Draft, review, approval and release  │
└──────────────────┬───────────────────┘
                   │
       ┌───────────┼───────────┬─────────────┐
       │           │           │             │
       ▼           ▼           ▼             ▼
 Public UI     AIDI/JSON-LD   APIs and     Audit and
 and themes    and provenance export       compliance
```

## Core Capabilities

### User-Defined Entity Types

Administrators can define the kinds of information their organisation manages.

Each entity type can have:

- custom fields
- validation rules
- relationships to other entity types
- lifecycle rules
- publishing behaviour
- presentation settings
- machine-legibility mappings

This allows Bones to support different organisations and sectors without reducing everything to predefined pages or content types.

### Governed Records

Bones manages records created from those definitions.

The platform architecture covers:

- generated administration forms
- validation
- revision history
- concurrent editing protection
- authorisation
- destructive-change safeguards
- stable identifiers
- complete audit trails

### Publishing and Presentation

Creating a record does not automatically make it public.

Bones separates stored data from approved public output through governed publishing workflows. Published records can be delivered through site-specific URLs, templates and themes while remaining connected to their source records.

### AIDI and Machine Legibility

AIDI—AI Discovery Infrastructure—is a core Bones subsystem.

It converts eligible published records and relationships into governed machine-readable output, initially including JSON-LD.

AIDI is designed to provide:

- stable public entity identifiers
- traceable provenance
- controlled semantic mappings
- output validation
- synchronisation with publishing state
- drift detection and reconciliation
- automatic withdrawal of outdated output

AIDI does not invent business facts. It derives machine-readable claims from governed source records.

### Audit and Compliance

Bones is designed so important actions and outputs can be inspected and verified.

This includes:

- actor and action history
- authorisation evidence
- publishing history
- output provenance
- automated policy checks
- release and compatibility controls

### Modules and Extensions

Bones follows a modular-monolith architecture.

Modules can extend the platform through governed contracts while keeping core data ownership, permissions, publishing and machine-readable truth inside defined platform boundaries.

### Data Ownership and Portability

The architecture includes governed export so organisations can retrieve their records, relationships and related platform data without depending on undocumented internal structures.

## Example Journey

A complete Bones workflow is intended to let an administrator:

1. Create an entity type called `Project`.
2. Add fields such as title, completion date and status.
3. Relate each Project to a Client and Sector.
4. Create and edit Project records through generated forms.
5. Submit a record for review.
6. Publish the approved revision.
7. Render it through a custom website design.
8. Generate synchronised JSON-LD automatically.
9. Trace every published and machine-readable claim back to its source.
10. Unpublish the record and automatically withdraw its public outputs.

The goal is to deliver this without building a separate custom feature for every new business object.

## Architecture

Bones 9 is being developed as a governed Laravel modular monolith.

Its architecture follows twelve connected areas:

1. Platform Foundation
2. Kernel and Contracts
3. Data Model
4. Record Engine
5. Publishing and Workflow
6. Modules and Extensions
7. Admin Product UX
8. Presentation and Delivery
9. AIDI and Machine Legibility
10. Infrastructure and Reliability
11. Governance, Security and Quality
12. Distribution and Operations

Security, accessibility, testing, observability and compatibility apply across the entire platform.

## Example Machine-Readable Output

The exact output is generated from governed records and versioned semantic mappings. A simplified example is:

```json
{
  "@context": "https://schema.org",
  "@type": "Service",
  "@id": "https://www.dbeta.co.uk/id/service/machine-legibility",
  "name": "Machine Legibility",
  "url": "https://www.dbeta.co.uk/machine-legibility-aidi-layer.html"
}
```

This output is a derived representation of the published record—not a separate hand-maintained source of truth.

## Current Status

Bones 9 is under active development.

The architecture and acceptance criteria describe the intended product. Individual capabilities are being implemented and verified through controlled development slices. Documentation should therefore distinguish between:

- specified architecture
- approved implementation work
- completed and tested functionality
- future roadmap capabilities

The repository should not be interpreted as evidence that every capability described above is already available in a production release.

## Principles

Bones is guided by several core principles:

- business data comes before pages
- users can define their own business objects
- one governed source can serve multiple outputs
- publishing is explicit and revision-aware
- machine-readable claims must be traceable
- presentation does not own business truth
- modules cannot bypass platform governance
- important behaviour must be testable and auditable
- organisations must retain control of their data

## DBETA

DBETA designs and develops structured digital platforms for organisations that need long-term control, scalability and machine legibility.

- [DBETA website](https://www.dbeta.co.uk/)
- [Digital architecture approach](https://www.dbeta.co.uk/structural-strategy.html)
- [Digital platform engineering](https://www.dbeta.co.uk/digital-platform-engineering.html)
- [Machine Legibility and AIDI](https://www.dbeta.co.uk/machine-legibility-aidi-layer.html)
- [DBETA Bones repository](https://github.com/donatastranauskis/dbeta-bones)

## Licence and Availability

Bones is proprietary DBETA technology.

Public repositories, examples or technical materials do not grant rights to use, reproduce or distribute the complete Bones platform unless an accompanying licence explicitly provides those rights.

For commercial enquiries, visit [dbeta.co.uk](https://www.dbeta.co.uk/).
