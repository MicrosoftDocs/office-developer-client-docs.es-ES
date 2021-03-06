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
ms.openlocfilehash: 47a62b331ff9f1c96576d42797ebb23ed61cd362
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416884"
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

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la libreta de direcciones. Los valores válidos son NULL, que indica la interfaz de libreta de direcciones estándar [IAddrBook](iaddrbookimapiprop.md)y IID_IAddrBook.
    
 _ulFlags_
  
> Reservado; debe ser cero.
    
 _lppAdrBook_
  
> [salida] Puntero a un puntero a la libreta de direcciones.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se proporcionó acceso a la libreta de direcciones.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se ha hecho correctamente, pero no se pudo cargar uno o varios proveedores de libreta de direcciones. Cuando se devuelve esta advertencia, la llamada debe controlarse como correcta. Para probar esta advertencia, use la **HR_FAILED** macro. Para obtener más información, vea [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::OpenAddressBook** se implementa para todos los objetos de soporte del proveedor de servicios. Los proveedores de servicios, normalmente proveedores de transporte y almacén de mensajes estrechamente acoplados, llaman a **OpenAddressBook** para obtener acceso a la libreta de direcciones. El puntero **IAddrBook** devuelto se puede usar para una variedad de tareas de libreta de direcciones, como abrir contenedores de libreta de direcciones, buscar usuarios de mensajería y mostrar cuadros de diálogo de direcciones. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **OpenAddressBook** puede devolver MAPI_W_ERRORS_RETURNED si no puede cargar uno o varios de los proveedores de libreta de direcciones en el perfil actual. Este valor es una advertencia y debe tratar la llamada como correcta. Incluso si todos los proveedores de libreta de direcciones no se pudieron cargar, **OpenAddressBook** sigue teniendo éxito, devolviendo MAPI_W_ERRORS_RETURNED y un puntero **IAddrBook** en el parámetro _lppAdrBook._ Dado **que OpenAddressBook** siempre devuelve un puntero **IAddrBook** válido, debe liberarlo cuando haya terminado de usarlo. 
  
Si no se pudo cargar uno o varios proveedores de libreta de direcciones, llame a [IMAPISupport::GetLastError](imapisupport-getlasterror.md) para obtener una estructura [MAPIERROR](mapierror.md) que contenga información sobre los proveedores que no se cargaron. 
  
## <a name="see-also"></a>Vea también



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

