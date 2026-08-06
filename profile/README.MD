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

## How Bones Differs

Bones is not primarily a page builder or a conventional content-management system.

| Approach | Primary focus |
|---|---|
| Traditional CMS | Pages and predefined content types |
| Page builder | Visual page composition |
| Headless CMS | Structured content delivered through APIs |
| Business application | A fixed operational data model and workflow |
| **Bones** | User-defined business entities with governance, publishing, presentation and machine-readable outputs |

Bones brings the data flexibility of a configurable business system together with the publishing and presentation capabilities expected from a modern digital platform.

The defining difference is that an organisation's entities, relationships and records remain the source of truth. Pages, APIs, integrations and machine-readable outputs are different governed uses of that information—not separate copies of it.

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

## Deployment Model

Bones is designed around isolated client installations rather than one shared public database containing every customer's information.

Each installation can support one or more explicitly separated workspaces and sites. Records, permissions, publishing state and operational activity remain governed within those boundaries.

This model is intended to provide:

- clear organisational data ownership
- strong separation between client environments
- controlled releases and upgrades
- installation-specific configuration and integrations
- local operation of core platform capabilities
- governed activation of licensed modules and services

Deployment options and managed-service arrangements will be introduced progressively as the platform moves towards wider availability.

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

## The Bones Ecosystem Roadmap

Bones is being developed as more than a single software product. The core platform is intended to support an expanding ecosystem of modules, industry solutions, AI assistants and connected tools.

### Bones Platform

The foundation of the ecosystem: user-defined entities, governed records, relationships, publishing, presentation, permissions, audit and machine-readable output.

### Industry Solutions

Bones can be configured and extended for different operational models without creating a separate platform for every sector.

Potential solution modules include:

- **Car rental and vehicle hire** — vehicles, fleets, locations, availability, bookings, customers, pricing and maintenance
- **Hotels and accommodation** — properties, rooms, facilities, rate plans, availability, reservations and guests
- **Travel and tourism** — destinations, attractions, itineraries, operators, experiences and availability
- **Professional services** — services, clients, projects, cases, people, expertise and outcomes
- **Property and real estate** — properties, units, agents, availability, enquiries, viewings and supporting documents
- **Construction and facilities** — sites, assets, contractors, inspections, maintenance schedules and compliance records
- **Education and training** — courses, programmes, tutors, locations, sessions, enrolments and learning resources
- **Events and venues** — events, sessions, speakers, venues, tickets, sponsors and schedules
- **Membership organisations** — members, organisations, benefits, subscriptions, committees and activities
- **Associations and professional bodies** — qualifications, standards, registers, continuing development and member services
- **Directories and listings** — organisations, professionals, services, categories, locations and verification status
- **Recruitment and talent** — roles, candidates, organisations, skills, applications and placement workflows
- **Nonprofits and community organisations** — programmes, beneficiaries, partners, volunteers, locations and impact evidence
- **Product and service catalogues** — products, variants, specifications, suppliers, availability and related services
- **Publishing and knowledge** — articles, authors, topics, evidence, publications and related resources
- **Research and innovation** — projects, experiments, organisations, researchers, findings and evidence
- **Public information services** — services, eligibility criteria, locations, guidance, responsible organisations and updates

These are examples of how the platform could be configured, not announcements of currently available products. Each solution would combine entity blueprints, workflows, permissions, Admin experiences and integrations while retaining the governance rules of the core platform.

### AI Assistants and Bots

Bones is intended to support task-specific AI assistants that work with governed organisational information.

Examples could include:

- sales and enquiry assistants
- customer-service assistants
- booking and availability assistants
- internal knowledge assistants
- content and publishing assistants
- compliance and quality-review assistants
- research and discovery assistants
- operational monitoring assistants

Unlike a generic chatbot working from disconnected documents, a Bones assistant could operate through defined entities, relationships, permissions and workflows.

AI assistants would not become an uncontrolled source of business truth. Their access and actions would remain bounded by platform permissions, validation, approval and audit rules.

### Modules and Themes

Modules will extend Bones with additional business capabilities, integrations, field types, workflows and operational tools.

Themes and presentation packages will allow the same governed information to support different brands, websites and digital experiences without moving business logic into templates.

### Partner Ecosystem

Developers, agencies and implementation partners will be able to build solutions through governed extension points, compatibility requirements and qualification tools.

This creates a path from DBETA-built modules to controlled partner development without weakening the security and data-ownership boundaries of the platform.

### Bones Marketplace

A future marketplace could provide controlled discovery and distribution of approved:

- modules
- industry solution packs
- themes
- integrations
- entity blueprints
- workflow packages
- AI assistants
- developer and operational tools

Marketplace distribution would be introduced only with appropriate signing, compatibility, review, update and lifecycle controls.

### Browser and Chrome Extensions

Browser tools could extend Bones beyond the Admin application.

Potential uses include:

- inspecting machine-readable information on a website
- validating AIDI and structured outputs
- identifying missing or inconsistent information
- capturing approved information into Bones
- connecting browser-based research to governed records
- supporting sales, content and operational workflows
- showing provenance and publication status

### AIDI Products

AIDI can support a family of machine-legibility tools built around the same governed data:

- structured-output generation
- validation and quality reporting
- semantic mapping
- provenance inspection
- drift detection
- discovery-readiness monitoring
- browser-based inspection
- AI-consumption interfaces

### Connected Ecosystem

Over time, Bones can become the governed information foundation connecting websites, business applications, integrations, AI assistants and machine-readable discovery.

```text
                         Bones Platform
                               │
          ┌────────────────────┼────────────────────┐
          │                    │                    │
   Industry Solutions      AI Assistants      Modules and Themes
          │                    │                    │
          └────────────────────┼────────────────────┘
                               │
                    Partner and Marketplace
                               │
          ┌────────────────────┼────────────────────┐
          │                    │                    │
    Browser Tools         AIDI Products      External Integrations
```

This roadmap describes the intended direction of the Bones ecosystem. Individual products and capabilities will be introduced progressively and should not be treated as currently available until formally released.

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
