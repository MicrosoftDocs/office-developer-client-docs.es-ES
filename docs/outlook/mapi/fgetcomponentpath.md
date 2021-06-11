---
title: FGetComponentPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FGetComponentPath
api_type:
- COM
ms.assetid: 2a303458-3283-409a-bc3b-b891f3fcfc22
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3456d81935a0a94bc2158eefd321da968dda9983
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335213"
---
# <a name="fgetcomponentpath"></a>FGetComponentPath

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve la ruta de acceso a la Mapi32.dll.
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a>Parameters

 _szComponent_
  
> [in] La clave de registro MSIComponentID descrita en [Mapi32.dll registro de código auxiliar](https://msdn.microsoft.com/library/dd162409.aspx)Configuración .
    
 _szQualifier_
  
> [in] La subclave MSIApplicationLCID o MSIOfficeLCID descrita en [Elegir una versión específica de MAPI para cargar](how-to-choose-a-specific-version-of-mapi-to-load.md). Los autores de llamadas pueden **pasar null** si no hay calificador. 
    
 _szDllPath_
  
> [in] La ruta de acceso a la Mapi32.dll privada, que tiene funcionalidad MAPI completa (las mismas exportaciones que el Mapi32.dll).
    
 _cchBufferSize_
  
> [in] El tamaño de  _szDllPath_, en caracteres.
    
 _fInstall_
  
> [in] Indica a MAPI que instale el componente Mapi32.dll privado si no está presente.
    
## <a name="return-value"></a>Valor devuelto

 **true**
  
> Se encontró la ruta de acceso.
    
 **false**
  
> No se encontró la ruta de acceso.
    
## <a name="remarks"></a>Comentarios

Use la **función FGetComponentPath** cuando necesite obtener la ruta de acceso a la ruta de acceso Mapi32.dll. 
  
## <a name="see-also"></a>Vea también



[Elegir una versión específica de MAPI para cargar](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Mapi32.dll registro de código auxiliar Configuración](https://msdn.microsoft.com/library/dd162409.aspx)

