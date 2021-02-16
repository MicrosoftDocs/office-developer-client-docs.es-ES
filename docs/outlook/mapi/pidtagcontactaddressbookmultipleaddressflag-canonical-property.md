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
ms.openlocfilehash: 6fabb03d552f195c200b0ecbd8fd69f470c0e1fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431571"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a>Propiedad canónica PidTagContactAddressBookMultipleAddressFlag

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una marca que es TRUE cuando el proveedor admite varias direcciones de correo electrónico por elemento de contacto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTAB_MULTI_ADDR_FLAG  <br/> |
|Identificador:  <br/> |0x6614  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Libreta de direcciones de contactos  <br/> |
   
## <a name="remarks"></a>Comentarios

Si esta propiedad es TRUE, el proveedor no permite contactos sin direcciones de correo electrónico. Si es FALSE, el proveedor muestra a todos los contactos si tienen o no una dirección de correo electrónico principal. Solo se respetará la dirección de correo electrónico principal. Se trata de una propiedad de un contenedor de libreta de direcciones de contactos y una columna de la tabla de contenedores de libreta de direcciones de contactos.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

