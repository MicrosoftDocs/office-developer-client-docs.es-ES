---
title: IMAPISupportOpenAddressBook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenAddressBook
api_type:
- COM
ms.assetid: d8da8be1-3efe-410a-bcce-49e522602d80
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 26550691ef959fa7cefa83827dd1391538bd2d38
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588177"
---
# <a name="imapisupportopenaddressbook"></a>IMAPISupport::OpenAddressBook

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a la libreta de direcciones.
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>Parámetros

 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la libreta de direcciones. Los valores válidos son NULL, que indica la interfaz de la libreta de direcciones estándar [IAddrBook](iaddrbookimapiprop.md)y IID_IAddrBook.
    
 _ulFlags_
  
> Reservado; debe ser cero.
    
 _lppAdrBook_
  
> [out] Un puntero a un puntero a la libreta de direcciones.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Le ha proporcionado el acceso a la libreta de direcciones.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se ha realizado correctamente, pero no se podrían cargados uno o más proveedores de libreta de direcciones. Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta. Para probar esta advertencia, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::OpenAddressBook** se implementa para todos los objetos de soporte técnico de proveedor de servicio. Proveedores de servicios, normalmente acoplado mensaje almacén y los proveedores de transporte, llame a **OpenAddressBook** para obtener acceso a la libreta de direcciones. El puntero **IAddrBook** devuelto se puede usar para una gran variedad de tareas de la libreta de direcciones, incluida la apertura de contenedores de libretas de direcciones, búsqueda de usuarios de mensajería y presentación de los cuadros de diálogo de dirección. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **OpenAddressBook** puede devolver MAPI_W_ERRORS_RETURNED si no puede cargar uno o varios de los proveedores de la libreta de direcciones en el perfil actual. Este valor es una advertencia y se debe tratar la llamada como correcta. Incluso si todos los proveedores de la libreta de direcciones no se pudo cargar, **OpenAddressBook** aún se realiza correctamente, devolver MAPI_W_ERRORS_RETURNED y un puntero **IAddrBook** en el parámetro _lppAdrBook_ . Debido a que **OpenAddressBook** siempre devuelve un puntero **IAddrBook** válido, debe liberar cuando haya terminado de usarlo. 
  
Si no se pudo cargar uno o más proveedores de libreta de direcciones, llame a [IMAPISupport::GetLastError](imapisupport-getlasterror.md) para obtener una estructura [MAPIERROR](mapierror.md) que contiene información sobre los proveedores que no se ha cargado. 
  
## <a name="see-also"></a>Recursos adicionales



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

