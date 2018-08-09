---
title: ScUNCFromLocalPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScUNCFromLocalPath
api_type:
- COM
ms.assetid: cc4abf1a-c08c-4462-9d7c-6af506dc07c9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 667eda2a018d2a5d712950a31e05ec0ba9bb32ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820603"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**Hace referencia a**: Outlook 
  
Busca a un homólogo de ruta de acceso UNC (convención) nomenclatura universal a la ruta de acceso local determinado.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a>Parámetros

 _szLocal_
  
> [entrada] Una ruta de acceso en el formato [ _unidad:_]\[ _ruta de acceso_] de un archivo o directorio.
    
 _szUNC_
  
> [out] Una ruta de acceso en el formato \\[ _servidor_]\[ _Compartir_]\[ _ruta de acceso_] del mismo archivo o directorio que para el parámetro _szLocal_ . 
    
 _cchUNC_
  
> [entrada] Tamaño del búfer para la cadena de salida.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> El equivalente de la ruta de acceso UNC se encuentra correctamente.
    
MAPI_E_INVALID_PARAMETER
  
> Uno o más parámetros no son válidos.
    
MAPI_E_TOO_BIG
  
>  _szUNC_ no es lo suficientemente grande como para contener el resultado. 
    
S_FALSE
  
> La ruta de acceso local ya era una cadena UNC.
    
## <a name="see-also"></a>Vea también



[ScLocalPathFromUNC](sclocalpathfromunc.md)

