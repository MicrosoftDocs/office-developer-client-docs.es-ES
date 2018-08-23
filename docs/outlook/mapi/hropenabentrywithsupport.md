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
ms.openlocfilehash: 58a6249295810e32c0a0f845e4830b8f393885ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579385"
---
# <a name="hropenabentrywithsupport"></a>HrOpenABEntryWithSupport

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
No use esta función.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
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
  
> [entrada] El número de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones para abrir.
    
 _lpInterface_
  
>  [entrada] Un puntero al identificador de interfaz (IID) de la interfaz que se usará para tener acceso a la entrada open. Pasando NULL, devuelve la interfaz estándar del objeto. Para los usuarios de mensajería, es la interfaz estándar de [IMailUser: IMAPIProp](imailuserimapiprop.md). Para las listas de distribución, es [IDistList: IMAPIContainer](idistlistimapicontainer.md), y para los contenedores, es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o una interfaz en la jerarquía de herencia. 
    
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
    
 _lpulObjType_
  
> [out] Un puntero al tipo de la entrada que se abrió.
    
 _lppUnk_
  
> [out] Un puntero a un puntero de la entrada que se abrió.
    

