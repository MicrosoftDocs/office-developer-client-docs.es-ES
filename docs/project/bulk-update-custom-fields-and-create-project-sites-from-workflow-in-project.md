---
title: Actualización masiva de campos personalizados y creación de sitios de proyecto en Project Online
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: Para ayudar a los clientes a sacar el máximo partido de Project Online y mejorar nuestra extensibilidad y flexibilidad del servicio, hemos agregado dos métodos al modelo de objetos del lado cliente que puede usar en flujos de trabajo y aplicaciones de Project Online.
ms.openlocfilehash: 4de42471cd8c2f12a982447ccffc27ec8104fa31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355443"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a>Actualización en masa de los campos personalizados y crear sitios de proyecto desde un flujo de trabajo en Project Online

Para ayudar a los clientes a sacar el máximo partido de Project Online y mejorar la extensibilidad y flexibilidad de nuestro servicio, hemos agregado dos métodos al modelo de objetos del lado cliente que puede usar en flujos de trabajo y aplicaciones de Project Online.
  
|||
|:-----|:-----|
|**UpdateCustomFields** <br/> |Actualiza de forma masiva los campos personalizados del proyecto. Solo para Project Online. Solo está disponible en la API de REST.  <br/> |
|**CreateProjectSite** <br/> | Crea un sitio de proyecto. Solo para Project Online. Disponible en la API de REST, el modelo de objetos de cliente administrado y el modelo de objetos de cliente javaScript.  <br/> |
   
Además de proporcionar más flexibilidad, estos métodos también ofrecen mejoras significativas de rendimiento al guardar y publicar proyectos en un flujo de trabajo. En este artículo se describe cómo usar los métodos de la API de REST y se proporcionan instrucciones para crear un flujo de trabajo que actualiza de forma masiva campos personalizados y un flujo de trabajo que crea un sitio de Project.
  
