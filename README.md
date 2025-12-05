# 🐍 Inventory Management System – Python

Sistema de gestión de inventario desarrollado en **Python** como proyecto de la materia *Programación I – Algoritmos y Estructuras de Datos I (UADE)*.

Permite administrar:

- Productos
- Clientes
- Compras (entradas de stock)
- Ventas (salidas de stock)
- Reportes básicos del inventario

e incluye validación de usuarios, persistencia en archivos y pruebas unitarias.

---

## 🎯 Objetivo

- Registrar y administrar los productos del inventario.
- Consultar de forma rápida el estado de stock.
- Soportar decisiones de negocio (reabastecimiento, entradas/salidas).
- Mantener el inventario organizado para reducir errores.

---

## 🧩 Funcionalidades principales

### 🔐 Validación de usuarios
Antes de acceder al sistema, el usuario debe autenticarse con **usuario y contraseña**.  
Las credenciales se validan contra una lista / archivo seguro.

### 📦 Gestión de productos
- Alta de productos con:
  - ID (formato `PR` + 3 dígitos)
  - Nombre
  - Categoría / proveedor
  - Cantidad
  - Precio
- Modificación de productos (precio, cantidad, etc.).
- Baja lógica/física de productos.
- Visualización de productos y consulta por ID.
- Reporte de **productos con stock bajo** y valor total del inventario.

### 👥 Gestión de clientes
- Alta de clientes (ID, nombre, teléfono).
- Baja de clientes.
- Listado de **últimos clientes cargados**.

### 🧾 Compras (entradas)
- Registro de compras con:
  - ID de compra
  - ID de producto
  - Cantidad comprada
  - Proveedor
- Actualización del stock al recibir la compra.
- Visualización de **últimas compras** realizadas.

### 💸 Ventas (salidas)
- Registro de ventas con:
  - ID de venta
  - ID de cliente
  - ID de producto
  - Cantidad vendida
- Descuento automático del stock (verifica stock disponible).
- Visualización de **últimas ventas**.

---

## 🧠 Diseño y arquitectura

El sistema está modularizado en varios paquetes:

```text
carga_de_informacion/   # Altas de productos, clientes, compras, ventas
dar_de_baja/            # Bajas de productos y clientes
productos/              # búsquedas, ordenamiento, modificación
mostrar_ultimos/        # reportes de últimas compras, ventas, clientes
Pruebas_unitarias/      # tests automatizados
trabajo.py              # menú principal y orquestación

Características técnicas:

Uso intensivo de listas y diccionarios para manejar:

productos

clientes

compras

ventas

Manejo de archivos (.txt, .json) para persistencia de datos.

Menú principal estructurado por secciones:

[1] Productos

[2] Clientes

[3] Compras

[4] Ventas

[0] Salir

Código pensado para ser extensible: se pueden agregar nuevas opciones al menú sin romper el flujo existente.

🧪 Pruebas

El proyecto incluye una carpeta de pruebas unitarias:

Pruebas_unitarias/
  Funciones.py
  test_Funciones.py


Las pruebas se ejecutan con pytest:

pytest Pruebas_unitarias/

▶️ Cómo ejecutar el sistema

Clonar el repositorio:

git clone https://github.com/Ezrasaf/inventory-management-python.git
cd inventory-management-python


(Opcional) Crear entorno virtual e instalar dependencias:

python -m venv venv
venv\Scripts\activate          # Windows
# source venv/bin/activate     # Linux / Mac

pip install -r requirements.txt    # si se define


Ejecutar el menú principal:

python trabajo.py


(ajustar la ruta si se mueve a src/)

🧑‍💻 Stack tecnológico

Lenguaje: Python 3.x

Paradigma: Programación estructurada y modular

Persistencia: Archivos de texto y JSON

Testing: pytest

Control de versiones: Git + GitHub

Gestión del proyecto: Trello (sprints, backlog)

👤 Autor

Ezrasaf – Estudiante de Ingeniería en Informática (UADE)
Interesado en Backend, Python, Datos y Automatización.


4. Abajo → **Commit new file**

Listo: tu proyecto Python ahora se ve como un **mini ERP de inventario profesional** en tu GitHub.
