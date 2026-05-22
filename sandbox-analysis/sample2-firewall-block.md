# Sample 2 — Blocage par règle Firewall

## Action appliquée
Blocage de l'IP du serveur C2 via le Firewall Manager.

## IOC
| Type | Valeur |
|------|--------|
| IP C2 | 154.35.10.113 |

## Pourquoi cette approche ?
Le malware contactait cette IP pour recevoir des instructions C2.  
Bloquer l'IP au niveau firewall coupe la communication entre  
la machine compromise et le serveur de l'attaquant.

## Limite
L'attaquant peut changer d'IP à tout moment (comme observé  
sur les samples suivants). Le blocage par IP seul est fragile  
sur le long terme.  
→ Compléter avec un blocage DNS et des règles comportementales.

## MITRE ATT&CK
| Tactic | Technique | ID |
|--------|-----------|----|
| Command & Control | Application Layer Protocol | T1071 |
