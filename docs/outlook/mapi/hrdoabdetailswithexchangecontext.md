---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: cb6138072cd5dedc528168d4056041661c40fd06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817052"
---
# <a name="hrdoabdetailswithexchangecontext"></a>HrDoABDetailsWithExchangeContext

  
  
**Se aplica a**: Outlook 
  
Se asegura de que se abre el método **OpenEntry** por el proveedor de la libreta de direcciones de Exchange esperado. Esta función funciona de manera similar a [IAddrBook::Details](iaddrbook-details.md), pero abre el **entryID** de la libreta de direcciones de Exchange identificado mediante el parámetro _pEmsmdbUID_ . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
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

## <a name="parameters"></a>Sintaxis

 _pmsess_
  
> La ha iniciado la sesión **IMAPISession**. No puede ser NULL.
    
 _pEmsmdbUID_
  
> Un puntero a un **emsmdbUID** que identifica el servicio de Exchange que contiene el proveedor de la libreta de direcciones de Exchange que se usa la función para abrir el identificador de entrada. Si el identificador de entrada entrante no es un identificador de entrada Exchange proveedor de la libreta de direcciones, se omite este parámetro y la función se comporta como [IAddrBook::OpenEntry](iaddrbook-openentry.md). Si este parámetro es NULL o cero **MAPIUID**, esta función también actúa exactamente igual que [IAddrBook::OpenEntry](iaddrbook-openentry.md). 
    
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
    

