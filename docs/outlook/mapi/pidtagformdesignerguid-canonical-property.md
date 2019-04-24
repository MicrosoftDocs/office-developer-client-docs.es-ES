---
title: Propiedad canónica PidTagFormDesignerGuid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormDesignerGuid
api_type:
- HeaderDef
ms.assetid: 8d7f5789-610c-47f6-a109-5513d677ef60
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b0e0847a3a9e21f080a852738ec8afbc98a2263f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316236"
---
# <a name="pidtagformdesignerguid-canonical-property"></a>Propiedad canónica PidTagFormDesignerGuid

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador único del objeto que se usa para diseñar un formulario.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_FORM_DESIGNER_GUID  <br/> |
|Identificador:  <br/> |0x3309  <br/> |
|Tipo de datos:  <br/> |PT_GUID  <br/> |
|Área:  <br/> |Common MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad suele contener el identificador único global (GUID) del programa de diseño que se usa para crear el formulario. Esta propiedad puede estar vacía. 
  
La estructura [MAPIUID](mapiuid.md) contiene la definición del identificador único. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

