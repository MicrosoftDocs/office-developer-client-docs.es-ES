---
title: Actualizar campos personalizados de forma masiva y crear sitios de proyecto en Project Online
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: Para ayudar a los clientes a sacar el máximo partido de Project Online y mejorar nuestra extensibilidad y flexibilidad de servicio, hemos agregado dos métodos al modelo de objetos del lado cliente que puede usar en Project Online aplicaciones y flujos de trabajo.
ms.openlocfilehash: 4de42471cd8c2f12a982447ccffc27ec8104fa31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355443"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a>Actualización en masa de los campos personalizados y crear sitios de proyecto desde un flujo de trabajo en Project Online

Para ayudar a los clientes a sacar el máximo partido de Project Online y mejorar nuestra extensibilidad y flexibilidad de servicio, hemos agregado dos métodos al modelo de objetos del lado cliente que puede usar en Project Online aplicaciones y flujos de trabajo.
  
|||
|:-----|:-----|
|**UpdateCustomFields** <br/> |Actualizaciones masivas de campos personalizados del proyecto. Solo para Project Online. Disponible solo en la API de REST.  <br/> |
|**CreateProjectSite** <br/> | Crea un Project web. Solo para Project Online. Disponible en la API de REST, el modelo de objetos de cliente administrado y el modelo de objetos de cliente de JavaScript.  <br/> |
   
Además de proporcionar más flexibilidad, estos métodos también ofrecen mejoras significativas en el rendimiento al guardar y publicar proyectos en un flujo de trabajo. En este artículo se describe cómo usar los métodos de la API de REST y se proporcionan instrucciones para crear un flujo de trabajo que actualice de forma masiva campos personalizados y un flujo de trabajo que cree un Project sitio.
  
