# Vulnerability Findings

## F-01: FTP Service Exposed

### Risk Level

Medium

### Description

The Nmap scan identified that FTP service was publicly accessible on port 21.

### Impact

Publicly accessible FTP services can increase the attack surface of the server and may expose file transfer services to unauthorized access attempts if not properly secured.

### Recommendation

Disable FTP if not required or replace it with secure alternatives such as SFTP or FTPS. Restrict access using firewall rules and strong authentication.

---

## F-02: Additional Web Service Exposed

### Risk Level

Low

### Description

An additional web service was detected on port 8080.

### Impact

Additional exposed services increase the attack surface and should be reviewed to ensure they are intended and properly secured.

### Recommendation

Review the necessity of the service and restrict access where appropriate.

---

## F-03: Strict-Transport-Security Header Not Set

### Risk Level

Low

### Description

OWASP ZAP detected that the Strict-Transport-Security (HSTS) header was not set for the tested response.

### Impact

The absence of HSTS may allow protocol downgrade attacks and reduce transport security protections.

### Recommendation

Configure the web server to enforce the Strict-Transport-Security header.

---

## F-04: Retrieved From Cache

### Risk Level

Informational

### Description

The response was served from cache.

### Impact

If sensitive information is cached, it may become accessible to unauthorized users through shared caching mechanisms.

### Recommendation

Ensure sensitive content is not cached and implement appropriate cache-control headers.
