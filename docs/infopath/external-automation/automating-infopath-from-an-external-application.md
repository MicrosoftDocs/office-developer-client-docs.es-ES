---
title: Automatizar InfoPath desde una aplicación externa
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath ofrece automatización de aplicación desde el código escrito con COM y secuencias de comandos con los métodos del objeto Application y la colección XDocuments.
ms.openlocfilehash: 0e3fcc50ec11f5fc8791d37144767bf0398ccda7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815757"
---
# <a name="automating-infopath-from-an-external-application"></a>Automatizar InfoPath desde una aplicación externa

Microsoft InfoPath ofrece automatización de aplicación desde el código escrito con COM y secuencias de comandos con los métodos del objeto **Application** y la colección **XDocuments** . 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>Información general de la aplicación y los objetos XDocument

El objeto **Application** contiene los siguientes métodos empleados para automatización: 
  
|**Método**|**Descripción**|
|:-----|:-----|
|**CacheSolution** <br/> |Examina el en la memoria caché y, si es necesario, la actualiza desde la ubicación publicada de la plantilla de formulario.  <br/> |
|**Quit** <br/> |Cierra la aplicación de Microsoft Office InfoPath.  <br/> |
|**RegisterSolution** <br/> |Instala la plantilla de formulario de Microsoft Office InfoPath especificada.  <br/> |
|**UnregisterSolution** <br/> |Desinstala la plantilla de formulario de Microsoft Office InfoPath especificada.  <br/> |
   
La colección **XDocuments** contiene los siguientes métodos que se pueden usar para la automatización externa: 
  
|**Método**|**Descripción**|
|:-----|:-----|
|Método **Close**  <br/> |Cierra el formulario de Microsoft Office InfoPath especificado.  <br/> |
|**New** (método)  <br/> |Crea un nuevo formulario de Microsoft Office InfoPath.  <br/> |
|Método **NewFromSolution**  <br/> |Crea un nuevo formulario de Microsoft Office InfoPath basado en la plantilla de formulario especificada.  <br/> |
|Método **NewFromSolutionWithData**  <br/> |Crea un nuevo formulario de Microsoft Office InfoPath mediante la plantilla de formulario y los datos XML especificada.  <br/> |
|**Open** (método)  <br/> |Abre el formulario de Microsoft Office InfoPath especificado.  <br/> |
   
Para usar el objeto **Application** desde una aplicación externa, utilice la función **CreateObject** con el ProgID de la aplicación InfoPath ("InfoPath.Application") para crear una variable de objeto que representa la aplicación InfoPath. A continuación, puede usar la propiedad **XDocuments** para tener acceso a la colección **XDocuments** y usar sus métodos para abrir o crear un formulario de InfoPath. En el ejemplo siguiente se muestra la creación de una referencia al objeto **Application** utilizando la 6.0 de Microsoft Visual Basic o Visual Basic para aplicaciones (VBA), lenguaje de programación: 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> Debido a que la función **CreateObject** crea una variable de objeto mediante el enlace, finalización automática de instrucciones no estará disponible en el Editor de Visual Basic. Hacer referencia a los vínculos en las tablas anteriores para obtener información acerca de la sintaxis llamada correcta. 
  

