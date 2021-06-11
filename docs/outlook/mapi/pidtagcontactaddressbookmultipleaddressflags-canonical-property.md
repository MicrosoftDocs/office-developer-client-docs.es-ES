---
title: Propiedad canónica PidTagContactAddressBookMultipleAddressFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ecd795490d953f1aa237dfbd77585ba79c8b3234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429253"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a>Propiedad canónica PidTagContactAddressBookMultipleAddressFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene marcas que indican si los proveedores admitirán varias direcciones de correo electrónico por elemento de contacto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTAB_MULTI_ADDR_FLAGS  <br/> |
|Identificador:  <br/> |0x6625  <br/> |
|Tipo de datos:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Libreta de direcciones de contactos  <br/> |
   
## <a name="remarks"></a>Comentarios

Si las marcas de esta propiedad son TRUE, el proveedor no incluye contactos sin direcciones de correo electrónico. Solo se respetará la dirección de correo electrónico principal. Se trata de una propiedad de una sección de perfil de libreta de direcciones de contactos.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

