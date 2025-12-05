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

### 🔧 Características Técnicas

- Manipulación de datos mediante **listas**, **diccionarios** y estructuras propias.
- Persistencia de información en archivos:
  - `.txt` para registros planos
  - `.json` para estructuras complejas
- Menú interactivo con opciones numeradas.
- Código extensible: se pueden agregar nuevas opciones sin romper la lógica actual.
- Separación clara entre:
  - **lógica de negocio**
  - **manejo de archivos**
  - **operaciones CRUD**

---

## 🧪 Pruebas Unitarias

El proyecto incluye un módulo de testing con **pytest**, ubicado en:

Pruebas_unitarias/
Funciones.py
test_Funciones.py

go
Copiar código

Para ejecutar los tests:

```bash
pytest Pruebas_unitarias/
▶️ Cómo Ejecutar el Sistema
Cloná el repositorio:

bash
Copiar código
git clone https://github.com/Ezrasaf/inventory-management-python.git
cd inventory-management-python
(Opcional) Crear un entorno virtual:

bash
Copiar código
python -m venv venv
venv\Scripts\activate      # Windows
# source venv/bin/activate # Linux / Mac
Ejecutar el sistema:

bash
Copiar código
python trabajo.py
🛠 Tecnologías Utilizadas
Python 3.x

Persistencia en JSON y TXT

pytest para testing

Git + GitHub para control de versiones

Documentación y gestión del proyecto con Trello

📚 Documentación del Proyecto
Este proyecto se realizó siguiendo etapas, sprints, roles y flujos definidos, documentados en:

Informe del Proyecto (PDF)

Diagrama del sistema y sus módulos

(Se recomienda agregar los documentos dentro de una carpeta /docs del repositorio.)

👤 Autor
Ezrasaf
Estudiante de Ingeniería en Informática – UADE
Interesado en Backend, Python, SQL e Ingeniería de Datos.

⭐ Valor del Proyecto en Portfolio
Este proyecto demuestra:

Capacidad para diseñar un sistema real desde cero

Trabajo modular en Python

CRUD completo

Persistencia en archivos

Testing automatizado

Documentación y seguimiento con metodología ágil

Es ideal para postular a posiciones de:

Backend Jr

Python Developer Jr

IT / Soporte Técnico con programación

Data Engineering (nivel inicial con Python + SQL)
