---
tipo: fase
fase: 4
horas-estimadas: 75–85
tags: [so/fase4]
---
# Fase 4 — Windows avanzado y Active Directory

↑ [[Home]] · Anterior: [[F3 Índice]] · Siguiente: [[F5 Índice]]

Construyes la telemetría y el entorno de dominio que un SOC real monitoriza.

## Módulos
- [ ] [[M4.1 PowerShell scripting avanzado]] · 14 h
- [ ] [[M4.2 WMI-CIM y tareas programadas]] · 10 h
- [ ] [[M4.3 Redes Windows - SMB, RDP, WinRM y firewall]] · 12 h
- [ ] [[M4.4 Active Directory - dominio, LDAP y GPO]] · 16 h
- [ ] [[M4.5 Autenticación NTLM y Kerberos]] · 12 h
- [ ] [[M4.6 Event Log, ETW, Sysmon y Sysinternals]] · 16 h

## Proyecto de portafolio
`windows-ad-telemetry-lab`: documentación del lab AD (diagramas, pasos), script PowerShell que recolecte y normalice eventos clave, tabla "evento ↔ significado ↔ técnica MITRE" y guía de despliegue de Sysmon.
Plataformas: TryHackMe (rutas Windows y AD) · HackTheBox Academy (Windows/AD).

## Checklist de dominio de la fase
- [ ] Escribo funciones PowerShell con manejo de errores
- [ ] Consulto con CIM/WQL y tareas programadas
- [ ] Configuro SMB/RDP/WinRM y firewall
- [ ] Levanto un dominio AD y aplico GPO
- [ ] Explico NTLM y el flujo Kerberos
- [ ] Filtro el Event Log, conozco 10+ event IDs y despliego Sysmon
