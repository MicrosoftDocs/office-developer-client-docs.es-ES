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
ms.openlocfilehash: b53dd9aaaf18dba5c7e33e0bc7d984de757634a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414539"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Busca un equivalente de ruta de acceso de convención de nomenclatura universal (UNC) a la ruta de acceso local determinada.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a>Parameters

 _szLocal_
  
> [in] Ruta de acceso con el formato [ _unidad:_] \[ _ruta_] de un archivo o directorio.
    
 _szUNC_
  
> [salida] Una ruta de acceso con el formato [ servidor ] compartir ] ruta ] del \\ mismo archivo o directorio que para el parámetro  \[  \[  _szLocal._ 
    
 _cchUNC_
  
> [in] Tamaño del búfer de la cadena de salida.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> El equivalente de ruta de acceso UNC se ha localizado correctamente.
    
MAPI_E_INVALID_PARAMETER
  
> Uno o varios parámetros no son válidos.
    
MAPI_E_TOO_BIG
  
>  _szUNC_ no era lo suficientemente grande como para contener el resultado. 
    
S_FALSE
  
> La ruta de acceso local ya era una cadena UNC.
    
## <a name="see-also"></a>Vea también



[ScLocalPathFromUNC](sclocalpathfromunc.md)

