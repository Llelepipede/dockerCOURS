Oh oh problémo 😕: tu as une application node qui utilise un contenaire de base de données PostgreSQL vue précédemment, comment tu vas les faire communiquer ? 

Sachant qu'un contenaire est isolé... 🤔 Débrouille-toi !

 L'application devrait renvoyer les noms dans la table "personnes".

 docker build -t exo5db .
 docker run --name essaieDB --network exo6 -e POSTGRES_PASSWORD=password exo5db
 docker build -t exo6 .  
 docker run --name exo6node --network exo6 exo6