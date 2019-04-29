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
  
Muestra un cuadro de diálogo que muestra los detalles de una entrada de la libreta de direcciones en particular.
  
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
  
> contempla Un puntero al controlador de la ventana principal del cuadro de diálogo devuelto.
    
 _lpfnDismiss_
  
> a Un puntero a una función basada en el prototipo [DISMISSMODELESS](dismissmodeless.md) o null. Este miembro sólo se aplica a la versión no modal del cuadro de diálogo, como se indica en la marca DIALOG_SDI que se va a establecer. MAPI llama a la función **DISMISSMODELESS** cuando el usuario cierra el cuadro de diálogo Dirección no modal, para informar a un cliente que llama a **IMAPISupport::D etails** que el cuadro de diálogo ya no está activo. 
    
 _lpvDismissContext_
  
> a Un puntero a la información de contexto que se va a pasar a la función **DISMISSMODELESS** señalada por el parámetro _lpfnDismiss_ . Este parámetro solo se aplica a la versión no modal del cuadro de diálogo, al incluir la marca DIALOG_SDI en el parámetro _ulFlags_ . 
    
 _cbEntryID_
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada para el que se muestran los detalles.
    
 _lpfButtonCallback_
  
> a Un puntero a una función basada en el prototipo de función [LPFNBUTTON](lpfnbutton.md) . Una función **LPFNBUTTON** agrega un botón al cuadro de diálogo Detalles. 
    
 _lpvButtonContext_
  
> a Puntero a los datos usados como parámetro para la función especificada por el parámetro _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> a Un puntero a una cadena que contiene el texto que se va a aplicar al botón de agregado si ese botón es extensible. El parámetro _lpszButtonText_ debe ser null si no se necesita un botón extensible. 
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla el tipo de texto para el parámetro _lpszButtonText_ . Se puede establecer la siguiente marca: 
    
DIALOG_MODAL
  
> Mostrar la versión modal del cuadro de diálogo Dirección común. Esta marca se excluye mutuamente con DIALOG_SDI.
    
DIALOG_SDI
  
>  Mostrar la versión no modal del cuadro de diálogo Dirección común. Esta marca se excluye mutuamente con DIALOG_MODAL. 
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El cuadro de diálogo Detalles se mostró correctamente para la entrada de la libreta de direcciones.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::D etails** se implementa para los objetos de compatibilidad del proveedor de la libreta de direcciones. Los proveedores de la libreta de direcciones llaman a **detalles** para mostrar un cuadro de diálogo que proporciona detalles sobre una entrada determinada en la libreta de direcciones. Los parámetros _lpfButtonCallback_, _lpvButtonContext_y _lpszButtonText_ pueden usarse para agregar un botón definido por el cliente al cuadro de diálogo. Cuando se hace clic en el botón, MAPI llama a la función de devolución de llamada a la que apunta _lpfButtonCallback_y pasa el identificador de entrada del botón y los datos de _lpvButtonContext_. Si no es necesario un botón extensible, _lpszButtonText_ debe ser nulo. 
  
## <a name="see-also"></a>Ver también



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

