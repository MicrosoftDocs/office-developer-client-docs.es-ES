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
ms.openlocfilehash: bead72ab2b394634217c9ae219a03a98752ef27d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817089"
---
# <a name="iablogongetlasterror"></a>IABLogon::GetLastError

  
  
**Hace referencia a**: Outlook 
  
Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de proveedor de la libreta de direcciones anterior. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parámetros

 _hResult_
  
> [entrada] Un identificador para el valor de error generado en la llamada al método anterior.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las cadenas en la estructura **MAPIERROR** devuelta en el parámetro _lppMAPIError_ están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI. 
    
 _lppMAPIError_
  
> [out] Un puntero a un puntero a una estructura **MAPIERROR** que contiene información de versión, el componente y el contexto para el error. El parámetro _lppMAPIError_ se puede establecer en NULL si el proveedor no puede proporcionar una estructura **MAPIERROR** con la información apropiada. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y el proveedor de la libreta de direcciones no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y el proveedor de la libreta de direcciones admite sólo Unicode.
    
## <a name="remarks"></a>Comentarios

Los proveedores de la libreta de direcciones implementan el método **GetLastError** para proporcionar información acerca de una llamada de método anteriores que no se pudo. Los autores de llamadas pueden proporcionar a sus usuarios con información detallada sobre el error mediante la inclusión de los datos de la estructura **MAPIERROR** en un cuadro de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la estructura **MAPIERROR** indicada por el parámetro _lppMAPIError_ si el proveedor de la libreta de direcciones proporciona la estructura y sólo si **GetLastError** devuelve S_OK. En ocasiones, el proveedor de la libreta de direcciones no puede determinar qué era el último error o no tiene nada más para informar sobre el error. En esta situación, el proveedor de la libreta de direcciones devuelve un puntero a NULL en _lppMAPIError_ en su lugar. 
  
Para obtener más información acerca del método **GetLastError** , vea [Errores de MAPI extendida](mapi-extended-errors.md).
  
## <a name="see-also"></a>Vea también



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

