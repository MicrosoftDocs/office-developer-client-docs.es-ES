---
title: Propiedad canónica PidLidAutoProcessState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAutoProcessState
api_type:
- COM
ms.assetid: 9e724af6-5b56-4eb3-a94c-1015ebce197c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0918c15d87219c1ee20b177ae21e718e0289cf04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342066"
---
# <a name="pidlidautoprocessstate-canonical-property"></a>Propiedad canónica PidLidAutoProcessState

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica las opciones que se usan en el procesamiento automático de mensajes de correo electrónico.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidSniffState  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Id. largo (LID):  <br/> |0x0000851A  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

La propiedad puede estar ausente, en cuyo caso se usa el valor predeterminado de "0x00000000". Si se establece, esta propiedad debe establecerse en uno de los valores de la tabla siguiente.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0x00000000  <br/> |No procese automáticamente el mensaje.  <br/> |
|0x00000001  <br/> |Procese el mensaje automáticamente o cuando se abra el mensaje.  <br/> |
|0x00000002  <br/> |Procese el mensaje solo cuando se abra el mensaje.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

