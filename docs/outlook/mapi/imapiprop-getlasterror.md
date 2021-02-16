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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435834"
---
# <a name="imapipropgetlasterror"></a>IMAPIProp::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parámetros

 _hResult_
  
> [entrada] Identificador del código de error generado en la llamada al método anterior.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que indica el formato del texto devuelto en la estructura **MAPIERROR** a la que  _apunta lppMAPIError_. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas deben estar en formato Unicode. Si no MAPI_UNICODE marca, las cadenas deben estar en formato ANSI.
    
 _lppMAPIError_
  
> [salida] Puntero a un puntero a la estructura **MAPIERROR** que contiene información de versión, componente y contexto del error. El  _parámetro lppMAPIError_ se puede establecer en NULL si no hay información de error que devolver. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha devuelto la información de error.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció MAPI_UNICODE marca y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.
    
## <a name="remarks"></a>Comentarios

El **método IMAPIProp::GetLastError** proporciona información acerca de una llamada de método anterior que ha fallado. Los clientes pueden proporcionar a sus usuarios información detallada sobre el error incluyendo los datos de la estructura **MAPIERROR** en un cuadro de diálogo. 
  
Todas las implementaciones de **GetLastError** proporcionadas por MAPI son implementaciones ANSI, excepto para la implementación [de IAddrBook.](iaddrbookimapiprop.md) El **método GetLastError** incluido con **IAddrBook admite** Unicode. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Los detalles de la implementación de este método por parte de un proveedor de transporte remoto y los mensajes que devuelve este método están en función del proveedor de transporte, ya que las condiciones de error concretas que llevan a varios valores HRESULT serán diferentes para distintos proveedores de transporte.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la estructura **MAPIERROR** a la que apunta el parámetro  _lppMAPIError,_ si **GetLastError** proporciona uno, solo si el valor devuelto es S_OK. A **veces, GetLastError** no puede determinar cuál fue el último error o no tiene nada más que informar sobre el error. En esta situación, se devuelve un puntero a NULL  _en lppMAPIError_ en su lugar. 
  
Para liberar la memoria de la **estructura MAPIERROR,** llame a la [función MAPIFreeBuffer.](mapifreebuffer.md) 
  
Para obtener más información acerca **del método GetLastError,** vea [errores extendidos de MAPI.](mapi-extended-errors.md)
  
## <a name="see-also"></a>Consulte también



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Errores extendidos de MAPI](mapi-extended-errors.md)

