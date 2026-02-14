# Mobexler - Lab VirtualBox

TP Sécurité Mobile – Mobexler + Android cible

## Objectif du lab

- Faire tourner Mobexler sans erreur
- Avoir Internet via NAT
- Pouvoir communiquer en ADB avec un téléphone Android sur le réseau Host-Only "lab"
- Pouvoir revenir rapidement à l’état propre avec le snapshot CLEAN

## Configuration réseau de la VM

- Adaptateur 1 → **NAT** → Internet (IP 10.0.2.15 / passerelle 10.0.2.2)
- Adaptateur 2 → **Host-Only** réseau "lab" → communication avec l’Android

<img width="570" height="282" alt="{5526EEC8-9618-45D8-836E-7BE02819915F}" src="https://github.com/user-attachments/assets/46091fe0-f610-4046-a79e-f090275d5b60" />
<img width="561" height="300" alt="{06B005CF-FC5A-4766-B7FE-852284773EE6}" src="https://github.com/user-attachments/assets/13550de3-322d-4039-9658-d5cd11a96337" />



## Vérifications de base une fois la VM démarrée

### 1. Internet qui marche

``bash
ping -c 4 8.8.8.8

<img width="1152" height="416" alt="{5CEE5AF9-8037-4F02-9587-4514EFDE4A0F}" src="https://github.com/user-attachments/assets/dbe57785-27f9-4cc4-bba8-ecb3a84c843a" />

###2. Les interfaces réseau
Bash :ip a

<img width="1920" height="923" alt="{12D45C0A-2D88-4618-B312-665B9F3454FC}" src="https://github.com/user-attachments/assets/8dce2d85-ce4a-4a44-842b-298e8983b93d" />

<img width="1863" height="758" alt="{BB412545-F6B6-45D6-B2C8-DBCCBE0975B0}" src="https://github.com/user-attachments/assets/4b62bb4c-eef1-4365-8137-9f51fcec85f4" />



### 3. La table de routage
Bash: ip route
<img width="1439" height="277" alt="{28F2EB4A-EFFD-4D79-BB6C-D313A23A9F15}" src="https://github.com/user-attachments/assets/63c2fd81-eb3e-42ab-8428-c61cb7755181" />


### 4. Connexion ADB
Basha :db connect 192.168.155.101:5555
<img width="914" height="488" alt="{CD174EB3-4110-4183-935F-39D7DAAD612C}" src="https://github.com/user-attachments/assets/43688932-9b85-4443-bd49-585f8bc204e1" />


                                                ######### EXPLICALTION D'INSTALLATION #########

Apres avoir choisis l'option B dans la derniere partie du lab1, j'ai installer Genymotion sur ma machine personnel et non sur la vm, puis apres l'avoir lance j'ai utiliser connexion ADB comme vu sur l'etape 4
<img width="1077" height="825" alt="{59629EBC-1C15-43E4-AABE-52BFC4264DB2}" src="https://github.com/user-attachments/assets/03b41c04-7d98-462c-bff8-04989f769f49" />






### 5. Snapchot clean
<img width="1920" height="974" alt="{CD9F9468-2220-49D5-ACA3-FABB71EB1248}" src="https://github.com/user-attachments/assets/fbea3e85-9084-4ae3-96d1-3719ec4a3575" />

Nomme comme dans le lab 1, CLEAN_BASELINE_TP1




