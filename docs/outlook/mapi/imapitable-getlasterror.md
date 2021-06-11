---
title: IMAPITableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetLastError
api_type:
- COM
ms.assetid: 832e2c18-ddba-4d18-a391-710d21fe23e6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2444ea7e05367423e7920be3a871c2ab68aad76d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419005"
---
# <a name="imapitablegetlasterror"></a>IMAPITable::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior en la tabla. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in] HRESULT que contiene el error generado en la llamada al método anterior.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla el tipo de las cadenas devueltas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas de la **estructura MAPIERROR** devueltas en el parámetro  _lppMAPIError_ están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI. 
    
 _lppMAPIError_
  
> [salida] Puntero a un puntero a la estructura **MAPIERROR** devuelta que contiene información de versión, componente y contexto del error. El  _parámetro lppMAPIError_ se puede establecer en NULL si no se puede proporcionar una estructura **MAPIERROR** con la información adecuada. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> La marca MAPI_UNICODE se estableció y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.
    
## <a name="remarks"></a>Comentarios

El **método IMAPITable::GetLastError** devuelve información detallada, si está disponible, acerca de una llamada al método anterior que falló. Esta información se puede mostrar en un mensaje o en un cuadro de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llama **a GetLastError** siempre que necesites mostrar información sobre un error al usuario. 
  
Puede usar la estructura [MAPIERROR](mapierror.md) a la que apunta el parámetro  _lppMAPIError_ si el objeto table proporciona uno solo si **GetLastError** devuelve S_OK. A veces, la implementación de la tabla no puede determinar cuál fue el último error o no tiene nada más que informar sobre el error. En esta situación, el puntero de  _lppMAPIError_ se establece en NULL. 
  
Para liberar toda la memoria asignada a la **estructura MAPIERROR,** llame a la [función MAPIFreeBuffer.](mapifreebuffer.md) 
  
Para obtener más información acerca **del método GetLastError,** vea [Mapi Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Vea también



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

