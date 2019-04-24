---
title: Actualizar masivamente campos personalizados y crear sitios de proyectos en Project online
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: Para ayudar a los clientes a sacar el máximo partido de Project online y mejorar nuestra extensibilidad y flexibilidad del servicio, hemos agregado dos métodos para el modelo de objetos del lado cliente que puede usar en las aplicaciones y los flujos de trabajo de Project online.
ms.openlocfilehash: 4de42471cd8c2f12a982447ccffc27ec8104fa31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355443"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a>Actualización en masa de los campos personalizados y crear sitios de proyecto desde un flujo de trabajo en Project Online

Para ayudar a los clientes a sacar el máximo partido de Project online y mejorar nuestra extensibilidad y flexibilidad del servicio, hemos agregado dos métodos para el modelo de objetos del lado cliente que puede usar en las aplicaciones y los flujos de trabajo de Project online.
  
|||
|:-----|:-----|
|**UpdateCustomFields** <br/> |Actualizaciones masivas campos personalizados de Project. Solo para Project online. Disponible solo en la API de REST.  <br/> |
|**CreateProjectSite** <br/> | Crea un sitio de proyecto. Solo para Project online. Disponible en la API de REST, el modelo de objetos de cliente administrado y el modelo de objetos de cliente de JavaScript.  <br/> |
   
Además de proporcionar más flexibilidad, estos métodos también ofrecen mejoras de rendimiento significativas al guardar y publicar proyectos en un flujo de trabajo. En este artículo se describe cómo usar los métodos en la API de REST y se proporcionan instrucciones para crear un flujo de trabajo que actualiza masivamente campos personalizados y un flujo de trabajo que crea un sitio de proyecto.
  
