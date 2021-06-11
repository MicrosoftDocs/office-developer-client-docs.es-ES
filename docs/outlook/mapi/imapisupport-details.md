---
title: IMAPISupportDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Details
api_type:
- COM
ms.assetid: 1a62efa2-dd6b-4acb-a760-defa601c20c9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bdc57a6e951e54640fe3c638977c6a5f16986e68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426782"
---
# <a name="imapisupportdetails"></a>IMAPISupport::Details

  
  
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
  
> [salida] Puntero al controlador a la ventana primaria del cuadro de diálogo devuelto.
    
 _lpfnDismiss_
  
> [in] Puntero a una función basada en el prototipo [DISMISSMODELESS](dismissmodeless.md) o NULL. Este miembro solo se aplica a la versión modeless del cuadro de diálogo, tal como se indica en la DIALOG_SDI marca que se va a establecer. MAPI llama a la función **DISMISSMODELESS** cuando el usuario descarta el cuadro de diálogo dirección de modeless e informa a un cliente que llama a **IMAPISupport::D etails** que el cuadro de diálogo ya no está activo. 
    
 _lpvDismissContext_
  
> [in] Puntero a la información de contexto que se pasa a la **función DISMISSMODELESS** a la que apunta el _parámetro lpfnDismiss._ Este parámetro solo se aplica a la versión modeless del cuadro de diálogo, incluyendo la marca DIALOG_SDI en el _parámetro ulFlags._ 
    
 _cbEntryID_
  
> [in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [in] Puntero al identificador de entrada para el que se muestran los detalles.
    
 _lpfButtonCallback_
  
> [in] Puntero a una función basada en el prototipo de función [LPFNBUTTON.](lpfnbutton.md) Una **función LPFNBUTTON** agrega un botón al cuadro de diálogo de detalles. 
    
 _lpvButtonContext_
  
> [in] Puntero a los datos usados como parámetro para la función especificada por el _parámetro lpfButtonCallback._ 
    
 _lpszButtonText_
  
> [in] Puntero a una cadena que contiene texto que se aplicará al botón agregado si ese botón es extensible. El  _parámetro lpszButtonText_ debe ser NULL si no se necesita un botón extensible. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla el tipo de texto del parámetro _lpszButtonText._ Se puede establecer la siguiente marca: 
    
DIALOG_MODAL
  
> Mostrar la versión modal del cuadro de diálogo dirección común. Esta marca es mutuamente exclusiva con DIALOG_SDI.
    
DIALOG_SDI
  
>  Mostrar la versión modeless del cuadro de diálogo dirección común. Esta marca es mutuamente exclusiva con DIALOG_MODAL. 
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El cuadro de diálogo detalles se mostró correctamente para la entrada de la libreta de direcciones.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::D etails** se implementa para objetos de soporte del proveedor de libreta de direcciones. Los proveedores de libreta de direcciones llaman a **Detalles** para mostrar un cuadro de diálogo que proporciona detalles sobre una entrada determinada de la libreta de direcciones. Los  _parámetros lpfButtonCallback_,  _lpvButtonContext_ y  _lpszButtonText_ se pueden usar para agregar un botón definido por el cliente al cuadro de diálogo. Cuando se hace clic en el botón, MAPI llama a la función de devolución de llamada señalada por  _lpfButtonCallback_, pasando tanto el identificador de entrada del botón como los datos de  _lpvButtonContext_. Si no se necesita un botón extensible,  _lpszButtonText_ debe ser NULL. 
  
## <a name="see-also"></a>Vea también



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

