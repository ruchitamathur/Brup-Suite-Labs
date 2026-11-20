# Lab: SQL Injection Vulnerability in WHERE Clause

## Objective

Retrieve hidden records by exploiting SQL Injection.

## Category

SQL Injection

## Severity

High

## OWASP Mapping

A03:2021 - Injection

## CWE Mapping

CWE-89

## Lab Scenario

The application does not sanitize user input before
incorporating it into SQL queries.

## Discovery

Intercepted request using Burp Proxy.

Parameter:

category=Gifts

## Testing Payload

' OR '1'='1

## Exploitation Steps

1. Intercept request in Burp Suite.
2. Send request to Repeater.
3. Modify parameter.
4. Observe returned records.

## Impact

Attacker can:
- Access unauthorized data
- Extract sensitive information
- Modify database contents

## Remediation

- Parameterized Queries
- Stored Procedures
- Input Validation

## Lessons Learned

Importance of server-side validation and query parameterization.