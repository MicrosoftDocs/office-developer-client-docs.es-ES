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
ms.openlocfilehash: e240ec4e7a61b9e7484f467926501f8c5f5a59f8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592349"
---
# <a name="iaddrbookdetails"></a>IAddrBook::Details

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muestra un cuadro de diálogo que muestra detalles acerca de una entrada de la libreta de direcciones determinada.
  
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

## <a name="parameters"></a>Parámetros

 _lpulUIParam_
  
> [entrada] Un puntero a un identificador de la ventana primaria para el cuadro de diálogo.
    
 _lpfnDismiss_
  
> [entrada] Un puntero a una función basándose en el prototipo [DISMISSMODELESS](dismissmodeless.md) o NULL. Este miembro sólo se aplica a la versión del cuadro de diálogo no modal indicada por el indicador DIALOG_SDI que se va a establecer. MAPI llama a la función **DISMISSMODELESS** cuando el usuario cierra el cuadro de diálogo no modal de dirección, que le informa de un cliente que llama a **Detalles** que el cuadro de diálogo ya no está activo. 
    
 _lpvDismissContext_
  
> [entrada] Un puntero a la información de contexto para pasar a la función **DISMISSMODELESS** indicada por el parámetro _lpfnDismiss_ . Este parámetro sólo se aplica a la versión del cuadro de diálogo no modal mediante la inclusión de la marca DIALOG_SDI en el parámetro _ulFlags indicado_ . 
    
 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada de la entrada para la que se muestran los detalles.
    
 _lpfButtonCallback_
  
> [entrada] Un puntero a una función según el prototipo de función [LPFNBUTTON](lpfnbutton.md) . Una función **LPFNBUTTON** agrega un botón en el cuadro de diálogo detalles. 
    
 _lpvButtonContext_
  
> [entrada] Un puntero a los datos que se usan como un parámetro para la función especificada por el parámetro _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> [entrada] Un puntero a una cadena que contiene el texto que se aplicará a la se ha agregado un botón, si ese botón es extensible. El parámetro _lpszButtonText_ debe ser NULL si no es necesario un botón extensible. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de texto para el parámetro _lpszButtonText_ . Se pueden establecer los siguientes indicadores: 
    
AB_TELL_DETAILS_CHANGE
  
> Indica que **Detalles** devuelve S_OK si realmente se realizan cambios en la dirección; de lo contrario, **Detalles** devuelve S_FALSE. 
    
DIALOG_MODAL
  
> Mostrar la versión del cuadro de diálogo dirección comunes, que siempre se muestra en los clientes de Outlook no modal. Este marcador es mutuamente excluyente con DIALOG_SDI.
    
DIALOG_SDI
  
>  Mostrar la versión del cuadro de diálogo dirección comunes no modal. Este indicador se omite para los clientes de Outlook que no sean. 
    
MAPI_UNICODE. 
  
> Las cadenas que se pasan en están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El cuadro de diálogo detalles se mostró correctamente para la entrada de la libreta de direcciones.
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente de llaman al método **Detalles** para mostrar un cuadro de diálogo que proporciona información detallada sobre una entrada determinada en la libreta de direcciones. Puede usar los parámetros _lpfButtonCallback_, _lpvButtonContext_y _lpszButtonText_ para agregar un botón definido por el cliente para el cuadro de diálogo. Cuando se hace clic en el botón, MAPI llama a la función de devolución de llamada que apunta _lpfButtonCallback_, pasando el identificador de entrada de los datos y el botón en _lpvButtonContext_. Si no necesita un botón extensible, _lpszButtonText_ debe ser nulo. 
  
 **Detalles** admite las cadenas de caracteres Unicode; Las cadenas de Unicode se convierten en el formato de caracteres de varios bytes (MBCS) de la cadena antes de que se muestren en el cuadro de diálogo de detalles. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnOpenEntryID  <br/> |MFCMAPI usa el método **Details** para mostrar un cuadro de diálogo que muestra los detalles de una entrada de la libreta de direcciones.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

