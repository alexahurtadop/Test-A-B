# Test-A-B
We will analyze an international online store where an A/B test was conducted. The test results are available along with the technical specifications. Interpreting these data is important to understand the impact of the changes introduced in the recommendation system.  

**Technical Description**

Nombre de la prueba: recommender_system_test
Grupos: А (control), B (nuevo embudo de pago)
Launch date: 2020-12-07
Fecha en la que dejaron de aceptar nuevos usuarios: 2020-12-21
Fecha de finalización: 2021-01-01
Audiencia: 15% de los nuevos usuarios de la región de la UE
Propósito de la prueba: probar cambios relacionados con la introducción de un sistema de recomendaciones mejorado
Resultado esperado: dentro de los 14 días posteriores a la inscripción, los usuarios mostrarán una mejor conversión en vistas de la página del producto (el evento product_page), instancias de agregar artículos al carrito de compras (product_card) y compras (purchase). En cada etapa del embudo product_page → product_card → purchase, habrá al menos un 10% de aumento.
Número previsto de participantes de la prueba: 6 000

We have four datasets to develop the project, which contain the following information:

`ab_project_marketing_events_us.csv`: Calendario de eventos de marketing para 2020

- `name`: el nombre del evento de marketing
- `regions`: regiones donde se llevará a cabo la campaña publicitaria
- `start_dt`: fecha de inicio de la campaña
- `finish_dt`: fecha de finalización de la campaña

`final_ab_new_users_upd_us.csv`: Todos los usuarios que se registraron en la tienda en línea desde el 7 hasta el 21 de diciembre de 2020

- `user_id`
- `first_date`: fecha de inscripción
- `region`
- `device`: dispositivo utilizado para la inscripción

`final_ab_events_upd_us.csv`: Todos los eventos de los nuevos usuarios en el período comprendido entre el 7 de diciembre de 2020 y el 1 de enero de 2021

- `user_id`
- `event_dt`: fecha y hora del evento
- `event_name`: nombre del tipo de evento
- `details`: datos adicionales sobre el evento (por ejemplo, el pedido total en USD) para los eventos purchase

`final_ab_participants_upd_us.csv`: Tabla con los datos de los participantes de la prueba

- `user_id`
- `ab_test`: nombre de la prueba
- `group`: el grupo de prueba al que pertenecía el usuario
