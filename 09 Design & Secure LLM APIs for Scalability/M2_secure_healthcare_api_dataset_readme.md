# HealthTech Access Logs Dataset

## Overview
This dataset contains anonymized API access logs, authentication events, and prompt injection attempts from HealthTech Inc's AI-powered medical document analysis platform. The data supports security analysis, authentication testing, and threat detection exercises.

## Dataset Schema
- `log_id`: Unique identifier for each log entry (e.g., "log_001")
- `timestamp`: Event timestamp in ISO 8601 format
- `user_id`: Anonymized user identifier
- `endpoint`: API endpoint path
- `method`: HTTP method
- `auth_method`: Authentication method used (oauth2, jwt, api_key, none)
- `scopes`: OAuth2 scopes granted (patient:read, patient:write, admin)
- `api_key_role`: API key role (read-only, clinician, admin)
- `status_code`: HTTP status code
- `response_time_ms`: Response time in milliseconds
- `prompt`: User prompt text (for injection detection)
- `blocked_reason`: Reason for blocking (prompt_injection_detected, etc.)
- `failure_reason`: Authentication failure reason

## Usage Notes
- Load using authentication analysis utilities in the starter notebook
- Use logs to test OAuth2 scope validation and JWT token verification
- Analyze prompt injection attempts to validate defense mechanisms
- Follow HIPAA data handling protocols when processing logs

## Sample Size
The full dataset contains 5,000 log entries. This sample file includes 10 representative examples covering successful authentication, failures, and injection attempts. The complete dataset will be provided in the Coursera lab environment.

## Security Patterns
- Successful OAuth2/JWT authentication with proper scopes
- Failed authentication attempts (missing tokens, insufficient permissions)
- Prompt injection attempts with various attack patterns
- API key usage with role-based access control

## Privacy & Compliance
All patient identifiers have been anonymized. PHI has been redacted. Follow HealthTech's HIPAA-compliant data handling checklist when exporting metrics or sharing results externally.

