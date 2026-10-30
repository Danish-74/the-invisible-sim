# The Invisible SIM
### Telecom API Security Research Lab

A hands-on cybersecurity research project exploring authentication, authorization, and insecure direct object access in a simulated telecom subscriber API.

## Project Overview

The Invisible SIM demonstrates how missing authentication and authorization controls can expose subscriber information through insecure API endpoints.

This project uses a local Flask application and fictional subscriber records to simulate the issue safely.

## Objectives

- Understand API authentication and authorization.
- Demonstrate unauthorized access to subscriber records.
- Test access-control weaknesses using cURL.
- Implement Bearer token authentication.
- Enforce subscriber-level ownership checks.

## Technology Stack

- Python
- Flask
- Kali Linux
- cURL
- REST API
- GitHub

## Security Testing

| Test | Expected HTTP response |
|---|---:|
| Request without authentication | 401 Unauthorized |
| Access another subscriber's record | 403 Forbidden |
| Access own subscriber record | 200 OK |
| Request nonexistent subscriber | 404 Not Found |

## Security Improvements

The initial API implementation allowed unauthenticated access to simulated subscriber records.

The secured implementation introduces:

- Bearer token authentication.
- Subscriber ownership validation.
- Appropriate HTTP status codes.
- Localhost-only execution.

## Project Structure

```text
the-invisible-sim/
├── app.py
├── requirements.txt
├── .gitignore
├── reports/
│   └── security-assessment.md
└── screenshots/
    ├── 01-unauthenticated-access.png
    ├── 02-unauthorized-subscriber-access.png
    ├── 03-authorized-access.png
    └── 04-subscriber-not-found.png
```

## Ethical Considerations

This project is strictly educational.

- All subscriber records are fictional.
- Testing is performed in a local environment.
- No real telecom systems or customer data are involved.

## Limitations

This is a small educational simulation. Its hardcoded tokens are not suitable for production use.

## Author

**Danish Rashid**

Cybersecurity | SOC Operations | API Security Research
