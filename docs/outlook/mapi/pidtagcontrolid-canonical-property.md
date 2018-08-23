---
title: Propiedad canónica PidTagControlId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2868533e0383309e013bb82aaa4300a0a40e335a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577516"
---
# <a name="pidtagcontrolid-canonical-property"></a>Propiedad canónica PidTagControlId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un identificador único para un control que se utiliza en un cuadro de diálogo. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTROL_ID  <br/> |
|Identificador:  <br/> |0x3F07  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Tabla MAPI para mostrar  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad contiene un identificador único para el control. Este identificador debe contener una estructura [GUID](guid.md) y un valor de tipo **LONG**binary. Todos los controles en el cuadro de diálogo deben usar el mismo **GUID** para identificar el proveedor de servicios, y cada control debe usar un único valor de **tipo LONG** para asegurarse de que los controles no entrar en conflicto. 
  
Esta propiedad se usa en las notificaciones. Por ejemplo, las notificaciones enviadas en la tabla para mostrar deben establecer esta propiedad para identificar de forma única el control que se debe actualizar. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

