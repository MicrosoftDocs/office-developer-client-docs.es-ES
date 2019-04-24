---
title: IABLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetLastError
api_type:
- COM
ms.assetid: d157e29e-7731-4e47-b4a7-e8622b223001
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 311299b00143667b3f2fb22bd7be6c3a52c7141d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349031"
---
# <a name="iablogongetlasterror"></a>IABLogon::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior del proveedor de la libreta de direcciones. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _Valores_
  
> a Identificador del valor de error generado en la llamada al método anterior.
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla el tipo de cadenas devueltas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas de la estructura **MAPIERROR** devueltas en el parámetro _lppMAPIError_ están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI. 
    
 _lppMAPIError_
  
> contempla Un puntero a un puntero a una estructura **MAPIERROR** que contiene información sobre la versión, el componente y el contexto del error. El parámetro _lppMAPIError_ puede establecerse en NULL si el proveedor no puede proporcionar una estructura **MAPIERROR** con la información adecuada. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y el proveedor de la libreta de direcciones no admite Unicode, o no se estableció MAPI_UNICODE y el proveedor de la libreta de direcciones solo admite Unicode.
    
## <a name="remarks"></a>Comentarios

Los proveedores de la libreta de direcciones implementan el método **GetLastError** para proporcionar información sobre una llamada a un método anterior que no se ha realizado correctamente. Los autores de llamadas pueden proporcionar a sus usuarios información detallada acerca del error al incluir los datos de la estructura **MAPIERROR** en un cuadro de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la estructura **MAPIERROR** apuntado por el parámetro _lppMAPIError_ si el proveedor de la libreta de direcciones proporciona la estructura y solo si **GetLastError** Devuelve S_OK. A veces, el proveedor de la libreta de direcciones no puede determinar qué ha sido el último error o no tiene nada más para informar sobre el error. En esta situación, el proveedor de la libreta de direcciones devuelve un puntero a NULL en _lppMAPIError_ en su lugar. 
  
Para obtener más información sobre el método **GetLastError** , vea [errores extendidos de MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>Vea también



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

