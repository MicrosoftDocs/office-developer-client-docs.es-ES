---
title: Automatizar InfoPath desde una aplicación externa
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath proporciona automatización de aplicaciones a partir del código escrito mediante COM y script mediante los métodos del objeto Application y la colección XDocuments.
ms.openlocfilehash: 7eccbca34b93aff7909de92eebc04d012d4dd97c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303811"
---
# <a name="automating-infopath-from-an-external-application"></a>Automatizar InfoPath desde una aplicación externa

Microsoft InfoPath proporciona automatización de aplicaciones a partir del código escrito mediante COM y script mediante los métodos del objeto **Application** y la colección **XDocuments** . 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>Información general sobre los objetos Application y XDocument

El objeto **Application** contiene los siguientes métodos usados para la automatización: 
  
|**Método**|**Descripción**|
|:-----|:-----|
|**CacheSolution** <br/> |Examina el en la memoria caché y, si es necesario, lo actualiza desde la ubicación de publicación de la plantilla de formulario.  <br/> |
|**Quit** <br/> |Sale de la aplicación Microsoft Office InfoPath.  <br/> |
|**Aplicado** <br/> |Instala la plantilla de formulario de Microsoft Office InfoPath especificada.  <br/> |
|**UnregisterSolution** <br/> |Desinstala la plantilla de formulario de Microsoft Office InfoPath especificada.  <br/> |
   
La **** colección XDocuments contiene los siguientes métodos que se pueden usar para la automatización externa: 
  
|**Método**|**Descripción**|
|:-----|:-----|
|Método **Close**  <br/> |Cierra el formulario de Microsoft Office InfoPath especificado.  <br/> |
|**New** (método)  <br/> |Crea un nuevo formulario de Microsoft Office InfoPath.  <br/> |
|**NewFromSolution** (método)  <br/> |Crea un nuevo formulario de Microsoft Office InfoPath basado en la plantilla de formulario especificada.  <br/> |
|Método **NewFromSolutionWithData**  <br/> |Crea un nuevo formulario de Microsoft Office InfoPath con los datos XML y la plantilla de formulario especificados.  <br/> |
|**Open** (método)  <br/> |Abre el formulario de Microsoft Office InfoPath especificado.  <br/> |
   
Para usar el objeto **Application** desde una aplicación externa, use la función **CreateObject** con el ProgID de la aplicación InfoPath ("InfoPath. Application") para crear una variable de objeto que represente la aplicación InfoPath. A continuación, puede utilizar **** la propiedad XDocuments para tener acceso a la colección **XDocuments** y utilizar sus métodos para abrir o crear un formulario de InfoPath. En el siguiente ejemplo se muestra la creación de una referencia al objeto **Application** mediante el lenguaje de programación Microsoft visual Basic 6,0 o Visual Basic para aplicaciones (VBA): 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> Debido a que la función **CreateObject** crea una variable de objeto con enlace en tiempo de ejecución, la finalización automática de instrucciones no estará disponible en el editor de Visual Basic. Consulte los vínculos de las tablas anteriores para obtener información sobre la sintaxis de llamada correcta. 
  

