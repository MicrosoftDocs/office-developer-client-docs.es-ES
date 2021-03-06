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
ms.openlocfilehash: 34e8a3c73715a75b8007646e5ba3b0dc3e1ae919
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331195"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a>Propiedad canónica PidLidSharingResponseType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el tipo de respuesta con la que respondió el destinatario de la solicitud de uso compartido. Esta es una propiedad de un mensaje de uso compartido.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidSharingResponseType  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Sharing  <br/> |
|Id. largo (LID):  <br/> |0x00008A27  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Compartir  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de esta propiedad debe establecerse en uno de los siguientes valores:
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0x00000000  <br/> |Sin respuesta  <br/> |
|0x00000001  <br/> |Aceptadas  <br/> |
|0x00000002  <br/> |Denegado  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Comparte carpetas de buzones entre clientes.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

