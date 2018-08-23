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
ms.openlocfilehash: 4b4b60084b8cb53a0a245b502b8fe70241fb4eb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591696"
---
# <a name="pidtagrulestable-canonical-property"></a>Propiedad canónica PidTagRulesTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una tabla con todas las reglas que se aplica a una carpeta.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RULES_TABLE  <br/> |
|Identificador:  <br/> |0x3FE1  <br/> |
|Tipo de datos:  <br/> |PT OBJECT  <br/> |
|Área:  <br/> |Reglas del servidor  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad está presente en todos los objetos de carpeta en un servidor de Exchange que tienen las reglas. Los valores incluidos en esta propiedad se usan para leer y modificar las reglas. Puede usar el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con el identificador de la interfaz **IID_IExchangeModifyTable** para obtener un [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) interfaz a la tabla de reglas en una carpeta. Puede usar esta interfaz para leer y modificar las reglas. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas. 
    
## <a name="see-also"></a>Recursos adicionales



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

