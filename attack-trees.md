# Attack Trees

The following diagrams represent the three priority threat scenarios discussed in the case study. They are conceptual attack paths, not proof that an attack was performed or that every branch is technically feasible.

## 1. Exploit the public website

```mermaid
flowchart TD
    A[Compromise website or data] --> B[Exploit application weakness]
    B --> C[SQL injection]
    B --> D[Remote script execution]
    C --> E[Manipulate database queries]
    E --> F[Access or alter unauthorised data]
    D --> G[Upload or execute remote script]
    G --> H[Access server files]
    H --> I[Attempt further compromise]
    I --> J[Potential data breach or wider network impact]
```

**Risk treatment:** Remediate the application; use parameterised queries and server-side validation; prevent execution in upload directories; restrict file-system permissions; segment the network; and monitor for suspicious activity.

## 2. Steal proprietary product designs

```mermaid
flowchart TD
    A[Obtain proprietary design files] --> B[Gain access to systems holding designs]
    B --> C[Compromise or misuse an authorised account]
    B --> D[Use an unmanaged or insecure remote device]
    C --> E[Access design repository or server]
    D --> E
    E --> F[Copy or exfiltrate design files]
    F --> G[Potential loss of intellectual property]
```

**Risk treatment:** Limit access to managed corporate devices; apply least privilege and periodic access reviews; encrypt sensitive design files; and monitor access to high-value information.

## 3. Compromise the Manufacturing Control System

```mermaid
flowchart TD
    A[Disrupt or compromise MCS] --> B[Compromise a connected user or support path]
    B --> C[Compromise supervisor workstation or email]
    B --> D[Abuse or compromise vendor remote access]
    C --> E[Reach an MCS-related environment]
    D --> E
    E --> F[Interfere with production systems or availability]
    F --> G[Production disruption and reduced output]
```

**Risk treatment:** Separate email and general-purpose activity from MCS controllers; restrict and log vendor access; use approved secure remote-maintenance sessions; and define supplier security and incident-response requirements.
