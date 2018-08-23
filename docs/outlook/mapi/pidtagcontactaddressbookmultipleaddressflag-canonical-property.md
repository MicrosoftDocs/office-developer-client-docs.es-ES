---
title: Propiedad canónica PidTagContactAddressBookMultipleAddressFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 34f61f3ef64e5751f9be3df534c4379583447799
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592699"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a>Propiedad canónica PidTagContactAddressBookMultipleAddressFlag

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un indicador que es TRUE cuando el proveedor es compatible con varias direcciones de correo electrónico por elemento de contacto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTAB_MULTI_ADDR_FLAG  <br/> |
|Identificador:  <br/> |0x6614  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Libreta de direcciones de contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

Si esta propiedad es TRUE, el proveedor no admite los contactos sin direcciones de correo electrónico. Si es FALSE, el proveedor muestra todos los contactos o no tienen una dirección de correo electrónico principal. Tendrá en cuenta sólo la dirección de correo electrónico principal. Se trata de una propiedad en un contenedor de la libreta de direcciones de contacto y una columna en la tabla de contenedores de la libreta de direcciones de contacto.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

