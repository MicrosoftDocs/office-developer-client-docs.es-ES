---
title: Obtener acceso a campos personalizados de empresa de Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: 'Project Online es un servicio de Office 365 que las empresas pueden ampliar para satisfacer las necesidades empresariales. Un área de extensión es Campos personalizados de empresa (ECF). Los ECF son campos de valor de tipo que pueden agregarse a los proyectos, recursos y tareas. La siguiente tabla enumera ECF que se asocian con proyectos, recursos y tareas, y proporciona un ejemplo de un valor para una instancia de ese ECF:'
localization_priority: Priority
ms.openlocfilehash: 9f754f1446890ae021bf6f7000ffba11e2a2df33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355086"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a>Obtener acceso a campos personalizados de empresa de Project Online

Project Online es un servicio de Office 365 que las empresas pueden ampliar para satisfacer las necesidades empresariales. Un área de extensión es Campos personalizados de empresa (ECF). Los ECF son campos de valor de tipo que pueden agregarse a los proyectos, recursos y tareas. La siguiente tabla enumera ECF que se asocian con proyectos, recursos y tareas, y proporciona un ejemplo de un valor para una instancia de ese ECF:
  
|Nombre del ECF|Tipo de ECF|Asociación|Valor de ejemplo|
|:-----|:-----|:-----|:-----|
|Justificación  <br/> |TEXTO  <br/> |Proyecto  <br/> |Un usuario final puede registrar estadísticas vitales y datos de mantenimiento, con resultados que incluyan una evaluación de mantenimiento y un plan de acción individualizado para mejorar el mantenimiento.  <br/> |
|Clasificación de riesgos  <br/> |TEXTO  <br/> |Proyecto  <br/> |Bajo  <br/> |
|RENTABILIDAD DE LA INVERSIÓN  <br/> |NÚMERO  <br/> |Proyecto  <br/> |2.10  <br/> |
|Costo total  <br/> |COSTO  <br/> |Proyecto  <br/> |$1,031,514  <br/> |
|Equipo de lanzamiento  <br/> |TEXTO  <br/> |Recursos  <br/> |Sí  <br/> |
|Rol del puesto  <br/> |TEXTO  <br/> |Recursos  <br/> |Herramienta de comprobación  <br/> |
|Estado de marca  <br/> |MARCA  <br/> |Tarea  <br/> |No  <br/> |
|Mantenimiento  <br/> |TEXTO  <br/> |Tarea  <br/> |No especificado  <br/> |
   
Los ECF se definen en la instancia de Project Web Application (PWA), como ajenos a cualquier proyecto, recurso o tarea. Sin embargo, pueden asociarse con un proyecto, tarea o recurso. Este artículo proporciona una introducción a los campos personalizados usando una aplicación de ejemplo y se centra en cómo recuperar los valores de ECF. 
  
Puedes descargar el ejemplo completo en https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.
  
Además, Project Online es compatible con campos personalizados locales como entidades de solo lectura específicas del proyecto, el recurso o la tarea. Para obtener más información sobre los campos personalizados locales, consulta el ejemplo https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.
  
## <a name="background-materials"></a>Materiales del contexto

Un artículo anterior, [Desarrollo de una aplicación de Project Online con el modelo de objetos de cliente](developing-a-project-online-application-using-the-client-side-object-model.md), proporciona el contexto y la orientación inicial para desarrollar aplicaciones con CSOM. Consulta este artículo para los siguientes elementos:
  
- Información de contexto sobre Project, ediciones independientes y en la nube 
    
- Entorno de desarrollo (ediciones de Visual Studio y bibliotecas de software)
    
- Configuración de proyecto de Visual Studio para una aplicación de .NET con la biblioteca de CSOM
    
- Cómo conectarse al servicio de Project Online
    
## <a name="preliminaries-class-level-declarations"></a>Preliminares (declaraciones de clase)

La clase para esta aplicación define dos elementos de datos: el contexto del proyecto y el diccionario pwaECF.
  
El objeto de contexto del proyecto forma parte del CSOM de Project y conecta la aplicación y la instancia de PWA. Todas las solicitudes de servicio usan el contexto del proyecto.
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

El contexto necesita que el extremo de la conexión cree una instancia en una aplicación. El extremo de conexión es la dirección URL de tu instancia de PWA. 
  
El diccionario pwaECF almacena los ECF del proyecto definidos en el nivel de PWA. El diccionario usa ECF. InternalName como la clave y el objeto CustomField como el valor. El diccionario se completa en el método ListPWACustomFields y, a continuación, se usa como referencia del método Main. 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a>Método Main

El método Main administra el flujo de la aplicación. Como sucede con otras aplicaciones que utilizan el CSOM de Project Online, Main inicializa el contexto del proyecto. 
  
1. Recupera y enumera los ECF en la PWA de Project Online.
    
   Esta funcionalidad se implementa en el método ListPWACustomFields.
    
