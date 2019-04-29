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
ms.openlocfilehash: 55e6c8fb013e544ae04740aeaeb23ac23949cffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425641"
---
# <a name="pidtagprovidericon-canonical-property"></a>Propiedad canónica PidTagProviderIcon

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una cadena Unicode que especifica un icono o iconos personalizados que se mostrarán para un proveedor MAPI en la barra de estado de Microsoft Office Outlook en los Estados en línea y sin conexión.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROVIDER_ICON, PR_PROVIDER_ICON_W  <br/> |
|Identificador:  <br/> |0x3417  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Almacén de mensajes MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades especifican el archivo de recursos que contiene un icono personalizado que representa un proveedor MAPI en un estado en línea y, opcionalmente, otro icono personalizado en el estado sin conexión. Outlook siempre solicita estas propiedades en representación Unicode. 
  
Por ejemplo, el siguiente valor de propiedad indica a Outlook que debe cargar el identificador de icono 1001 desde el módulo mymod32. dll y usar dicho icono para `mymod32.dll,#1001`el estado de conexión:. Dado que no hay ningún icono específico del proveedor para el estado sin conexión, en este caso, se usa el icono estándar de Outlook sin conexión en la barra de estado. 
  
El siguiente valor de propiedad indica a Outlook que debe cargar el identificador de icono 1001 desde el módulo mymod32. dll y usar dicho icono para el estado en línea, así como cargar el icono identificador 1002 desde el mismo módulo que se va `mymod32.dll,#1001,#1002`a usar para el estado sin conexión:. No se usa ningún icono de Outlook en la barra de estado. 
  
De forma predeterminada, si no se especifican iconos personalizados, el proveedor se representa mediante los iconos predeterminados de Outlook para el estado de conexión y el estado sin conexión. De manera opcional, el proveedor puede especificar un nombre para mostrar que se mostrará junto al icono en la barra de estado. Para obtener más información, vea **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

