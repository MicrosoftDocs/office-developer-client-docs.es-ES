---
title: IMAPIFormInfoSaveForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.SaveForm
api_type:
- COM
ms.assetid: 18a10f14-0795-4d4d-b590-f4cef4f2902a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 391ea3ef4f44db2a9d007241232f58db27647ba2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321717"
---
# <a name="imapiforminfosaveform"></a>IMAPIFormInfo::SaveForm

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Guarda una descripción de un formulario en particular en un archivo de configuración.
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a>Parameters

 _szFileName_
  
> a Una cadena que nombra el archivo de mensaje de Descripción del formulario donde se guarda su descripción. Este nombre de archivo debe tener la extensión. FDM.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_EXTENDED_ERROR 
  
> No se pudo escribir el archivo de configuración. Para obtener la estructura [MAPIERROR](mapierror.md) asociada con el error, llame al método [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) . 
    
MAPI_E_NO_SUPPORT 
  
> Es probable que se haya llamado a **SaveForm** para guardar un formulario en el contenedor de formulario local. **SaveForm** no es compatible con el contenedor de formulario local. 
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente llaman al método **IMAPIFormInfo:: SaveForm** para guardar una descripción del formulario actual en el archivo que tiene el nombre de archivo especificado. **SaveForm** crea un archivo de configuración. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede reinstalar formularios seleccionándolos en una lista de mensajes de descriptor de formulario en un cuadro de diálogo que muestren los proveedores de bibliotecas de formularios. La extensión recomendada para los mensajes de descriptor de formulario es. FDM.
  
Llame al método [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) si **SaveForm** devuelve MAPI_E_EXTENDED_ERROR y Compruebe la estructura devuelta **MAPIERROR** para determinar la condición que provocó el error. 
  
## <a name="see-also"></a>Vea también



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

