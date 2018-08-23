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
ms.openlocfilehash: faba91d813d27f7ea45e978724ce0d4707803cba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590109"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="see-also"></a>Recursos adicionales



[ScLocalPathFromUNC](sclocalpathfromunc.md)

