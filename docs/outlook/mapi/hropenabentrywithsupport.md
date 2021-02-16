---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b8574264bdb470906cc097cec56b39a943937d11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417647"
---
# <a name="hropenabentrywithsupport"></a>HrOpenABEntryWithSupport

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
No use esta función.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithSupport(
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID  lpInterface,
  ULONG  ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parámetros

 _lpSup_
  
> 
    
 _cbEntryID_
  
> [entrada] Recuento de bytes del identificador de entrada especificado por el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [entrada] Puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se debe abrir.
    
 _lpInterface_
  
>  [entrada] Puntero al identificador de interfaz (IID) de la interfaz que se usará para tener acceso a la entrada abierta. Si se pasa NULL, se devuelve la interfaz estándar del objeto. Para los usuarios de mensajería, la interfaz estándar [es IMailUser : IMAPIProp](imailuserimapiprop.md). Para las listas de distribución, es [IDistList : IMAPIContainer](idistlistimapicontainer.md)y, para contenedores, es [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Los autores de llamadas pueden  _establecer lpInterface_ en la interfaz estándar adecuada o una interfaz en la jerarquía de herencia. 
    
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
    
 _lpulObjType_
  
> [salida] Puntero al tipo de la entrada abierta.
    
 _lppUnk_
  
> [salida] Puntero a un puntero de la entrada abierta.
    

