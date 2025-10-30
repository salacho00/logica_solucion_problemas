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



## 📋 Visualización con Swagger UI

Otra forma de poder visualizar los cambios es por medio de Swagger UI, el cual nos permite ver todos los métodos sin tener que crearlos manualmente. Para poder usarlo debes ejecutar el SpringBoot y después irte a esta web:

[localhost:8080/swagger-ui/index.html](localhost:8080/swagger-ui/index.html)


Una vez en la web debería aparecer esto:

<img width="1890" height="1021" alt="Captura de pantalla 2025-10-30 135843" src="https://github.com/user-attachments/assets/92e46765-e937-4fa9-8fc2-f3fc9409907d" />


Aquí estarán todos los métodos GET y POST.

---

### 👤 Gestión de Clientes

#### Crear cliente
- **Ruta:** `http://localhost:8080/api/bank/customers`
- **Método CRUD:** POST

<img width="1776" height="476" alt="Captura de pantalla 2025-10-30 141036" src="https://github.com/user-attachments/assets/d6a8a72d-66b3-46c8-b482-e69dd68ffaf6" />


---

#### Lista de todos los clientes
- **Ruta:** `http://localhost:8080/api/bank/customers`
- **Método CRUD:** GET

<img width="1776" height="859" alt="Captura de pantalla 2025-10-30 141334" src="https://github.com/user-attachments/assets/3d3e3bd8-e431-411a-bcf1-9bec4b491bf1" />


---

#### Buscar cliente por id
- **Ruta:** `http://localhost:8080/api/bank/customers/{customerId}`
- **Método CRUD:** GET

<img width="648" height="475" alt="Captura de pantalla 2025-10-30 141526" src="https://github.com/user-attachments/assets/129baa99-6e78-402a-b7c3-71e5708f8f15" />


---

### 💰 Gestión de Cuentas

#### Crear cuenta de ahorros o de corriente
- **Ruta:** `http://localhost:8080/api/bank/customers/{customerId}/accounts`
- **Método CRUD:** POST

**⚠️ Importante:** En donde dice "type" hay que colocar si es de ahorros (`SAVINGS`) o va a ser de corriente (`CHECKING`)

<img width="650" height="635" alt="Captura de pantalla 2025-10-30 142055" src="https://github.com/user-attachments/assets/5388ef47-b427-40c0-8cf4-a30ec141439b" />


---

#### Lista de cuentas de un cliente
- **Ruta:** `http://localhost:8080/api/bank/customers/{customerId}/accounts`
- **Método CRUD:** GET

<img width="1760" height="480" alt="Captura de pantalla 2025-10-30 143321" src="https://github.com/user-attachments/assets/74de86fb-f81a-49c6-bbae-e83238b5e65b" />


---

#### Para buscar solo una cuenta
- **Ruta:** `http://localhost:8080/api/bank/accounts/{accountId}`
- **Método CRUD:** GET

<img width="1772" height="629" alt="Captura de pantalla 2025-10-30 143712" src="https://github.com/user-attachments/assets/db464be8-7e08-446f-84b6-d9952dea487e" />


---

### 💸 Operaciones Bancarias

#### Hacer depósitos
- **Ruta:** `http://localhost:8080/api/bank/accounts/ACC01/deposit?amount=200`
- **Método CRUD:** POST

En el primer parámetro debes poner el id de la cuenta y en el segundo parámetro debes poner el valor del monto que vas a añadir a la cuenta


<img width="1774" height="463" alt="Captura de pantalla 2025-10-30 144147" src="https://github.com/user-attachments/assets/733c19fd-3af6-4233-980e-b9660068c790" />

---

#### Hacer retiros
- **Ruta:** `http://localhost:8080/api/bank/accounts/ACC01/withdraw?amount=50`
- **Método CRUD:** POST

Aquí es el mismo proceso que depositar solo que ahora es retirar

<img width="1778" height="464" alt="Captura de pantalla 2025-10-30 144401" src="https://github.com/user-attachments/assets/e1d64e1f-6ea1-4c5b-9cb8-3332feb1d685" />


---

#### Transferir dinero a otra cuenta
- **Ruta:** `http://localhost:8080/api/bank/accounts/ACC01/transfer`
- **Método CRUD:** POST

Aquí debes poner de parámetro la cuenta donde va a salir el dinero, y en el body pones hacia que cuenta va a parar el dinero junto a cuanto dinero va a ser

<img width="1771" height="463" alt="Captura de pantalla 2025-10-30 144658" src="https://github.com/user-attachments/assets/bb43c722-44bf-456b-a838-e356b831ee9e" />


---

### 📊 Consultas y Operaciones

#### Todas las transacciones de una cuenta
- **Ruta:** `http://localhost:8080/api/bank/accounts/ACC01/transactions`
- **Método CRUD:** GET

<img width="1760" height="724" alt="Captura de pantalla 2025-10-30 145302" src="https://github.com/user-attachments/assets/69debfdc-fb7e-408b-b368-35716c56772c" />


---

#### Aplicar intereses
- **Ruta:** `http://localhost:8080/api/bank/accounts/ACC01/apply-interest`
- **Método CRUD:** POST

<img width="1766" height="316" alt="Captura de pantalla 2025-10-30 145453" src="https://github.com/user-attachments/assets/f02edc05-86f1-4057-a82f-f28e65962089" />


---
##  Autor

Proyecto desarrollado por **Juan Pablo Salazar Mora** como práctica de desarrollo y aprendizaje

