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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434252"
---
# <a name="iablogongetlasterror"></a>IABLogon::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior del proveedor de libreta de direcciones. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parámetros

 _hResult_
  
> [entrada] Identificador del valor de error generado en la llamada al método anterior.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla el tipo de cadenas devueltas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas de la **estructura MAPIERROR** devueltas en el parámetro  _lppMAPIError_ están en formato Unicode. Si no MAPI_UNICODE marca, las cadenas están en formato ANSI. 
    
 _lppMAPIError_
  
> [salida] Puntero a un puntero a una **estructura MAPIERROR** que contiene información de versión, componente y contexto del error. El  _parámetro lppMAPIError_ se puede establecer en NULL si el proveedor no puede proporcionar una **estructura MAPIERROR** con la información adecuada. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció MAPI_UNICODE marca y el proveedor de libreta de direcciones no admite Unicode o MAPI_UNICODE no se estableció y el proveedor de libreta de direcciones solo admite Unicode.
    
## <a name="remarks"></a>Comentarios

Los proveedores de libretas de direcciones implementan **el método GetLastError** para proporcionar información sobre una llamada de método anterior que ha fallado. Los autores de llamadas pueden proporcionar a sus usuarios información detallada sobre el error incluyendo los datos de la estructura **MAPIERROR** en un cuadro de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la estructura **MAPIERROR** a la que apunta el parámetro  _lppMAPIError_ si el proveedor de libreta de direcciones proporciona la estructura y sólo si **GetLastError** devuelve S_OK. A veces, el proveedor de libreta de direcciones no puede determinar cuál fue el último error o no tiene nada más que informar sobre el error. En esta situación, el proveedor de libreta de direcciones devuelve un puntero a NULL  _en lppMAPIError_ en su lugar. 
  
Para obtener más información acerca **del método GetLastError,** vea [errores extendidos de MAPI.](mapi-extended-errors.md)
  
## <a name="see-also"></a>Consulte también



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

