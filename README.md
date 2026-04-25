# ids-api-contract

Contract repository for the OpenWrt IDS/IPS platform backend API.

## Purpose

This repository contains the OpenAPI contract for the backend services used by the IDS/IPS platform.  
It defines the API structure for:

- alerts
- devices and agent heartbeat
- reports

The contract repository acts as the source of truth for request payloads, response models, and endpoint definitions.

## Structure

```text
ids-api-contract/
├── openapi/
│   └── ids-backend.yaml
├── schemas/
│   ├── Alert.yaml
│   ├── Device.yaml
│   └── Report.yaml
├── examples/
│   ├── alert-example.json
│   └── device-status-example.json
└── README.md