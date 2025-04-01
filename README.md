# SeminarDesk Public API Specification

This repository contains the OpenAPI 3.0.3 specification for SeminarDesk's Public API. This specification serves as the source of truth for all Public API documentation and client implementations.

## Overview

The SeminarDesk Public API provides access to:
- Events and event dates information
- Booking creation functionality
- User account management
- Price calculations
- File management

This API is designed for integration with:
- Custom booking workflows
- Event listings on external websites
- Mobile applications
- Third-party systems (CRM, etc.)

## Getting Started

### Authentication

The Public API supports:
- Bearer token authentication (for user-specific operations)
- API keys (for server-to-server integration)

### Base URL

```
https://{tenantId}.seminardesk.de/api
```

Replace `{tenantId}` with your unique tenant identifier assigned by SeminarDesk.

### Documentation

The complete documentation is available at:
- https://app.swaggerhub.com/apis/SeminarDesk/public/v1

## Implementation Notes

- Response fields that are not explicitly marked as nullable may be null in some cases
- Date and time values are provided in ISO 8601 format
- Currency values are provided as floating-point numbers with two decimal places

## Key Endpoints

The Public API includes endpoints for:

- `/tenant` - Retrieve general information about the tenant
- `/eventDates` - Get lists of event dates
- `/events/{eventId}` - Get details of a specific event
- `/priceSummary` - Calculate prices for bookings
- `/booking` - Create new bookings
- `/accounts` - Manage user accounts
- `/facilitators` - Access facilitator information

## Support

For questions about the API specification:
- Create an issue in this repository
- Contact support@seminardesk.de
