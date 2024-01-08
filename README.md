<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
 
        form {
            background-color: #fff;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
            width: 400px; /* Ancho del formulario */
        }
 
        label {
            display: block;
            margin-bottom: 10px;
        }
 
        input,
        select {
            width: 100%;
            padding: 10px;
            margin-bottom: 20px;
            box-sizing: border-box;
        }
 
        input[type="submit"] {
            background-color: #4caf50;
            color: #fff;
            cursor: pointer;
        }
 
        input[type="submit"]:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>
    <form>
        <div>
            <label for="dni">DNI:</label>
            <input type="text" id="dni" name="dni" pattern="[0-9]{8}[A-Z]" title="El DNI debe tener 8 dígitos seguidos de una letra mayúscula" required>
        </div>
 
        <div>
            <label for="nombreCompleto">Nombre Completo:</label>
            <input type="text" id="nombreCompleto" name="nombreCompleto" pattern="^[A-ZÁÉÍÓÚÑa-záéíóúñüÜ\s']{1,50}$" title="Ingrese un nombre válido (máximo 50 caracteres)">
        </div>
 
        <div>
            <label for="telefono">Teléfono:</label>
            <input type="tel" id="telefono" name="telefono" pattern="^\+\d{2} \d{3}-\d{6}$" title="Formato válido: +34 657-444939" required>
        </div>
 
        <div>
            <label for="tarifa">Tarifa:</label>
            <select id="tarifa" name="tarifa" required>
                <option value="" disabled selected hidden>Seleccione una tarifa</option>
                <option value="joven">Tarifa Joven</option>
                <option value="senior">Tarifa Senior</option>
                <option value="planasuperior">Tarifa Plana Superior</option>
            </select>
        </div>
 
        <div>
            <label for="fechaInicio">Fecha de Inicio del Servicio:</label>
            <input type="date" id="fechaInicio" name="fechaInicio" required>
        </div>
 
        <div>
            <label for="Varios correos electronicos">Uno o Varios Correos electronicos</label>
            <input type="email" id="Correos electronicos"name="Correos electronicos" multiple required>
        </div>
 
        <div>
            <label for="Codigo Postal">Codigo Postal</label>
            <input type="text" id="Codigo Postal" name="Codigo Postal" pattern="[0-9]{5}" required>
        </div>
 
        <div>
           <label  for="Opinion">Opinion</label>
            <input type="text" id="Opinion" class="Opinion" rows="7" maxlength="20" >
        </div>
 
        <div>
            <label for="Calificacion">Calificacion</label>
            <input type="number" id="Calificacion" name="Calificacion" min="0" max="10" step="1">
        </div>
 
        <input type="submit" value="Enviar">
        <input type="reset" value="Restablecer">
 
        <div>
        <p>Notificaciones Por SMS</p>
         <p style="text-align: center;"> Si</p><input type="radio" id="Notificaciones por SMS" name="Notificaciones por SMS" >
 
         <p style="text-align: center;"> No</p> <input type="radio" id="Notificaciones por SMS" name="Notificaciones por SMS">
        </div>
 
        <div>
         <label for="Condiciones de Servicio" style="color: lightgreen;"> Condiciones de Servicio</label>
         <p>
            Al utilizar nuestro servicio de venta de líneas telefónicas, aceptas cumplir con un uso aceptable para fines legítimos, evitando actividades ilegales o fraudulentas. Durante el registro y el uso de tu cuenta, te comprometes a proporcionar información para mantener la confidencialidad y asumir la responsabilidad de tu cuenta. Al realizar compras, reconoces tu obligación de pagar los montos indicados, sujetos a posibles cambios de precios. La entrega y activación de la línea seguirán los plazos establecidos, y la cancelación estará sujeta a nuestras políticas. Como usuaria, eres responsable del uso adecuado de la línea y debes respetar nuestras políticas de privacidad y seguridad de datos. Nos reservamos el derecho de modificar, suspender o terminar el servicio según sea necesario.
          </p>
       
          <!-- Casilla de verificación para aceptar las condiciones -->
          <form action="procesar" method="post">
            <input type="checkbox" id="Aceptar" name="Aceptar">
            <label for="Aceptar">Acepto las condiciones descritas anteriormente</label>
        </div>
         
    </form>
</body>
</html>
