Romain VANARDOIS # m1_web_symfony_project
Projet Master 1 Hitema - Symfony

Projet

Je vais développer une solution d'hébergement.
Les utilisateurs peuvent s'inscrire, se connecter et ajouter des services.
Les utilisateurs peuvent se modifier et modifier leurs services.
Des administrateurs peuvent tout consulter et tout modifier.

Mes entités seront :

Des utilisateurs (User) : id, email, firstname, lastname, password, role
Des services (Service)(VPS Portfolio): id, name, price_month, price_year, User, Type, Processor, Storage, RAM
Des types de services (Type)(VPS, Dédié ...) : id, name, price_month, url_image
Un processeur de service (Processor)(I7, Xeon ...) : id, name, product_collection, frequency, heart, thread, price_month
Un stockage de service (Storage)(SSD 500Go, HD 40 Go): id, name, size, type, price_month
Une RAM de service (RAM)(8 Go DDR3,4 Go DDR2 ...): id, name, size, type, price_month

Mes associations d'entités seront :

Un utilisateur pourra avoir plusieurs services.
Un service aura un type de service.
Un processeur aura des services.
Un stockage aura des services.
Une RAM aura des services.
Un service pourra avoir des storages.

Mon administrateur pourra :

CRUD Utilisateurs
CRUD Services
CRUD Type
CRUD Processor
CRUD Storage
CRUD Ram

Un utilisateurs poura :
CRUD Utilisateur (self)
CRUD Services (self services)

La structure de mon site sera la suivante :

/services : moteur de recherche des services
/services/create : créer un bien
/services/{id} : consultation d'un service
/services/{id}/update : modifier un service
/services/{id}/delete : supprimer un service

/{user}/account : compte de l'utilisateur
/{user}/pasword : gestion du mot de passe
/{user}/services : liste les services de l'utilisateur

/admin/users :liste des utilisateurs
/admin/user/create : créer un utilisateur
/admin/user/{id} : modifier un utilisateur
/admin/user/{id}/delete : supprimer un utilisateur

/admin/services : liste des services
/admin/services/create : créer un service
/admin/services/{id} : modifier un service
/admin/services/{id}/delete : supprimer un service

/admin/types/ : liste des types de service
/admin/types/create : créer un type de service
/admin/types/{id} : modifier un type de service
/admin/types/{id}/delete : supprimer un type de service

/admin/processor/ : liste des processeurs de service
/admin/processor/create : créer un processeur de service
/admin/processor/{id} : modifier un processeur de service
/admin/processor/{id}/delete : supprimer un processeur de service

/admin/storage/ : liste des stockages de service
/admin/storage/create : créer un stockage de service
/admin/storage/{id} : modifier un stockage de service
/admin/storage/{id}/delete : supprimer un stockage de service

/admin/ram/ : liste des rams de service
/admin/ram/create : créer une ram de service
/admin/ram/{id} : modifier une ram de service
/admin/ram/{id}/delete : supprimer une ram de service

calcule du prix en fonction des options

