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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341723"
---
# <a name="iaddrbookdetails"></a>IAddrBook::Details

  
  
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
  
> a Un puntero a un controlador de la ventana principal del cuadro de diálogo.
    
 _lpfnDismiss_
  
> a Un puntero a una función basada en el prototipo [DISMISSMODELESS](dismissmodeless.md) o null. Este miembro sólo se aplica a la versión no modal del cuadro de diálogo, como se indica en la marca DIALOG_SDI que se va a establecer. MAPI llama a la función **DISMISSMODELESS** cuando el usuario cierra el cuadro de diálogo Dirección no modal, para informar a un cliente que está llamando **detalles** que el cuadro de diálogo ya no está activo. 
    
 _lpvDismissContext_
  
> a Un puntero a la información de contexto que se va a pasar a la función **DISMISSMODELESS** señalada por el parámetro _lpfnDismiss_ . Este parámetro solo se aplica a la versión no modal del cuadro de diálogo, al incluir la marca DIALOG_SDI en el parámetro _ulFlags_ . 
    
 _cbEntryID_
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada de la entrada para la que se muestran los detalles.
    
 _lpfButtonCallback_
  
> a Un puntero a una función basada en el prototipo de función [LPFNBUTTON](lpfnbutton.md) . Una función **LPFNBUTTON** agrega un botón al cuadro de diálogo Detalles. 
    
 _lpvButtonContext_
  
> a Puntero a los datos que se usaron como parámetro para la función especificada por el parámetro _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> a Un puntero a una cadena que contiene el texto que se va a aplicar al botón agregado, si ese botón es extensible. El parámetro _lpszButtonText_ debe ser null si no necesita un botón extensible. 
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla el tipo de texto para el parámetro _lpszButtonText_ . Se pueden establecer los siguientes indicadores: 
    
AB_TELL_DETAILS_CHANGE
  
> Indica que **detalles** Devuelve S_OK si los cambios se realizan realmente en la dirección; de lo contrario, **detalles** devuelve S_FALSE. 
    
DIALOG_MODAL
  
> Mostrar la versión modal del cuadro de diálogo Dirección común, que siempre se muestra en clientes que no son de Outlook. Esta marca se excluye mutuamente con DIALOG_SDI.
    
DIALOG_SDI
  
>  Mostrar la versión no modal del cuadro de diálogo Dirección común. Esta marca se omite para clientes que no son de Outlook. 
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El cuadro de diálogo Detalles se mostró correctamente para la entrada de la libreta de direcciones.
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente llaman **** al método details para mostrar un cuadro de diálogo que proporciona detalles sobre una entrada determinada de la libreta de direcciones. Puede usar los parámetros _lpfButtonCallback_, _lpvButtonContext_y _lpszButtonText_ para agregar un botón definido por el cliente al cuadro de diálogo. Cuando se hace clic en el botón, MAPI llama a la función de devolución de llamada a la que apunta _lpfButtonCallback_y pasa el identificador de entrada del botón y los datos de _lpvButtonContext_. Si no necesita un botón extensible, _lpszButtonText_ debe ser null. 
  
 Los **detalles** son compatibles con las cadenas de caracteres Unicode; Las cadenas Unicode se convierten en el formato de cadena de caracteres multibyte (MBCS) antes de que se muestren en el cuadro de diálogo Detalles. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CBaseDialog:: OnOpenEntryID  <br/> |MFCMAPI usa el **** método details para mostrar un cuadro de diálogo que muestra los detalles de una entrada de la libreta de direcciones.  <br/> |
   
## <a name="see-also"></a>Vea también



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

