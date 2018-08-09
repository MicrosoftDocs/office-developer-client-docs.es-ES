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
ms.openlocfilehash: fbe955d3e7a509edf6ba10678e1e2538c9185193
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819316"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a>Propiedad canónica PidTagContactAddressBookMultipleAddressFlags

  
  
**Hace referencia a**: Outlook 
  
Contiene los indicadores que indica si los proveedores de será compatible con correo electrónico varias direcciones por elemento de contacto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTAB_MULTI_ADDR_FLAGS  <br/> |
|Identificador:  <br/> |0x6625  <br/> |
|Tipo de datos:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Libreta de direcciones de contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

Si las marcas de esta propiedad están TRUE, el proveedor no incluye contactos sin direcciones de correo electrónico. Tendrá en cuenta sólo la dirección de correo electrónico principal. Se trata de una propiedad en una sección de perfil de la libreta de direcciones de contacto.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

