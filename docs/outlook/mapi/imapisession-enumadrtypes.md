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
ms.openlocfilehash: 6bd13eb7180302a5ab770586cf36856ca5a22676
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817433"
---
# <a name="imapisessionenumadrtypes"></a>IMAPISession::EnumAdrTypes

  
  
**Hace referencia a**: Outlook 
  
En desuso. Devuelve los tipos de direcciones que se pueden controlar por todos los proveedores de transporte en la sesión. 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de marcadores que indica el formato para los tipos de dirección devuelta. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Los tipos de direcciones están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., los tipos de direcciones están en formato ANSI.
    
 _lpcAdrTypes_
  
> [out] Un puntero a un recuento de los tipos de dirección indicada por el parámetro _lpppszAdrTypes_ . 
    
 _lpppszAdrTypes_
  
> [out] Un puntero a una matriz de punteros a tipos de direcciones.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los tipos de direcciones se recuperaron correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession:: EnumAdrTypes** devuelve una lista de los tipos de direcciones que se pueden controlar por todos los proveedores de transporte activo en la sesión. No se incluyen los tipos de direcciones para los proveedores de transporte que no están cargados actualmente en la lista. Registrar los proveedores de transporte para controlar uno o varios tipos de direcciones cuando MAPI llama a su método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llamar a [MAPIFreeBuffer](mapifreebuffer.md) para liberar la matriz de cadena indicada por el parámetro _lpppszAdrTypes_ . 
  
## <a name="see-also"></a>Vea también



[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

