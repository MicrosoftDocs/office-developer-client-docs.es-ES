---
title: Propiedad canónica PidTagOwnStoreEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnStoreEntryId
api_type:
- COM
ms.assetid: 6a82ee90-10a1-49e0-8f3a-a2cd9f490f99
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 16a23c4e711bf9f7b670dff8b3e8f65371aa6bda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427377"
---
# <a name="pidtagownstoreentryid-canonical-property"></a>Propiedad canónica PidTagOwnStoreEntryId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador de entrada del almacén de mensajes estrechamente acoplado de un transporte.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_OWN_STORE_ENTRYID  <br/> |
|Identificador:  <br/> |0x3E06  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propiedades del almacén de mensajes  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad especifica el identificador de entrada del almacén estrechamente acoplado, si existe uno. Por ejemplo, un proveedor de transporte puede especificar el identificador de entrada del almacén de carpetas privadas para que la cola MAPI pueda conectar el proveedor de transporte al almacén.
  
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

