---
title: IAddrBookDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Details
api_type:
- COM
ms.assetid: 4eee4382-98c3-4714-8920-8d72edef00b8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5fbd20a6b5d5598b8fa51f9c369eefac9a1ea2e9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424682"
---
# <a name="iaddrbookdetails"></a>IAddrBook::Details

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muestra un cuadro de diálogo que muestra detalles sobre una entrada de libreta de direcciones determinada.
  
```cpp
HRESULT Details(
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulUIParam_
  
> [in] Puntero a un controlador de la ventana primaria del cuadro de diálogo.
    
 _lpfnDismiss_
  
> [in] Puntero a una función basada en el prototipo [DISMISSMODELESS](dismissmodeless.md) o NULL. Este miembro solo se aplica a la versión modeless del cuadro de diálogo, tal como se indica en la DIALOG_SDI marca que se va a establecer. MAPI llama a **la función DISMISSMODELESS** cuando el usuario descarta el cuadro de diálogo dirección de modeless e informa a un cliente que llama a **Details** de que el cuadro de diálogo ya no está activo. 
    
 _lpvDismissContext_
  
> [in] Puntero a la información de contexto que se pasa a la **función DISMISSMODELESS** a la que apunta el _parámetro lpfnDismiss._ Este parámetro solo se aplica a la versión modeless del cuadro de diálogo, incluyendo la marca DIALOG_SDI en el _parámetro ulFlags._ 
    
 _cbEntryID_
  
> [in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [in] Puntero al identificador de entrada de la entrada para la que se muestran los detalles.
    
 _lpfButtonCallback_
  
> [in] Puntero a una función basada en el prototipo de función [LPFNBUTTON.](lpfnbutton.md) Una **función LPFNBUTTON** agrega un botón al cuadro de diálogo de detalles. 
    
 _lpvButtonContext_
  
> [in] Puntero a datos que se usó como parámetro para la función especificada por el _parámetro lpfButtonCallback._ 
    
 _lpszButtonText_
  
> [in] Puntero a una cadena que contiene texto que se aplicará al botón agregado, si ese botón es extensible. El  _parámetro lpszButtonText_ debe ser NULL si no necesita un botón extensible. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla el tipo de texto del parámetro _lpszButtonText._ Se pueden establecer las siguientes marcas: 
    
AB_TELL_DETAILS_CHANGE
  
> Indica que **Details** devuelve S_OK si realmente se realizan cambios en la dirección; de lo contrario, **Details** devuelve S_FALSE. 
    
DIALOG_MODAL
  
> Muestra la versión modal del cuadro de diálogo dirección común, que siempre se muestra en clientes que no Outlook direcciones. Esta marca es mutuamente exclusiva con DIALOG_SDI.
    
DIALOG_SDI
  
>  Mostrar la versión modeless del cuadro de diálogo dirección común. Esta marca se omite para clientes que no Outlook cliente. 
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El cuadro de diálogo detalles se mostró correctamente para la entrada de la libreta de direcciones.
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente llaman al **método Details** para mostrar un cuadro de diálogo que proporciona detalles sobre una entrada determinada en la libreta de direcciones. Puede usar los parámetros  _lpfButtonCallback_,  _lpvButtonContext_ y  _lpszButtonText_ para agregar un botón definido por el cliente al cuadro de diálogo. Cuando se hace clic en el botón, MAPI llama a la función de devolución de llamada señalada por  _lpfButtonCallback_, pasando tanto el identificador de entrada del botón como los datos de  _lpvButtonContext_. Si no necesita un botón extensible,  _lpszButtonText_ debe ser NULL. 
  
 **Los detalles** admiten cadenas de caracteres Unicode; Las cadenas Unicode se convierten al formato de cadena de caracteres multibyte (MBCS) antes de que se muestren en el cuadro de diálogo detalles. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnOpenEntryID  <br/> |MFCMAPI usa el **método Details** para mostrar un cuadro de diálogo que muestra los detalles de una entrada de libreta de direcciones.  <br/> |
   
## <a name="see-also"></a>Vea también



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

