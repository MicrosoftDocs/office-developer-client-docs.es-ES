---
title: Automatizar InfoPath desde una aplicación externa
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath proporciona automatización de aplicaciones a partir de código escrito mediante COM y script mediante métodos del objeto Application y la colección XDocuments.
ms.openlocfilehash: 7eccbca34b93aff7909de92eebc04d012d4dd97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412670"
---
# <a name="automating-infopath-from-an-external-application"></a>Automatizar InfoPath desde una aplicación externa

Microsoft InfoPath proporciona automatización de aplicaciones a partir de código escrito mediante COM y script mediante métodos del objeto **Application** y la **colección XDocuments.** 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>Información general sobre los objetos Application y XDocument

El **objeto Application** contiene los métodos siguientes usados para la automatización: 
  
|**Método**|**Descripción**|
|:-----|:-----|
|**CacheSolution** <br/> |Examina la memoria caché y, si es necesario, la actualiza desde la ubicación publicada de la plantilla de formulario.  <br/> |
|**Quit** <br/> |Sale de la Microsoft Office InfoPath.  <br/> |
|**RegisterSolution** <br/> |Instala la plantilla de formulario Microsoft Office infoPath especificada.  <br/> |
|**UnregisterSolution** <br/> |Desinstala la plantilla de formulario Microsoft Office infoPath especificada.  <br/> |
   
La **colección XDocuments** contiene los siguientes métodos que se pueden usar para la automatización externa: 
  
|**Método**|**Descripción**|
|:-----|:-----|
|Método **Close**  <br/> |Cierra el formulario de InfoPath Microsoft Office especificado.  <br/> |
|**Nuevo método**  <br/> |Crea una nueva Microsoft Office formulario de InfoPath.  <br/> |
|**NewFromSolution (método)**  <br/> |Crea una nueva Microsoft Office formulario de InfoPath basado en la plantilla de formulario especificada.  <br/> |
|**Método NewFromSolutionWithData**  <br/> |Crea una nueva Microsoft Office formulario de InfoPath mediante los datos XML especificados y la plantilla de formulario.  <br/> |
|**Open (método)**  <br/> |Abre el formulario Microsoft Office InfoPath especificado.  <br/> |
   
Para usar el objeto **Application** desde una aplicación externa, utilice la función **CreateObject** con el ProgID de la aplicación de InfoPath ("InfoPath.Application") para crear una variable de objeto que represente la aplicación InfoPath. A continuación, puede usar la propiedad **XDocuments** para tener acceso a la colección **XDocuments** y usar sus métodos para abrir o crear un formulario de InfoPath. En el siguiente ejemplo se muestra la creación de una referencia al objeto **Application** mediante el lenguaje de programación Microsoft Visual Basic 6.0 o Visual Basic para Aplicaciones (VBA): 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> Dado que **la función CreateObject** crea una variable de objeto mediante el enlace en tiempo de ejecución, la finalización automática de instrucciones no estará disponible en el Editor Visual Basic. Consulte los vínculos de las tablas anteriores para obtener información sobre la sintaxis de llamada correcta. 
  

