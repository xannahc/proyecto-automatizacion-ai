# proyecto-automatizacion-ai
# Sistema de Reservas Automatizado con IA (Human-in-the-Loop) 

Este proyecto es un ecosistema de automatización que procesa solicitudes de reserva en lenguaje natural, gestiona una base de datos relacional y requiere aprobación humana antes de la confirmación final.

## Arquitectura y Tecnologías
* Orquestador: n8n
* Procesamiento IA: Agente IA (OpenRouter / OpenAI)
* Base de Datos: Airtable (Base relacional de Clientes y Reservas)
* Canal de Salida: Gmail (Notificaciones y validación HITL)

## Enlaces del Proyecto (Entregables)
* Video Demostración: (https://drive.google.com/file/d/17JgJGb5lZSEAYBzw3ZvB-h0WufuPYpSK/view?usp=sharing) El peso del archivo no permite subirse al repositorio. Pero tiene los permisos para visualizarlo.
* Base de Datos: https://airtable.com/appEJKcnTPrTed8ki/shrq6G0HbPGUJzQ9p
* Diagrama de Arquitectura: Puede visualizarle en los archivos adjuntos del repositorio.
* Código del flujo: Puede visualizarle en los archivos adjuntos del repositorio.

## Características Técnicas
* Human-in-the-Loop: El flujo se pausa a la espera de la decisión de un agente humano (Aprobar/Rechazar) antes de actualizar la base de datos.
* Resiliencia (Error Handling): Incluye un Error Trigger global que notifica al administrador si alguna API (IA o Airtable) falla, evitando bucles y caídas silenciosas.
