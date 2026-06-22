# Finanzas Personales

App web básica (HTML, CSS, JavaScript). Los datos se guardan en archivos **.json** dentro de la carpeta `data/`.

## Uso

1. Abre `index.html` en **Chrome** o **Edge** (o con un servidor local como Live Server).
2. La app intenta cargar automáticamente la carpeta `data/` que está junto a los HTML.
3. Solo si no la encuentra, te pedirá seleccionar la carpeta del proyecto o `data` (una vez; luego la recuerda).

Cada cambio actualiza los archivos:

- `data/usuarios.json`
- `data/cuentas.json`
- `data/historialPagos.json`
- `data/gastosHormiga.json`
- `data/prestamos.json`
- `data/sesion.json`

## Páginas

| Página | Descripción |
|--------|-------------|
| `dashboard.html` | Cuentas y gastos recurrentes |
| `pagos.html` | Control de pagos mensuales por cuenta |
| `hormiga.html` | Gastos pequeños del día |
| `prestamos.html` | Préstamos que realizas |
| `resumen.html` | Total del mes: cuentas pagadas + gastos hormiga |

## Modelo préstamo

```json
{
  "id": "...",
  "usuarioId": 1,
  "prestante": "Juan",
  "monto": 500000,
  "intereses": 5,
  "fechaVencimiento": "2026-12-31",
  "cuotas": 12,
  "cuotasPagadas": 3
}
```

- `intereses`: porcentaje sobre el capital.
- Total a devolver = monto + (monto × intereses / 100).
- Valor cuota = total / cuotas.

## Estructura

```
personal/
├── index.html
├── dashboard.html
├── pagos.html
├── hormiga.html
├── prestamos.html
├── resumen.html
├── data/
├── css/styles.css
└── js/
```
