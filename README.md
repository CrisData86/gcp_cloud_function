# gcp_cloud_function
Este script es un controlador para ejecutar diferentes etapas de un proceso ETL (Extract, Transform, Load) basado en funciones en la nube. Aquí está lo que hace:

Importa tres funciones principales: ingest_data, transform_data, y etl_data desde los módulos ingest_data.py, transform_data.py, y etl_data.py respectivamente. Estos módulos probablemente contienen la lógica específica para cada etapa del proceso ETL.

Define una función main(request) que actúa como la función principal que será invocada por la plataforma de la nube.

Dentro de main(request), primero recopila el JSON de la solicitud que se espera contenga un mensaje que indica qué función debe ejecutarse (ingest_data, transform_data, o etl).

Luego, basado en el mensaje recibido, selecciona la función correspondiente de un diccionario de opciones y ejecuta esa función. Cada función toma dos argumentos opcionales: date_start y date_end, que se pasan a las funciones específicas.

Si no se proporciona un mensaje válido en la solicitud JSON, devuelve un mensaje de advertencia solicitando que se inserten parámetros.

Finalmente, si el script se ejecuta directamente (es decir, no se importa como un módulo), llama a la función main().

En resumen, este script actúa como un enrutador para ejecutar diferentes partes del proceso ETL basado en la solicitud recibida. Dependiendo del mensaje recibido en la solicitud JSON, ejecutará la función correspondiente para realizar la tarea de ingestión de datos, transformación de datos o carga de datos.






