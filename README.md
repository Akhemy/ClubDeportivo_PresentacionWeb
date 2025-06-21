# Sistema Club Deportivo - Proyecto Integrador

> **Desarrollo de Sistemas Orientado a Objetos**  
> Instituto de Formación Técnica Superior N° 29  
> Grupo 16 - 2025

##  Descripción del Proyecto

Sistema integral de gestión para club deportivo desarrollado en **C# con Windows Forms** aplicando principios de **Programación Orientada a Objetos**. El sistema permite administrar socios, no socios, pagos, carnets y generar reportes de vencimientos.

###  Objetivos Cumplidos
- ✅ **Registro de socios y no socios** con validaciones completas
- ✅ **Cobro de cuotas** mensuales y diarias (efectivo/tarjeta)
- ✅ **Generación de carnets** para socios con cuota al día
- ✅ **Listado de vencimientos** con campos calculados
- ✅ **Base de datos relacional** con integridad referencial

##  Equipo de Desarrollo

| Integrante | 
|------------|
| **Flores, Fernanda** 
| **Alvarez, Silvana Paola** 
| **Croci, Gisela** 
| **Olave Troncoso, Pamela B.** 

**Profesora:** Silvia Cañizares

##  Arquitectura del Sistema

### **Stack Tecnológico**
```
Frontend:  Windows Forms (.NET Framework 4.7.2)
Backend:   C# con principios POO
Database:  MySQL 8.0 (XAMPP)
IDE:       Visual Studio Community
Tools:     phpMyAdmin, Git, GitHub
```

### **Patrones Aplicados**
- 🔧 **DAO (Data Access Object)** - Separación de lógica de datos
- 🏭 **Factory Pattern** - Para conexiones de base de datos  
- 🎯 **MVC Conceptual** - Separación de responsabilidades


## 📁 Estructura del Proyecto

```
ClubDeportivo_PresentacionWeb/
├── 📄 index.html                 # Página web de presentación
├── 📋 README.md                  # Este archivo
├── 💻 codigo/
│   ├── 🖼️ Forms/                # Formularios Windows Forms
│   │   ├── FormLogin.cs
│   │   ├── FormRegistro.cs
│   │   ├── FormPagos.cs
│   │   ├── FormCarnet.cs
│   │   └── FormVencimientos.cs
│   ├── 🗄️ Data/                 # Capa de acceso a datos (DAO)
│   │   ├── DatabaseConnection.cs
│   │   ├── PersonaDAO.cs
│   │   ├── SocioDAO.cs
│   │   └── CuotaDAO.cs
│   ├── 🏗️ Models/               # Entidades del sistema
│   │   ├── Persona.cs
│   │   ├── Socio.cs
│   │   ├── Cuota.cs
│   │   └── Carnet.cs
│   └── 🗃️ Database/             # Scripts de base de datos
│       └── club_deportivo.sql
└── 📚 docs/                     # Documentación
    ├── manual-usuario.pdf
    ├── bocetos-iniciales/
    └── casos-de-uso.md
```

## 🚀 Características Principales

### 🔐 **Sistema de Login**
- Autenticación básica con credenciales admin/admin
- Configuración dinámica de base de datos MySQL
- Validación de conexión antes de inicio

### 📋 **Registro de Personas**
- Diferenciación entre **Socios** y **No Socios**
- Validaciones robustas de DNI (7-8 dígitos, no inicia con 0)
- **Apto físico obligatorio** para registro
- Generación automática de número de socio

### 💰 **Gestión de Pagos**
- **Cuotas mensuales** para socios ($15,000)
- **Pagos diarios** para no socios ($2,000)
- Soporte para **efectivo** y **tarjeta de crédito**
- Sistema de **cuotas con descuentos** (3 cuotas: 10%, 6 cuotas: 15%)
- Validación completa de datos de tarjeta

### 🎫 **Generación de Carnets**
- Solo para **socios con cuota al día**
- **Validación en cascada:** DNI → Persona → Socio → Estado
- Vista previa con datos completos
- Fechas de emisión y vencimiento automáticas

### 📊 **Reportes de Vencimientos**
- Consulta por rango de fechas
- **Campos calculados** con lógica SQL (CASE WHEN)
- Coloreado visual por estado (Verde: Al día, Amarillo: Por vencer, Rojo: Vencida)
- Exportación de reportes

## 🗄️ Modelo de Base de Datos

### **E
