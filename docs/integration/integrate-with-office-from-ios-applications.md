---
title: Integración con Office desde aplicaciones de iOS
manager: soliver
ms.date: 06/04/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f3a277ba-7ba1-4eea-83b5-915b409f3093
description: Office para iOS proporciona una solución extensible que permite la integración con aplicaciones de terceros. Este artículo describe cómo se puede realizar la integración con Office desde una aplicación de iOS pasando los usuarios desde la aplicación a Office y, a continuación, devolviéndolos a la aplicación.
ms.openlocfilehash: d17a096c17eadab0cd94ee1dce18e979e80fa65d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299751"
---
# <a name="integrate-with-office-from-ios-applications"></a>Integración con Office desde aplicaciones de iOS

Office para iOS proporciona una solución extensible que permite la integración con aplicaciones de terceros. Este artículo describe cómo se puede realizar la integración con Office desde una aplicación de iOS pasando los usuarios desde la aplicación a Office y, a continuación, devolviéndolos a la aplicación.
  
Puede permitir que los usuarios que ejecutan Office en un dispositivo iOS abran y editen archivos almacenados en SharePoint o en OneDrive desde cualquier aplicación y, a continuación, devolverlos rápidamente a la aplicación original cuando hayan terminado de editar el archivo. Para ello, pasa los archivos a Office a través de controladores de protocolo y se asegura de que la invocación a Office se realiza de una forma que Office pueda entender.
  
Cuando un usuario ha terminado de editar un archivo, puede elegir la flecha atrás en la aplicación de Office para cerrar el documento y regresar a la aplicación de almacenamiento original, siempre que usted pase información específica a la aplicación de Office cuando esta se inicia.
  
## <a name="verify-that-office-has-been-installed"></a>Comprobar que Office está instalado

La aplicación de referencia deberá comprobar primero que una determinada aplicación de Office está instalada. Las siguientes aplicaciones de Office se pueden instalar en dispositivos iOS para la visualización y edición de documentos:
  
- Excel
    
- OneNote
    
- PowerPoint
    
- Word
    
Use el método [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html) para determinar si la aplicación puede abrir el recurso. Este método toma la dirección URL para el recurso como un parámetro y devuelve **No** si la aplicación que acepta la dirección URL no está disponible. Si **canOpenURL** devuelve **No**, deberá solicitar al usuario que instale Office.
  
### <a name="prompt-the-user-to-install-office"></a>Solicitar al usuario que instale Office

 Si una determinada aplicación de Office no está instalada, puede usar un objeto [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html) para representar la tienda de aplicaciones de iTunes en su aplicación y mostrar al usuario la aplicación de Office que debe instalar. La siguiente tabla enumera los identificadores de iTunes que se deben usar para invocar cada una de las aplicaciones de Office en el controlador de vistas de productos del Store Kit. 
  
|**Aplicación de Office**|**Identificador de iTunes**|
|:-----|:-----|
|Excel  <br/> |[https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4) <br/> |
|OneNote (iPhone)  <br/> |[https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4) <br/> |
|PowerPoint  <br/> |[https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4) <br/> |
|Word  <br/> |[https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4) <br/> |
   
## <a name="invoke-office"></a>Invocar a Office

Cuando la aplicación de Office está instalada, la aplicación de referencia puede invocar a Office pasando los siguientes detalles: 
  
- Protocolo de Office
    
- Modo de apertura
    
- Dirección URL
    
- Protocolo de retorno
    
- Contexto del documento
    
Formato de esquema:
  
 `<Office protocol><open mode>|u|<URL>|p|<passback protocol>|c|<document context>`
  
El siguiente ejemplo muestra una solicitud para invocar un archivo de Word para su edición:
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx|p|clouddrive|c|folderviewQ4`
  
### <a name="office-protocols"></a>Protocolos de Office

La siguiente tabla enumera los protocolos para cada aplicación de Office. 
  
|**Aplicación**|**Protocolo**|
|:-----|:-----|
|Excel  <br/> |ms-excel:  <br/> |
|OneNote  <br/> |onenote:  <br/> |
|PowerPoint  <br/> |ms-powerpoint:  <br/> |
|Word  <br/> |ms-word:  <br/> |
   
### <a name="open-mode"></a>Modo de apertura

Las aplicaciones de Office pueden abrir archivos directamente en el modo de visualización (ofv) o edición (ofe). El modo de edición es el predeterminado. 
  
Formato de esquema:
  
 `<ofv or ofe>`
  
### <a name="url"></a>URL

La dirección URL incluye tres partes: 
  
- La declaración de que el archivo se abrirá para su edición (ofe)
    
- El descriptor de la dirección URL (|u|)
    
- La dirección URL
    
La dirección URL se debe codificar y debe ser un vínculo directo al archivo (no una redirección). Si la dirección URL está en un formato que Office no puede gestionar o simplemente se produce un error en la descarga, Office no devolverá al usuario a la aplicación que realizó la invocación. 
  
Formato de esquema:
  
 `|u|<document URL>`
  
### <a name="passback-protocol-optional"></a>Protocolo de retorno (opcional)

Si desea que Office devuelva a los usuarios a su aplicación de iOS cuando elijan la flecha atrás, la aplicación que realizó la invocación deberá usar el protocolo de retorno, que incluye el descriptor "|p|" seguido del protocolo de la aplicación (sin los dos puntos). Deberá asegurarse de que la aplicación pueda gestionar correctamente la respuesta de Office.
  
Formato de esquema:
  
 `|p|<passback protocol>`
  
### <a name="document-context-optional"></a>Contexto del documento (opcional)

Office no usa el contexto del documento, pero la aplicación de referencia podría necesitarlo cuando Office devuelve a un usuario. Si desea que el contexto del documento se devuelva con la aplicación, use el descriptor '|c|' seguido del contexto que desea como una cadena. Office no limita la longitud de la cadena más allá de los límites que imponga el sistema operativo.
  
Formato de esquema:
  
 `|c|<document context>`
  
## <a name="return-users-to-the-referring-application"></a>Devolver a los usuarios a la aplicación de referencia

Por motivos de seguridad, Office solo devuelve a los usuarios a la aplicación de referencia si el archivo se abrió correctamente. Cuando el usuario elige la flecha atrás, Office responde a la aplicación que realiza la invocación con el protocolo de retorno, el modo de apertura, la dirección URL, el estado de carga pendiente y el contexto del documento. El estado de carga pendiente usa el descriptor |z|, y el valor es sí o no.
  
Formato de esquema:
  
 `<app protocol>:ofe|u|<URL>|z|<yes or no>|c|<doc context> Example: clouddrive:ofe|u|https://contoso/Q4/budget.docx|z|no|c|folderviewQ4`
  
## <a name="see-also"></a>Vea también
<a name="bk_addresources"> </a>

- [Método canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [Clase UIApplication](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [Objeto SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html)
    

