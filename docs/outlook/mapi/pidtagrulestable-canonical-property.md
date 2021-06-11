---
title: Propiedad canónica PidTagRulesTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fc520720-8190-4dff-8f6c-1bebf7080b57
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e1c670cd566e838104ae3d5480c2297f8632d899
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428504"
---
# <a name="pidtagrulestable-canonical-property"></a>Propiedad canónica PidTagRulesTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una tabla con todas las reglas aplicadas a una carpeta.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RULES_TABLE  <br/> |
|Identificador:  <br/> |0x3FE1  <br/> |
|Tipo de datos:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Reglas del lado servidor  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad está presente en todos los objetos de carpeta de Exchange Server que tienen reglas. Los valores incluidos en esta propiedad se usan para leer y modificar reglas. Puede usar el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con el identificador de interfaz IID_IExchangeModifyTable para obtener una [interfaz IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) **a** la tabla de reglas de una carpeta. Puede usar esta interfaz para leer y modificar esas reglas. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas. 
    
## <a name="see-also"></a>Vea también



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

