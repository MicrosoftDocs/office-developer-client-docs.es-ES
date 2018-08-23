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
ms.openlocfilehash: fa39128ffaaaa3530b74a660c14971834a99561b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566351"
---
# <a name="fgetcomponentpath"></a>FGetComponentPath

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve la ruta de acceso para el archivo Mapi32.dll privada.
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a>Parámetros

 _szComponent_
  
> [entrada] La clave del registro MSIComponentID se describe en [Configuración de Mapi32.dll código auxiliar del registro](http://msdn.microsoft.com/en-us/library/dd162409.aspx).
    
 _szQualifier_
  
> [entrada] La subclave MSIApplicationLCID o MSIOfficeLCID que se describe en [Elija una versión específica de MAPI para carga](how-to-choose-a-specific-version-of-mapi-to-load.md). Los autores de llamadas pueden pasar **null** si no hay ningún calificador. 
    
 _szDllPath_
  
> [entrada] La ruta de acceso para el archivo Mapi32.dll privada, que tiene la funcionalidad completa de MAPI (las exportaciones mismas como el archivo Mapi32.dll).
    
 _cchBufferSize_
  
> [entrada] El tamaño de _szDllPath_, en caracteres.
    
 _fInstall_
  
> [entrada] Indica a MAPI para instalar el componente de Mapi32.dll privado si está presente.
    
## <a name="return-value"></a>Valor devuelto

 **True**
  
> Se encontró la ruta de acceso.
    
 **False**
  
> No se encontró la ruta de acceso.
    
## <a name="remarks"></a>Comentarios

Use la función **FGetComponentPath** cuando se necesita para obtener la ruta de acceso para el archivo Mapi32.dll privada. 
  
## <a name="see-also"></a>Recursos adicionales



[Elegir una versión específica de MAPI para cargar](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Configuración de Mapi32.dll código auxiliar del registro](http://msdn.microsoft.com/en-us/library/dd162409.aspx)

