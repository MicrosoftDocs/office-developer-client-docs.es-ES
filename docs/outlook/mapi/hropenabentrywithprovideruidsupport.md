---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da40e240b60fa42c48185600b74c6162a966e6f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409548"
---
# <a name="hropenabentrywithprovideruidsupport"></a>HrOpenABEntryWithProviderUIDSupport

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Realiza la misma función que la función [HrOpenABEntryWithProviderUID,](hropenabentrywithprovideruid.md) excepto que la función **HrOpenABEntryWithProviderUIDSupport** abre la entrada con el objeto de soporte especificado en lugar de usar la sesión y la libreta de direcciones. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUIDSupport(
  const MAPIUID *pEmsabpUID,
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parámetros

 _pEmsabpUID_
  
> [entrada] Puntero a un parámetro  _emsabpUID_ que identifica el proveedor de libretas de direcciones de Exchange que esta función debe usar para mostrar detalles sobre el identificador de entrada. Si el identificador de entrada entrante no es un identificador de entrada de proveedor de libreta de direcciones de Exchange, este parámetro se omite y la llamada de función actúa exactamente igual que [IAddrBook::D etails](iaddrbook-details.md). Si este parámetro es NULL o un MAPIUID cero, esta función también actúa exactamente igual que [IAddrBook::D etails](iaddrbook-details.md).
    
 _lpSup_
  
> 
    
 _cbEntryID_
  
> [entrada] Recuento de bytes del identificador de entrada especificado por el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [entrada] Puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se debe abrir.
    
 _lpInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) de la interfaz que se usará para tener acceso a la entrada abierta. Si se pasa NULL, se devuelve la interfaz estándar del objeto. Para los usuarios de mensajería, la interfaz estándar [es IMailUser : IMAPIProp](imailuserimapiprop.md). Para las listas de distribución es [IDistList : IMAPIContainer](idistlistimapicontainer.md)y para contenedores es [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Los autores de llamadas pueden  _establecer lpInterface_ en la interfaz estándar adecuada o una interfaz en la jerarquía de herencia. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla el tipo de texto para el _parámetro lpszButtonText._ Se pueden establecer las siguientes marcas: 
    
AB_TELL_DETAILS_CHANGE
  
> Indica que Details devuelve TRUE si realmente se realizan cambios en la dirección; de lo contrario, Details devuelve FALSE.
    
DIALOG_MODAL
  
> Muestra la versión modal del cuadro de diálogo dirección común. Esta marca es mutuamente exclusiva con DIALOG_SDI.
    
DIALOG_SDI
  
> Muestra la versión modelada del cuadro de diálogo de dirección común. Esta marca es mutuamente exclusiva con DIALOG_MODAL.
    
MAPI_UNICODE
  
> Las cadenas pasadas están en formato Unicode. Si no MAPI_UNICODE marca, las cadenas están en formato ANSI.
    
 _lpulObjType_
  
> [salida] Puntero al tipo de la entrada abierta.
    
 _lppUnk_
  
> [salida] Puntero a un puntero de la entrada abierta.
    

