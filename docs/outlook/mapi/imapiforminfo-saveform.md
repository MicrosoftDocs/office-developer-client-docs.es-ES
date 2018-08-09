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
ms.openlocfilehash: 5e2d757fe329f9a57447723d72a859c7d82fc2b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817299"
---
# <a name="imapiforminfosaveform"></a>IMAPIFormInfo::SaveForm

  
  
**Hace referencia a**: Outlook 
  
Guarda una descripción de un formulario determinado en un archivo de configuración.
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a>Parámetros

 _szFileName_
  
> [entrada] Una cadena que nombra el archivo de mensaje de descripción del formulario donde se ha guardado su descripción. Este nombre de archivo debe tener la extensión de .fdm.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_EXTENDED_ERROR 
  
> No se pudo escribir el archivo de configuración. Para obtener la estructura [MAPIERROR](mapierror.md) que está asociada con el error, llame al método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) . 
    
MAPI_E_NO_SUPPORT 
  
> Probablemente se ha llamado **SaveForm** para guardar un formulario en el contenedor de forma local. **SaveForm** no se admite en el contenedor de forma local. 
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente de llaman al método **IMAPIFormInfo::SaveForm** para guardar una descripción del formulario actual en el archivo que tiene el nombre de archivo determinado. **SaveForm** crea un archivo de configuración. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede volver a instalar formularios seleccionándolos en una lista de mensajes de descriptor de formulario en un cuadro de diálogo que para mostrar de los proveedores de biblioteca de formularios. La extensión recomendada para los mensajes de descriptor de formulario es .fdm.
  
Llamar al método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) si **SaveForm** devuelve MAPI_E_EXTENDED_ERROR y comprobar la estructura **MAPIERROR** devuelta para determinar la condición que provocó el error. 
  
## <a name="see-also"></a>Vea también



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

