
📀 **Exemple**
- Trame émise par le maître : `04 03 00 02 0001 25 CA`

|N° Esclave| code fonction| @ du premier mot à lire | Nombre de mots à lire | Mot de contrôle
|--|--|--|--|--|
|4|3 = lecture registre| MSB : 00 et LSB : 02 | MSB : 00 et LSB : 01 | CRC : 25 CA

- Réponse de l'esclave avec erreur : `04 83 02 01 31`

|N° Esclave| code fct| code d'exception | Mot de contrôle
|--|--|--|--|
|4| 83 =3 (lecture registre) + 80=83|  02 (Illegal data access) | CRC : 01 31

- Réponse de l'esclave sans erreur : `04 03 02 02 58 B8 DE`

|N° Esclave| code fonction| Nombre d'octets données | Données du registre | Mot de contrôle
|--|--|--|--|--|
|4|3 = lecture registre| 02 | MSB 02 et LSB : 58 | B8 DE
