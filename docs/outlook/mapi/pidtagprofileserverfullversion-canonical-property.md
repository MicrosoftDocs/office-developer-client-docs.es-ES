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
  
Especifica la versión completa y la información de compilación sobre el servidor de Microsoft Exchange al que se conectan las cuentas de un perfil.
  
## 

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|Identificador:  <br/> |0x663B  <br/> |
|Tipo de propiedad:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Configuración del perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Un perfil puede especificar una o más cuentas que se conectan a un servidor de Exchange, pero deben estar conectadas al mismo servidor de Exchange.
  
Las versiones de Outlook anteriores a Microsoft Office Outlook 2007 no admiten esta propiedad. Para esas versiones de Outlook, Compruebe la existencia de **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** en el perfil. 
  
Por lo general, si el buzón activo está conectado a un servidor de Exchange, Outlook 2007 almacena información de la versión completa de Exchange Server en la propiedad **PR_PROFILE_SERVER_FULL_VERSION** del perfil activo. Outlook almacena la información en una estructura **EXCHANGE_STORE_VERSION_NUM** que contiene los números de versión principales y secundarias, así como los números de compilación principales y secundarias. Por ejemplo, para almacenar el identificador de versión de Exchange Server de **8.0.685.24**, el número de versión principal es 8 y el número de versión secundaria es 0, y el número de compilación principal es 685 y el número de compilación menor es 24.
  
Es probable que solo exista un **PR_PROFILE_SERVER_VERSION** o **PR_PROFILE_SERVER_FULL_VERSION** en un perfil, pero no hay ninguna garantía que siempre exista en un perfil. Outlook no escribe en ninguna de las dos propiedades hasta que se haya conectado correctamente al servidor de Exchange. 
  
En el modelo de objetos de Outlook, puede usar la propiedad **ExchangeMailboxServerVersion** del objeto **namespace** para buscar la versión de Exchange Server en la que se hospeda el buzón activo. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjuntos de propiedades.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

