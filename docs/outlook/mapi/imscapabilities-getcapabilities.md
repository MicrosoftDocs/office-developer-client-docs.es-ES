---
title: IMSCapabilitiesGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSCapabilities.GetCapabilities
api_type:
- COM
ms.assetid: c77a8ef1-0730-d458-b35f-451d3f450fac
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0211a326e94c5847c040040e0e0e4e9ddd1d760d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583277"
---
# <a name="imscapabilitiesgetcapabilities"></a>IMSCapabilities::GetCapabilities

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Obtiene información sobre lo que puede admitir un almacén se basa en el selector especificado.
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a>Parámetros

 *mscapSelector* 
  
> [entrada] Selector que indica qué capacidades para devolver.
    
## <a name="return-value"></a>Valor devuelto

MSCAP_SECURE_FOLDER_HOMEPAGES
  
> Compatibilidad con páginas principales de carpeta en un almacén no predeterminado. Puede devolverse si no se especifica **MSCAP_SEL_FOLDER** en *mscapSelector* . 
    
MSCAP_RES_ANNOTATION
  
> Si una restricción contiene cualquier argumento no válido, como las propiedades no válidas, el almacén de pasa por alto los argumentos no válidos y procesa sólo los argumentos válidos. Puede devolverse si no se especifica **MSCAP_SEL_RESTRICTION** en *mscapSelector* . 
    
NULL
  
> El almacén no es compatible con ninguna capacidad basada en el selector de determinado.
    

