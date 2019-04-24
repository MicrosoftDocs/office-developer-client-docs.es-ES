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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347764"
---
# <a name="hropenabentrywithsupport"></a>HrOpenABEntryWithSupport

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
No use esta función.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp. h  <br/> |
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

## <a name="parameters"></a>Parameters

 _lpSup_
  
> 
    
 _cbEntryID_
  
> a El recuento de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se va a abrir.
    
 _lpInterface_
  
>  a Puntero al identificador de interfaz (IID) de la interfaz que se va a usar para obtener acceso a la entrada abierta. Al pasar NULL, se devuelve la interfaz estándar del objeto. Para los usuarios de mensajería, la interfaz estándar es [IMailUser: IMAPIProp](imailuserimapiprop.md). Para las listas de distribución, es [IDistList: IMAPIContainer](idistlistimapicontainer.md)y, para los contenedores, es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o en una interfaz de la jerarquía de herencia. 
    
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
    
 _lpulObjType_
  
> contempla Puntero al tipo de la entrada abierta.
    
 _lppUnk_
  
> contempla Un puntero a un puntero de la entrada abierta.
    

