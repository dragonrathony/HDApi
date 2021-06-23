<?php

require __DIR__.'/HomeDepotApi.php';

$hdapi = new \HomeDepotApi();

// optionally set location
if(!empty($_POST['zipCode']))
	$hdapi->setLocationFromZipCode($_POST['zipCode']);

$price = $hdapi->fetchProductPrice($_POST['itemId']);