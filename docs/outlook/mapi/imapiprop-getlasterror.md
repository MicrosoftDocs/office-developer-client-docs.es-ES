---
title: IMAPIPropGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f67dbb4d883f2f66099f2e2b9bc06b6c35b98236
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575836"
---
# <a name="imapipropgetlasterror"></a>IMAPIProp::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parámetros

 _hResult_
  
> [entrada] Un identificador para el código de error generado en la llamada al método anterior.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de marcadores que indica el formato para el texto devuelto en la estructura **MAPIERROR** que señala _lppMAPIError_. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las cadenas deben estar en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas deben estar en formato ANSI.
    
 _lppMAPIError_
  
> [out] Un puntero a un puntero a la estructura **MAPIERROR** que contiene información de versión, el componente y el contexto para el error. El parámetro _lppMAPIError_ se puede establecer en NULL si no hay ninguna información de error que devolver. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se devuelve la información de error.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIProp::GetLastError** proporciona información acerca de una llamada de método anteriores que no se pudo. Los clientes pueden proporcionar a sus usuarios con información detallada sobre el error mediante la inclusión de los datos de la estructura **MAPIERROR** en un cuadro de diálogo. 
  
Todas las implementaciones de **GetLastError** proporcionado por MAPI son implementaciones de ANSI, excepto para la implementación de [IAddrBook](iaddrbookimapiprop.md) . El método **GetLastError** incluido con **IAddrBook** es compatible con Unicode. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Los detalles de un control remoto de transporte del proveedor de implementación de este método y ¿cuáles son los mensajes de que este método devuelve hasta el proveedor de transporte, debido a que las condiciones de error concretos que conducen a distintos valores HRESULT será diferentes para el transporte diferente proveedores.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la estructura **MAPIERROR** indicada por el parámetro _lppMAPIError_ , si **GetLastError** proporciona uno, sólo si el valor devuelto es S_OK. A veces **GetLastError** no puede determinar qué era el último error o no tiene nada más para informar sobre el error. En esta situación, se devuelve un puntero a NULL en _lppMAPIError_ en su lugar. 
  
Para liberar la memoria para la estructura **MAPIERROR** , llame a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para obtener más información acerca del método **GetLastError** , vea [Errores de MAPI extendida](mapi-extended-errors.md).
  
## <a name="see-also"></a>Recursos adicionales



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MAPI extendida de errores](mapi-extended-errors.md)

