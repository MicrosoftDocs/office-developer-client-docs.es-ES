---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 357ace3267f22d751a20a12c96f108ee2f8ae1e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595205"
---
# <a name="tchar"></a>TCHAR

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Una cadena de caracteres Win32 que puede utilizarse para describir las cadenas ANSI, DBCS o Unicode. Para las plataformas ANSI y DBCS, TCHAR se define como sigue:
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a>Comentarios

Para las plataformas Unicode, TCHAR se define como sinónimos con el tipo de WCHAR. 
  
Los clientes MAPI pueden usar el tipo de datos TCHAR para representar una cadena del tipo de la WCHAR o char. Asegúrese de definir el UNICODE constante simbólico y limitar la plataforma cuando es necesario. MAPI interpretará la información de la plataforma y traducir internamente TCHAR por la cadena apropiada. El tipo de propiedad MAPI, PT_TSTRING, funciona igual que el tipo de datos TCHAR. Cuando la plataforma es compatible con Unicode, las propiedades de tipo PT_TSTRING se asignan al tipo PT_UNICODE en tiempo de compilación. Cuando la plataforma no es compatible con Unicode, estas propiedades se asignan al tipo PT_STRING8.
  
Para obtener más información acerca de esta funcionalidad, vea [Conjuntos de caracteres](mapi-character-sets.md) y la [Lista de tipos de propiedad](property-types.md). 
  
## <a name="see-also"></a>Vea también



[Tipos de datos MAPI](mapi-data-types.md)

