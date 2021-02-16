---
title: Secciones del proveedor de servicios MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ea192ec6356cc3b929bf8379567144d3a54223f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405565"
---
# <a name="mapisvcinf-service-provider-sections"></a>Secciones del proveedor de servicios MapiSvc.inf

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Mapisvc.inf incluye una sección de proveedor de servicios  para cada una de las entradas enumeradas en la entrada Proveedores de la sección de servicios de mensajes anterior. **Las** secciones del proveedor de servicios son similares a las secciones de servicio de mensajes en que ambos tipos de secciones contienen entradas en este formato: 
  
**etiqueta de propiedad** = valor de propiedad 
  
Sin embargo, las secciones del proveedor de servicios y las secciones de servicio de mensajes difieren en que dichas entradas de propiedad son el único tipo de entrada incluido en las secciones del proveedor de servicios. No puede haber secciones adicionales o vinculadas para los proveedores de servicios; toda la información del proveedor de servicios debe estar incluida en una sección. 
  
Algunas de las propiedades establecidas en las secciones de servicio de mensajes también se establecen en las secciones del proveedor de servicios porque estas propiedades tienen sentido para ambas. La **PR_DISPLAY_NAME** propiedad es un ejemplo. Tanto los proveedores de servicios como los servicios de mensajes tienen un nombre que se usa para mostrar en la interfaz de usuario de configuración. Según el proveedor de servicios, ese nombre puede ser o no el mismo. Otras propiedades son específicas de los proveedores de servicios. 
  
Las secciones típicas del proveedor de servicios incluyen las siguientes entradas, todas ellas obligatorias:
  
**PR_DISPLAY_NAME**  =   _string_
  
**PR_PROVIDER_DISPLAY**  =   _string_
  
**PR_PROVIDER_DLL_NAME**  =   _nombre del archivo DLL_
  
**PR_RESOURCE_TYPE**  =   _long_
  
**PR_RESOURCE_FLAGS**  =   _máscara de bits_
  
La **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) es similar a **PR_SERVICE_DLL_NAME**; indica el nombre de archivo de la DLL que contiene el proveedor de servicios. El código de servicio de mensajes puede almacenarse con uno de sus proveedores de servicios en el mismo archivo DLL o existir como una DLL independiente. Tenga en cuenta que no se incluye ningún sufijo en la entrada independientemente de la plataforma de destino; MAPI se encarga de agregar un sufijo si es necesario. 
  
**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) representa el tipo de proveedor de servicios; los proveedores de servicios lo establecen en la constante predefinida adecuada. Los valores válidos MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER y MAPI_AB_PROVIDER.
  
Otra entrada de propiedad que se aplica tanto a los servicios de mensajes como a los proveedores de **servicios,** la entrada PR_RESOURCE_FLAGS ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) indica opciones. La configuración de esta entrada de propiedad puede variar en función del proveedor de servicios. Por ejemplo, algunos proveedores  de al almacenamiento de mensajes PR_RESOURCE_FLAGS en STATUS_NO_DEFAULT_STORE si nunca pueden funcionar como el almacén de mensajes predeterminado. 
  
A continuación se muestran tres ejemplos de secciones de proveedores de servicios. La **sección [Proveedor ab]** es la sección del proveedor de servicios para el servicio de libreta de direcciones predeterminado. Las **secciones [MsgService Prov1]** y **[MsgService Prov2]** pertenecen a Mi propio servicio; La primera es una sección de proveedor de libreta de direcciones y la segunda es una sección de proveedor de almacén de mensajes. 
  
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


