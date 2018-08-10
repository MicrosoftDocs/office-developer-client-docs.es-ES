---
title: Actualizar los campos personalizados de forma masiva y crear sitios de proyecto en Project Online
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: Para ayudar a los clientes obtener el máximo partido de Project Online y mejorar nuestros extensibilidad de servicio y flexibilidad, hemos agregado dos métodos para el modelo de objetos de cliente que pueden usar los flujos de trabajo y aplicaciones de Project Online.
ms.openlocfilehash: 4f8fee5de5efb69f410b78e9ce93b9dc9bb133f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821319"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a>Actualización en masa de los campos personalizados y crear sitios de proyecto desde un flujo de trabajo en Project Online

Para ayudar a los clientes obtener el máximo partido de Project Online y mejorar nuestros extensibilidad de servicio y flexibilidad, hemos agregado dos métodos para el modelo de objetos de cliente que pueden usar los flujos de trabajo y aplicaciones de Project Online.
  
|||
|:-----|:-----|
|**UpdateCustomFields** <br/> |Masiva actualiza los campos personalizados de proyecto. Para Project Online solo. Disponible sólo en la API de REST.  <br/> |
|**CreateProjectSite** <br/> | Crea un sitio de proyecto. Para Project Online solo. Está disponible en la API de REST, el modelo de objetos de cliente administrado y el modelo de objetos de cliente de JavaScript.  <br/> |
   
Además de proporcionar más flexibilidad, estos métodos también ofrecen importantes mejoras de rendimiento al guardar y publicar proyectos en un flujo de trabajo. En este artículo se describe cómo utilizar los métodos de la API de REST y proporciona instrucciones para crear un flujo de trabajo que los campos personalizados de forma masiva actualizaciones y un flujo de trabajo que se crea un sitio de proyecto.
  
