
# 🔐 Cours de Cybersécurité : Injections SQL

## 1. Introduction

L'injection SQL est une attaque qui permet d'injecter du code malicieux dans une requête SQL via des champs de formulaire ou des URL mal sécurisées.

## 2. Objectifs pédagogiques

- Comprendre comment fonctionnent les injections SQL
- Identifier les failles potentielles dans une application web
- Pratiquer l'exploitation sur une plateforme sécurisée

## 3. Exemple de champ vulnérable

```sql
SELECT * FROM utilisateurs WHERE nom = '$nom';
```

Avec l'entrée : `' OR '1'='1`  
=> toute la table est retournée

## 4. Plateforme recommandée : DVWA

### Installation locale (XAMPP / LAMP) :

1. Télécharger DVWA : https://github.com/digininja/DVWA
2. Copier dans le dossier `htdocs` (XAMPP) ou `/var/www/html` (LAMP)
3. Accéder via `http://localhost/DVWA`
4. Configurer la base et tester les injections dans l'onglet **SQL Injection**

## 5. Exercices proposés

- Testez `' OR '1'='1 --`
- Essayez de deviner le nombre de colonnes via `ORDER BY`
- Utilisez `UNION SELECT` pour voler des informations

## 6. Prévention

- Utiliser des requêtes préparées (ex : PDO en PHP)
- Ne jamais concaténer directement les entrées utilisateur
- Filtrer et valider tous les inputs

## 7. Ressources complémentaires

- [OWASP - SQL Injection](https://owasp.org/www-community/attacks/SQL_Injection)
- [PortSwigger Web Security Academy](https://portswigger.net/web-security/sql-injection)

---

**Fin du support**
