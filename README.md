# TryHackMe — PicoSecure Writeup

## Présentation
Lab de cybersécurité blue team sur la plateforme TryHackMe.  
Objectif : analyser des samples malveillants, identifier les comportements suspects,  
bloquer les menaces et créer des règles de détection Sigma.

## Compétences démontrées
- Analyse de malware en sandbox
- Blocage de menaces (hash, firewall, DNS, registry)
- Création de règles Sigma (Sysmon EventID 1, 3, 13)
- Mapping MITRE ATT&CK

## Outils utilisés
- PicoSecure Sandbox
- Sigma Rule Builder
- Firewall Manager
- DNS Filter
- MITRE ATT&CK Framework

## Résumé des samples

| Sample | Action | IOC |
|--------|--------|-----|
| Sample1 | Blocage hash | cbda8ae000aa9cbe7c8b982bae006c2a |
| Sample2 | Blocage firewall | 154.35.10.113 |
| Sample3 | Blocage DNS | emudyn.bresonicz.info |
| Sample4 | Règle Sigma — Registry | DisableRealtimeMonitoring |
| Sample5 | Règle Sigma — Network | beacon.bat / bababa10la.cn |
| Sample6 | Règle Sigma — Process | cmd.exe spawn / exfiltr8.log |
