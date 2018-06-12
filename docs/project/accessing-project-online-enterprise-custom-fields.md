---
title: Obtener acceso a Project Online campos personalizados de empresa
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: 'Project Online es un servicio de Office 365 que las empresas pueden ampliar para satisfacer las necesidades empresariales. Un área de extensión es campos personalizados de empresa (ECFs). ECFs son campos de valor de tipo que se pueden agregar a proyectos, recursos y tareas. En la siguiente tabla se enumera ECFs que asocian con proyectos, recursos y tareas y proporciona un ejemplo de un valor de una instancia de ese ECF:'
ms.openlocfilehash: d6c8f97ffc887b33e5d81af8e463cf10502845dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821306"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a>Obtener acceso a Project Online campos personalizados de empresa

Project Online es un servicio de Office 365 que las empresas pueden ampliar para satisfacer las necesidades empresariales. Un área de extensión es campos personalizados de empresa (ECFs). ECFs son campos de valor de tipo que se pueden agregar a proyectos, recursos y tareas. En la siguiente tabla se enumera ECFs que asocian con proyectos, recursos y tareas y proporciona un ejemplo de un valor de una instancia de ese ECF:
  
|Nombre ECF|Tipo ECF|Asociación|Valor de ejemplo|
|:-----|:-----|:-----|:-----|
|Justificación  <br/> |TEXT  <br/> |Project  <br/> |Un usuario final puede registrar estadísticas vitales y datos de mantenimiento, con los resultados que incluyen una evaluación de mantenimiento y una acción individual plan hacia la salud mejor.  <br/> |
|Clasificación de riesgos  <br/> |TEXT  <br/> |Project  <br/> |Low  <br/> |
|RENDIMIENTO DE LA INVERSIÓN  <br/> |NÚMERO  <br/> |Project  <br/> |2,10  <br/> |
|Costo total  <br/> |COSTO  <br/> |Project  <br/> |$1,031,514  <br/> |
|Inicio del equipo  <br/> |TEXT  <br/> |Recursos  <br/> |Sí  <br/> |
|Rol de posición  <br/> |TEXT  <br/> |Recursos  <br/> |Evaluador  <br/> |
|Estado de marca  <br/> |MARCA  <br/> |Tarea  <br/> |No  <br/> |
|Mantenimiento  <br/> |TEXT  <br/> |Tarea  <br/> |No se ha especificado  <br/> |
   
ECFs se definen en la instancia de Project Web Application (PWA), externa desde cualquier proyecto, recurso o tarea. Sin embargo, pueden resultar asociados a un proyecto, recurso o tarea. En este artículo se proporciona una introducción a los campos personalizados con una aplicación de ejemplo y se centra en la recuperación de valores de ECF. 
  
Puede descargar el ejemplo completo en https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.
  
Además, Project Online admite los campos personalizados locales como de sólo lectura entidades específicas para el proyecto específico, recurso o tarea. Para obtener más información en los campos personalizados locales, vea el ejemplo https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.
  
## <a name="background-materials"></a>Material de fondo

Un artículo anterior, [desarrollar una aplicación de Project Online mediante el modelo de objetos de cliente](developing-a-project-online-application-using-the-client-side-object-model.md), proporciona información y la orientación inicial para el desarrollo de aplicaciones con CSOM. Consulte este artículo para los siguientes elementos:
  
- Información general acerca de Project, ediciones independientes y basada en la nube 
    
- Entorno de desarrollo (ediciones de Visual Studio y bibliotecas de software)
    
- Instalación de proyecto de Visual Studio para una aplicación de .NET mediante la biblioteca de CSOM
    
- Conectar con el servicio de Project Online
    
## <a name="preliminaries-class-level-declarations"></a>Preliminar (declaraciones de nivel de clase)

La clase para esta aplicación define dos elementos de datos: el contexto del proyecto y el diccionario pwaECF.
  
El objeto de contexto de proyecto es parte del proyecto CSOM y conecta a la aplicación y la instancia de PWA. Todas las solicitudes al servicio de utilizan el contexto del proyecto.
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

El contexto necesita que el extremo de conexión para crear una instancia de una aplicación. El extremo de la conexión es la dirección URL de la instancia de PWA. 
  
El diccionario pwaECF almacena el proyecto ECFs definidos en el nivel de PWA. El diccionario usa la ECF. InternalName como la clave y el objeto CustomField como el valor. El diccionario se rellenó en el método ListPWACustomFields y, a continuación, se utiliza como referencia en el método Main. 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a>Principal (método)

El método Main administra el flujo de la aplicación. Como con otras aplicaciones que usan el CSOM de Project Online, Main inicializa el contexto del proyecto. 
  
