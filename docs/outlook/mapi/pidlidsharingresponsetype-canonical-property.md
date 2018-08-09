---
title: Propiedad canónica PidLidSharingResponseType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingResponseType
api_type:
- COM
ms.assetid: c27b1239-3612-4bb3-9f22-4b89ee9900cd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a645ee26b56355c6594f5667585becbcff2e3eec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818934"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a>Propiedad canónica PidLidSharingResponseType

  
  
**Hace referencia a**: Outlook 
  
Especifica el tipo de respuesta con el que ha respondido el destinatario de la solicitud para compartir. Esto es una propiedad de un mensaje para compartir.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidSharingResponseType  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Sharing  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008A27  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Uso compartido  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de esta propiedad debe establecerse en uno de los siguientes valores:
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0x00000000  <br/> |No hay respuesta  <br/> |
|0x00000001  <br/> |Aceptado  <br/> |
|0x00000002  <br/> |Denegado  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Comparte las carpetas de buzón de correo entre los clientes.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

