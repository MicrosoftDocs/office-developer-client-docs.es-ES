---
title: ScLocalPathFromUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScLocalPathFromUNC
api_type:
- COM
ms.assetid: ef5eb5c6-251e-4a3a-8855-7c28804a29ab
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: e94692ac4eb401109fcb522e6224c8748bef37f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820587"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**Se aplica a**: Outlook 
  
Busca a un homólogo de ruta de acceso local a la ruta (UNC) de la convención de nomenclatura universal determinado. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a>Sintaxis

 _szUNC_
  
> [entrada] Una ruta de acceso en el formato \\[ _servidor_]\[ _Compartir_]\[ _ruta de acceso_] de un archivo o directorio.
    
 _szLocal_
  
> [out] Una ruta de acceso en el formato [ _unidad:_]\[ _ruta de acceso_] del mismo archivo o directorio que para el parámetro _szUNC_ . 
    
 _cchLocal_
  
> [entrada] Tamaño del búfer para la cadena de salida.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Una ruta de acceso local se encuentra correctamente.
    
MAPI_E_TOO_BIG
  
>  _szLocal_ no es lo suficientemente grande como para contener el resultado. 
    
S_FALSE
  
> La cadena UNC ya era una ruta de acceso local.
    
MAPI_E_NOT_FOUND
  
> No se encontró la ruta de acceso local.
    
## <a name="see-also"></a>Ver también



[ScUNCFromLocalPath](scuncfromlocalpath.md)

