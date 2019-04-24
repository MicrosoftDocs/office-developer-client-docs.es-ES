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
  
Devuelve la ruta de acceso al archivo Mapi32. dll privado.
  
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
  
> a La clave de MSIComponentID REG que se describe en la [configuración del registro de código auxiliar de Mapi32. dll](https://msdn.microsoft.com/library/dd162409.aspx).
    
 _szQualifier_
  
> a La subclave MSIApplicationLCID o MSIOfficeLCID que se describe en [elegir una versión específica de MAPI que se va a cargar](how-to-choose-a-specific-version-of-mapi-to-load.md). Los llamadores pueden pasar **null** si no hay ningún calificador. 
    
 _szDllPath_
  
> a La ruta de acceso al privado Mapi32. dll, que tiene la funcionalidad completa de MAPI (las mismas exportaciones que el archivo Mapi32. dll).
    
 _cchBufferSize_
  
> a El tamaño de _szDllPath_, en caracteres.
    
 _fInstall_
  
> a Indica a MAPI que instale el componente Mapi32. dll privado si no está presente.
    
## <a name="return-value"></a>Valor devuelto

 **true**
  
> Se encontró la ruta de acceso.
    
 **false**
  
> No se encontró la ruta de acceso.
    
## <a name="remarks"></a>Comentarios

Use la función **FGetComponentPath** cuando necesite obtener la ruta de acceso al archivo Mapi32. dll privado. 
  
## <a name="see-also"></a>Vea también



[Elegir una versión específica de MAPI para cargar](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Configuración del registro de código auxiliar de Mapi32. dll](https://msdn.microsoft.com/library/dd162409.aspx)

