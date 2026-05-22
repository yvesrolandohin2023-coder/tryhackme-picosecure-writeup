# Sample 3 — Blocage par filtre DNS

## Action appliquée
Blocage du domaine C2 via le DNS Filter.

## IOC
| Type | Valeur |
|------|--------|
| Domaine C2 | emudyn.bresonicz.info |

## Pourquoi cette approche ?
Le malware utilisait ce domaine pour résoudre l'adresse IP du C2.  
Bloquer la résolution DNS empêche la machine de trouver le serveur,  
même si l'IP change.

## Avantage vs blocage IP
Plus résilient : si l'attaquant change d'IP mais garde le même domaine,  
le blocage DNS reste efficace.

## Limite
Si l'attaquant enregistre un nouveau domaine, le blocage devient  
obsolète. Surveiller les domaines DGA (Domain Generation Algorithm).

## MITRE ATT&CK
| Tactic | Technique | ID |
|--------|-----------|----|
| Command & Control | Dynamic Resolution | T1568 |
