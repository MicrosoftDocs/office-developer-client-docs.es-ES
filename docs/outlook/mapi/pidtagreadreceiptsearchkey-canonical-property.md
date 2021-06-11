---
title: Propiedad canónica PidTagReadReceiptSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptSearchKey
api_type:
- COM
ms.assetid: a0ea5628-1393-4ab8-bc34-a58cf130db51
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: aa92e224f10fd652078b965c8e3a0b5ab59cc388
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320044"
---
# <a name="pidtagreadreceiptsearchkey-canonical-property"></a>Propiedad canónica PidTagReadReceiptSearchKey

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una clave de búsqueda para el usuario de mensajería al que el sistema de mensajería debe dirigir un informe de lectura de un mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_READ_RECEIPT_SEARCH_KEY  <br/> |
|Identificador:  <br/> |0x0053  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Sobre MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se omite a menos **que la propiedad PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) esté establecida en TRUE.
  
Si una aplicación cliente quiere recibir informes de lectura en sí, puede dejar esta propiedad sin establecer o establecerla en la clave de búsqueda incluida en la propiedad **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) en el momento del envío del mensaje.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas en los mensajes de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidef.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

