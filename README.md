# 🖥️ Gestion des Salles et Machines
> Application Java utilisant **Hibernate ORM**, **JPA** et **MySQL**

---

## 🛠️ Stack technique
| Technologie | Rôle |
|---|---|
| Java + Maven | Langage & build |
| Hibernate ORM + JPA | Persistance des données |
| MySQL | Base de données |
| JUnit | Tests |

---

## 📚 Concepts mis en œuvre
- Mapping d'entités JPA (`@Entity`, `@OneToMany`, `@ManyToOne`)
- Interface DAO générique + couche Service
- Opérations CRUD complètes
- Requêtes HQL, NamedQuery et NativeQuery
- Architecture en couches : **DAO → Service → Test**

---

## ⚙️ Configuration
### `pom.xml`
Dépendances : `hibernate-core`, `mysql-connector-java`, `junit`

### `hibernate.cfg.xml`
```xml
<property name="hibernate.connection.url">
    jdbc:mysql://localhost:3307/mabase?useSSL=false&amp;serverTimezone=UTC
</property>
<property name="hibernate.connection.username">root</property>
<property name="hibernate.connection.password">••••</property>
<property name="hibernate.hbm2ddl.auto">update</property>
```

---

## 🗂️ Structure du projet
```
src/
├── entities/
│   ├── Machine.java       # Entité JPA
│   └── Salle.java         # Entité JPA
├── dao/
│   └── IDao.java          # Interface générique CRUD
├── services/
│   ├── MachineService.java
│   └── SalleService.java
├── util/
│   └── HibernateUtil.java # SessionFactory singleton
└── test/
    └── MachineServiceTest.java
```

---



## 📸 Résultats observés dans la console

### 📌 Création des tables dans MySQL
<img width="405" height="749" alt="image" src="https://github.com/user-attachments/assets/8d78bf88-5b5f-40fb-8907-2438157471ca" />


### 📌 MachineServiceTest – 5 tests passés
<img width="1555" height="784" alt="image" src="https://github.com/user-attachments/assets/2bc0d35f-90fe-407a-b005-a99f3f979b6d" />

### 📌 SalleServiceTest – 5 tests passés
<img width="1919" height="1016" alt="image" src="https://github.com/user-attachments/assets/a112cd74-f46b-4bf9-9193-bf4cd892f070" />



### 📌Résultat – Recherche par date & affichage des salles
<img width="1656" height="627" alt="image" src="https://github.com/user-attachments/assets/50e23bcc-e674-479d-9a38-e883ec9c2dfd" />
<img width="684" height="736" alt="image" src="https://github.com/user-attachments/assets/04cebab5-b1de-4f29-bfce-d3aead270825" />


---




