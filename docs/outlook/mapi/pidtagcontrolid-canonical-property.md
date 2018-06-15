---
title: Propiedad canónico PidTagControlId
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 799f83b397cbef9d7dcb6c9a88154b88afe35675
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19819386"
---
# <a name="pidtagcontrolid-canonical-property"></a>Propiedad canónico PidTagControlId

  
  
**Se aplica a**: Outlook 
  
Contiene un identificador único para un control que se utiliza en un cuadro de diálogo. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTROL_ID  <br/> |
|Identificador:  <br/> |0x3F07  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Tabla MAPI para mostrar  <br/> |
   
## <a name="remarks"></a>Notas

Esta propiedad contiene un identificador único para el control. Este identificador debe contener una estructura [GUID](guid.md) y un valor de tipo **LONG**binary. Todos los controles en el cuadro de diálogo deben usar el mismo **GUID** para identificar el proveedor de servicios, y cada control debe usar un único valor de **tipo LONG** para asegurarse de que los controles no entrar en conflicto. 
  
Esta propiedad se usa en las notificaciones. Por ejemplo, las notificaciones enviadas en la tabla para mostrar deben establecer esta propiedad para identificar de forma única el control que se debe actualizar. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

