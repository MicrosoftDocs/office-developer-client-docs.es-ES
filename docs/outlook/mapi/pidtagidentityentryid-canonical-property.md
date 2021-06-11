---
title: Propiedad canónica PidTagIdentityEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityEntryId
api_type:
- HeaderDef
ms.assetid: 61a9d403-e0e5-45c3-8d18-4d53207ab927
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 099df2211e87e253ab1be520378b3a2b2ca7d4c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423338"
---
# <a name="pidtagidentityentryid-canonical-property"></a>Propiedad canónica PidTagIdentityEntryId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador de entrada de la identidad de un proveedor de servicios tal como se define en un sistema de mensajería. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_IDENTITY_ENTRYID  <br/> |
|Identificador:  <br/> |0x3E01  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad no aparece como una propiedad en ningún objeto, sino solo como una columna en una tabla de estado. Forma parte de la identidad del proveedor de servicios que expone la fila de tabla de estado. La identidad del proveedor normalmente hace referencia a su cuenta en el servidor, pero puede hacer referencia a cualquier representación que el proveedor defina dentro del sistema de mensajería. 
  
Esta proprerty se establece normalmente en el identificador de entrada de libreta de direcciones adecuado. 
  
Un proveedor de servicios que proporciona cualquiera de las propiedades de identidad debe proporcionar todas ellas. Los proveedores que pertenecen al mismo servicio de mensajes deben exponer los mismos valores para las propiedades de identidad. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

