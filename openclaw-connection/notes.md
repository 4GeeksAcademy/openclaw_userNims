# Notas de Configuración — OpenClaw Connection

1. Canal Telegram: Se integró mediante BotFather configurando `"dmPolicy": "pairing"`, lo que garantiza que solo el operador autenticado por consola pueda interactuar con el agente.
2. Pasarela Zapier MCP: Se utilizó Zapier MCP como un gateway aislado (sandboxed proxy), eliminando la necesidad de exponer tokens API en bruto en el entorno de OpenClaw.
3. Principio de mínimo privilegio: Se empleó una cuenta de Google dedicada exclusivamente para pruebas, evitando el acceso cruzado a datos personales sensibles.
4. Gestión de ambigüedad: Ante instrucciones iniciales incompletas, se comprobó que el modelo suspende la ejecución y solicita activamente los parámetros faltantes antes de invocar las herramientas.
5. Ejecución con mcporter: Las llamadas a Google Docs y Google Calendar se articularon mediante el cliente `mcporter`, verificándose su correcta ejecución en la pestaña Historial de Zapier.