1. Recuperar y la ECFs en el Project Online PWA de la lista.
    
   Esta funcionalidad se implementa en el método ListPWACustomFields.
    
2. Recuperar proyectos con campos personalizados y campos no personalizados.
    
   Al recuperar proyectos con ECFs, las necesidades de la solicitud de consulta al servicio de Project Online incluir los siguientes elementos: 
    
   - **IncludeCustomFields** &ndash; Este elemento solicita el servicio para devolver una colección de PublishedProjects donde cada proyecto publicado incluye una extensión que es compatible con los campos personalizados. A menos que se especifica este elemento, Project Online devuelve objetos PublishedProject que no incluyen datos de campo personalizado.
    
   - **IncludeCustomFields.CustomFields** &ndash; este elemento solicita el servicio para rellenar los objetos PublishedProject con datos de CustomFields.
    
   La siguiente solicitud especifica el identificador de proyecto y nombre, así como la extensión del objeto de campos personalizados y los valores de campo personalizado.
    
   ```cs
        var projBlk = projContext.LoadQuery(
        projContext.Projects.Include(
            p => p.Id, 
            p => p.Name,
            p => p.IncludeCustomFields,
            p => p.IncludeCustomFields.CustomFields
        ));
    
   ```

3. Se examinan en cada proyecto.
    
   Los objetos de proyecto utilizados en esta aplicación son el tipo de PublishedProject debido a que los valores se recuperan y se muestran. 
    
   Si necesita actualizar los valores de datos en uno o más proyectos, ¿puede desproteger el proyecto llevando a cabo la actualización y la aplicación usaría un objeto DraftProject para recuperar los valores y actualizar el proyecto.
    
4. Obtener acceso a las entradas de ECF para un proyecto
    
   Cada instancia ECF separa el valor del campo del resto de la información de ECF. El valor del campo se almacena como parte de un par de clave y valor. El resto de la información se almacena en un objeto CustomField.
    
   Obtener acceso a los valores ECF en un proyecto consta de dos partes:
    
   - Recorrer en iteración la colección de CustomFields
    
   - Obtener acceso a la entrada correcta mediante dos construcciones.
    
   Cada proyecto almacena entradas ECF asociadas en dos lugares, una colección de CustomFields es enumerable y y los valores de campo como parte de pares clave/valor. En los pares clave/valor, el valor de internalName es la clave y el valor del campo es el valor. Utilizar un diccionario para mantener y obtener acceso a los valores de campo. 
    
   Las propiedades ECF, que no sean los valores de campo, se almacenan en objetos CustomField, un objeto por proyecto. Usar una colección CustomFields para tener acceso a la ECFs asociados con un proyecto individual. 
    
5. Cada proyecto almacena el ECFs asociados en una colección donde cada entrada ECF consta de una clave--el nombre interno de la ECF--y un objeto que contiene el valor de la ECF. Transferir un diccionario para tener acceso a las entradas individuales a la colección. Sigue la declaración.
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   El valor de una entrada de diccionario corresponde al tipo de datos de la ECF. El objeto para cada ECF se asigna a uno de los diversos tipos. ECFs mayoría usan tipos simples que se ajustan a las variables estándares. El siguiente fragmento muestra que está implicado un procesamiento mínimo para varios tipos:
    
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

   La tabla de búsqueda de valores de texto, sin embargo, requiere procesamiento adicional. La aplicación recupera la tabla de consulta adecuados desde el servicio y envía la instancia ECF (con uno o varios valores) recorriendo la tabla de búsqueda. El siguiente fragmento de código muestra el procesamiento de texto ECFs, incluidas las con valores simples y aquellas utilizando tablas de búsqueda: 
    
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

   Esta aplicación simplemente genera los valores; Sin embargo, es posible obtener más significado de los valores de datos.
    
## <a name="listpwacustomfields"></a>ListPWACustomFields

El método ListPWACustomFields recupera y enumera los ECFs asociados con los proyectos. Este método muestra el ECFs registrados en la instancia de PWA que puede asociarse con proyectos individuales. El punto de entrada para obtener acceso a la ECFs usa el elemento CustomFields del contexto de proyecto, como se muestra en la siguiente solicitud de consulta:
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

El método no se comprueba para ver si un proyecto utiliza un ECF específico.
  
## <a name="see-also"></a>Ver también

- [Portal del proyecto de desarrollo](http://dev.office.com/project.aspx)
- [Información general: Los campos personalizados de empresa y tablas de búsqueda](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)
- [Local y campos personalizados de empresa](https://msdn.microsoft.com/en-us/library/office/ms447495(v=office.14).aspx)
- [Agregar o editar campos personalizados de empresa en Project Server 2013](https://docs.microsoft.com/en-us/project/add-or-edit-enterprise-custom-fields-in-project-server)
    

