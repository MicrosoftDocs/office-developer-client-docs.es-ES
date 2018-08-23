---
title: Propiedad canónica PidTagProviderIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderIcon
api_type:
- COM
ms.assetid: 59c84b1f-13b5-484b-b703-2fb9fcc6c7eb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 61dc61872e8d1ed525d5ac3c46c56ccc3e45ea5e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593700"
---
# <a name="pidtagprovidericon-canonical-property"></a>Propiedad canónica PidTagProviderIcon

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una cadena Unicode que especifica un icono personalizado o los iconos que se mostrará para un proveedor de MAPI en la barra de estado de Microsoft Office Outlook en Estados en línea y sin conexión.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROVIDER_ICON, PR_PROVIDER_ICON_W  <br/> |
|Identificador:  <br/> |0x3417  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Almacén de mensajes MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades especifican el archivo de recursos que contiene un icono personalizado que representa un proveedor de MAPI en un estado en línea, y, opcionalmente, otro icono personalizado en el estado sin conexión. Outlook siempre solicita estas propiedades en la representación Unicode. 
  
Por ejemplo, el valor de la propiedad siguiente indica a Outlook a cargar icono identificador 1001 desde el módulo mymod32.dll y usar ese icono para el estado en línea: `mymod32.dll,#1001`. Dado que no hay ningún icono específicas del proveedor para el estado sin conexión, en este caso, se utiliza el icono estándar de sin conexión de Outlook en la barra de estado. 
  
El valor de la propiedad siguiente indica a Outlook para cargar el icono identificador 1001 desde el módulo mymod32.dll y usar ese icono para el estado en línea y también cargar icono identificador 1002 desde este mismo módulo que se usará para el estado sin conexión: `mymod32.dll,#1001,#1002`. No hay icono de Outlook se usa en la barra de estado. 
  
De forma predeterminada, si no se especifican ningún iconos personalizados, el proveedor está representado por los iconos de Outlook predeterminado para el estado en línea y el estado sin conexión. El proveedor, opcionalmente, puede especificar un nombre para mostrar que se debe mostrar junto al icono en la barra de estado. Para obtener más información, vea **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).
  
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

