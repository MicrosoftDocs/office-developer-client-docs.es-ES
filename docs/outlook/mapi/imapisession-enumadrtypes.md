---
title: IMAPISessionEnumAdrTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.EnumAdrTypes
api_type:
- COM
ms.assetid: 9a3702a4-8a6b-4c0c-a90f-02be3a2bfa05
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3b2e41c4b1bfc4879717df0c73bbcd45a724ca60
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439292"
---
# <a name="imapisessionenumadrtypes"></a>IMAPISession::EnumAdrTypes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Obsoleto. Devuelve los tipos de direcciones que pueden controlar todos los proveedores de transporte de la sesión. 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Máscara de bits de marcas que indica el formato de los tipos de direcciones devueltos. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Los tipos de dirección están en formato Unicode. Si no MAPI_UNICODE marca, los tipos de dirección están en formato ANSI.
    
 _lpcAdrTypes_
  
> [salida] Puntero a un recuento de tipos de direcciones a los que apunta el parámetro _lpppszAdrTypes._ 
    
 _lpppszAdrTypes_
  
> [salida] Puntero a una matriz de punteros a tipos de direcciones.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los tipos de dirección se recuperaron correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISession::EnumAdrTypes** devuelve una lista de los tipos de direcciones que pueden controlar todos los proveedores de transporte activos en la sesión. Los tipos de dirección para los proveedores de transporte que no están cargados actualmente no se incluyen en la lista. Los proveedores de transporte se registran para controlar uno o más tipos de direcciones cuando MAPI llama a su [método IXPLogon::AddressTypes.](ixplogon-addresstypes.md) 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame [a MAPIFreeBuffer](mapifreebuffer.md) para liberar la matriz de cadenas a la que apunta el parámetro _lpppszAdrTypes._ 
  
## <a name="see-also"></a>Consulte también



[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

