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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351250"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Busca una ruta de acceso local equivalente a la ruta de acceso UNC (Convención de nomenclatura universal) dada. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
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
  
> a Una ruta de acceso con \\el formato [ _servidor_]\[ _RecursoCompartido_]\[ _ruta_] de un archivo o directorio.
    
 _szLocal_
  
> contempla Una ruta de acceso con el formato [ _unidad:_]\[ _ruta de acceso_] del mismo archivo o directorio que para el parámetro _szUNC_ . 
    
 _cchLocal_
  
> a Tamaño del búfer para la cadena de salida.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Una ruta de acceso local se encontró correctamente.
    
MAPI_E_TOO_BIG
  
>  _szLocal_ no era lo suficientemente grande como para contener el resultado. 
    
S_FALSE
  
> La cadena UNC ya era una ruta de acceso local.
    
MAPI_E_NOT_FOUND
  
> No se encontró una ruta de acceso local.
    
## <a name="see-also"></a>Vea también



[ScUNCFromLocalPath](scuncfromlocalpath.md)

