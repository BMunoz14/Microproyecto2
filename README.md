********Chatbot************
despues de cargar la imagen utilizar el siguiente comando en CMD para descargar el modelo Qwen:
curl -X POST http://IP_BALANCEADOR_AKS/api/pull -H "Content-Type: application/json" -d "{""name"": ""qwen2.5:1.5b""}"

y despues de descargar el modelo en powershell puedes usar el siguiente comando para obtener una respuesta del modelo LLM:

Invoke-RestMethod -Uri "http://IP_BALANCEADOR_AKS/api/generate" -Method Post -Headers @{ "Content-Type" = "application/json; charset=utf-8" } -Body '{"model": "qwen2.5:1.5b", "prompt": "Hola, ¿cómo estás?", "stream": false}' | Select-Object -ExpandProperty response

Para utlizar otros modelos visita https://ollama.com/search
