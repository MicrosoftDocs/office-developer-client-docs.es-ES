---
title: Propiedad canónica PidTagAccessControlListTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 48667fda-ddc4-42ac-9231-761db0a4c1a9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 40a2bc8a27ec3ce3df610b9c7364719c2b5ee750
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572791"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a>Propiedad canónica PidTagAccessControlListTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una tabla que consta de todos los el sistema acceso a listas de control de (SACL) aplicadas a una carpeta.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ACL_TABLE  <br/> |
|Identificador:  <br/> |0x3FE0  <br/> |
|Tipo de datos:  <br/> |PT OBJECT  <br/> |
|Área:  <br/> |Control de acceso  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad está presente en todos los objetos de carpeta en un servidor de Exchange. Los valores incluidos en esta propiedad se usan para la lectura y modificación de control de acceso (ACL) enumera en las carpetas. Puede usar el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con el identificador de la interfaz **IID_IExchangeModifyTable** para obtener un [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) interfaz para la tabla de ACL de una carpeta. Puede usar esta interfaz para leer y modificar estas ACL. 
  
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

