---
title: HrDoABDetailsWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 27741887-8405-49ed-b080-613613faf91b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 47cf87fce0af3b866018bf03a34a05ea42cef82c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426684"
---
# <a name="hrdoabdetailswithprovideruid"></a>HrDoABDetailsWithProviderUID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Garantiza que el proveedor de libreta de direcciones de Exchange esperado abre el método **OpenEntry** . Esta función funciona de manera similar a [IAddrBook::D etails](iaddrbook-details.md) pero abre **entryID** mediante la libreta de direcciones de Exchange identificada por _pEmsabpUID_.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithProviderUID(
  const MAPIUID   *pEmsabpUID,
  LPADRBOOK        pAddrBook,
  ULONG_PTR FAR *  lpulUIParam,
  LPFNDISMISS      lpfnDismiss,
  LPVOID           lpvDismissContext,
  ULONG            cbEntryID,
  LPENTRYID        lpEntryID,
  LPFNBUTTON       lpfButtonCallback,
  LPVOID           lpvButtonContext,
  LPSTR           lpszButtonText,
  ULONG            ulFlags
);
```

## <a name="parameters"></a>Parameters

 _pEmsabpUID_
  
> a Un puntero a una _emsabpUID_ que identifica el proveedor de la libreta de direcciones de Exchange esta función debe usarse para mostrar detalles sobre el identificador de entrada. Si el identificador de entrada entrante no es un identificador de entrada de proveedor de libreta de direcciones de Exchange, se omite este parámetro y la llamada a la función actúa exactamente como [IAddrBook::D etails](iaddrbook-details.md). Si este parámetro es NULL o un MAPIUID de ceros, esta función también actúa exactamente como [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> a La libreta de direcciones que se usa para abrir el identificador de entrada. No puede ser nulo.
    
 _lpulUIParam_
  
> contempla Identificador de la ventana principal del cuadro de diálogo.
    
 _lpfnDismiss_
  
> a Un puntero a una función basada en el prototipo **DISMISSMODELESS** o null. Este miembro sólo se aplica a la versión no modal del cuadro de diálogo, como se indica en la marca DIALOG_SDI que se va a establecer. MAPI llama a la función **DISMISSMODELESS** cuando el usuario cierra el cuadro de diálogo Dirección no modal, para informar a un cliente que está llamando detalles que el cuadro de diálogo ya no está activo. 
    
 _lpvDismissContext_
  
> a Un puntero a la información de contexto que se va a pasar a la función **DISMISSMODELESS** señalada por el parámetro _lpfnDismiss_ . Este parámetro solo se aplica a la versión no modal del cuadro de diálogo incluyendo la marca **DIALOG_SDI** en el parámetro _ulFlags_ . 
    
 _cbEntryID_
  
> a El recuento de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se va a abrir.
    
 _lpfButtonCallback_
  
> a Un puntero a una función basada en el prototipo de función **LPFNBUTTON** . Una función **LPFNBUTTON** agrega un botón al cuadro de diálogo Detalles. 
    
 _lpvButtonContext_
  
> a Puntero a los datos que se usaron como parámetro para la función especificada por el parámetro _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> a Un puntero a una cadena que contiene el texto que se va a aplicar al botón agregado, si ese botón es extensible. El parámetro _lpszButtonText_ debe ser NULL cuando no es necesario un botón extensible. 
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla el tipo de texto para el parámetro _lpszButtonText_ . Se pueden establecer los siguientes indicadores: 
    
AB_TELL_DETAILS_CHANGE
  
> Indica que los detalles devuelven TRUE si los cambios se realizan realmente en la dirección; de lo contrario, devolverá FALSE.
    
DIALOG_MODAL
  
> Muestra la versión modal del cuadro de diálogo Dirección común. Esta marca se excluye mutuamente con DIALOG_SDI.
    
DIALOG_SDI
  
> Muestra la versión no modal del cuadro de diálogo Dirección común. Esta marca se excluye mutuamente con DIALOG_MODAL.
    
MAPI_UNICODE
  
> Las cadenas pasadas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.
    

