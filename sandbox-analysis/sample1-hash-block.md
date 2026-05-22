# Sample 1 — Blocage par Hash MD5

## Action appliquée
Blocage du fichier malveillant via son hash MD5 dans le gestionnaire de hashes.

## IOC
| Type | Valeur |
|------|--------|
| MD5  | cbda8ae000aa9cbe7c8b982bae006c2a |

## Pourquoi cette approche ?
Le hash est un identifiant unique du fichier.  
Bloquer le hash empêche toute exécution du binaire exact sur le système,  
même si le fichier est renommé.

## Limite
Si l'attaquant recompile ou modifie le binaire (1 bit suffit),  
le hash change et le blocage devient inefficace.  
→ Compléter avec des règles comportementales (Sigma/YARA).

## MITRE ATT&CK
| Tactic | Technique | ID |
|--------|-----------|----|
| Defense | Indicator Blocking | T1553 |
