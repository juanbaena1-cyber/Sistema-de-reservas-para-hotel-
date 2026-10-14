# HotelSync: Sistema Inteligente de Gestión de Reservas Hoteleras

## De qué trata
Este proyecto nació de una idea sencilla: ayudar a un hotel que todavía lleva sus reservas en un cuaderno. Esa forma de trabajar es poco práctica y se presta para errores, así que propongo un sistema que junte en un solo lugar las reservas, las habitaciones, los huéspedes y los pagos.

## Lo que vi en el documento
- El sistema debe permitir hacer reservas, saber qué habitaciones hay disponibles según las personas que van a hospedarse, registrar a cada huésped con su habitación y manejar los pagos de forma segura.
- Hay cuatro tipos de usuario: el administrador, el recepcionista, el huésped y las agencias o plataformas externas. Cada uno puede hacer cosas distintas.
- Quedaron definidos 17 requerimientos funcionales (habitaciones, reservas, huéspedes y pagos) y varios de calidad: seguridad, rapidez, funcionamiento todo el día, facilidad de uso y posibilidad de crecer.

## Dificultades que encontré
- Dos personas pueden reservar la misma habitación para las mismas fechas, o las fechas se cruzan entre una entrada y una salida.
- Es difícil controlar los pagos duplicados, las cancelaciones y los cambios de fecha.
- Recepción no siempre sabe con certeza qué habitaciones están libres, ocupadas o por desocupar.
- Llevar todo en un cuaderno no es práctico para un hotel.
- Hace falta seguridad cuando las reservas y los pagos llegan por páginas de convenio y no directamente por el hotel.

## Cómo funciona
1. Alguien consulta la disponibilidad por fechas y número de personas.
2. Se crea la reserva y el sistema revisa que no se cruce con otra en la misma habitación.
3. Se registra el pago o anticipo. Solo con eso la reserva queda confirmada y llega un correo de confirmación.
4. En el check-in se asigna la habitación al huésped.
5. En el check-out la habitación se libera y se actualiza su estado.
6. Si la reserva cambia o se cancela, se aplican las políticas del hotel y se vuelve a validar la disponibilidad.

## Estructura del proyecto
```
sistema_reservas_hotel/
├── documentacion/   
├── base_datos/       
├── backend/          
│   ├── habitaciones/
│   ├── reservas/
│   ├── huespedes/
│   ├── pagos/
│   ├── usuarios/
│   ├── reportes/
│   └── integraciones/
├── frontend/         las pantallas
│   ├── portal_huesped/
│   └── panel_interno/   (administrador y recepción)
└── pruebas/          casos para comprobar las reglas
```
