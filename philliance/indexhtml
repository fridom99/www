<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, shrink-to-fit=no">
    <title>Philliance formation</title>
    <meta name="description" content="Ma page">
    <link rel="stylesheet" href="assets/bootstrap/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Lora:400,700,400italic,700italic">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Cabin:700">
    <link rel="stylesheet" href="assets/fonts/font-awesome.min.css">

    <link href="//maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" rel="stylesheet" id="bootstrap-css">
    <script src="//maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js"></script>
    <script src="//cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
    <script src="asset/script.js"></script>
<!------ Include the above in your HEAD tag ---------->

    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.0.8/css/all.css">

    <link rel="stylesheet" href="asset/style.css">

</head>

<body>

    

<?php


			// --------------------------------------------------------------
			// Paramètres de connection à la Base de Données sur le serveur
			// --------------------------------------------------------------
			$pdo_conn = array();
			$pdo_conn['hostname'] = 'localhost'; // voir hébergeur ou "localhost" en local
			$pdo_conn['database'] = 'philliance'; // nom de la BdD
			$pdo_conn['username'] = 'root'; // identifiant "root" en local
			$pdo_conn['password'] = ''; // mot de passe (vide en local)
			// ------------------------
			// connexion à la Base de Données
			try {
			// chaine de connexion (DSN)
			$pdo_conn['strConn'] = 'mysql:host='.$pdo_conn['hostname'].';dbname='.$pdo_conn['database'];
			$pdo_conn['extraParam'] = array(
			PDO::ATTR_ERRMODE => PDO::ERRMODE_EXCEPTION, // rapport d'erreurs sous forme d'exceptions
			PDO::ATTR_PERSISTENT => true, // Connexions persistantes
			PDO::MYSQL_ATTR_INIT_COMMAND => "SET NAMES utf8" // encodage UTF-8
			);
			// Instancie la connexion
			$pdo = new PDO($pdo_conn['strConn'], $pdo_conn['username'], $pdo_conn['password'], $pdo_conn['extraParam']);
			}
			catch(PDOException $e){
			$msg = 'ERREUR PDO dans ' . $e->getFile().' L.' . $e->getLine().' : ' . $e->getMessage();
			die($msg);
			}
?>

<?php 
$query = $pdo->query("SELECT * FROM `etudiant`");

$resultat = $query->fetchAll();

//Afficher le résultat dans un tableau

print("<table border=\"1\">");

foreach ($resultat as $key => $variable)
{
print("<tr>");
print("<td>".$resultat[$key]['nom']."</td>");
print("<td>".$resultat[$key]['prenom']."</td>");
print("<td>".$resultat[$key]['mail']."</td>");
print("<tr>");
}

print("</table>");

?>
<?php
    //On définit deux cookies
    setcookie('user_id', '1234');
    setcookie('user_pref', 'dark_theme', time()+3600*24, '/', '', true, true);
    
    //On modifie la valeur du cookie user_id
    setcookie('user_id', '5678');
    
    //On supprime le cookie user_pref
     //setcookie('user_pref', '', time()-3600, '/', '', false, false);
?>

<?php

            if(isset($_COOKIE['user_id'])){
                echo 'Votre ID de session est le ' .$_COOKIE['user_id']. '<br>';
            }
            if(isset($_COOKIE['user_pref'])){
                echo 'Votre thème préféré est ' .$_COOKIE['user_pref'];
            }else{
                echo 'Pas de thème préféré défini';
            }
        ?>
    <article class="bg-secondary mb-3">  
            <div class="card-body text-center">

            <p><a class="btn btn-warning" target="_blank" href="http://bootstrap-ecommerce.com/">Philliance
            <i class="fa fa-window-restore "></i></a></p>
            </div>
    </article>

    <div class="container">
        
        
        <div class="row">
            
            <aside class="col-sm-4">
        
        <div class="card">
        <article class="card-body connecter">
            <h4 class="card-title text-center mb-4 mt-1">Connectez-vous</h4>
            <hr>
            <!-- <p class="text-success text-center">Some message goes here</p> -->
            <form method="post" action="index.php" >
                <div class="form-group">
                <div class="input-group">
                    <div class="input-group-prepend">
                        <span class="input-group-text"> <i class="fa fa-user"></i> </span>
                    </div>
                    <input name="mail" class="form-control" placeholder="<?php print($resultat[$key]['mail']) ?>" type="email">
                </div> <!-- input-group.// -->
                </div> <!-- form-group// -->
                <div class="form-group">
                <div class="input-group">
                    <div class="input-group-prepend">
                        <span class="input-group-text"> <i class="fa fa-lock"></i> </span>
                    </div>
                    <input name="code "class="form-control" placeholder="******" type="password">
                </div> <!-- input-group.// -->
                </div> <!-- form-group// -->
                <div class="form-group">
                <button type="submit" class="btn btn-primary btn-block"> Se connecter  </button>
                </div> <!-- form-group// -->
                <p class="text-center"><a href="#" class="btn">Mot de passe oublié ?</a></p>
            </form>
        </article>
        </div> <!-- card.// -->
        
            </aside> <!-- col.// -->
        </div> <!-- row.// -->
        
        </div> 
        <!--container end.//-->
        
        
        <br><br><br>




</body>

</html>