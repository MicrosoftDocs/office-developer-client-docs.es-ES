---
title: Propiedad canónico PidTagProfileServerFullVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 284b4b451a31a9478caf31fe855d38bfeab2caf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819950"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a>Propiedad canónico PidTagProfileServerFullVersion

  
  
**Se aplica a**: Outlook 
  
Especifica información de versión y de compilación completa acerca de Microsoft Exchange Server a la que están conectadas cuentas en un perfil.
  
## 

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|Identificador:  <br/> |0x663B  <br/> |
|Tipo de propiedad:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Configuración de perfiles de MAPI  <br/> |
   
## <a name="remarks"></a>Notas

Un perfil puede especificar una o más cuentas que se conectan a un servidor de Exchange, pero deben estar conectados al mismo servidor de Exchange.
  
Versiones de Outlook anteriores a Microsoft Office Outlook 2007 no admiten esta propiedad. Para las versiones de Outlook, compruebe la existencia de **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** en el perfil. 
  
Por lo general, si el buzón activo está conectado a un servidor de Exchange, Outlook 2007 almacena información completa de la versión de Exchange Server en la propiedad **PR_PROFILE_SERVER_FULL_VERSION** en el perfil activo. Outlook almacena la información en una estructura **EXCHANGE_STORE_VERSION_NUM** que contiene los números de versión principal y secundaria y los números de compilación principales y secundarias. Por ejemplo, para almacenar el identificador de la versión de Exchange Server de **8.0.685.24**, el número de versión principal es 8 y número de versión secundaria es 0 y el número de versión de compilación principal es 685 y número de compilación secundaria es 24.
  
Solo uno de **PR_PROFILE_SERVER_VERSION** o **PR_PROFILE_SERVER_FULL_VERSION** es probable que existan en un perfil, pero no hay ninguna garantía de que siempre existe alguna en un perfil. Outlook no se escribe en cualquiera de las propiedades hasta que se haya conectado correctamente al servidor de Exchange. 
  
En el modelo de objetos de Outlook, puede usar la propiedad **ExchangeMailboxServerVersion** del objeto **NameSpace** para buscar la versión de Exchange Server en el que se hospeda el buzón activo. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

