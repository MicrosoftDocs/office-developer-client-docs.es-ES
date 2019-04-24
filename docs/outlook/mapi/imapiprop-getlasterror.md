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
ms.openlocfilehash: 8c31cbf0472d3d64c7327fcfc80480ef27a1638e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342052"
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

## <a name="parameters"></a>Parameters

 _Valores_
  
> a Identificador del código de error generado en la llamada al método anterior.
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que indica el formato del texto devuelto en la estructura **MAPIERROR** apuntado por _lppMAPIError_. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas deben estar en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas deben estar en formato ANSI.
    
 _lppMAPIError_
  
> contempla Un puntero a un puntero a la estructura **MAPIERROR** que contiene información sobre la versión, el componente y el contexto del error. El parámetro _lppMAPIError_ puede establecerse en NULL si no hay información de error que se va a devolver. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se devolvió la información del error.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIProp:: GetLastError** proporciona información sobre una llamada a un método anterior que produjo un error. Los clientes pueden proporcionar a sus usuarios información detallada acerca del error al incluir los datos de la estructura **MAPIERROR** en un cuadro de diálogo. 
  
Todas las implementaciones de **GetLastError** que proporciona MAPI son implementaciones ANSI, excepto para la implementación de [IAddrBook](iaddrbookimapiprop.md) . El método **GetLastError** incluido con **IAddrBook** admite Unicode. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Los detalles de la implementación de este método por un proveedor de transporte remoto y los mensajes que devuelve este método son para el proveedor de transporte, ya que las condiciones de error específicas que conducen a varios valores HRESULT serán diferentes para el transporte diferente. doctores.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la estructura **MAPIERROR** apuntado por el parámetro _LppMAPIError_ , si **GetLastError** sólo proporciona uno, solo si el valor devuelto es S_OK. A veces, **GetLastError** no puede determinar qué ha sido el último error o no tiene nada más para informar sobre el error. En esta situación, un puntero a NULL se devuelve en _lppMAPIError_ en su lugar. 
  
Para liberar la memoria de la estructura **MAPIERROR** , llame a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para obtener más información sobre el método **GetLastError** , vea [errores extendidos de MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>Vea también



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Errores extendidos de MAPI](mapi-extended-errors.md)

