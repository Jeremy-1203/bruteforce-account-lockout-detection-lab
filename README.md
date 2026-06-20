# Windows Brute Force Attack and Account Lockout Detection Lab

## Overview

This project demonstrates how Splunk Enterprise can be used to detect brute force login attempts and account lockout events using Windows Security Event Logs.

A Windows 11 virtual machine was deployed in VirtualBox and configured to send Windows Event Logs to Splunk Enterprise. Multiple failed login attempts were generated against the Student account to simulate a brute force attack. The attack resulted in a Windows account lockout, and the related security events were investigated using Splunk.

## Tools Used

* Splunk Enterprise
* Windows 11 Enterprise
* Oracle VirtualBox
* Windows Security Event Logs

## Lab Architecture

Windows 11 Virtual Machine

↓

Windows Security Event Logs

↓

Splunk Enterprise

↓

Security Monitoring and Investigation

## Objectives

* Simulate a brute force attack against a Windows account
* Generate failed login events
* Trigger a Windows account lockout
* Collect and analyze Windows Security Event Logs
* Detect Event ID 4625 (Failed Login)
* Detect Event ID 4740 (Account Lockout)
* Practice SIEM monitoring and incident investigation

## Event IDs Investigated

### Event ID 4625 – Failed Login Attempt

Search Query:

index=main EventCode=4625

Purpose:
Used to identify unsuccessful authentication attempts against a Windows account.

### Event ID 4740 – Account Lockout

Search Query:

index=main EventCode=4740

Purpose:
Used to identify when a Windows account becomes locked due to excessive failed login attempts.

## Investigation Findings

### Failed Login Activity

Multiple incorrect passwords were entered against the Student account.

Splunk successfully collected and displayed Event ID 4625 entries showing failed authentication attempts.

### Account Lockout Activity

After repeated failed login attempts, Windows automatically locked the Student account.

Splunk successfully detected Event ID 4740, confirming that the account lockout policy had been triggered.

## Results

* Generated multiple failed login attempts
* Simulated a brute force attack scenario
* Triggered a Windows account lockout
* Collected Windows Security Event Logs in Splunk
* Detected Event ID 4625 and Event ID 4740
* Performed security event investigation using Splunk

## Screenshots

1. Failed Login Attempt
2. Windows Account Lockout Message
3. Splunk Event ID 4625 Detection Results
4. Splunk Event ID 4740 Detection Results

## Skills Demonstrated

* Security Information and Event Management (SIEM)
* Splunk Enterprise
* Windows Event Log Analysis
* Authentication Monitoring
* Incident Investigation
* Security Event Detection
* Splunk Search Processing Language (SPL)
* Virtualization with VirtualBox

## Outcome

This project demonstrates the ability to simulate a common attack scenario, collect security logs, investigate authentication events, and identify account lockout activity using Splunk Enterprise.

