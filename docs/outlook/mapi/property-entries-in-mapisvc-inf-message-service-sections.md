---
title: Entradas de propiedad en las secciones del servicio de mensajes MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ad2732f2f8dba4f506318a1b6faefb617a60584a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428000"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a>Entradas de propiedad en las secciones del servicio de mensajes MapiSvc.inf

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las entradas que establecen propiedades usan este formato:
  
 **etiqueta de propiedad** **=** valor de propiedad 
  
La etiqueta de propiedad puede ser una etiqueta de propiedad MAPI estándar si los datos de configuración representan una de las propiedades predefinidas por MAPI, o una etiqueta no estándar si los datos no representan una propiedad MAPI. La etiqueta no estándar se realiza combinando el valor de un identificador de propiedad con un tipo de propiedad. El resultado es un número hexadecimal de 8 dígitos. El valor de la propiedad puede ser lo que tenga sentido para la etiqueta de propiedad. 
  
Las secciones del servicio de mensajes pueden contener una variedad de entradas en función del servicio de mensajes que se esté configurando. Las siguientes propiedades MAPI se incluyen normalmente en una sección de servicios de mensajes en el formato de la lista:
  
 **PR_DISPLAY_NAME**  =   _string_
  
 **PR_SERVICE_DLL_NAME**  =   _nombre del archivo DLL_
  
 **PR_SERVICE_ENTRY_NAME**  =   _nombre de la función de punto de entrada_
  
 **PR_SERVICE_SUPPORT_FILES**  =   _lista de archivos_
  
 **PR_SERVICE_DELETE_FILES**  =   _lista de archivos_
  
 **PR_RESOURCE_FLAGS**  =   _máscara de bits_
  
La **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) es el nombre del servicio de mensajes que se muestra en la interfaz de usuario, el nombre que el usuario asocia con el servicio de mensajes. El nombre para mostrar es una entrada opcional en mapisvc.inf. A veces, el nombre para mostrar se conste de dos partes; una parte asignada por el servicio de mensajes y una parte asignada por el usuario. Si el usuario es responsable de asignar una de las partes, esto suele controlarse con un cuadro de diálogo especial conocido como hoja de propiedades suministrada por el servicio de mensajes bajo el control de una aplicación cliente. 
  
La información proporcionada para la **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) es el nombre de la DLL que contiene el servicio de mensajes. La información proporcionada para la **entrada PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) es el nombre de la función de punto de entrada dentro de esa DLL a la que MAPI llama para configurar el servicio de mensajes. 
  
Los archivos enumerados en **la PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) son archivos que deben instalarse con el servicio de mensajes. Del mismo modo, los archivos de **la PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) deben quitarse cuando se quita el servicio de mensajes. 
  
La **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) es una colección de opciones definidas para el servicio de mensajes. Por ejemplo, el bit SERVICE_SINGLE_COPY se establece cuando el servicio de mensajes solo puede aparecer una vez en un perfil determinado. El SERVICE_NO_PRIMARY_IDENTITY se establece si el servicio de mensajes no proporciona información de identidad. 
  
A continuación se muestran dos ejemplos de entradas de propiedad no estándar. La primera entrada especifica la ruta de acceso al archivo usado por la Libreta de direcciones predeterminada como valor de propiedad; la segunda entrada especifica un valor de propiedad numérica. Ambas entradas tienen un significado específico para el servicio de mensajes AB.
  
```cpp
6600001e=full path to file
66040003=integer

```


