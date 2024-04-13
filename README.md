



body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f8f9fa;
    margin: 0;
    padding: 0;
}

.navbar {
    background-color: #343a40 !important;
}

.navbar-brand {
    font-weight: bold;
    font-size: 1.5rem;
}

.navbar-brand:hover {
    color: #ffffff;
}

.nav-link {
    color: #ffffff !important;
    font-weight: bold;
}

.nav-link:hover {
    color: #ffffff !important;
}

.jumbotron {
    background: linear-gradient(45deg, #4CAF50, #2196F3);
    color: #ffffff;
    padding: 100px 20px;
    margin-bottom: 50px;
    border-radius: 0;
    text-align: center;
}

.jumbotron h1 {
    font-size: 3.5rem;
    font-weight: bold;
    margin-bottom: 20px;
}

.jumbotron p {
    font-size: 1.5rem;
    margin-bottom: 30px;
}

.section-title {
    color: #007bff;
    margin-bottom: 30px;
}

.form-container {
    background-color: #ffffff;
    border-radius: 10px;
    box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.1);
    padding: 30px;
}

.form-group label {
    font-weight: bold;
}

.btn-primary {
    background-color: #007bff;
    border-color: #007bff;
}

.btn-primary:hover {
    background-color: #0056b3;
    border-color: #0056b3;
}

.table {
    background-color: #ffffff;
    border-radius: 10px;
    box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.1);
}

.table th, .table td {
    border-top: none;
    border-bottom: 1px solid #dee2e6;
}

.table th {
    background-color: #f8f9fa;
    border-color: #dee2e6;
    color: #495057;
    font-weight: bold;
}

.table td {
    color: #495057;
}

.btn-lg {
    padding: 15px 30px;
    font-size: 1.5rem;
}

.container {
    max-width: 1200px;
    margin: auto;
    padding: 0 20px;
}

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ENTREGABLE 1</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
    <link rel="stylesheet" href="estilos.css">
<style>body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-image: url(imagenes/1301602.png);
    background-size: cover;
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-position: center;
    margin: 0;
    padding: 0;
}
</style>

</head>
<body>
    

    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <a class="navbar-brand" href="#">SITIO WEB QUE GESTIONA USUARIOS REGISTRADOS</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ml-auto">
                <li class="nav-item">
                    <a class="nav-link" href="#home">Home</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#login">Login</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#registro">Registro</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#usuarios">Listado de Usuarios</a>
                </li>
            </ul>
        </div>
    </nav>

    <div class="container mt-5">

       
        <section id="home">
            <h2 class="text-center mb-4">¡Bienvenido a la Gestión de Usuarios!</h2>
            <p class="lead text-center">Este es el sitio web para administrar usuarios registrados.</p>
        </section>

        
        <section id="login" style="display: none;">
            <h2 class="text-center mb-4">Iniciar Sesión</h2>
            <div class="row justify-content-center">
                <div class="col-md-6">
                    <form>
                        <div class="form-group">
                            <label for="loginEmail">Correo Electrónico</label>
                            <input type="email" class="form-control" id="loginEmail" placeholder="Ingrese su correo electrónico">
                        </div>
                        <div class="form-group">
                            <label for="loginPassword">Contraseña</label>
                            <input type="password" class="form-control" id="loginPassword" placeholder="Ingrese su contraseña">
                        </div>
                        <button type="submit" class="btn btn-primary btn-block">Iniciar Sesión</button>
                    </form>
                </div>
            </div>
        </section>

        
        <section id="registro" style="display: none;">
            <h2 class="text-center mb-4">Registro de Usuario</h2>
            <div class="row justify-content-center">
                <div class="col-md-6">
                    <form id="registroForm">
                        <div class="form-group">
                            <label for="registroNombre">Nombre</label>
                            <input type="text" class="form-control" id="registroNombre" placeholder="Ingrese su nombre">
                        </div>
                        <div class="form-group">
                            <label for="registroEmail">Correo Electrónico</label>
                            <input type="email" class="form-control" id="registroEmail" placeholder="Ingrese su correo electrónico">
                        </div>
                        <button type="submit" class="btn btn-primary btn-block">Registrarse</button>
                    </form>
                </div>
            </div>
        </section>

    
        <section id="usuarios" style="display: none;">
            <h2 class="text-center section-title">Listado de Usuarios</h2>
            <div class="table-responsive">
                <table class="table">
                    <thead>
                        <tr>
                            <th scope="col">Nombre</th>
                            <th scope="col">Correo Electrónico</th>
                        </tr>
                    </thead>
                    <tbody id="tablaUsuarios">
                     
                    </tbody>
                </table>
            </div>
        </section>

    </div>

   
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.5.3/dist/umd/popper.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>

    
    <script>
        $(document).ready(function(){
            $(".nav-link").click(function(){
                var target = $(this).attr("href");
                $(target).show().siblings("section").hide();
            });

            $("#registroForm").submit(function(event){
                event.preventDefault(); 
                var nombre = $("#registroNombre").val();
                var email = $("#registroEmail").val();

             
                var fila = "<tr><td>" + nombre + "</td><td>" + email + "</td></tr>";
                $("#tablaUsuarios").append(fila);
            });
        });
    </script>

</body>
</html>


