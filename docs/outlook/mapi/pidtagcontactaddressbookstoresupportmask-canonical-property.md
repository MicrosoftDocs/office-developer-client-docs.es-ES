---
title: Propiedad canónica PidTagContactAddressBookStoreSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookStoreSupportMask
api_type:
- HeaderDef
ms.assetid: 34f649c8-29bf-470f-9b05-31b69d069259
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fb40e2c191056fe164c6a06bfdcf4b8e3d6eb92c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434441"
---
# <a name="pidtagcontactaddressbookstoresupportmask-canonical-property"></a>Propiedad canónica PidTagContactAddressBookStoreSupportMask

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)) obtenida del almacén que contiene la carpeta Contactos.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTAB_STORE_SUPPORT_MASK  <br/> |
|Identificador:  <br/> |0x6611  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Libreta de direcciones de contactos  <br/> |
   
## <a name="remarks"></a>Comentarios

El proveedor de libreta de direcciones de contactos usa esta propiedad para evaluar la idoneidad de las características admitidas del almacén. Se trata de una propiedad en un contenedor de libreta de direcciones de contactos y una columna en la tabla de contenedores de libreta de direcciones de contactos.
  
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