2. Recuperar proyectos con campos personalizados y campos no personalizados.
    
   Cuando se recuperan proyectos con los ECF, la solicitud de consulta al servicio de Project Online debe incluir los siguientes elementos: 
    
   - **IncludeCustomFields** &ndash;Este elemento solicita que el servicio devuelva una recopilación de PublishedProjects donde cada proyecto publicado incluye una extensión que admite campos personalizados. A menos que se especifique este elemento, Project Online devuelve objetos de PublishedProject que no incluyen datos de Campo personalizado.
    
   - **IncludeCustomFields.CustomFields** &ndash; Este elemento solicita al servicio rellenar los objetos de PublishedProject con datos de CustomFields.
    
   La solicitud siguiente especifica la Id. y el nombre de proyecto, así como la extensión del objeto de campos personalizados y los valores del campo personalizado.
    
   ```cs
        var projBlk = projContext.LoadQuery(
        projContext.Projects.Include(
            p => p.Id, 
            p => p.Name,
            p => p.IncludeCustomFields,
            p => p.IncludeCustomFields.CustomFields
        ));
    
   ```

3. Examina cada proyecto.
    
   Los objetos del proyecto utilizados en esta aplicación son del tipo PublishedProject porque se recuperan y se muestran los valores. 
    
   Si necesitas actualizar los valores de datos de uno o varios proyectos, el proyecto que se somete a la actualización se retira y la aplicación usa un objeto DraftProject para recuperar los valores y actualizar el proyecto.
    
4. Acceso a las entradas de ECF para un proyecto
    
   Cada instancia de ECF separa el valor del campo del resto de la información de ECF. El valor del campo se almacena como parte de un par clave/valor. El resto de la información se almacena en un objeto CustomField.
    
   La obtención de acceso a los valores de ECF consta de dos partes:
    
   - Movimiento cíclico a través de una recopilación de CustomFields
    
   - Acceso a la entrada correcta utilizando dos construcciones.
    
   Cada proyecto almacena entradas de ECF asociadas en dos lugares, una recopilación de CustomFields que se puede enumerar y valores de campo como parte de los pares clave/valor. En los pares clave/valor, internalName es la clave y el valor del campo es el valor. Utiliza un diccionario para mantener los valores de campo y acceder a ellos. 
    
   Las propiedades de ECF, a excepción de los valores de campo, se almacenan en objetos CustomField, a razón de un objeto por proyecto. Usa una recopilación de CustomFields para acceder a los ECF asociados a un proyecto individual. 
    
5. Cada proyecto almacena los ECF asociados en una recopilación en donde cada entrada de ECF se compone de una clave (el nombre interno del ECF) y un objeto que contiene el valor del ECF. Transferir la recopilación a un diccionario para tener acceso a las entradas individuales. Luego, sigue la declaración.
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   El valor de una entrada de diccionario corresponde al tipo de datos del ECF. El objeto para cada ECF se asigna a uno de los distintos tipos. La mayoría de los ECF usan tipos simples que se ajustan a variables estándar. El siguiente fragmento muestra que interviene un procesamiento mínimo para varios tipos:
    
   ```cs
    switch (cf.FieldType)
    {
        case CustomFieldType.COST:
            decimal costValue = (decimal)oVal;
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                costValue.ToString("C"));
            break;
        case CustomFieldType.DATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FINISHDATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.DURATION:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FLAG:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.NUMBER:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
    
   ```

   Sin embargo, la tabla de búsqueda de valores TEXT requiere un procesamiento adicional. La aplicación recupera la tabla de búsqueda adecuada del servicio y genera la instancia de ECF (con uno o varios valores), mediante un recorrido por la tabla de búsqueda. El siguiente fragmento de código muestra el procesamiento de ECF TEXT, incluidos aquellos con valores simples y aquellos que usan tablas de búsqueda: 
    
   ```cs
    case CustomFieldType.TEXT:
        if (!cf.LookupTable.ServerObjectIsNull.HasValue ||
            (cf.LookupTable.ServerObjectIsNull.HasValue && 
            cf.LookupTable.ServerObjectIsNull.Value))
        { //No lookup table
            Console.WriteLine("\tFieldType:\t{0}\n\tText:\t{1}", cf.FieldType, 
                oVal.ToString());
        }
        else
        { //Lookup table
            Console.WriteLine("\tFieldType:\t{0} - using Lookup Table", cf.FieldType);
            String[] entries = (String[])oVal;
            foreach (String entry in entries)
            {
                var luEntry = projContext.LoadQuery(cf.LookupTable.Entries
                    .Where(e => e.InternalName == entry));
                projContext.ExecuteQuery();
                Console.WriteLine("\tLookup Value:\t{0}", luEntry.First().FullValue);  
            }
        }
        break;
    
   ```

   Esta aplicación simplemente genera los valores; sin embargo, es posible obtener más significado de los valores de datos.
    
## <a name="listpwacustomfields"></a>ListPWACustomFields

El método ListPWACustomFields recupera y enumera los ECF asociados con los proyectos. Este método enumera los ECF registrados en la instancia de PWA que pueden asociarse con proyectos individuales. El punto de entrada para tener acceso a los ECF usa el elemento CustomFields del contexto del proyecto, como en la siguiente petición de consulta:
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

El método no comprueba si un proyecto utiliza un ECF específico.
  
## <a name="see-also"></a>Ver también

- [Portal de desarrollo del proyecto](https://developer.microsoft.com/es-ES/project)
- [Información general: campos personalizados de empresa y tablas de búsqueda](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)
- [Campos personalizados locales y de empresa](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)
- [Adición o modificación de campos personalizados de empresa en Project Server 2013](https://docs.microsoft.com/project/add-or-edit-enterprise-custom-fields-in-project-server)
    

