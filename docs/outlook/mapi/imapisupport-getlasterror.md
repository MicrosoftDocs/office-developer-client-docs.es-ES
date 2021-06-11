---
title: IMAPISupportGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c34c175c43ada03e982f08a27f675448ea24a567
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438550"
---
# <a name="imapisupportgetlasterror"></a>IMAPISupport::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error del objeto de soporte técnico anterior. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in] Identificador del valor de error generado en la llamada al método anterior para el objeto de soporte técnico.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla el tipo de cadenas devueltas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas de la **estructura MAPIERROR** devueltas en el parámetro  _lppMAPIError_ están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI. 
    
 _lppMAPIError_
  
> [salida] Puntero a un puntero a la estructura **MAPIERROR** que contiene información de versión, componente y contexto del error. El  _parámetro lppMAPIError_ se puede establecer en NULL si no se puede proporcionar una estructura **MAPIERROR** con la información de error adecuada. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realiza correctamente y devuelve el valor o los valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> La marca MAPI_UNICODE se estableció y MAPI no admite Unicode, o MAPI_UNICODE no se estableció y MAPI solo admite Unicode.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::GetLastError** se implementa para todos los objetos de soporte técnico. Los autores de llamadas pueden proporcionar a sus usuarios información detallada sobre el error al incluir los datos de la estructura **MAPIERROR** en un cuadro de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar el puntero a la estructura **MAPIERROR,** si MAPI proporciona uno, en el parámetro  _lppMAPIError_ solo si **GetLastError** devuelve S_OK. A veces MAPI no puede determinar cuál fue el último error o no tiene nada más que informar sobre el error. En esta situación,  _lppMAPIError_ devuelve un puntero a NULL en su lugar. 
  
Para obtener más información acerca **del método GetLastError,** vea [Mapi Extended Errors](mapi-extended-errors.md).
  
Para liberar toda la memoria asignada por MAPI, llame a la [función MAPIFreeBuffer](mapifreebuffer.md) para la estructura **MAPIERROR** devuelta. 
  
## <a name="see-also"></a>Vea también



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Errores extendidos mapi](mapi-extended-errors.md)

