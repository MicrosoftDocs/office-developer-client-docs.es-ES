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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e7607a57da5b618a20d6c8e360c7e3cb4f933856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432236"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Busca un equivalente de ruta de acceso local a la ruta de acceso de convención de nomenclatura universal (UNC) determinada. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a>Parameters

 _szUNC_
  
> [in] Ruta de acceso con el \\ formato [ _servidor_] \[ _compartir_] \[ _ruta_] de un archivo o directorio.
    
 _szLocal_
  
> [salida] Ruta de acceso con el formato [ _unidad:_] ruta ] del \[ mismo archivo o directorio que para el _parámetro szUNC._ 
    
 _cchLocal_
  
> [in] Tamaño del búfer de la cadena de salida.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Se ha localizado correctamente una ruta de acceso local.
    
MAPI_E_TOO_BIG
  
>  _szLocal_ no era lo suficientemente grande como para contener el resultado. 
    
S_FALSE
  
> La cadena UNC ya era una ruta de acceso local.
    
MAPI_E_NOT_FOUND
  
> No se encontró una ruta de acceso local.
    
## <a name="see-also"></a>Vea también



[ScUNCFromLocalPath](scuncfromlocalpath.md)

