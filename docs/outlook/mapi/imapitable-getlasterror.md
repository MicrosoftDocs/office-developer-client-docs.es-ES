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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: b8ee83ad550106ae82f3308b9ef5692f66f5f5b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817591"
---
# <a name="imapitablegetlasterror"></a>IMAPITable::GetLastError

  
  
**Se aplica a**: Outlook 
  
Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior en la tabla. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Sintaxis

 _hResult_
  
> [entrada] HRESULT que contiene el error generado en la llamada al método anterior.
    
 _ulFlags_
  
> [entrada] Máscara de bits de indicadores que controla el tipo de las cadenas devueltas. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las cadenas en la estructura **MAPIERROR** devuelta en el parámetro _lppMAPIError_ están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI. 
    
 _lppMAPIError_
  
> [out] Puntero a un puntero a la estructura **MAPIERROR** devuelta que contiene información de versión, el componente y el contexto para el error. El parámetro _lppMAPIError_ se puede establecer en NULL si no se puede proporcionar una estructura **MAPIERROR** con la información apropiada. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación sólo es compatible con Unicode.
    
## <a name="remarks"></a>Notas

El método **IMAPITable::GetLastError** devuelve información detallada, si está disponible, acerca de una llamada al método anterior con errores. Esta información se puede mostrar en un mensaje o un cuadro de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llamar a **GetLastError** cada vez que necesite mostrar información sobre un error al usuario. 
  
Se puede hacer uso de la [MAPIERROR](mapierror.md) estructura indicada por el parámetro _lppMAPIError_ si el objeto de tabla suministra uno sólo si **GetLastError** devuelve S_OK. En ocasiones, la implementación de la tabla no puede determinar qué era el último error o no tiene nada más para informar sobre el error. En esta situación, el puntero en _lppMAPIError_ se establece en NULL. 
  
Para liberar toda la memoria asignada para la estructura **MAPIERROR** , llame a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para obtener más información acerca del método **GetLastError** , vea [Errores de MAPI extendida](mapi-extended-errors.md).
  
## <a name="see-also"></a>Ver también



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)

