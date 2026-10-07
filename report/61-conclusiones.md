# Conclusiones y Recomendaciones

## Conclusiones

* A través del uso de la metodología Lean UX y el desarrollo del Lean UX Canvas, el equipo logró centrar el proceso de diseño en las necesidades reales de los transportistas independientes y emprendedores Pymes, validando que existe una alta demanda por la optimización de rutas y la reducción de fletes vacíos en Lima.
* El proceso de Event Storming permitió al equipo tener una visión integral del flujo del negocio, facilitando la identificación precisa de los *Bounded Contexts* necesarios para la propuesta de Domain-Driven Design de la solución Trazza.
* El diseño e implementación de las arquitecturas (C4 Model) estableció una base tecnológica robusta y escalable sobre la nube (AWS), asegurando que tanto la plataforma web como el motor de *matchmaking* logístico interactúen eficientemente mediante APIs REST.
* La planificación mediante metodologías ágiles (Scrum) y el control de versiones (GitFlow) fueron vitales para cumplir a tiempo con las entregas de cada Sprint, fomentando la colaboración continua y la integración constante de los módulos de la Landing Page y Web Applications.

## Recomendaciones

* Se recomienda para fases futuras profundizar en la integración del monitoreo por hardware (IoT/GPS) directamente en los vehículos, con el objetivo de elevar la trazabilidad de los fletes e incrementar la confianza de los emprendedores.
* Se sugiere realizar más pruebas de usabilidad y A/B testing con la primera versión funcional de la plataforma para refinar aún más el flujo de "Matchmaking" e incorporar métricas directas del usuario final.
* Mantener actualizadas las convenciones de *Clean Architecture* en las siguientes iteraciones de desarrollo del backend para evitar acoplamiento a medida que el negocio requiera escalar a rutas interprovinciales.