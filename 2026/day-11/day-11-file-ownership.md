# Day 11 Challenge

## Files & Directories Created
[list all files/directories]
- touch devops-file.txt
- touch team-notes.txt
- touch project-config.yaml
- mkdir app-logs/
- mkdir -p heist-project/vault
- mkdir -p heist-project/plans
- touch heist-project/vault/gold.txt
- touch heist-project/plans/strategy.conf
-   ls -lR heist-project/
-   heist-project/:
total 8
drwxr-xr-x 2 professor planners 4096 Feb 19 21:57 plans
drwxr-xr-x 2 professor planners 4096 Feb 19 21:57 vault

-   heist-project/plans:
total 0
-rw-r--r-- 1 professor planners 0 Feb 19 21:57 strategy.conf

-   heist-project/vault:
total 0
-   -rw-r--r-- 1 professor planners 0 Feb 19 21:57 gold.txt
- mkdir bank-heist/
- touch bank-heist/access-codes.txt
- touch bank-heist/blueprints.pdf
- touch bank-heist/escape-plan.txt

## Ownership Changes
[before/after for each file]
- devops-file.txt:  harsh harsh  → tokyo:harsh → berlin:harsh
- team-notes.txt:   harsh harsh  →  harsh:heist-team
- project-config.yaml:  harsh harsh  →  professor:heist-team
- access-codes.txt:  harsh harsh    →   tokyo:vault-team
- blueprints.pdf:    harsh harsh    →   berlin:tech-team
- escape-plan.txt:   harsh harsh    →   nairobi:vault-team

## Commands Used
[your commands here]
- touch
- useradd
- groupadd
- chown (-R for recurssive permission)
- mkdir
- mkdir -p
- ls -lR (list recusrsive)

## What I Learned
[3 key points about file ownership]

- I learnt to create multiple file and directories to create at a time.
- I learnt to change ownership of the file.
- I observed the changes in files and directories after modifying ownerships.