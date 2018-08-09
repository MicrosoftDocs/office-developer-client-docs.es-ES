---
title: Entradas de las propiedades de las secciones de servicios de mensaje MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 30f5e0b59bacfab91a3a6c77c0b345d6299df9e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820442"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a>Entradas de las propiedades de las secciones de servicios de mensaje MapiSvc.inf

  
  
**Hace referencia a**: Outlook 
  
Las entradas que establecer las propiedades de usar este formato:
  
 **etiqueta (propiedad)** **=** valor de la propiedad 
  
La etiqueta de propiedad puede ser una etiqueta de propiedad MAPI estándar si los datos de configuración representan una de las propiedades predeterminadas de MAPI o una etiqueta no estándar si los datos no representan una propiedad MAPI. La etiqueta no estándar se realiza mediante la combinación del valor de un identificador de propiedad con un tipo de propiedad. El resultado es un número hexadecimal de 8 dígitos. El valor de la propiedad puede ser todo lo que tiene sentido para la etiqueta de propiedad. 
  
Las secciones de servicio de mensaje pueden contener una gran variedad de entradas de función que se está configurando el servicio de mensajes. Normalmente, se incluyen las siguientes propiedades MAPI en una sección de servicios de mensaje en el formato de lista:
  
 **PR_DISPLAY_NAME** =  _cadena_
  
 **PR_SERVICE_DLL_NAME** =  _nombre del archivo DLL_
  
 **PR_SERVICE_ENTRY_NAME** =  _nombre de función de punto de entrada_
  
 **PR_SERVICE_SUPPORT_FILES** =  _lista de archivos_
  
 **PR_SERVICE_DELETE_FILES** =  _lista de archivos_
  
 **PR_RESOURCE_FLAGS** =  _máscara de bits_
  
La cadena de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) es el nombre del servicio de mensaje que se muestra en la interfaz de usuario, el nombre que el usuario se asocia con el servicio de mensajes. El nombre para mostrar es una entrada opcional en mapisvc.inf. En ocasiones, el nombre para mostrar se constar de dos partes; un elemento asignado por el servicio de mensajes y un elemento asignado por el usuario. Si el usuario es responsable de asignar uno de los elementos, normalmente esto se controla con un cuadro de diálogo especial conocido como una hoja de propiedades suministrada por el servicio de mensajes bajo el control de una aplicación cliente. 
  
La información proporcionada para la entrada de **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) es el nombre del archivo DLL que contiene el servicio de mensajes. La información proporcionada para la entrada de **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) es el nombre de la función de punto de entrada dentro de ese archivo DLL que llama MAPI para configurar el servicio de mensajes. 
  
Los archivos que aparecen en la entrada de **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) son archivos que deben estar instalados con el servicio de mensajes. Del mismo modo, se deben quitar los archivos en la entrada de **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) cuando se quita el servicio de mensajes. 
  
La entrada **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) es una colección de opciones definida para el servicio de mensajes. Por ejemplo, se establece el bit SERVICE_SINGLE_COPY cuando el servicio de mensajes sólo puede aparecer una vez en un perfil dado. Si el servicio de mensajes no proporciona información de identidad, se establece el bit SERVICE_NO_PRIMARY_IDENTITY. 
  
Siguen dos ejemplos de entradas de la propiedad no estándar. La primera entrada especifica la ruta de acceso para el archivo usado por la libreta de direcciones predeterminada como el valor de la propiedad; la segunda entrada especifica un valor numérico (propiedad). Ambas entradas tienen un significado específico para el servicio de mensajes AB.
  
```cpp
6600001e=full path to file
66040003=integer

```


