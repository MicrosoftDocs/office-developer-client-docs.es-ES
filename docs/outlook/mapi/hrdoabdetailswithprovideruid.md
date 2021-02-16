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
  
Garantiza que el proveedor de libreta de direcciones de Exchange espera abrir el método **OpenEntry.** Esta función funciona de forma similar a [IAddrBook::D etails,](iaddrbook-details.md) pero abre **entryID** con la libreta de direcciones de Exchange identificada por  _pEmsabpUID_.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp.h  <br/> |
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

## <a name="parameters"></a>Parámetros

 _pEmsabpUID_
  
> [entrada] Puntero a una  _emsabpUID_ que identifica al proveedor de libreta de direcciones de Exchange que esta función debe usar para mostrar detalles en el identificador de entrada. Si el identificador de entrada entrante no es un identificador de entrada de proveedor de libreta de direcciones de Exchange, este parámetro se omite y la llamada de función actúa exactamente igual que [IAddrBook::D etails](iaddrbook-details.md). Si este parámetro es NULL o un MAPIUID cero, esta función también actúa exactamente igual que [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> [entrada] La libreta de direcciones usada para abrir el identificador de entrada. No puede ser NULL.
    
 _lpulUIParam_
  
> [salida] Identificador de la ventana principal del cuadro de diálogo.
    
 _lpfnDismiss_
  
> [entrada] Puntero a una función basada en el prototipo **DISMISSMODELESS** o NULL. Este miembro se aplica solo a la versión no modelada del cuadro de diálogo, tal como se indica en la DIALOG_SDI marca que se está configurando. MAPI llama a la función **DISMISSMODELESS** cuando el usuario descarta el cuadro de diálogo de dirección no modelada e informa a un cliente que llama a Details de que el cuadro de diálogo ya no está activo. 
    
 _lpvDismissContext_
  
> [entrada] Puntero a la información de contexto que se pasa a la **función DISMISSMODELESS** a la que apunta el parámetro _lpfnDismiss._ Este parámetro solo se aplica a la versión no modelada del cuadro de diálogo incluyendo la marca **DIALOG_SDI** en el _parámetro ulFlags._ 
    
 _cbEntryID_
  
> [entrada] Recuento de bytes del identificador de entrada especificado por el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [entrada] Puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se debe abrir.
    
 _lpfButtonCallback_
  
> [entrada] Puntero a una función basada en el prototipo de función **LPFNBUTTON.** Una **función LPFNBUTTON** agrega un botón al cuadro de diálogo de detalles. 
    
 _lpvButtonContext_
  
> [entrada] Puntero a datos que se usó como parámetro para la función especificada por el _parámetro lpfButtonCallback._ 
    
 _lpszButtonText_
  
> [entrada] Puntero a una cadena que contiene texto que se aplicará al botón agregado, si ese botón es extensible. El  _parámetro lpszButtonText_ debe ser NULL cuando no se necesite un botón extensible. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla el tipo de texto para el _parámetro lpszButtonText._ Se pueden establecer las siguientes marcas: 
    
AB_TELL_DETAILS_CHANGE
  
> Indica que Details devuelve TRUE si realmente se realizan cambios en la dirección; de lo contrario, Details devuelve FALSE.
    
DIALOG_MODAL
  
> Muestra la versión modal del cuadro de diálogo dirección común. Esta marca es mutuamente exclusiva con DIALOG_SDI.
    
DIALOG_SDI
  
> Muestra la versión no modelada del cuadro de diálogo de direcciones comunes. Esta marca es mutuamente exclusiva con DIALOG_MODAL.
    
MAPI_UNICODE
  
> Las cadenas pasadas están en formato Unicode. Si no MAPI_UNICODE marca, las cadenas están en formato ANSI.
    

