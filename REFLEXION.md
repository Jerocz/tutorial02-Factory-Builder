# Reflexion - Tutorial 02

Jeronimo Carvajal Zuluaga

El OrdenBuilder reduce el riesgo de errores porque centraliza en un solo lugar como se crea una orden. Si la orden se creara directamente en la vista, cada vista tendria que acordarse de calcular el subtotal, aplicar el IVA, validar que haya productos y pasar todos los campos en el orden correcto; si una vista se equivoca o se le olvida un paso, se guarda una orden con datos incorrectos y es dificil encontrar donde fallo. Con el Builder la orden se arma paso a paso con metodos que dicen claramente que hacen (con_usuario, con_productos, para_envio) y el metodo build() valida que la informacion este completa antes de tocar la base de datos, lanzando un error si falta algo. Ademas, si cambia la regla de calculo (por ejemplo el IVA), solo se modifica el Builder y todas las partes que crean ordenes quedan actualizadas automaticamente.