> [!NOTE]
> Para obtener más información sobre cómo llamar a las API de REST desde flujos de trabajo de SharePoint 2013, vea [usar los servicios REST de SharePoint desde el flujo de trabajo con el método post](https://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl) y [llamar a SharePoint 2013 Rest API desde un flujo de trabajo de SharePoint Designer](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/). 
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a>Actualización masiva de campos personalizados de Project desde un flujo de trabajo
<a name="BulkUpdateCustomFields"> </a>

Anteriormente, los flujos de trabajo solo podían actualizar un campo personalizado a la vez. La actualización de los campos personalizados de Project a la vez puede dar lugar a una experiencia deficiente para el usuario final cuando los usuarios pasan de una página de detalles del proyecto. Cada actualización requería una solicitud de servidor independiente mediante la acción **establecer el campo de proyecto** , y la actualización de varios campos personalizados en una red de ancho de banda bajo y de alta latencia dio como resultado una sobrecarga no trivial. Para resolver este problema, agregamos el método **UpdateCustomFields** a la API de REST que permite actualizar masivamente campos personalizados. Para usar **UpdateCustomFields**, debe pasar un diccionario que contenga los nombres y valores de todos los campos personalizados que desee actualizar.
  
El método REST se puede encontrar en el siguiente punto de conexión:
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> Reemplace el `<site-url>` marcador de posición de los ejemplos por la dirección URL del sitio de Project Web App (PWA `<guid>` ) y el marcador de posición con el UID del proyecto. 
  
En esta sección se describe cómo crear un flujo de trabajo que actualiza masivamente campos personalizados para un proyecto. El flujo de trabajo sigue estos pasos de alto nivel:
  
- Esperar a que se proteja el proyecto en el que desea realizar la actualización
    
- ComPilar un conjunto de datos que define todas las actualizaciones de campos personalizados para el proyecto
    
- DesProteger el proyecto
    
- Llamar a **UpdateCustomFields** para aplicar las actualizaciones de campos personalizados al proyecto 
    
- Registrar información relevante en la lista de historial del flujo de trabajo (si es necesario)
    
- Publicar el proyecto
    
- Proteger el proyecto
    
El último flujo de trabajo de un extremo a otro tiene el siguiente aspecto:
  
![Flujo de trabajo de un extremo a otro] (media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "Flujo de trabajo de un extremo a otro")
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a>Para crear un flujo de trabajo que actualice masivamente campos personalizados

1. Opcional. Almacene la dirección URL completa del proyecto en una variable que puede usar en todo el flujo de trabajo.
    
    ![Almacenar la dirección URL del proyecto en una variable] (media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "Almacenar la dirección URL del proyecto en una variable")
  
2. Agregue la acción **esperar el evento del proyecto** al flujo de trabajo y elija el evento **cuando un proyecto se proteja** . 
    
    ![Esperar a que se proteja el proyecto] (media/699aa9c7-b3c9-426e-a775-96993a13559c.png "Esperar a que se proteja el proyecto")
  
3. Cree un diccionario de **requestHeader** con la acción de **crear un diccionario** . Usará el mismo encabezado de solicitud para todas las llamadas de servicio Web de este flujo de trabajo. 
    
    ![Crear el Diccionario requestHeader] (media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Crear el Diccionario requestHeader")
  
4. Agregue los dos elementos siguientes al diccionario.
    
    |Nombre|Tipo|Valor|
    |:-----|:-----|:-----|
    |Accept  <br/> |String  <br/> |Application/JSON; OData = verbose  <br/> |
    |Content-Type  <br/> |String  <br/> |Application/JSON; OData = verbose  <br/> |
   
    ![Adición de un encabezado de aceptación] (media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Adición de un encabezado de aceptación")
  
5. Cree un diccionario de **requestBody** con la acción de **crear un diccionario** . Este diccionario almacena todas las actualizaciones de campos que desea aplicar. 
    
    Cada actualización del campo personalizado requiere cuatro filas: el tipo de metadatos del campo (1), (2) clave, (3) valor y (4) tipo de valor.
    
    - **__metadata/tipo** Tipo de metadatos del campo. Este registro es siempre el mismo y usa los siguientes valores: 
    
       - Nombre: customFieldDictionary (i)/__metadata/Type (donde **i** es el índice de cada campo personalizado en el diccionario, comenzando por 0) 
            
       - Tipo: String
            
       - Valor: SP. Clavevalor
    
       ![Definición de una actualización de campo personalizado] (media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "Definición de una actualización de campo personalizado")
  
    - **Clave** Nombre interno del campo personalizado, con el formato: *Custom_ce23fbf43fa0e411941000155d3c8201* 
    
       Puede encontrar el nombre interno de un campo personalizado desplazándose hasta su punto de conexión de **InternalName** :`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`
    
       Si ha creado los campos personalizados manualmente, los valores serán diferentes de un sitio a un sitio. Si planea volver a usar el flujo de trabajo en varios sitios, asegúrese de que los identificadores de campo personalizados sean correctos.
    
    - **Valor** de Valor que se va a asignar al campo personalizado. En el caso de los campos personalizados que están vinculados a tablas de consulta, debe usar los nombres internos de las entradas de la tabla de búsqueda en lugar de los valores reales de la tabla de búsqueda. 
    
       Puede encontrar el nombre interno de la entrada de la tabla de búsqueda en el siguiente punto de conexión:`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`
    
       Si tiene configurado un campo personalizado de tabla de búsqueda para que acepte varios valores, `;#` use para concatenar valores (como se muestra en el siguiente Diccionario de ejemplo). 
    
    - **ValueType** El tipo de campo personalizado que se va a actualizar. 
    
       - Para los campos Text, Duration, Flag y LookupTable, use EDM. String.
    
       - Para los campos numéricos, use EDM. Int32, EDM. Double o cualquier otro tipo de número aceptado por OData.
    
       - Para los campos de fecha, use EDM. DateTime
    
       El Diccionario de ejemplo que se muestra a continuación define actualizaciones para tres campos personalizados. La primera es para un campo personalizado de tabla de búsqueda de varios valores, la segunda es para un campo de número y la tercera es para un campo de fecha. Tenga en cuenta cómo se incrementa el índice de **customFieldDictionary** . 
    
       > [!NOTE]
       > Estos valores solo tienen fines ilustrativos. Los pares clave-valor que se usarán dependen de los datos de PWA. 
  
       |Nombre|Tipo|Valor|
       |:-----|:-----|:-----|
       |customFieldDictionary (0)/__metadata/Type  <br/> |String  <br/> |Pack. Clavevalor  <br/> |
       |customFieldDictionary (0)/Key  <br/> |String  <br/> |Ce23fbf43fa0e411941000155d3c8201\_personalizado  <br/> |
       |customFieldDictionary (0)/Value  <br/> |String  <br/> |Entrada\_b9a2fd69279de411940f00155d3c8201; #Entry\_baa2fd69279de411940f00155d3c8201  <br/> |
       |customFieldDictionary (0)/ValueType  <br/> |String  <br/> |Edm.String  <br/> |
       |customFieldDictionary (1)/__metadata/Type  <br/> |String  <br/> |Pack. Clavevalor  <br/> |
       |customFieldDictionary (1)/Key  <br/> |String  <br/> |Custom_c7f114c97098e411940f00155d3c8201  <br/> |
       |customFieldDictionary (1)/Value  <br/> |String  <br/> |90,5  <br/> |
       |customFieldDictionary (1)/ValueType  <br/> |String  <br/> |Edm.Double  <br/> |
       |customFieldDictionary (2)/__metadata/Type  <br/> |String  <br/> |Pack. Clavevalor  <br/> |
       |customFieldDictionary (2)/Key  <br/> |String  <br/> |Custom_c6fb67e0b9a1e411941000155d3c8201  <br/> |
       |customFieldDictionary (2)/Value  <br/> |String  <br/> |2015-04-01T00:00:00.0000000  <br/> |
       |customFieldDictionary (2)/ValueType  <br/> |String  <br/> |Edm.DateTime  <br/> |
   
       ![Diccionario que define actualizaciones de campos personalizados] (media/41a1f18f-a6b2-40ff-904b-437baf962621.png "Diccionario que define actualizaciones de campos personalizados")
  
6. Agregue una acción de **servicio Web http de llamada** para desproteger el proyecto. 
    
    ![Llamar al método Checkout] (media/8ce56014-0317-419b-afa7-229d05c86885.png "Llamar al método Checkout")
  
7. Edite las propiedades de la llamada al servicio web para especificar el encabezado de la solicitud. Para abrir el cuadro de diálogo **propiedades** , haga clic con el botón secundario en la acción y elija **propiedades**.
    
    ![Especificar el encabezado de la solicitud en las propiedades de llamada de servicio Web] (media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "Especificar el encabezado de la solicitud en las propiedades de llamada de servicio Web")
  
8. Agregue una acción **llamar al servicio Web http** para llamar al método **UpdateCustomFields** . 
    
    ![Crear una acción llamar al servicio Web http] (media/9a73a201-c035-41b4-8798-506ac48b90f8.png "Crear una acción llamar al servicio Web http")
  
    Anote el `/Draft/` segmento de la dirección URL del servicio Web. La dirección URL completa debe tener un aspecto similar a este:`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
    
    ![Llamar al método UpdateCustomFields] (media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "Llamar al método UpdateCustomFields")
  
9. Edite las propiedades de la llamada de servicio web para enlazar los parámetros **RequestHeader** y **RequestContent** a los diccionarios que ha creado. También puede crear una nueva variable para almacenar la **ResponseContent**.
    
    ![Enlazar los diccionarios al encabezado y al contenido de la solicitud] (media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "Enlazar los diccionarios al encabezado y al contenido de la solicitud")
  
10. Opcional. Leer en el Diccionario de respuesta para comprobar el estado del trabajo en cola y registrar la información en la lista de historial de flujo de trabajo.
    
    ![Configuración del registro] (media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "Configuración del registro")
  
11. Agregue una llamada de servicio Web al punto de conexión de **publicación** para publicar el proyecto. Use siempre el mismo encabezado de solicitud. 
    
    ![Llamar al método Publish] (media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Llamar al método Publish")
  
    ![Propiedades de la llamada al servicio Web de publicación] (media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "Propiedades de la llamada al servicio Web de publicación")
  
12. Agregue una llamada de servicio Web final al extremo de **protección** para proteger el proyecto en. 
    
    ![Llamar al método checkin] (media/430510cb-0774-4911-af7f-b565b83eba0e.png "Llamar al método checkin")
  
    ![Propiedades de la llamada al servicio Web checkin] (media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "Propiedades de la llamada al servicio Web checkin")

<a name="CreateProjectSite"> </a>

## <a name="create-a-project-site-from-a-workflow"></a>Crear un sitio de proyecto desde un flujo de trabajo

Cada proyecto puede tener sus propios sitios de SharePoint dedicados donde los miembros del equipo pueden colaborar, compartir documentos, generar problemas, etc. Anteriormente, los sitios solo podían crearse automáticamente en la primera publicación o manualmente por el jefe de proyecto en Project Professional o por el administrador en la configuración de PWA, o podrían deshabilitarse.
  
Hemos agregado el método **CreateProjectSite** para que pueda elegir cuándo crear sitios de proyecto. Esto es especialmente útil para las organizaciones que quieren crear sus sitios automáticamente cuando una propuesta de proyecto alcanza una etapa específica en un flujo de trabajo predefinido, en lugar de en la primera publicación. PosPoner la creación del sitio de proyecto mejora significativamente el rendimiento de la creación de un proyecto. 
  
**Requisitos previos:** Antes de poder usar **CreateProjectSite**, la opción **permitir que los usuarios elijan** para la creación de sitios de proyecto en la configuración de **PWA** _GT_ * * Connected SharePoint sites * * > **Settings**.
  
![Configuración de "permitir que los usuarios elijan" en la configuración de PWA] (media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "Configuración permitir que los usuarios elijan en la configuración de PWA")
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a>Para crear un flujo de trabajo que cree un sitio de proyecto

1. Cree o edite un flujo de trabajo existente y seleccione el paso en el que desea crear los sitios del proyecto.
    
2. Cree un diccionario de **requestHeader** con la acción de **crear un diccionario** . 
    
    ![Crear el Diccionario requestHeader] (media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Crear el Diccionario requestHeader")
  
3. Agregue los dos elementos siguientes al diccionario.
    
    |Nombre|Tipo|Valor|
    |:-----|:-----|:-----|
    |Accept  <br/> |String  <br/> |Application/JSON; OData = verbose  <br/> |
    |Content-Type  <br/> |String  <br/> |Application/JSON; OData = verbose  <br/> |
   
    ![Adición de un encabezado de aceptación] (media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Adición de un encabezado de aceptación")
  
4. Agregue la acción **llamar al servicio Web http** . Cambie el tipo de solicitud para que use **post**y establezca la dirección URL con el siguiente formato:
    
    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`
    
    ![Crear el URI del extremo de CreateProjectSite] (media/42a90a5e-8d1b-4667-a933-785175212847.png "Crear el URI del extremo de CreateProjectSite")
  
    Pase el nombre del sitio de proyecto al método **CreateProjectSite** como una cadena. Para usar el nombre del proyecto como nombre del sitio, pase una cadena vacía. Asegúrese de usar nombres únicos para que funcione el siguiente sitio de proyecto que cree. 
    
5. Edite las propiedades de la llamada de servicio web para enlazar el parámetro **RequestHeader** al diccionario que ha creado. 
    
    ![Enlazar el diccionario a la solicitud] (media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "Enlazar el diccionario a la solicitud")
  
## <a name="see-also"></a>Vea también

- [Tareas de programación de Project](project-programming-tasks.md)
- [Modelo de objeto del cliente (CSOM) para Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Flujos de trabajo en SharePoint 2013](https://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
    

