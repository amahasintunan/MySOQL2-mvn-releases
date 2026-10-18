# MySOQL — Salesforce SOQL Query Tool

<img width="1169" height="729" alt="Screenshot 2026-10-17 at 12 46 28 PM" src="https://github.com/user-attachments/assets/0c978656-2c16-4aba-8a70-cae3d5f0e1d2" />

**MySOQL** is a platform-independent Java Swing desktop application that provides a graphical user interface (GUI) for Salesforce Object Query Language (SOQL), similar to Salesforce Workbench. Operating via HTTP APIs, it allows users to save and manage connections across multiple Salesforce orgs while offering both manual and UI-driven query generation.

For authentication setup, refer to the Salesforce guide on creating a Connected App for OAuth.\
https://help.salesforce.com/s/articleView?id=platform.ev_relay_create_connected_app.htm&type=5

## What's in this package

| File | Description |
|------|-------------|
| `mysoql.jar` | Application JAR |
| `mysoql2.sh` | Linux/Mac launcher (restart loop on exit code 11) |
| `mysoql2.bat` | Windows launcher |
| `mysoql.xml` | Application config (fetch limits, LCSD, browser path) |
| `mysoql.ini` | JAVA_HOME config |
| `log4j2.xml` | Logging config |
| `misc/` | Runtime dependency jars (Tika, Log4j, Gson, Guava) |

## Requirements

- JDK 17+
- A Salesforce org with OAuth2 connected app credentials

## Quick start

```bash
# Linux/macOS
./mysoql2.sh

# Windows
.\mysoql2.bat
```

If `java` is not on your PATH, set `JAVA_HOME` in `mysoql.ini`.

## Features

- OAuth2 authentication to Salesforce orgs
- SOQL query editor with multi-statement support
- Paginated query results
- Export to XML, CSV, HTML
- LOB cell inspection (MIME detection, text/image render, translation)
- Language & character set detection (Apache Tika)
- Connection browser with org metadata navigation
