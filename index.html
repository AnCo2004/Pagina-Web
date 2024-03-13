<?php
include "configs/config.php";
include "configs/funciones.php";
	//Verificacion de variable
if(!isset($p)){
	$p = "principal";
}else{
	$p = $p;
}

//Consulta para filtrar los productos por cateegoria
if(isset($cat)){
	$sc = $mysqli->query("SELECT * FROM categorias WHERE id = '$cat'");
	$rc = mysqli_fetch_array($sc);
	?>
	<h1>Categoria Filtrada por: <?=$rc['categoria']?></h1>
	<?php
}

//Agregar los productos al carrito en la sesion iniciada
if(isset($agregar) && isset($cant)){
		if(!isset($_SESSION['id_cliente'])){
		redir("?p=login");
	}


	$idp = clear($agregar);
	$cant = clear($cant);
	$id_cliente = clear($_SESSION['id_cliente']);

	$v = $mysqli->query("SELECT * FROM carro WHERE id_cliente = '$id_cliente' AND id_producto = '$idp'");

	if(mysqli_num_rows($v)>0){

		$q = $mysqli->query("UPDATE carro SET cant = cant + $cant WHERE id_cliente = '$id_cliente' AND id_producto = '$idp'");
	
	}else{

		$q = $mysqli->query("INSERT INTO carro (id_cliente,id_producto,cant) VALUES ($id_cliente,$idp,$cant)");

	}

}

//Eliminar productos agregados al carrito
if(isset($eliminar)){
	$eliminar = clear($eliminar);
	$mysqli->query("DELETE FROM carro WHERE id = '$eliminar'");
}
?>

