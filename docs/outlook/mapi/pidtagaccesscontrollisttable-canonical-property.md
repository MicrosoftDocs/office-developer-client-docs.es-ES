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
ms.openlocfilehash: 9c71a2b806b810906c13ea4750e5491b1544f640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424507"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a>Propiedad canónica PidTagAccessControlListTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una tabla que consta de todas las listas de control de acceso al sistema (SACL) que se aplican a una carpeta.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ACL_TABLE  <br/> |
|Identificador:  <br/> |0x3FE0  <br/> |
|Tipo de datos:  <br/> |PT OBJECT  <br/> |
|Área:  <br/> |Control de acceso  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad está presente en todos los objetos de carpeta de un servidor de Exchange. Los valores incluidos en esta propiedad se usan para leer y modificar las listas de control de acceso (ACL) de las carpetas. Puede usar el método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) con el identificador de interfaz **IID_IExchangeModifyTable** para obtener una interfaz [IExchangeModifyTable: IUNKNOWN](iexchangemodifytableiunknown.md) a la tabla de ACL de una carpeta. Puede usar esta interfaz para leer y modificar estas ACL. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

