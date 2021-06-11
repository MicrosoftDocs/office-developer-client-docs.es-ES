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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428749"
---
# <a name="imapiforminfosaveform"></a>IMAPIFormInfo::SaveForm

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Guarda una descripción de un formulario determinado en un archivo de configuración.
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a>Parameters

 _szFileName_
  
> [in] Cadena que nombra el archivo de mensaje de descripción del formulario donde se guarda su descripción. Este nombre de archivo debe tener la extensión .fdm.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_EXTENDED_ERROR 
  
> No se pudo escribir el archivo de configuración. Para obtener la [estructura MAPIERROR](mapierror.md) asociada al error, llame al [método IMAPIProp::GetLastError.](imapiprop-getlasterror.md) 
    
MAPI_E_NO_SUPPORT 
  
> **Probablemente se llamó** a SaveForm para guardar un formulario en el contenedor de formularios local. **SaveForm** no se admite en el contenedor de formularios local. 
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente llaman al método **IMAPIFormInfo::SaveForm** para guardar una descripción del formulario actual en el archivo que tiene el nombre de archivo especificado. **SaveForm** crea un archivo de configuración. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede volver a instalar los formularios seleccionándolos en una lista de mensajes descriptores de formulario en un cuadro de diálogo que muestran los proveedores de bibliotecas de formularios. La extensión recomendada para los mensajes de descriptor de formulario es .fdm.
  
Llame al [método IMAPIProp::GetLastError](imapiprop-getlasterror.md) si **SaveForm** devuelve MAPI_E_EXTENDED_ERROR y compruebe la estructura **MAPIERROR** devuelta para determinar la condición que provocó el error. 
  
## <a name="see-also"></a>Vea también



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

