---
title: Propiedad canónica PidTagDeferredSendUnits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendUnits
api_type:
- HeaderDef
ms.assetid: 2386be9f-18c9-4949-a2aa-efc8e212801c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: becc076efe0f4f805eb2a8db071b70ad731ee256
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359909"
---
# <a name="pidtagdeferredsendunits-canonical-property"></a>Propiedad canónica PidTagDeferredSendUnits

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica la unidad de tiempo por la que se debe multiplicar **el valor PR_DEFERRED_SEND_NUMBER** propiedad ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DEFERRED_SEND_UNITS  <br/> |
|Identificador:  <br/> |0x3FEC  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Si se establece, esta propiedad debe tener uno de los siguientes valores:
  
|||
|:-----|:-----|
|**PidTagDeferredSendUnits** <br/> |Descripción  <br/> |
|0  <br/> |Minutos, por ejemplo, 60 segundos  <br/> |
|1   <br/> |Horas, por ejemplo, 60 x 60 segundos  <br/> |
|2   <br/> |Día, por ejemplo 24 x 60 x 60 segundos  <br/> |
|3   <br/> |Semana, por ejemplo, 7 x 24 x 60 x 60 segundos  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.
    
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