> [!NOTE]
> Para obtener más información sobre cómo llamar a las API de REST de los flujos de trabajo de SharePoint 2013, vea [uso de REST de SharePoint services de flujo de trabajo con el método POST](http://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl) y [llamar a la API de Rest de SharePoint 2013 desde un flujo de trabajo de SharePoint Designer](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/). 
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a>Proyecto de campos personalizados de un flujo de trabajo para la actualización masiva
<a name="BulkUpdateCustomFields"> </a>

Anteriormente, los flujos de trabajo sólo podrían actualizar un campo personalizado a la vez. Actualización de los campos personalizados de proyecto uno a la vez, se puede producir una experiencia de usuario final deficiente cuando los usuarios realizar la transición entre páginas de detalles del proyecto. Cada actualización necesaria una solicitud de servidor independiente mediante la acción **Establecer campo de proyecto** y actualizar varios campos personalizados en una latencia alta, baja-ancho de banda de red como resultado de una sobrecarga no trivial. Para resolver este problema, hemos agregado el método **UpdateCustomFields** a la API de REST que permite que masiva de actualización de campos personalizados. Para usar **UpdateCustomFields**, pase en un diccionario que contiene los nombres y valores de todos los campos personalizados que desea actualizar.
  
El método REST puede encontrarse en el extremo siguiente:
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> Reemplace el `<site-url>` marcador de posición en los ejemplos con la dirección URL del sitio de Project Web App (PWA) y la `<guid>` marcador de posición con el UID del proyecto. 
  
En esta sección se describe cómo crear un flujo de trabajo que masiva actualiza los campos personalizados para un proyecto. El flujo de trabajo sigue estos pasos de alto nivel:
  
- Espere a que el proyecto que desea actualizar para obtener protegido
    
- Crear un conjunto de datos que define todas las actualizaciones de campo personalizado para el proyecto
    
- Desproteger el proyecto
    
- Llame a **UpdateCustomFields** para aplicar las actualizaciones de campo personalizado al proyecto 
    
- Registrar la información relevante a la lista de historial de flujo de trabajo (si es necesario)
    
- Publicar el proyecto
    
- Proteger el proyecto
    
El flujo de trabajo final, end-to-end tiene este aspecto:
  
![Flujo de trabajo de extremo a otro] (media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "Flujo de trabajo de extremo a otro")
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a>Para crear un flujo de trabajo que masiva actualiza los campos personalizados

1. Opcional. Almacene la dirección URL completa del proyecto en una variable que se puede usar en todo el flujo de trabajo.
    
    ![Almacén de la dirección URL del proyecto en una variable] (media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "Almacén de la dirección URL del proyecto en una variable")
  
2. Agregue la acción **esperar el evento de proyecto** al flujo de trabajo y elija el evento **cuando se protege un proyecto** . 
    
    ![Espere a que el proyecto para protegerse] (media/699aa9c7-b3c9-426e-a775-96993a13559c.png "Espere a que el proyecto para protegerse")
  
3. Crear un diccionario de **requestHeader** mediante la acción de **compilación de diccionario** . Debe usar el mismo encabezado de solicitud para todas las llamadas al servicio web en este flujo de trabajo. 
    
    ![Crear el diccionario requestHeader] (media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Crear el diccionario requestHeader")
  
4. Agregue los dos elementos siguientes para el diccionario.
    
    |Nombre|Tipo|Valor|
    |:-----|:-----|:-----|
    |Accept  <br/> |String  <br/> |Application/json; OData = verbose  <br/> |
    |Content-Type  <br/> |String  <br/> |Application/json; OData = verbose  <br/> |
   
    ![Adición de un encabezado Accept] (media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Adición de un encabezado Accept")
  
5. Crear un diccionario de **requestBody** mediante la acción de **compilación de diccionario** . Este diccionario almacena todas las actualizaciones de campo que se desean aplicar. 
    
    Cada actualización de campo personalizado requiere cuatro filas: el campo tipo de metadatos (1), (2) clave, valor (3) y tipo de valor (4).
    
    - **tipo/__metadata** El tipo del campo metadatos. Este registro siempre es el mismo y utiliza los siguientes valores: 
    
       - Nombre: customFieldDictionary (i) / __metadata/tipo (donde **i** es el índice de cada campo personalizado en el diccionario, comenzando por 0) 
            
       - Tipo: String
            
       - Valor: SP. KeyValue
    
       ![Definición de una actualización de campo personalizado] (media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "Definición de una actualización de campo personalizado")
  
    - **Clave** El nombre interno del campo personalizado, en el formato: *Custom_ce23fbf43fa0e411941000155d3c8201* 
    
       Puede encontrar el nombre interno de un campo personalizado navegando a su extremo **InternalName** :`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`
    
       Si creó manualmente los campos personalizados, los valores será diferente para cada sitio. Si piensa volver a usar el flujo de trabajo en varios sitios, asegúrese de que el campo personalizado identificadores son correctos.
    
    - **Valor** El valor para asignar el campo personalizado. Para los campos personalizados que están vinculados a las tablas de búsqueda, debe usar los nombres internos de las entradas de tabla de búsqueda en lugar de los valores de tabla de búsqueda real. 
    
       Puede encontrar el nombre interno de la entrada de la tabla de búsqueda en el extremo siguiente:`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`
    
       Si tiene un campo personalizado de tabla de búsqueda configurado para aceptar varios valores, use `;#` a concatene los valores (tal como se muestra en el diccionario de ejemplo que aparece a continuación). 
    
    - **Tipo de valor** El tipo del campo personalizado que se va a actualizar. 
    
       - Para los campos de texto, duración, marca y LookupTable, use Edm.String
    
       - Para campos numéricos, utilice Edm.Int32, Edm.Double o cualquier otro aceptado OData número tipo
    
       - Para los campos de fecha, use Edm.DateTime
    
       El diccionario de ejemplo siguiente define las actualizaciones para tres campos personalizados. La primera es para un campo personalizado de valor búsqueda tabla varios, la segunda es para un campo de número y la tercera es para un campo de fecha. Tenga en cuenta cómo los incrementos de índice **customFieldDictionary** . 
    
       > [!NOTE]
       > Estos valores son únicamente con fines de ilustración. Los pares de clave y valor que va a utilizar dependen de los datos de PWA. 
  
       |Nombre|Tipo|Valor|
       |:-----|:-----|:-----|
       |tipo/__metadata/customFieldDictionary (0)  <br/> |String  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary (0) / clave  <br/> |String  <br/> |Personalizar\_ce23fbf43fa0e411941000155d3c8201  <br/> |
       |customFieldDictionary (0) / valor  <br/> |String  <br/> |Entrada\_b9a2fd69279de411940f00155d3c8201; #Entry\_baa2fd69279de411940f00155d3c8201  <br/> |
       |customFieldDictionary (0) o tipo de valor  <br/> |String  <br/> |Edm.String  <br/> |
       |customFieldDictionary (1) / __metadata/tipo  <br/> |String  <br/> |SP. KeyValue  <br/> |
       |(1) o clave de customFieldDictionary  <br/> |String  <br/> |Custom_c7f114c97098e411940f00155d3c8201  <br/> |
       |customFieldDictionary (1) y valor  <br/> |String  <br/> |90.5  <br/> |
       |customFieldDictionary (1) o tipo de valor  <br/> |String  <br/> |Edm.Double  <br/> |
       |customFieldDictionary (2) / __metadata/tipo  <br/> |String  <br/> |SP. KeyValue  <br/> |
       |(2) o clave de customFieldDictionary  <br/> |String  <br/> |Custom_c6fb67e0b9a1e411941000155d3c8201  <br/> |
       |customFieldDictionary (2) y valor  <br/> |String  <br/> |2015-04-01T00:00:00.0000000  <br/> |
       |customFieldDictionary (2) o tipo de valor  <br/> |String  <br/> |Edm.DateTime  <br/> |
   
       ![Diccionario que define las actualizaciones de campo personalizado] (media/41a1f18f-a6b2-40ff-904b-437baf962621.png "Diccionario que define las actualizaciones de campo personalizado")
  
6. Agregar una acción de **Llamar al servicio Web de HTTP** para desproteger el proyecto. 
    
    ![Llame al método Checkout] (media/8ce56014-0317-419b-afa7-229d05c86885.png "Llame al método Checkout")
  
7. Editar las propiedades de la llamada al servicio web para especificar el encabezado de solicitud. Para abrir el cuadro de diálogo **Propiedades** , haga clic en la acción y elija **Propiedades**.
    
    ![Especificar el encabezado de solicitud de servicio web llame a las propiedades] (media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "Especificar el encabezado de solicitud de servicio web llame a las propiedades")
  
8. Agregar una acción de **Servicio Web HTTP de llamada** para llamar al método **UpdateCustomFields** . 
    
    ![Crear una acción llamar al servicio Web de HTTP] (media/9a73a201-c035-41b4-8798-506ac48b90f8.png "Crear una acción llamar al servicio Web de HTTP")
  
    Tenga en cuenta el `/Draft/` segmento en la dirección URL del servicio web. La dirección URL completa debe tener este aspecto:`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
    
    ![Llame al método UpdateCustomFields] (media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "Llame al método UpdateCustomFields")
  
9. Editar las propiedades de la llamada al servicio web para enlazar los parámetros **RequestHeader** y **RequestContent** a los diccionarios que creó. También puede crear una nueva variable para almacenar el **ResponseContent**.
    
    ![Enlazar los diccionarios en el encabezado de la solicitud y contenido] (media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "Enlazar los diccionarios en el encabezado de la solicitud y contenido")
  
10. Opcional. Leer desde el diccionario de respuesta para comprobar el estado de los trabajos en cola y la información de registro en la lista de historial de flujo de trabajo.
    
    ![Configuración del registro] (media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "Configuración del registro")
  
11. Agregue una llamada al servicio web al extremo de **Publicar** para publicar el proyecto. Use siempre el mismo encabezado de solicitud. 
    
    ![Llame al método de publicación] (media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Llame al método de publicación")
  
    ![Llamar las propiedades para el servicio web de publicación] (media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "Llamar las propiedades para el servicio web de publicación")
  
12. Agregue una llamada al servicio web final al extremo de **Checkin** para proteger el proyecto. 
    
    ![Llame al método Checkin] (media/430510cb-0774-4911-af7f-b565b83eba0e.png "Llame al método Checkin")
  
    ![Llamar las propiedades para el servicio web de Checkin] (media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "Llamar las propiedades para el servicio web de Checkin")

<a name="CreateProjectSite"> </a>

## <a name="create-a-project-site-from-a-workflow"></a>Crear un sitio de proyecto desde un flujo de trabajo

Cada proyecto puede tener sus propio dedicados sitios de SharePoint donde los miembros del equipo pueden colaborar, compartir documentos, provocar problemas y así sucesivamente. Anteriormente, podrían sólo se crean los sitios automáticamente en primer lugar publicar o manualmente por el jefe de proyecto en Project Professional o por el administrador en PWA configuración o se ha podrían deshabilitar.
  
Hemos agregado el método **CreateProjectSite** para que pueda elegir cuándo se debe crear sitios de proyecto. Esto es especialmente útil para las organizaciones que desean crear sus sitios de forma automática cuando una propuesta de proyecto alcanza una fase determinada en un flujo de trabajo predefinido, en lugar de en primer lugar publicación. Posponer la creación de sitios de proyecto significativamente mejora el rendimiento de la creación de un proyecto. 
  
**Necesario como requisito previo:** Antes de poder usar **CreateProjectSite**, se debe establecer la opción de **Permitir a los usuarios elegir** para la creación de sitios de proyecto en **PWA configuración** > ** sitios de SharePoint conectados ** > **configuración**.
  
![Configuración "Permitir a los usuarios elegir" en configuración de PWA] (media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "Configuración de permitir a los usuarios elegir en configuración de PWA")
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a>Para crear un flujo de trabajo que se crea un sitio de proyecto

1. Crear o editar un flujo de trabajo existente y seleccione el paso donde desea crear los sitios del proyecto.
    
2. Crear un diccionario de **requestHeader** mediante la acción de **compilación de diccionario** . 
    
    ![Crear el diccionario requestHeader] (media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Crear el diccionario requestHeader")
  
3. Agregue los dos elementos siguientes para el diccionario.
    
    |Nombre|Tipo|Valor|
    |:-----|:-----|:-----|
    |Accept  <br/> |String  <br/> |Application/json; OData = verbose  <br/> |
    |Content-Type  <br/> |String  <br/> |Application/json; OData = verbose  <br/> |
   
    ![Adición de un encabezado Accept] (media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Adición de un encabezado Accept")
  
4. Agregar la acción de **Llamar al servicio Web de HTTP** . Cambie el tipo de solicitud para usar **POST**y establecer la dirección URL con el siguiente formato:
    
    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`
    
    ![Crear el URI del extremo de CreateProjectSite] (media/42a90a5e-8d1b-4667-a933-785175212847.png "Crear el URI del extremo de CreateProjectSite")
  
    Pase el nombre del sitio del proyecto para el método **CreateProjectSite** como una cadena. Para usar el nombre del proyecto como el nombre del sitio, pase una cadena vacía. Asegúrese de utilizar nombres únicos, por lo que funcionará el siguiente sitio de proyecto que cree. 
    
5. Editar las propiedades de la llamada al servicio web a la que enlazar el parámetro **RequestHeader** el diccionario que creó. 
    
    ![El diccionario a la solicitud de enlace] (media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "El diccionario a la solicitud de enlace")
  
## <a name="see-also"></a>Vea también

- [Tareas de programación de Project](project-programming-tasks.md)
- [Modelo de objetos de cliente (COM) de Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Flujos de trabajo en SharePoint 2013](http://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
    

