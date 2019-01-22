---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: 'Última modificación: 23 de julio de 2011'
localization_priority: Priority
ms.openlocfilehash: 2b04ebe6d05cd72a59fe6d44c9138468fd7ddec1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710450"
---
# <a name="tchar"></a>TCHAR

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Una cadena de caracteres Win32 que puede usarse para describir las cadenas DBCS, ANSI o Unicode. Para las plataformas ANSI y DBCS, TCHAR se define como se muestra aquí:
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a>Observaciones

Para las plataformas Unicode, TCHAR se define como sinónimo de tipo WCHAR. 
  
Los clientes MAPI pueden usar el tipo de datos TCHAR para representar una cadena de tipo WCHAR o char. Asegúrese de definir la constante simbólica UNICODE y de limitar la plataforma cuando sea necesario. MAPI interpretará la información de la plataforma y traducirá TCHAR a la cadena apropiada de manera interna. El tipo de propiedad MAPI, PT_TSTRING, funciona igual que el tipo de datos TCHAR. Cuando la plataforma admite Unicode, a las propiedades de tipo PT_TSTRING se les asigna el tipo PT_UNICODE a la hora de la compilación. Cuando la plataforma no admite Unicode, a estas propiedades se les asigna el tipo PT_STRING8.
  
Para más información sobre esta funcionalidad, consulte [Juegos de caracteres](mapi-character-sets.md) y [Lista de tipos de propiedad](property-types.md). 
  
## <a name="see-also"></a>Vea también



[Tipos de datos MAPI](mapi-data-types.md)