<!DOCTYPE html>
<html lang="es">
	<head>
		<meta charset="utf-8">
		<meta http-equiv="X-UA-Compatible" content="IE=edge">
		<meta name="viewport" content="width=device-width, initial-scale=1">
			<title>UIB.CHO</title>

		<!-- Google font -->
		<link href="https://fonts.googleapis.com/css?family=Montserrat:400,500,700" rel="stylesheet">

		<!-- Bootstrap -->
		<link type="text/css" rel="stylesheet" href="css/bootstrap.min.css"/>

		<!-- Slick -->
		<link type="text/css" rel="stylesheet" href="css/slick.css"/>
		<link type="text/css" rel="stylesheet" href="css/slick-theme.css"/>

		<!-- nouislider -->
		<link type="text/css" rel="stylesheet" href="css/nouislider.min.css"/>

		<!-- Font Awesome Icon -->
		<link rel="stylesheet" href="css/font-awesome.min.css">

		<!-- Custom stlylesheet -->
		<link type="text/css" rel="stylesheet" href="css/style.css"/>

    <script src="https://code.iconify.design/1/1.0.7/iconify.min.js"></script>
    

	
    </head>
	<body>
		<!-- HEADER -->
		<header>
			<!-- TOP HEADER -->
			<div id="top-header">
				<div class="container">

					<ul class="header-links pull-left">
						<li><a href="#"><i class="fa fa-phone"></i> +021-95-51-84</a></li>
						<li><a href="#"><i class="fa fa-envelope-o"></i> email@email.com</a></li>
						
							<?php
							//Verificar el inico de sesion de los usuarios, mostrar nombre guardado en la base de datos
			if(isset($_SESSION['id_cliente'])){
		?>

						<li><a href="#"><i class="fa fa-users"></i><?=nombre_cliente($_SESSION['id_cliente'])?></a></li>

						<?php
		
			}
		?>
					</ul>

					<?php
					/*se utiliza para mostrar condicionalmente
					diferentes enlaces en el de navegación en función 
					de si un usuario ha iniciado sesión o no*/
		if(!isset($_SESSION['id_cliente'])){
		?>
					<ul class="header-links pull-right">
						<li><a  href="?p=registro"><i class="fa fa-id-card-o"></i>Registrar</a></li>
						<li><a  href="?p=login" ><i class="fa fa-user-circle-o"></i>Inicio Sesion</a></li>
					</ul>
					
			
			<?php
			}else{
			?>
			<ul class="header-links pull-right">
					
						<li><a  href="?p=salir" ><i class="fa fa-user-circle-o"></i>Cerrar Sesion</a></li>
					</ul>
					
			<?php
		}
				?>
				</div>
			</div>
			<!-- /TOP HEADER -->

			<!-- MAIN HEADER -->
			<div id="header">
				<!-- container -->
				<div class="container">
					<!-- row -->
					<div class="row">
						<!-- LOGO -->
						<div class="col-md-3">
							<div class="header-logo">
								<a href="#" class="logo">
									<img  id="imglog" src="img/logo.png" alt="">
								</a>
							</div>
						</div>
						<!-- /LOGO -->

						<!-- SEARCH BAR -->
						<div class="col-md-6">
							<div class="header-search">
								<form>
									<select class="input-select"  id="categoria" name="cat" >
										<?php
										/*Parte del buscar en donde se puede elegir la categria directamente a buscar,
										de la tabla categorias*/
										$cats = $mysqli->query("SELECT * FROM categorias ORDER BY categoria ASC");
										while($rcat = mysqli_fetch_array($cats)){
											?>
											<option value="<?=$rcat['id']?>"><?=$rcat['categoria']?></option>
											<?php
										}
										?>
									</select>

									<input class="input"  name="busq"  placeholder="Coloca el nombre del producto">
									<button  type="submit" name="buscar" class="search-btn" >Buscar</button>
								</form>
							</div>
						</div>
						<!-- /SEARCH BAR -->

						<!-- ACCOUNT -->
						<div class="col-md-3 clearfix">
							<div class="header-ctn">
								<!-- Wishlist -->
								<div>
									<a href="#">
										<i class="fa fa-heart-o"></i>
										<span>Deseos</span>
										<div class="qty">
                                    <?php 
									/*mostrará el recuento de elementos almacenados 
									en la variable de sesión'deseo'. Si la variable de sesión
									 'deseo' no está configurada, mostrará 0. */
                                                    if (isset($_SESSION['deseo'])) {
                                                     echo count($_SESSION['deseo']);
                                                    } else {

                                                      echo 0;
                                                       }

                                                     ?>  
										</div>
									</a>
								</div>
								<!-- /Wishlist -->

								<!-- Cart -->
								<div class="dropdown">
									<a class="dropdown-toggle" data-toggle="dropdown" aria-expanded="true">
										<i class="fa fa-shopping-cart"></i>
										<span>Carrito</span>
										<div class="qty">

										<?php 
										/*Recuento de las notificaciones asociadas con el 
										usuario de los productos agregados al carrito*/
									if(!isset($_SESSION['id_cliente'])){						
										?>  O  

											<?php  }else{
																	
     $not = $mysqli->query("SELECT count(id) as notificacion  from carro where id_cliente = '".$_SESSION['id_cliente']."' "); 
                            $numnot = mysqli_fetch_assoc($not);
							echo $numnot['notificacion'];
									}
										?>
                        
                      </div>
									</a>
									<div class="cart-dropdown">
										<div class="cart-list">

											<?php
	if ( isset($_SESSION['id_cliente'])) {
$id_cliente = clear($_SESSION['id_cliente']);
$q = $mysqli->query("SELECT * FROM carro WHERE id_cliente = '$id_cliente'");
$monto_total = 0;
while($r = mysqli_fetch_array($q)){
	$q2 = $mysqli->query("SELECT * FROM productos WHERE id = '".$r['id_producto']."'");
	$r2 = mysqli_fetch_array($q2);

		$preciototal = 0;
			if($r2['oferta']>0){
				if(strlen($r2['oferta'])==1){
					$desc = "0.0".$r2['oferta'];
				}else{
					$desc = "0.".$r2['oferta'];
				}

				$preciototal = $r2['price'] -($r2['price'] * $desc);
			}else{
				$preciototal = $r2['price'];
			}
	
	$nombre_producto = $r2['name'];

	$cantidad = $r['cant'];

	$precio_unidad = $r2['price'];
	$precio_total = $cantidad * $preciototal;
	$imagen_producto = $r2['imagen'];

	$monto_total = $monto_total + $precio_total;

?>
											<div class="product-widget">
												<div class="product-img">
										<img src="img/productos/<?=$imagen_producto?>" class="imagen_carro"/>
												</div>

											<div class="product-body">
													<h3 class="product-name"><a href="#"><?=$nombre_producto?></a></h3>
													 <h4 class="product-price"><?=$precio_unidad?> <?=$divisa?></h4>
												</div>
										     <a class="delete   btnEliminar swalDefaultError"   href="?p=carrito&eliminar=<?=$r['id']?>"><i class="fa fa-close"></i></a>


										  
											</div>
	<?php
}
?>
										
										</div>
										<div class="cart-summary">
									    <small> Item(s) selecionado</small>
								  <h5>$:  <?=$monto_total?>.00 <?=$divisa?> </h5>
										</div>
										<div class="cart-btns">
										   <a href="?p=miscompras">Ver Compras</a>
									  <a id="caja" href="?p=carrito"> Caja <i class="fa fa-arrow-circle-right"></i></a>
										</div>
									</div>

                                                      <?php   }     else {
                                                         echo '<h5>Sin productos..</h>';


                                                      } ?>
								</div>
								<!-- /Cart -->

								<!-- Menu Toogle -->
								<div class="menu-toggle">
									<a href="#">
										<i class="fa fa-bars"></i>
										<span>Menu</span>
									</a>
								</div>
								<!-- /Menu Toogle -->
							</div>
						</div>
						<!-- /ACCOUNT -->
					</div>
					<!-- row -->
				</div>
				<!-- container -->
			</div>
			<!-- /MAIN HEADER -->
		</header>
		<!-- /HEADER -->

		<!-- NAVIGATION -->
		<nav id="navigation">
			<!-- container -->
			<div class="container">
				<!-- responsive-nav -->
				<div id="responsive-nav">
					<!-- NAV -->
					<ul class="main-nav nav navbar-nav" id="ulnav">
						<li class="active"><a  href="?p=principal">Inicio</a></li>
						<li><a  href="?p=productos">Productos</a></li>
					
										<?php
						if(isset($_SESSION['id_cliente'])){
						?>
						<li><a  href="?p=carrito">Mi Carrito</a></li>
						<li><a  href="?p=miscompras">Mis Compras</a></li>
							<?php
								}
								?>
			
						<li><a  href="?p=ofertas">Ofertas</a></li>
					
					</ul>
					<!-- /NAV -->
					<a type="button" id="ff"  href="?p=agregar_productos"  class="btn btn-outline-success">Vender</a>
				</div>
				<!-- /responsive-nav -->
						</div>
			<!-- /container -->
		</nav>
		<!-- /NAVIGATION -->
	<div class="cuerpo">
		<?php
			if(file_exists("modulos/".$p.".php")){
				include "modulos/".$p.".php";
			}else{
				echo "<i>No se ha encontrado el modulo <b>".$p."</b> <a href='./'>Regresar</a></i>";
			}
		?>
	</div>


		<!-- FOOTER -->
		<footer id="footer">
			<!-- top footer -->
			<div class="section">
				<!-- container -->
				<div class="container">
					<!-- row -->
					<div class="row">
						<div class="col-md-3 col-xs-6">
							<div class="footer">
								<h3 class="footer-title">Sobre nosotros</h3>
								<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut.</p>
								<ul class="footer-links">
									<li><a href="#"><i class="fa fa-map-marker"></i>1734 Stonecoal Road</a></li>
									<li><a href="#"><i class="fa fa-phone"></i>+57 301*******</a></li>
									<li><a href="#"><i class="fa fa-envelope-o"></i>gcordobapalacios12@email.com</a></li>
								</ul>
							</div>
						</div>

						<div class="col-md-3 col-xs-6">
							<div class="footer">
								<h3 class="footer-title">Categorías</h3>
								<ul class="footer-links">
									<li><a href="#">Las mejores ofertas</a></li>
									<li><a href="#">Tecnologia</a></li>
									<li><a href="#">Electrodomesticos</a></li>
									<li><a href="#">Ropa y accesorios</a></li>
									<li><a href="#">Vehiculos</a></li>
								</ul>
							</div>
						</div>

						<div class="clearfix visible-xs"></div>

						<div class="col-md-3 col-xs-6">
							<div class="footer">
								<h3 class="footer-title">Información</h3>
								<ul class="footer-links">
									<li><a href="#">Sobre nosotros</a></li>
									<li><a href="#">Contacta con nosotros</a></li>
									<li><a href="#">Política de privacidad</a></li>
									<li><a href="#">Pedidos y Devoluciones</a></li>
									<li><a href="#">Términos y condiciones</a></li>
								</ul>
							</div>
						</div>

						<div class="col-md-3 col-xs-6">
							<div class="footer">
								<h3 class="footer-title">Servicio</h3>
								<ul class="footer-links">
									<li><a href="#">Mi cuenta</a></li>
									<li><a href="#">Ver carrito</a></li>
									<li><a href="#">Lista de deseos</a></li>
									<li><a href="#">Seguimiento de mi pedido</a></li>
									<li><a href="#">Ayuda</a></li>
								</ul>
							</div>
						</div>
					</div>
					<!-- /row -->
				</div>
				<!-- /container -->
			</div>
			<!-- /top footer -->

			<!-- bottom footer -->
			<div id="bottom-footer" class="section">
				<div class="container">
					<!-- row -->
					<div class="row">
						<div class="col-md-12 text-center">
							<ul class="footer-payments">
								<li><a href="#"><i class="fa fa-cc-visa"></i></a></li>
								<li><a href="#"><i class="fa fa-credit-card"></i></a></li>
								<li><a href="#"><i class="fa fa-cc-paypal"></i></a></li>
								<li><a href="#"><i class="fa fa-cc-mastercard"></i></a></li>
								<li><a href="#"><i class="fa fa-cc-discover"></i></a></li>
								<li><a href="#"><i class="fa fa-cc-amex"></i></a></li>
							</ul>
							<span class="copyright">
								<!-- Link back to Colorlib can't be removed. Template is licensed under CC BY 3.0. -->
								Copyright &copy;<script>document.write(new Date().getFullYear());</script> All rights reserved | This template is made with <i class="fa fa-heart-o" aria-hidden="true"></i> by <a href="https://colorlib.com" target="_blank">Colorlib</a>
							<!-- Link back to Colorlib can't be removed. Template is licensed under CC BY 3.0. -->
							</span>
						</div>
					</div>
						<!-- /row -->
				</div>
				<!-- /container -->
			</div>
			<!-- /bottom footer -->
		</footer>
		<!-- /FOOTER -->

		<!-- jQuery Plugins -->
		<script src="js/jquery.min.js"></script>
		<script src="js/bootstrap.min.js"></script>
		<script src="js/slick.min.js"></script>
		<script src="js/nouislider.min.js"></script>
		<script src="js/jquery.zoom.min.js"></script>
		<script src="js/main.js"></script>

	</body>
</html>

