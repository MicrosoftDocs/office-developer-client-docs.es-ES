---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 353a663071a9f23f0d2330169d3ac7747e047c2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421371"
---
# <a name="hrdoabdetailswithexchangecontext"></a>HrDoABDetailsWithExchangeContext

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Garantiza que el proveedor de la libreta de direcciones espera Exchange abrir el método **OpenEntry.** Esta función funciona de forma similar a [IAddrBook::D etails](iaddrbook-details.md), pero abre **el entryID** mediante la libreta de direcciones Exchange identificada por el parámetro _pEmsmdbUID._ 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithExchangeContext(
  LPMAPISESSION   pmsess,
  const MAPIUID  *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags,
);
```

## <a name="parameters"></a>Parameters

 _pmsess_
  
> La sesión iniciada **en IMAPISession**. No puede ser NULL.
    
 _pEmsmdbUID_
  
> Puntero a un **emsmdbUID** que identifica el servicio Exchange que contiene el proveedor de libreta de direcciones de Exchange que usa la función para abrir el identificador de entrada. Si el identificador de entrada entrante no es un identificador de entrada Exchange proveedor de libreta de direcciones, este parámetro se omite y la función se comporta como [IAddrBook::OpenEntry](iaddrbook-openentry.md). Si este parámetro es NULL o un **MAPIUID** cero, esta función también actúa exactamente igual que [IAddrBook::OpenEntry](iaddrbook-openentry.md). 
    
 _pAddrBook_
  
> [in] La libreta de direcciones usada para abrir el identificador de entrada. No puede ser NULL.
    
 _lpulUIParam_
  
> [salida] Identificador de la ventana principal del cuadro de diálogo.
    
 _lpfnDismiss_
  
> [in] Puntero a una función basada en el prototipo **DISMISSMODELESS** o NULL. Este miembro solo se aplica a la versión modeless del cuadro de diálogo, tal como se indica en la DIALOG_SDI marca que se va a establecer. MAPI llama a **la función DISMISSMODELESS** cuando el usuario descarta el cuadro de diálogo dirección de modeless e informa a un cliente que llama a Details de que el cuadro de diálogo ya no está activo. 
    
 _lpvDismissContext_
  
> [in] Puntero a la información de contexto que se pasa a la **función DISMISSMODELESS** a la que apunta el _parámetro lpfnDismiss._ Este parámetro solo se aplica a la versión modeless del cuadro de diálogo al incluir la marca **DIALOG_SDI** en el _parámetro ulFlags._ 
    
 _cbEntryID_
  
> [in] Recuento de bytes del identificador de entrada especificado por el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [in] Puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se debe abrir.
    
 _lpfButtonCallback_
  
> [in] Puntero a una función basada en el prototipo de función **LPFNBUTTON.** Una **función LPFNBUTTON** agrega un botón al cuadro de diálogo de detalles. 
    
 _lpvButtonContext_
  
> [in] Puntero a datos que se usó como parámetro para la función especificada por el _parámetro lpfButtonCallback._ 
    
 _lpszButtonText_
  
> [in] Puntero a una cadena que contiene texto que se aplicará al botón agregado, si ese botón es extensible. El  _parámetro lpszButtonText_ debe ser NULL cuando no se necesite un botón extensible. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla el tipo de texto del parámetro _lpszButtonText._ Se pueden establecer las siguientes marcas: 
    
AB_TELL_DETAILS_CHANGE
  
> Indica que Details devuelve TRUE si realmente se realizan cambios en la dirección; de lo contrario, Details devuelve FALSE.
    
DIALOG_MODAL
  
> Muestra la versión modal del cuadro de diálogo dirección común. Esta marca es mutuamente exclusiva con DIALOG_SDI.
    
DIALOG_SDI
  
> Muestra la versión modeless del cuadro de diálogo dirección común. Esta marca es mutuamente exclusiva con DIALOG_MODAL.
    
MAPI_UNICODE
  
> Las cadenas pasadas están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.
    

