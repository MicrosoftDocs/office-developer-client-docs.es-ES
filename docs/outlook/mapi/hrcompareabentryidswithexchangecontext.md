---
title: HrCompareABEntryIDsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e537c25f-51b5-4f06-a20a-44ee540b9a1f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 730c24a179cc6aaf8dc2068199ffc206d30156b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817029"
---
# <a name="hrcompareabentryidswithexchangecontext"></a>HrCompareABEntryIDsWithExchangeContext

  
  
**Hace referencia a**: Outlook 
  
Compara dos de la libreta de dirección **identificadores** con seguridad en un perfil de Exchange varios. Esta función es una función de reemplazo para [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
HRESULT HrCompareABEntryIDsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG * lpulResult
);
```

## <a name="parameters"></a>Parámetros

 _pmsess_
  
> [entrada] La ha iniciado la sesión **IMAPISession**. No puede ser NULL.
    
 _pEmsmdbUID_
  
> [entrada] Un puntero a un **emsmdbUID** que identifica el servicio de Exchange que contiene el proveedor de libreta de direcciones de Exchange que se debe usar esta función para mostrar los detalles en el identificador de entrada. Si el identificador de entrada entrante no es un identificador de entrada del proveedor de libreta de direcciones de Exchange, este parámetro se omite y la llamada a la función se comporta como [IAddrBook::Details](iaddrbook-details.md). Si este parámetro es NULL o un cero MAPIUID, esta función se comporta como [IAddrBook::Details](iaddrbook-details.md).
    
 _pAddrBook_
  
> [entrada] La libreta de direcciones que se usó para abrir el identificador de entrada. No puede ser NULL.
    
 _cbEntryID1_
  
> [entrada] El número de bytes del primer identificador de entrada especificado por el parámetro _lpEntryID1_ . 
    
 _lpEntryID1_
  
> [entrada] Un puntero para el primer identificador de entrada que representa la entrada de la libreta de direcciones se va a comparar.
    
 _cbEntryID2_
  
> [entrada] El número de bytes del segundo identificador de entrada especificado por el parámetro _lpEntryID2_ . 
    
 _lpEntryID2_
  
> [entrada] Un puntero al segundo identificador de entrada utilizado en la comparación que representa la entrada de la libreta de direcciones se va a comparar.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpulResult_
  
> [out] Un puntero a la ubicación que contiene los resultados de la comparación. 
    

