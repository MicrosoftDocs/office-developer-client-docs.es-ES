---
title: IMAPISessionOpenAddressBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenAddressBook
api_type:
- COM
ms.assetid: 2b6a4c6a-bb71-4ea1-a3b6-90a2722880fb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 51bf5f8455d4cb790d0c955e96249b0f9deef1af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329424"
---
# <a name="imapisessionopenaddressbook"></a>IMAPISession::OpenAddressBook

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre la libreta de direcciones MAPI integrada y devuelve un puntero [IAddrBook](iaddrbookimapiprop.md) para obtener más acceso. 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> a Identificador de la ventana principal del cuadro de diálogo de direcciones comunes y otras pantallas relacionadas.
    
 _lpInterface_
  
> a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a la libreta de direcciones. Si se pasa **null** , se devuelve un puntero a la interfaz estándar de la libreta de direcciones, [IAddrBook: IMAPIProp](iaddrbookimapiprop.md). 
    
 _ulFlags_
  
> a Una máscara de direcciones de marcas que controla la apertura de la libreta de direcciones. Se puede establecer la siguiente marca:
    
AB_NO_DIALOG 
  
> SuPrime la presentación de cuadros de diálogo. Si no se establece la marca AB_NO_DIALOG, los proveedores de la libreta de direcciones que contribuyan a la libreta de direcciones integrada podrán pedir al usuario la información necesaria. 
    
 _lppAdrBook_
  
> contempla Un puntero a un puntero a la libreta de direcciones.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La libreta de direcciones se abrió correctamente.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se realizó correctamente, pero no se pudieron abrir los contenedores de uno o varios proveedores de la libreta de direcciones. Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta. Para probar esta advertencia, use la macro **HR_FAILED** . Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession:: OpenAddressBook** abre la libreta de direcciones MAPI integrada, una colección de los contenedores de nivel superior de todos los proveedores de la libreta de direcciones en el perfil. El puntero que se devuelve en el parámetro _lppAdrBook_ proporciona más acceso al contenido de la libreta de direcciones. Esto permite al autor de la llamada realizar tareas como abrir contenedores individuales, buscar usuarios de mensajería y mostrar cuadros de diálogo de direcciones comunes. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **OpenAddressBook** devuelve MAPI_W_ERRORS_RETURNED si no puede cargar uno o más proveedores de la libreta de direcciones en el perfil. Este valor es una advertencia, no un valor de error; controlarlo como lo haría en S_OK. **OpenAddressBook** siempre devuelve un puntero válido en el parámetro _lppAdrBook_ , independientemente de cuántos de los proveedores de libreta de direcciones no se pudieron cargar. Por lo tanto, siempre debe llamar al método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) de la libreta de direcciones en algún momento antes de cerrar la sesión. 
  
Cuando **OpenAddressBook** devuelve MAPI_W_ERRORS_RETURNED, llame a [IMAPISession:: GetLastError](imapisession-getlasterror.md) para obtener una estructura [MAPIERROR](mapierror.md) que contenga información sobre los proveedores con errores. Se devuelve una única estructura **MAPIERROR** que contiene información proporcionada por todos los proveedores. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIObjects. cpp  <br/> |CMapiObjects:: GetAddrBook  <br/> |MFCMAPI usa el método **IMAPISession:: OpenAddressBook** para obtener la libreta de direcciones integrada.  <br/> |
   
## <a name="see-also"></a>Vea también



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

