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
ms.openlocfilehash: b76c55fd9ddc3aa7698f75aa6ce965544b2c9aae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409261"
---
# <a name="imscapabilitiesgetcapabilities"></a>IMSCapabilities::GetCapabilities

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Obtiene información sobre lo que un almacén puede admitir en función del selector especificado.
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a>Parámetros

 *mscapSelector* 
  
> [entrada] Selector que indica las capacidades que se devolverán.
    
## <a name="return-value"></a>Valor devuelto

MSCAP_SECURE_FOLDER_HOMEPAGES
  
> Compatibilidad con las páginas de inicio de carpeta en un almacén no predeterminado. Esto se puede devolver **si MSCAP_SEL_FOLDER** se especifica en  *mscapSelector*  . 
    
MSCAP_RES_ANNOTATION
  
> Si una restricción contiene argumentos no válidos como propiedades no válidas, el almacén omite los argumentos no válidos y procesa sólo los argumentos válidos. Esto se puede devolver **si MSCAP_SEL_RESTRICTION** especificado en  *mscapSelector*  . 
    
NULL
  
> El almacén no admite ninguna funcionalidad basada en el selector determinado.
    

