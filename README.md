# proyecto-automatizacion-ai
# Sistema de Reservas Automatizado con IA (Human-in-the-Loop) 

Este proyecto es un ecosistema de automatización que procesa solicitudes de reserva en lenguaje natural, gestiona una base de datos relacional y requiere aprobación humana antes de la confirmación final.

## Arquitectura y Tecnologías
* Orquestador: n8n
* Procesamiento IA: Agente IA (OpenRouter / OpenAI)
* Base de Datos: Airtable (Base relacional de Clientes y Reservas)
* Canal de Salida: Gmail (Notificaciones y validación HITL)

## Enlaces del Proyecto (Entregables)
* Video Demostración: (https://drive.google.com/file/d/17JgJGb5lZSEAYBzw3ZvB-h0WufuPYpSK/view?usp=sharing)
* Base de Datos: (https://airtable.com/invite/l?inviteId=invyE0saeiRA5JZ6Q&inviteToken=161c3c37647f499c4cde3b21f525093b6e21984ffc3f905303e743b8d8ab7b51&utm_medium=email&utm_source=product_team&utm_content=transactional-alerts)
* Diagrama de Arquitectura: (https://drive.google.com/file/d/1qk-iNz854y3zi5tFnXYZki_wdH6ixsJG/view?usp=sharing)
* Código del flujo:(https://drive.google.com/file/d/1Dnpdqfz7fR69BDv4Jom_nHncuzoz4psQ/view?usp=sharing)

## Características Técnicas
* Human-in-the-Loop: El flujo se pausa a la espera de la decisión de un agente humano (Aprobar/Rechazar) antes de actualizar la base de datos.
* Resiliencia (Error Handling): Incluye un Error Trigger global que notifica al administrador si alguna API (IA o Airtable) falla, evitando bucles y caídas silenciosas.
