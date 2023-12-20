# RegistroCarroUser
Registra usuario con varios carros
REGISTRO DE USUARIO Y CARROS

Primer paso:
Al registrar un usuario en 
http://127.0.0.1:8080/res-usuario/1/Joel/Quispe
Este va a tener una id_usuario, nombre y apellido.

Segundo paso:
Registramos un carro
http://127.0.0.1:8080/res-auto/1/ABC-123/KIA/BLANCO/1
Este tiene una id_auto,placa,marca y id_usuario
Al final se pone una id del usuario creado en este caso 1,
para que el carro tenga relacion con el id_usuario.

Tercer paso:
Vamos al H2
http://127.0.0.1:8080/h2-console

URL: jdbc:h2:mem:dcbapp
User Name: sysdba
Password: masterkey

SELECT * FROM AUTO 
SELECT * FROM USUARIOS

Veremos los usuario que registramos y 
los autos registrados con el id usuario al final
Esto sucede por la anotacion en la clase auto @ManyToOne Y En usuario @OneToMany 
añadiendo el  @JsonBackReference y @JsonManagedReference para mayor control el los Json.
 
