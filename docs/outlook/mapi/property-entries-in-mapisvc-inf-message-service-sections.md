---
title: Entradas de propiedades en las secciones de servicios de mensaje MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ad2732f2f8dba4f506318a1b6faefb617a60584a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328521"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a>Entradas de propiedades en las secciones de servicios de mensaje MapiSvc. inf

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las entradas que establecen propiedades utilizan este formato:
  
 **etiqueta de propiedad** **=** valor de la propiedad 
  
La etiqueta de propiedad puede ser una etiqueta de propiedad MAPI estándar si los datos de configuración representan una de las propiedades predefinidas por MAPI, o una etiqueta no estándar si los datos no representan una propiedad MAPI. La etiqueta no estándar se realiza combinando el valor de un identificador de propiedad con un tipo de propiedad. El resultado es un número hexadecimal de 8 dígitos. El valor de la propiedad puede ser cualquiera que sea lógico para la etiqueta de propiedad. 
  
Las secciones del servicio de mensajes pueden contener una variedad de entradas que dependen del servicio de mensajes que se está configurando. Las siguientes propiedades MAPI se suelen incluir en una sección de servicios de mensajes en el formato enumerado:
  
 **** =  _Cadena_ PR_DISPLAY_NAME
  
 **PR_SERVICE_DLL_NAME** =  _nombre del archivo dll_
  
 **PR_SERVICE_ENTRY_NAME** =  _nombre de función de punto de entrada_
  
 **** =  _Lista de archivos de_ PR_SERVICE_SUPPORT_FILES
  
 **** =  _Lista de archivos de_ PR_SERVICE_DELETE_FILES
  
 **** =  _Máscara_ de PR_RESOURCE_FLAGS
  
La cadena **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) es el nombre del servicio de mensajes que se muestra en la interfaz de usuario, el nombre que el usuario asocia con el servicio de mensajes. El nombre para mostrar es una entrada opcional en MAPISVC. inf. A veces, el nombre para mostrar constará de dos partes; una parte asignada por el servicio de mensajes y una parte asignada por el usuario. Si el usuario es responsable de asignar una de las partes, normalmente se controla con un cuadro de diálogo especial conocido como una hoja de propiedades suministrada por el servicio de mensajes bajo el control de una aplicación cliente. 
  
La información proporcionada para la entrada **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) es el nombre de la dll que contiene el servicio de mensajes. La información proporcionada para la entrada **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) es el nombre de la función de punto de entrada dentro de la dll que MAPI llama para configurar el servicio de mensajes. 
  
Los archivos que aparecen en la entrada **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) son archivos que se deben instalar con el servicio de mensajes. Del mismo modo, los archivos de la entrada **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) deben quitarse cuando se quita el servicio de mensajes. 
  
La entrada **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) es una colección de opciones definidas para el servicio de mensajes. Por ejemplo, el bit SERVICE_SINGLE_COPY se establece cuando el servicio de mensajes solo puede aparecer una vez en un perfil determinado. El bit SERVICE_NO_PRIMARY_IDENTITY se establece si el servicio de mensajes no proporciona información de identidad. 
  
A continuación se muestran dos ejemplos de entradas de propiedades no estándar. La primera entrada especifica la ruta de acceso al archivo usado por la libreta de direcciones predeterminada como valor de la propiedad; la segunda entrada especifica un valor de propiedad numérica. Ambas entradas tienen significado específico del servicio de mensajes AB.
  
```cpp
6600001e=full path to file
66040003=integer

```