> [!NOTE]
> Para obtener más información sobre cómo llamar a las API de REST desde flujos de trabajo de SharePoint 2013, vea Usar los servicios REST de [SharePoint](https://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl) desde el flujo de trabajo con el método POST y llamar a la API de Rest de [SharePoint 2013](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/)desde un flujo de trabajo de SharePoint Designer. 
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a>Actualización masiva de campos personalizados del proyecto desde un flujo de trabajo
<a name="BulkUpdateCustomFields"> </a>

Anteriormente, los flujos de trabajo solo podían actualizar un campo personalizado a la vez. La actualización de campos personalizados de proyecto de uno en uno puede provocar una experiencia deficiente para el usuario final cuando los usuarios se desfila entre páginas de detalles del proyecto. Cada actualización requería una solicitud  de servidor independiente mediante la acción Establecer campo de proyecto y la actualización de varios campos personalizados en una red de latencia alta y ancho de banda bajo causaba una sobrecarga no trivial. Para resolver este problema, agregamos el método **UpdateCustomFields** a la API de REST que le permite actualizar en masa los campos personalizados. Para usar **UpdateCustomFields**, se pasa un diccionario que contiene los nombres y valores de todos los campos personalizados que desea actualizar.
  
El método REST se encuentra en el siguiente punto de conexión:
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> Reemplace el marcador de posición de los ejemplos por la dirección URL del sitio de Project Web App (PWA) y el marcador de posición  `<site-url>`  `<guid>` por el UID del proyecto. 
  
En esta sección se describe cómo crear un flujo de trabajo que actualice de forma masiva campos personalizados para un proyecto. El flujo de trabajo sigue estos pasos de alto nivel:
  
- Espere a que el proyecto que desea actualizar se pueda comprobar
    
- Crear un conjunto de datos que defina todas las actualizaciones de campos personalizados para el proyecto
    
- Des check out the project
    
- Llamar **a UpdateCustomFields** para aplicar las actualizaciones de campos personalizados al proyecto 
    
- Registrar información relevante en la lista de historial de flujo de trabajo (si es necesario)
    
- Publicar el proyecto
    
- Comprobar el proyecto
    
El flujo de trabajo final de un extremo a otro tiene este aspecto:
  
![Flujo de trabajo de](media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "") un extremo a otro
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a>Para crear un flujo de trabajo que actualice de forma masiva campos personalizados

1. Opcional. Almacene la dirección URL completa del proyecto en una variable que puede usar en todo el flujo de trabajo.
    
    ![Almacenar la dirección URL del proyecto en una variable]Almacenar la dirección URL del proyecto en una(media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "variable")
  
2. Agregue la **acción Esperar evento de proyecto** al flujo de trabajo y elija el evento Cuando se comprueba **un** proyecto. 
    
    ![Esperar a que se desproteba el proyecto.](media/699aa9c7-b3c9-426e-a775-96993a13559c.png "Espere a que se desproteba el proyecto")
  
3. Crea un diccionario **requestHeader** mediante la **acción Crear diccionario.** Usará el mismo encabezado de solicitud para todas las llamadas de servicio web de este flujo de trabajo. 
    
    ![Crear el diccionario requestHeader](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Crear el diccionario requestHeader")
  
4. Agregue los dos elementos siguientes al diccionario.
    
    |Nombre|Tipo|Valor|
    |:-----|:-----|:-----|
    |Accept  <br/> |String  <br/> |application/json; odata=verbose  <br/> |
    |Content-Type  <br/> |Cadena  <br/> |application/json; odata=verbose  <br/> |
   
    ![Agregar un encabezado Accept agregando](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "un encabezado Accept")
  
5. Cree un diccionario **requestBody** mediante la **acción Generar diccionario.** Este diccionario almacena todas las actualizaciones de campo que desea aplicar. 
    
    Cada actualización de campo personalizado requiere cuatro filas: el tipo de metadatos del campo (1), la clave (2), el valor (3) y el tipo de valor (4).
    
    - **__metadata/tipo** El tipo de metadatos del campo. Este registro siempre es el mismo y usa los siguientes valores: 
    
       - Nombre: customFieldDictionary(i)/__metadata/type (donde **i** es el índice de cada campo personalizado del diccionario, empezando por 0) 
            
       - Tipo: String
            
       - Valor: SP. KeyValue
    
       ![Definición de una actualización de campos personalizados](media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "Definición de una actualización de campo personalizado")
  
    - **Clave** El nombre interno del campo personalizado, con el formato: *Custom_ce23fbf43fa0e411941000155d3c8201* 
    
       Puede encontrar el nombre interno de un campo personalizado navegando a su extremo **InternalName:**`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`
    
       Si creó los campos personalizados manualmente, los valores serán diferentes de un sitio a otro. Si planea volver a usar el flujo de trabajo en varios sitios, asegúrese de que los nombres de campo personalizados sean correctos.
    
    - **Valor** Valor que se asignará al campo personalizado. Para los campos personalizados vinculados a tablas de búsqueda, debe usar los nombres internos de las entradas de la tabla de búsqueda en lugar de los valores reales de la tabla de búsqueda. 
    
       Puede encontrar el nombre interno de la entrada de la tabla de búsqueda en el siguiente punto de conexión: `https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`
    
       Si tiene un campo personalizado de tabla de búsqueda configurado para aceptar varios valores, úselo para concatenar valores (como se muestra en el siguiente  `;#` diccionario de ejemplo). 
    
    - **ValueType** Tipo del campo personalizado que va a actualizar. 
    
       - Para los campos Texto, Duración, Marca y LookupTable, use Edm.String
    
       - Para los campos Number, use Edm.Int32, Edm.Double o cualquier otro tipo de número aceptado por OData
    
       - Para los campos Date, use Edm.DateTime
    
       El siguiente diccionario de ejemplo define las actualizaciones de tres campos personalizados. El primero es para un campo personalizado de tabla de búsqueda de varios valores, el segundo es para un campo numérico y el tercero para un campo de fecha. Ten en cuenta cómo se incrementa el índice **customFieldDictionary.** 
    
       > [!NOTE]
       > Estos valores son solo para fines ilustrativos. Los pares clave-valor que usará dependen de los datos de PWA. 
  
       |Nombre|Tipo|Valor|
       |:-----|:-----|:-----|
       |customFieldDictionary(0)/__metadata/type  <br/> |String  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary(0)/Key  <br/> |String  <br/> |\_Ce23fbf43fa0e411941000155d3c8201  <br/> |
       |customFieldDictionary(0)/Value  <br/> |String  <br/> |Entry \_ b9a2fd69279de411940f00155d3c8201;#Entry \_ baa2fd69279de411940f00155d3c8201  <br/> |
       |customFieldDictionary(0)/ValueType  <br/> |String  <br/> |Edm.String  <br/> |
       |customFieldDictionary(1)/__metadata/type  <br/> |String  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary(1)/Key  <br/> |String  <br/> |Custom_c7f114c97098e411940f00155d3c8201  <br/> |
       |customFieldDictionary(1)/Value  <br/> |String  <br/> |90.5  <br/> |
       |customFieldDictionary(1)/ValueType  <br/> |String  <br/> |Edm.Double  <br/> |
       |customFieldDictionary(2)/__metadata/type  <br/> |String  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary(2)/Key  <br/> |String  <br/> |Custom_c6fb67e0b9a1e411941000155d3c8201  <br/> |
       |customFieldDictionary(2)/Value  <br/> |String  <br/> |2015-04-01T00:00:00.0000000  <br/> |
       |customFieldDictionary(2)/ValueType  <br/> |String  <br/> |Edm.DateTime  <br/> |
   
       ![Diccionario que define las actualizaciones de campos personalizados](media/41a1f18f-a6b2-40ff-904b-437baf962621.png "Dictionary que define las actualizaciones de campos personalizados")
  
6. Agregue una **acción llamar al servicio web HTTP** para desalmar el proyecto. 
    
    ![Llamar al método Checkout Llamar]al método(media/8ce56014-0317-419b-afa7-229d05c86885.png "Checkout")
  
7. Edite las propiedades de la llamada al servicio web para especificar el encabezado de la solicitud. Para abrir el **cuadro de diálogo** Propiedades, haga clic con el botón secundario en la acción y elija **Propiedades**.
    
    ![Especificar el encabezado de solicitud en las propiedades de llamada de servicio web]Especifique el encabezado de solicitud en las propiedades de llamada de servicio(media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "web")
  
8. Agregue una **acción llamar al servicio web HTTP** para llamar al método **UpdateCustomFields.** 
    
    ![Crear una acción llamar al servicio web HTTP]Crear una acción llamar al servicio web(media/9a73a201-c035-41b4-8798-506ac48b90f8.png "HTTP")
  
    Observe el  `/Draft/` segmento en la dirección URL del servicio web. La dirección URL completa debe tener este aspecto: `https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
    
    ![Llamar al método UpdateCustomFields Llamar](media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "al método UpdateCustomFields")
  
9. Edite las propiedades de la llamada al servicio web para enlazar los parámetros **RequestHeader** y **RequestContent** a los diccionarios que creó. También puede crear una nueva variable para almacenar **responseContent**.
    
    ![Enlazar los diccionarios al encabezado]de solicitud y el contenido Enlazar los diccionarios al(media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "encabezado y al contenido de la solicitud")
  
10. Opcional. Lea desde el diccionario de respuestas para comprobar el estado del trabajo en cola y registrar la información en la lista de historial del flujo de trabajo.
    
    ![Configuración del registro Configuración](media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "del registro")
  
11. Agregue una llamada de servicio web al punto de conexión **de** publicación para publicar el proyecto. Use siempre el mismo encabezado de solicitud. 
    
    ![Llamar al método Publish Para]llamar al método(media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Publish")
  
    ![Propiedades de las propiedades de la llamada de servicio web publicar]para la llamada de servicio web de(media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "publicación")
  
12. Agregue una llamada de servicio web final al punto de conexión **de protección** para comprobar el proyecto. 
    
    ![Llamar al método Checkin Llamar](media/430510cb-0774-4911-af7f-b565b83eba0e.png "al método Checkin")
  
    ![Propiedades de las propiedades de la llamada del servicio web de checkin](media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "para la llamada del servicio web de checkin")

<a name="CreateProjectSite"> </a>

## <a name="create-a-project-site-from-a-workflow"></a>Crear un sitio de proyecto a partir de un flujo de trabajo

Cada proyecto puede tener sus propios sitios de SharePoint dedicados donde los miembros del equipo pueden colaborar, compartir documentos, plantear problemas, entre otros. Anteriormente, el jefe de proyecto de Project Professional o el administrador de la configuración de PWA solo podía crear automáticamente los sitios en la primera publicación o manualmente, o bien se podían deshabilitar.
  
Hemos agregado el método **CreateProjectSite** para que pueda elegir cuándo crear sitios de proyecto. Esto es especialmente útil para las organizaciones que desean crear sus sitios automáticamente cuando una propuesta de proyecto llega a una fase específica de un flujo de trabajo predefinido, en lugar de publicarse por primera vez. Posponing project site creation significantly improves the performance of creating a project. 
  
**Requisito previo:** Para poder usar **CreateProjectSite**, la opción Permitir a los usuarios elegir debe establecerse para la creación de sitios de proyecto en Configuración de  **PWA** > ** Sitios de SharePoint conectados ** > **Configuración**.
  
![Configuración "Permitir que los usuarios elijan" en la configuración de PWA]Permitir a los usuarios(media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "elegir en la configuración de PWA")
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a>Para crear un flujo de trabajo que cree un sitio de proyecto

1. Cree o edite un flujo de trabajo existente y seleccione el paso donde desea crear los sitios de Project.
    
2. Crea un diccionario **requestHeader** mediante la **acción Crear diccionario.** 
    
    ![Crear el diccionario requestHeader](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Crear el diccionario requestHeader")
  
3. Agregue los dos elementos siguientes al diccionario.
    
    |Nombre|Tipo|Valor|
    |:-----|:-----|:-----|
    |Accept  <br/> |String  <br/> |application/json; odata=verbose  <br/> |
    |Content-Type  <br/> |Cadena  <br/> |application/json; odata=verbose  <br/> |
   
    ![Agregar un encabezado Accept agregando](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "un encabezado Accept")
  
4. Agregue la acción **Llamar al servicio web HTTP.** Cambie el tipo de solicitud para que use **POST** y establezca la dirección URL con el siguiente formato:
    
    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`
    
    ![Creación del URI del extremo CreateProjectSite](media/42a90a5e-8d1b-4667-a933-785175212847.png "creando el URI del extremo CreateProjectSite")
  
    Pase el nombre del sitio de Project al **método CreateProjectSite** como una cadena. Para usar el nombre del proyecto como nombre del sitio, pase una cadena vacía. Asegúrese de usar nombres únicos para que funcione el siguiente sitio de proyecto que cree. 
    
5. Edite las propiedades de la llamada al servicio web para enlazar el **parámetro RequestHeader** con el diccionario que creó. 
    
    ![Enlazar el diccionario a la solicitud Enlazar]el diccionario a la(media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "solicitud")
  
## <a name="see-also"></a>Consulte también

- [Tareas de programación de Project](project-programming-tasks.md)
- [Modelo de objeto del cliente (CSOM) para Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Flujos de trabajo en SharePoint 2013](https://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
    

