---
title: Secciones del proveedor de servicio de MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 05666d8d6b7279588b4b442151640fa1696aedda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586784"
---
# <a name="mapisvcinf-service-provider-sections"></a>Secciones del proveedor de servicio de MapiSvc.inf

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPISVC.inf incluye una sección de proveedor de servicio para cada una de las entradas que aparecen en la entrada de **proveedores** en la sección anterior de servicios de mensaje. Secciones de proveedor de **servicio** son similares a las secciones de servicio del mensaje en que ambos tipos de secciones contienen entradas en este formato: 
  
**etiqueta de la propiedad** = valor de la propiedad 
  
Sin embargo, las secciones de proveedor de servicio y mensaje servicio difieren en que esas entradas de la propiedad son el único tipo de entrada que se incluyen en las secciones de proveedor de servicio. No puede haber secciones adicionales o vinculadas para los proveedores de servicios; toda la información de servicio proveedor debe estar incluida en la uno sección. 
  
Algunas de las propiedades establecidas en las secciones del servicio de mensajes también se establecen en las secciones de proveedor de servicio debido a que estas propiedades que tenga sentido para ambos. La propiedad **PR_DISPLAY_NAME** es un ejemplo. Proveedores de servicio y servicios de mensajes tienen un nombre que se usa para mostrar en la interfaz de usuario de configuración. Según el proveedor de servicio, ese nombre puede o no ser el mismo. Otras propiedades son específicos de los proveedores de servicios. 
  
Secciones de proveedor de servicio típicos incluyen las siguientes entradas, que son necesarios:
  
**PR_DISPLAY_NAME** =  _cadena_
  
**PR_PROVIDER_DISPLAY** =  _cadena_
  
**PR_PROVIDER_DLL_NAME** =  _nombre del archivo DLL_
  
**PR_RESOURCE_TYPE** =  _largo_
  
**PR_RESOURCE_FLAGS** =  _máscara de bits_
  
La entrada **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) es similar a **PR_SERVICE_DLL_NAME**; indica el nombre de archivo para el archivo DLL que contiene el proveedor de servicios. Código de servicio de mensajes se pueden almacenar con uno de sus proveedores de servicios en el mismo archivo DLL o existe como un archivo DLL independiente. Tenga en cuenta que ningún sufijo está incluida en la entrada independientemente de la plataforma de destino; MAPI se ocupa de agregar un sufijo si es necesario. 
  
**PR_RESOURCE_TYPE** Entrada ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) representa el tipo de proveedor de servicios; proveedores de servicios a establecen la constante predefinida apropiada. Los valores válidos son MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER y MAPI_AB_PROVIDER.
  
Otra entrada de la propiedad que se aplica a servicios de mensajes y los proveedores de servicios, la entrada de **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) indica las opciones. La configuración de esta entrada de la propiedad puede variar según el proveedor de servicio. Por ejemplo, algunos proveedores de almacenes de mensaje podrían establecer **PR_RESOURCE_FLAGS** en STATUS_NO_DEFAULT_STORE si nunca pueden funcionar como almacén de mensajes predeterminado. 
  
Siguen tres ejemplos de las secciones de proveedor de servicio. La sección **[Proveedor AB]** es la sección del proveedor de servicio para el servicio de libreta de direcciones predeterminada. Las secciones **[MsgService Prov1]** y **[MsgService Prov2]** pertenecen a mi propio servicio; la primera es una sección del proveedor de libreta de direcciones y el segundo es una sección del proveedor de almacén de mensajes. 
  
```cpp
[AB Provider]
PR_DISPLAY_NAME=Default Address Book
PR_PROVIDER_DISPLAY=Default Address Book
PR_PROVIDER_DLL_NAME=AB.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
6600001e=C:\WINNT35\System32\DEFAB.TXT
[MsgService Prov1]
PR_DISPLAY_NAME=My Own Service
PR_PROVIDER_DISPLAY=My Own Address Book
PR_PROVIDER_DLL_NAME=MYXXX.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
[MsgService Prov2]
PR_DISPLAY_NAME=My Folders
PR_PROVIDER_DISPLAY=My Own Message Store
PR_RESOURCE_TYPE=MAPI_STORE_PROVIDER
PR_PROVIDER_DLL_NAME=MYZZZ.DLL
PR_RESOURCE_FLAGS=STATUS_NO_DEFAULT_STORE
66060003=00000000
66030003=00000000
34140102=78b2fa70aff711cd9bc800aa002fc45a
66090003=06000000
660A0003=03000000

```


