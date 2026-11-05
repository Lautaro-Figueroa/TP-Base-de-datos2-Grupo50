# 🗃️ Venta de Garage Web – Base de Datos (SQL Server)

Diseño e implementación de la base de datos de una plataforma de venta de artículos usados con **sistema de reservas**: el comprador paga una seña del 10 % y el artículo queda reservado por 72 horas. Si la venta no se concreta en ese plazo, el artículo vuelve automáticamente a estar disponible.

> Trabajo Práctico Integrador de **Base de Datos II** de la Tecnicatura Universitaria en Programación (UTN), desarrollado por el **Grupo 50**.

## 🧩 Modelo de datos

Tablas: `Usuarios`, `Articulos`, `Categorias`, `EstadosArticulo`, `ImagenesArticulo`, `Reservas`, `Ventas`, `Auditoria`

## ⚙️ Objetos de base de datos

| Tipo | Objeto | Qué hace |
|---|---|---|
| Stored Procedure | `SP_RegistrarReserva` | Registra una reserva con su seña y vencimiento |
| Stored Procedure | `SP_ReporteDeVentasPorFechas` | Reporte de ventas en un rango de fechas |
| Trigger | `TR_RestaurarDisponibilidadPorVentaFallida` | Vuelve a dejar disponible el artículo si la venta no se concreta |
| Trigger | `TR_NotificarCambioDePrecio` | Registra en `Auditoria` los cambios de precio |
| Trigger | `TR_AuditarArticuloPublicado` | Audita la publicación de nuevos artículos |
| Vista | `VW_ReservasActivas` | Reservas vigentes con su tiempo restante |
| Vista | `VW_ArticulosDisponibles` | Artículos disponibles para la venta |
| Vista | `VW_HistorialVentas` | Historial consolidado de ventas |
| Función | `CalcularTiempoRestante` | Calcula el tiempo restante de una reserva |

## 📁 Estructura

```
├── Creacion de DB/  → Creación de tablas y relaciones
├── INSERT/          → Datos de prueba
├── SP/              → Stored procedures
├── TRIGGERS/        → Triggers
└── VISTAS/          → Vistas y funciones
```

## 🛠️ Tecnologías

SQL Server · T-SQL

## 👨‍💻 Mi aporte

- Escribí el script de creación de las tablas **Articulos**, **ImagenesArticulo** y **Auditoria**.
- Desarrollé el **trigger** que restaura la disponibilidad, la **función** que calcula el tiempo restante de una reserva y la **vista** de reservas activas.

## ▶️ Cómo ejecutarlo

Ejecutar los scripts en SQL Server Management Studio en este orden: `Creacion de DB` → `INSERT` → `SP` → `TRIGGERS` → `VISTAS`.

## 👥 Equipo

[Marisel Alarcón](https://github.com/AlarconMarisel) · [Claudio Gobbi](https://github.com/ClaudioCesarGobbi) · [Lautaro Figueroa](https://github.com/Lautaro-Figueroa)
