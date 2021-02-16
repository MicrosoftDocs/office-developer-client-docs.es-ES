---
title: Propiedad canónica PidTagProfileServerFullVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9456178e9426d7a5fe17382d876f507daa0251f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341604"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a>Propiedad canónica PidTagProfileServerFullVersion

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica la versión completa y la información de compilación sobre la Microsoft Exchange Server a la que están conectadas las cuentas de un perfil.
  
## 

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|Identificador:  <br/> |0x663B  <br/> |
|Tipo de propiedad:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Configuración de perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Un perfil puede especificar una o más cuentas que se conectan a un Exchange Server, pero deben estar conectadas a la misma Exchange Server.
  
Las versiones de Outlook anteriores a Microsoft Office Outlook 2007 no admiten esta propiedad. Para esas versiones de Outlook, compruebe la existencia de PR_PROFILE_SERVER_VERSION **[en](pidtagprofileserverversion-canonical-property.md)** el perfil. 
  
Por lo general, si el buzón activo está conectado Exchange Server una Exchange Server, Outlook 2007 almacena la información completa de la versión Exchange Server en la propiedad **PR_PROFILE_SERVER_FULL_VERSION** del perfil activo. Outlook almacena la información en una **estructura EXCHANGE_STORE_VERSION_NUM** que contiene los números de versión principal y secundaria y los números de compilación principales y secundarias. Por ejemplo, para almacenar el identificador de versión Exchange Server de **8.0.685.24**, el número de versión principal es 8 y el número de versión secundaria es 0, y el número de compilación principal es 685 y el número de compilación secundaria es 24.
  
Solo uno de **PR_PROFILE_SERVER_VERSION** o **PR_PROFILE_SERVER_FULL_VERSION** probablemente exista en un perfil, pero no hay ninguna garantía de que siempre exista en un perfil. Outlook no escribe en ninguna de las propiedades hasta que se haya conectado correctamente al Exchange Server. 
  
En el modelo de objetos de Outlook, puede usar la propiedad **ExchangeMailboxServerVersion** del objeto **NameSpace** para buscar la versión de Exchange Server en la que se hospeda el buzón activo. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

