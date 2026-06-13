# ids-api-contract

Contract repository for the OpenWrt IDS/IPS platform backend API.

## Purpose

This repository contains the OpenAPI contract for the backend services used by the IDS/IPS platform.  
It defines the API structure for:

- devices and agent heartbeat
- alerts and incident actions (assign, contain, analyst roster)
- traffic statistics
- packet/forensics metadata
- dashboard console view models (`/api/console/*`)
- report exports (`/api/reports/*`, ClickHouse-backed download service)

Every response uses the standard `ApiResponse` envelope (`success`, `message`,
`data`, `timestamp`); resources and paged collections carry HATEOAS `links`.

The contract repository acts as the source of truth for request payloads, response models, and endpoint definitions.

## Structure

```text
ids-api-contract/
├── openapi/
│   └── ids-backend.yaml
├── schemas/
│   ├── Common.yaml      # ApiResponse envelope, pagination, links, errors
│   ├── Device.yaml
│   ├── Alert.yaml
│   ├── Traffic.yaml
│   ├── Forensics.yaml
│   ├── Console.yaml     # dashboard view models (incidents, dashboard, traffic, forensics)
│   └── Reports.yaml
├── examples/
│   ├── alert-example.json
│   └── device-status-example.json
└── README.md