#  APPBANK

Aplicación **Spring Boot** para la gestión de clientes bancarios.

---

##  Requisitos previos

Antes de ejecutar la aplicación, asegúrate de tener instalados los siguientes componentes:

- [Visual Studio Code](https://code.visualstudio.com/)
- [Java JDK](https://www.oracle.com/java/technologies/javase-downloads.html)
- Extensión de **Java** para VS Code (usa `Ctrl + Shift + X` para abrir la pestaña de extensiones)

>  Instala también **Spring Boot Extension Pack** y **Thunder Client** para probar tus endpoints fácilmente.


<img width="368" height="93" alt="Captura de pantalla 2025-10-23 092501" src="https://github.com/user-attachments/assets/4fc0de1e-b0dd-40c2-85c4-bbbd30a9b274" />
<img width="364" height="90" alt="Captura de pantalla 2025-10-23 092545" src="https://github.com/user-attachments/assets/25c6b6bd-6f42-41b6-ac82-1b03739ea36c" />
<img width="370" height="90" alt="Captura de pantalla 2025-10-23 092616" src="https://github.com/user-attachments/assets/e181b16e-c181-4763-9baf-e7dc2ef8105d" />



---

##  Abrir el proyecto

1. Abre **VS Code**.  
2. Dirígete a:  
   **File → Open Folder**  
   o usa el atajo `Ctrl + O`.  
3. Selecciona la carpeta del proyecto **APPBANK**.

<img width="402" height="498" alt="Captura de pantalla 2025-10-23 093734" src="https://github.com/user-attachments/assets/b98c95d9-ee4e-4698-9783-d9753651ebe9" />


---

##  Ejecutar Spring Boot

1. Una vez que VS Code detecte el entorno de Java, localiza los íconos de ejecución de Spring Boot (normalmente arriba del archivo principal).
2. Haz clic primero en el **botón de la flecha (Run)**.
3. Luego selecciona el **botón de ejecución de Spring Boot**.

<img width="435" height="661" alt="Captura de pantalla 2025-10-23 094153" src="https://github.com/user-attachments/assets/3325a64d-1264-4243-9d56-1f00b90bfd41" />


Si todo está configurado correctamente, deberías ver algo como esto en la terminal:

<img width="1452" height="230" alt="Captura de pantalla 2025-10-23 094415" src="https://github.com/user-attachments/assets/4212ec04-bf84-43ad-ae6d-bef519e2aee5" />


 Esto significa que la aplicación está corriendo sin problemas en el puerto **8080**.

---

##  CRUD de Customer

A continuación te mostramos cómo crear, listar y buscar clientes utilizando **Thunder Client** o cualquier cliente REST.

---

###  Crear un nuevo cliente (POST)

1. Abre la extensión **Thunder Client**.  
2. Crea una nueva request (**New Request**).  

<img width="373" height="127" alt="Captura de pantalla 2025-10-23 094848" src="https://github.com/user-attachments/assets/d7f11841-9dac-404b-900f-02868fbe287a" />
al crearlo te aparecera algo asi: 
<img width="984" height="400" alt="Captura de pantalla 2025-10-23 095103" src="https://github.com/user-attachments/assets/89c94721-9b7f-4a83-aa64-f30c412c4acc" />


3. Usa la siguiente URL:
  [http://localhost:8080/api/bank/customers](http://localhost:8080/api/bank/customers)

4. Selecciona el método **POST**.  
5. En la pestaña **Body**, selecciona formato **JSON** e ingresa los datos del cliente que deseas crear.  
6. Presiona **Send**.

<img width="1371" height="502" alt="Captura de pantalla 2025-10-23 095638" src="https://github.com/user-attachments/assets/f6164395-32a6-448b-aa4b-38f13baa0b0c" />


Si todo sale bien, recibirás un código de estado indicando una creación exitosa.

---

###  Obtener la lista de todos los clientes (GET)

1. Crea una nueva request en **Thunder Client**.  
2. Usa la misma URL:

http://localhost:8080/api/bank/customers


3. Cambia el método a **GET**.  
4. Presiona **Send**.

<img width="1429" height="552" alt="Captura de pantalla 2025-10-23 100342" src="https://github.com/user-attachments/assets/7c7e07b9-63ac-4aaa-aaaa-b488ad491b08" />


Esto devolverá la lista completa de clientes registrados.

---

###  Buscar cliente por ID (GET)

1. Crea otra request.  
2. Usa la URL con el ID del cliente:

[http://localhost:8080/api/bank/customers/{id_cliente}](http://localhost:8080/api/bank/customers/{id_cliente})


<img width="1267" height="322" alt="Captura de pantalla 2025-10-23 100844" src="https://github.com/user-attachments/assets/6b9a9184-f8fc-49e3-a0b4-d462c69191e1" />


Esto devolverá el cliente correspondiente al ID indicado.

---

##  Ver datos desde el navegador

También puedes consultar los endpoints directamente desde tu navegador:

- Lista de clientes:  
   [http://localhost:8080/api/bank/customers](http://localhost:8080/api/bank/customers)
- Buscar cliente por ID:  
   [http://localhost:8080/api/bank/customers/{id_cliente}](http://localhost:8080/api/bank/customers/{id_cliente})

<img width="1905" height="142" alt="Captura de pantalla 2025-10-23 103838" src="https://github.com/user-attachments/assets/6eb436f4-26af-4879-8c5e-8fa9585864fe" />

Ahora que ya sabes como funciona THUNDER CLIENT, vamos con los siguientes de una forma mas sencilla.

##  GESTIÓN DE CUENTAS

### Crear Cuenta de Ahorros (Savings)
- **Método:** `POST`  
- **URL:** [http://localhost:8080/api/bank/customers/{id_cliente}/accounts](http://localhost:8080/api/bank/customers/{id_cliente}/accounts)  
<img width="1223" height="506" alt="Captura de pantalla 2025-10-23 115106" src="https://github.com/user-attachments/assets/8ee254c1-8749-4605-a3e2-8aff4fe01f88" />


### Crear Cuenta Corriente (Checking)
- **Método:** `POST`  
- **URL:** [http://localhost:8080/api/bank/customers/{id_cliente}/accounts](http://localhost:8080/api/bank/customers/{id_cliente}/accounts)  
<img width="1198" height="452" alt="Captura de pantalla 2025-10-23 115412" src="https://github.com/user-attachments/assets/b4b8fd96-7e09-41ea-abfd-fb7138245652" />

### Buscar Cuenta por ID
- **Método:** `GET`  
- **URL:** [http://localhost:8080/api/bank/accounts/{id_cuenta}](http://localhost:8080/api/bank/accounts/{id_cuenta}) 
- **Ejemplo:** `ACC001`  

### Listar Cuentas de un Cliente
- **Método:** `GET`  
- **URL:** [http://localhost:8080/api/bank/customers/{id_cliente}/accounts](http://localhost:8080/api/bank/customers/{id_cliente}/accounts)  
- **Ejemplo:** `C001`
- el cliente no tiene que ser necesariamente 'C001', lo puedes identificar como quieras

---

##  TRANSACCIONES

### Realizar Depósito
- **Método:** `POST`  
- **URL:** [http://localhost:8080/api/bank/accounts/{id_cuenta}/deposit?amount={monto}](http://localhost:8080/api/bank/accounts/{id_cuenta}/deposit?amount={monto})  
- **Query Params:**  
  - `amount`: monto a depositar  
<img width="1220" height="327" alt="Captura de pantalla 2025-10-23 120316" src="https://github.com/user-attachments/assets/75e798a8-6734-4e62-ae34-d249a7233360" />
Aqui el query se usa para pasar parametros y valores, en este caso el parametro es monto y el valor q es 1000, una vez ingreses estos datos la URL se actuliza sola


### Realizar Retiro
- **Método:** `POST`  
- **URL:** [http://localhost:8080/api/bank/accounts/{id_cuenta}/withdraw?amount={monto}](http://localhost:8080/api/bank/accounts/{id_cuenta}/withdraw?amount={monto})  
- **Query Params:**  
  - `amount`: monto a retirar
    Aqui pasa lo mismo que deposito solo que ahora retira, pero se usa es query

### Realizar Transferencia
- **Método:** `POST`  
- **URL:** [http://localhost:8080/api/bank/accounts/{id_cuenta}/transfer](http://localhost:8080/api/bank/accounts/{id_cuenta}/transfer)  
<img width="715" height="328" alt="Captura de pantalla 2025-10-23 121339" src="https://github.com/user-attachments/assets/15807ac6-9f5d-4ac1-b5d6-ce82dbab289b" />


### Consultar Transacciones de una Cuenta
- **Método:** `GET`  
- **URL:** [http://localhost:8080/api/bank/accounts/{id_cuenta}/transactions](http://localhost:8080/api/bank/accounts/{id_cuenta}/transactions)  

---

##  INTERESES

### Aplicar Interés a Cuenta de Ahorros
- **Método:** `POST`  
- **URL:** [http://localhost:8080/api/bank/accounts/{id_cuenta}/apply-interest](http://localhost:8080/api/bank/accounts/{id_cuenta}/apply-interest)

##  Autor

Proyecto desarrollado por **Juan Pablo Salazar Mora** como práctica de desarrollo y aprendizaje

