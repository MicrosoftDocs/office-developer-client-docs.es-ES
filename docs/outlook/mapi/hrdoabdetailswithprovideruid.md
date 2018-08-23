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
ms.openlocfilehash: cb4f38615ac6cacb3acbaa456f0992bf55c3653d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568626"
---
# <a name="hrdoabdetailswithprovideruid"></a>HrDoABDetailsWithProviderUID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se asegura de que se abre el método **OpenEntry** por el proveedor de la libreta de direcciones de Exchange esperado. Esta función funciona de manera similar a [IAddrBook::Details](iaddrbook-details.md) , pero abre **entryID** utilizando la libreta de direcciones de Exchange identificada por _pEmsabpUID_.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
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
  
> [entrada] Un puntero a un _emsabpUID_ que identifica el proveedor de la libreta de direcciones de Exchange debe usar esta función para mostrar detalles en el identificador de entrada. Si el identificador de entrada entrante no es un identificador de entrada Exchange proveedor de la libreta de direcciones, este parámetro se omite y el actúa de llamada de función exactamente como [IAddrBook::Details](iaddrbook-details.md). Si este parámetro es NULL o un cero MAPIUID, esta función también actúa exactamente igual que [IAddrBook::Details](iaddrbook-details.md).
    
 _pAddrBook_
  
> [entrada] La libreta de direcciones que se usó para abrir el identificador de entrada. No puede ser NULL.
    
 _lpulUIParam_
  
> [out] Identificador de la ventana primaria para el cuadro de diálogo.
    
 _lpfnDismiss_
  
> [entrada] Un puntero a una función basándose en el prototipo **DISMISSMODELESS** o NULL. Este miembro sólo se aplica a la versión del cuadro de diálogo no modal indicada por el indicador DIALOG_SDI que se va a establecer. MAPI llama a la función **DISMISSMODELESS** cuando el usuario cierra el cuadro de diálogo no modal de dirección, que le informa de un cliente que llama a detalles que el cuadro de diálogo ya no está activo. 
    
 _lpvDismissContext_
  
> [entrada] Un puntero a la información de contexto para pasar a la función **DISMISSMODELESS** indicada por el parámetro _lpfnDismiss_ . Este parámetro sólo se aplica a la versión del cuadro de diálogo no modal mediante la inclusión de la marca **DIALOG_SDI** en el parámetro _ulFlags indicado_ . 
    
 _cbEntryID_
  
> [entrada] El número de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones para abrir.
    
 _lpfButtonCallback_
  
> [entrada] Un puntero a una función según el prototipo de función **LPFNBUTTON** . Una función **LPFNBUTTON** agrega un botón en el cuadro de diálogo detalles. 
    
 _lpvButtonContext_
  
> [entrada] Un puntero a los datos que se usan como un parámetro para la función especificada por el parámetro _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> [entrada] Un puntero a una cadena que contiene el texto que se aplicará a la se ha agregado un botón, si ese botón es extensible. El parámetro _lpszButtonText_ debe ser NULL cuando no es necesario un botón extensible. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de texto para el parámetro _lpszButtonText_ . Se pueden establecer los siguientes indicadores: 
    
AB_TELL_DETAILS_CHANGE
  
> Indica que detalles devuelve TRUE si realmente se realizan cambios en la dirección; de lo contrario, detalles devuelve FALSE.
    
DIALOG_MODAL
  
> Muestra la versión del cuadro de diálogo dirección comunes modal. Este marcador es mutuamente excluyente con DIALOG_SDI.
    
DIALOG_SDI
  
> Muestra la versión del cuadro de diálogo dirección comunes no modal. Este marcador es mutuamente excluyente con DIALOG_MODAL.
    
MAPI_UNICODE.
  
> Las cadenas que se pasan en están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.
    

