# 🏍️ MotoDash — Sistema de Gestión de Parqueadero

Sistema web para la gestión de entrada y salida de motos, con cálculo automático de cobros, historial de transacciones y panel administrativo.

---

## ✨ Características

- 🛵 Registro de entrada y salida de motos por placa
- 💰 Cálculo automático de tarifas (fracción, hora, día)
- 📋 Historial completo de cobros
- 📊 Dashboard con estadísticas del día
- 👥 Gestión de usuarios con roles (Admin / Operador)
- 🖨️ Impresión de recibos
- ⚙️ Configuración de tarifas desde el panel

---

## 💵 Lógica de Tarifas

| Tiempo | Cobro |
|--------|-------|
| 0 – 10 min | Fracción |
| 10 min – 1h 10min | 1 hora |
| 1h 10min – 1h 20min | 1 hora + fracción |
| 1h 20min – 2h 10min | 2 horas |
| Y así sucesivamente... | |

---

## 🛠️ Tecnologías

- **Backend:** PHP 8+
- **Base de datos:** MySQL
- **Frontend:** HTML, CSS, JavaScript (Vanilla)
- **Servidor local:** XAMPP

---

## 🚀 Instalación local

1. Clona el repositorio:
   ```bash
   git clone https://github.com/jdiegoces11/motodash.git
   ```

2. Copia la carpeta `motodash` dentro de `C:\xampp\htdocs\`

3. Importa la base de datos:
   - Abre `http://localhost/phpmyadmin`
   - Crea una BD llamada `motodash`
   - Importa el archivo `motodash.sql`

4. Configura la conexión en `config/db.php`:
   ```php
   $host     = "localhost";
   $usuario  = "root";
   $password = "";
   $base     = "motodash";
   ```

5. Abre en el navegador:
   ```
   http://localhost/motodash/
   ```

---

## 🔐 Usuarios por defecto

| Rol | Usuario | Contraseña |
|-----|---------|------------|
| Administrador | `admin` | `admin123` |
| Operador | `operador` | `operador123` |

---

## 📁 Estructura del proyecto

```
motodash/
├── api/
│   ├── activos.php
│   ├── config.php
│   ├── dashboard.php
│   ├── entrada.php
│   ├── historial.php
│   ├── salida.php
│   └── usuarios.php
├── auth/
│   └── logout.php
├── config/
│   └── db.php
├── css/
│   └── styles.css
├── js/
│   ├── app.js
│   └── layout.js
├── activos.php
├── configuracion.php
├── dashboard.php
├── historial.php
├── index.php
├── login.php
└── usuarios.php
```

---

## 📄 Licencia

Proyecto académico y profesional — desarrollado por Juan Diego Cespedes, Bucaramanga, Colombia.