> [!NOTE]
> Para obtener más información sobre cómo llamar SharePoint API de REST desde flujos de trabajo de SharePoint 2013, vea Using [SharePoint REST services from workflow with POST method](https://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl) y Calling the SharePoint [2013 Rest API from a SharePoint Designer Workflow](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/). 
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a>Actualizar de forma masiva campos personalizados del proyecto desde un flujo de trabajo
<a name="BulkUpdateCustomFields"> </a>

Anteriormente, los flujos de trabajo solo podían actualizar un campo personalizado a la vez. La actualización de campos personalizados de proyecto de una en una puede provocar una mala experiencia del usuario final cuando los usuarios se transiciónn entre Project de detalles. Cada actualización requería una solicitud de servidor independiente mediante la acción Establecer campo **Project** y la actualización de varios campos personalizados en una red de alta latencia y ancho de banda bajo dio como resultado una sobrecarga no trivial. Para resolver este problema, agregamos el método **UpdateCustomFields** a la API de REST que le permite actualizar de forma masiva campos personalizados. Para usar **UpdateCustomFields,** se pasa un diccionario que contiene los nombres y valores de todos los campos personalizados que desea actualizar.
  
El método REST se puede encontrar en el siguiente punto de conexión:
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> Reemplace el marcador de posición de los ejemplos por la dirección URL del sitio de Project Web App (PWA) y el marcador de posición por `<site-url>` `<guid>` el UID del proyecto. 
  
En esta sección se describe cómo crear un flujo de trabajo que actualice de forma masiva campos personalizados para un proyecto. El flujo de trabajo sigue estos pasos de alto nivel:
  
- Espere a que el proyecto que desea actualizar para que se pueda comprobar
    
- Crear un conjunto de datos que defina todas las actualizaciones de campo personalizadas para el proyecto
    
- Consulte el proyecto
    
- Llamar **a UpdateCustomFields** para aplicar las actualizaciones de campo personalizadas al proyecto 
    
- Registrar información relevante en la lista de historial de flujos de trabajo (si es necesario)
    
- Publicar el proyecto
    
- Check in the project
    
El flujo de trabajo final de un extremo a otro tiene este aspecto:
  
![Flujo de trabajo de]extremo a(media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "extremo Flujo de") trabajo completo
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a>Para crear un flujo de trabajo que actualice de forma masiva campos personalizados

1. Opcional. Almacena la dirección URL completa del proyecto en una variable que puedes usar en todo el flujo de trabajo.
    
    ![Almacenar la dirección URL del proyecto en una variable]Almacenar la dirección URL del proyecto en una(media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "variable")
  
2. Agregue la **acción Esperar Project evento** al flujo de trabajo y elija el evento Cuando se comprueba **un** proyecto. 
    
    ![Esperar a que se desproteba el proyecto en](media/699aa9c7-b3c9-426e-a775-96993a13559c.png "Esperar a que se desproteba el proyecto")
  
3. Cree un **diccionario requestHeader** con la **acción Crear diccionario.** Usará el mismo encabezado de solicitud para todas las llamadas de servicio web de este flujo de trabajo. 
    
    ![Crear el diccionario requestHeader](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Generar el diccionario requestHeader")
  
4. Agregue los dos elementos siguientes al diccionario.
    
    |Nombre|Tipo|Valor|
    |:-----|:-----|:-----|
    |Accept  <br/> |Cadena  <br/> |application/json; odata=verbose  <br/> |
    |Content-Type  <br/> |Cadena  <br/> |application/json; odata=verbose  <br/> |
   
    ![Agregar un encabezado Accept Agregar]un encabezado(media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Accept")
  
5. Cree un **diccionario requestBody** con la **acción Crear diccionario.** Este diccionario almacena todas las actualizaciones de campo que desea aplicar. 
    
    Cada actualización de campo personalizado requiere cuatro filas: el tipo de metadatos (1) del campo, (2) clave, (3) valor y (4) tipo de valor.
    
    - **__metadata/tipo** Tipo de metadatos del campo. Este registro siempre es el mismo y usa los siguientes valores: 
    
       - Nombre: customFieldDictionary(i)/__metadata/type (donde **i** es el índice de cada campo personalizado del diccionario, empezando por 0) 
            
       - Tipo: String
            
       - Valor: SP. KeyValue
    
       ![Definición de una actualización de campo personalizada Definición](media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "de una actualización de campo personalizada")
  
    - **Clave** El nombre interno del campo personalizado, con el formato: *Custom_ce23fbf43fa0e411941000155d3c8201* 
    
       Para encontrar el nombre interno de un campo personalizado, vaya al punto de conexión **InternalName:**`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`
    
       Si creó los campos personalizados manualmente, los valores variarán de un sitio a otro. Si planea reutilizar el flujo de trabajo en varios sitios, asegúrese de que los nombres de campo personalizados son correctos.
    
    - **Valor** Valor que se debe asignar al campo personalizado. Para los campos personalizados que están vinculados a tablas de búsqueda, debe usar los nombres internos de las entradas de tabla de búsqueda en lugar de los valores reales de la tabla de búsqueda. 
    
       Puede encontrar el nombre interno de la entrada de la tabla de búsqueda en el siguiente punto de conexión: `https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`
    
       Si tiene un campo personalizado de tabla de búsqueda configurado para aceptar varios valores, use para concatenar valores (como se muestra en el siguiente  `;#` diccionario de ejemplo). 
    
    - **ValueType** El tipo del campo personalizado que va a actualizar. 
    
       - Para los campos Text, Duration, Flag y LookupTable, use Edm.String
    
       - Para los campos Number, use Edm.Int32, Edm.Double o cualquier otro tipo de número aceptado por OData
    
       - Para los campos Date, use Edm.DateTime
    
       El siguiente diccionario de ejemplo define las actualizaciones de tres campos personalizados. El primero es para un campo personalizado de tabla de búsqueda de varios valores, el segundo es para un campo de número y el tercero para un campo de fecha. Observe cómo aumenta el índice **customFieldDictionary.** 
    
       > [!NOTE]
       > Estos valores son solo para fines ilustrativos. Los pares clave-valor que usará dependen de los PWA datos. 
  
       |Nombre|Tipo|Valor|
       |:-----|:-----|:-----|
       |customFieldDictionary(0)/__metadata/type  <br/> |Cadena  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary(0)/Key  <br/> |Cadena  <br/> |\_Ce23fbff43fa0e411941000155d3c8201  <br/> |
       |customFieldDictionary(0)/Value  <br/> |Cadena  <br/> |Entrada \_ b9a2fd69279de411940f00155d3c8201;#Entry \_ baa2fd69279de411940f00155d3c8201  <br/> |
       |customFieldDictionary(0)/ValueType  <br/> |Cadena  <br/> |Edm.String  <br/> |
       |customFieldDictionary(1)/__metadata/type  <br/> |Cadena  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary(1)/Key  <br/> |Cadena  <br/> |Custom_c7f114c97098e411940f00155d3c8201  <br/> |
       |customFieldDictionary(1)/Value  <br/> |Cadena  <br/> |90.5  <br/> |
       |customFieldDictionary(1)/ValueType  <br/> |Cadena  <br/> |Edm.Double  <br/> |
       |customFieldDictionary(2)/__metadata/type  <br/> |Cadena  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary(2)/Key  <br/> |Cadena  <br/> |Custom_c6fb67e0b9a1e411941000155d3c8201  <br/> |
       |customFieldDictionary(2)/Value  <br/> |Cadena  <br/> |2015-04-01T00:00:00  <br/> |
       |customFieldDictionary(2)/ValueType  <br/> |Cadena  <br/> |Edm.DateTime  <br/> |
   
       ![Diccionario que define actualizaciones de campos personalizadas](media/41a1f18f-a6b2-40ff-904b-437baf962621.png "Diccionario que define actualizaciones de campos personalizadas")
  
6. Agregue una **acción Llamar al servicio web HTTP** para desasalmar el proyecto. 
    
    ![Llamar al método Checkout Llamar]al método(media/8ce56014-0317-419b-afa7-229d05c86885.png "Checkout")
  
7. Edite las propiedades de la llamada al servicio web para especificar el encabezado de solicitud. Para abrir el **cuadro de diálogo** Propiedades, haga clic con el botón secundario en la acción y elija **Propiedades**.
    
    ![Especificar el encabezado de solicitud en las propiedades de llamada de]servicio web Especifique el encabezado de solicitud en las propiedades de llamada de servicio(media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "web")
  
8. Agregue una **acción Llamar al servicio web HTTP** para llamar al método **UpdateCustomFields.** 
    
    ![Crear una acción Llamar al servicio web HTTP]Crear una acción Llamar al servicio web(media/9a73a201-c035-41b4-8798-506ac48b90f8.png "HTTP")
  
    Tenga en  `/Draft/` cuenta el segmento en la dirección URL del servicio web. La dirección URL completa debe tener este aspecto: `https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
    
    ![Llamar al método UpdateCustomFields](media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "Llamar al método UpdateCustomFields")
  
9. Edite las propiedades de la llamada al servicio web para enlazar los parámetros **RequestHeader** y **RequestContent** a los diccionarios que creó. También puede crear una nueva variable para almacenar **ResponseContent**.
    
    ![Enlazar los diccionarios al encabezado]de solicitud y el contenido Enlazar los(media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "diccionarios") al encabezado y el contenido de la solicitud
  
10. Opcional. Lea en el diccionario de respuesta para comprobar el estado del trabajo de cola y registrar la información en la lista de historial de flujos de trabajo.
    
    ![Configuración del registro](media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "Configuración del registro")
  
11. Agregue una llamada de servicio web al extremo **Publicar** para publicar el proyecto. Use siempre el mismo encabezado de solicitud. 
    
    ![Llamar al método Publish](media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Llamar al método Publish")
  
    ![Propiedades de la llamada publicar servicio web]Propiedades de la llamada de servicio web(media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "Publicar")
  
12. Agregue una llamada final de servicio web al extremo **Checkin** para comprobar el proyecto. 
    
    ![Llamar al método Checkin](media/430510cb-0774-4911-af7f-b565b83eba0e.png "Llamar al método Checkin")
  
    ![Propiedades de la llamada del servicio web Checkin]Propiedades de la llamada del(media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "servicio web Checkin")

<a name="CreateProjectSite"> </a>

## <a name="create-a-project-site-from-a-workflow"></a>Crear un sitio Project desde un flujo de trabajo

Cada proyecto puede tener sus propios sitios de SharePoint dedicados donde los miembros del equipo pueden colaborar, compartir documentos, generar problemas, entre otros. Anteriormente, los sitios solo podían crearse automáticamente en la primera publicación o manualmente por el jefe de proyecto en Project Profesional o por el administrador en la configuración de PWA, o podrían deshabilitarse.
  
Hemos agregado el método **CreateProjectSite** para que pueda elegir cuándo crear sitios de proyecto. Esto resulta especialmente útil para las organizaciones que desean crear sus sitios automáticamente cuando una propuesta de proyecto llega a una fase específica de un flujo de trabajo predefinido, en lugar de publicarse por primera vez. Posponer la creación de sitios de proyecto mejora significativamente el rendimiento de la creación de un proyecto. 
  
**Requisito previo:** Para poder usar **CreateProjectSite**, la opción Permitir que los usuarios elijan debe establecerse para la creación de sitios de proyecto en  **PWA Configuración** > ** Sitios SharePoint conectados ** > **Configuración**.
  
![Configuración "Permitir que los usuarios elijan"]en la configuración PWA configuración Permitir que los usuarios(media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "elijan en PWA configuración")
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a>Para crear un flujo de trabajo que cree un Project sitio

1. Cree o edite un flujo de trabajo existente y seleccione el paso en el que desea crear los Project web.
    
2. Cree un **diccionario requestHeader** con la **acción Crear diccionario.** 
    
    ![Crear el diccionario requestHeader](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Generar el diccionario requestHeader")
  
3. Agregue los dos elementos siguientes al diccionario.
    
    |Nombre|Tipo|Valor|
    |:-----|:-----|:-----|
    |Accept  <br/> |Cadena  <br/> |application/json; odata=verbose  <br/> |
    |Content-Type  <br/> |Cadena  <br/> |application/json; odata=verbose  <br/> |
   
    ![Agregar un encabezado Accept Agregar]un encabezado(media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Accept")
  
4. Agregue la **acción Llamar al servicio web HTTP.** Cambie el tipo de solicitud para que use **POST** y establezca la dirección URL con el siguiente formato:
    
    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`
    
    ![Creación del URI del extremo CreateProjectSite]Creación del URI del(media/42a90a5e-8d1b-4667-a933-785175212847.png "extremo CreateProjectSite")
  
    Pase el nombre del sitio Project al **método CreateProjectSite** como una cadena. Para usar el nombre del proyecto como nombre del sitio, pase una cadena vacía. Asegúrese de usar nombres únicos para que el siguiente sitio del proyecto que cree funcione. 
    
5. Edite las propiedades de la llamada al servicio web para enlazar el **parámetro RequestHeader** al diccionario que creó. 
    
    ![Enlace del diccionario a la solicitud Enlace]del diccionario a la(media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "solicitud")
  
## <a name="see-also"></a>Vea también

- [Tareas de programación de Project](project-programming-tasks.md)
- [Modelo de objeto del cliente (CSOM) para Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Flujos de trabajo en SharePoint 2013](https://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
    

