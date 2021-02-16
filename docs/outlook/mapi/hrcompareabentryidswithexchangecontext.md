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
ms.openlocfilehash: 4bada5913623e2eb463a9e72347bd31eb22c414b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436436"
---
# <a name="hrcompareabentryidswithexchangecontext"></a>HrCompareABEntryIDsWithExchangeContext

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Compara dos identificadores de entrada de la libreta **de** direcciones de forma segura en un perfil de Exchange múltiple. Esta función es una función de reemplazo para [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |abhelp.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
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
  
> [entrada] La sesión iniciada **en IMAPISession**. No puede ser NULL.
    
 _pEmsmdbUID_
  
> [entrada] Puntero a **un emsmdbUID** que identifica el servicio de Exchange que contiene el proveedor de libreta de direcciones de Exchange que esta función debe usar para mostrar detalles en el identificador de entrada. Si el identificador de entrada entrante no es un identificador de entrada del proveedor de libreta de direcciones de Exchange, este parámetro se omite y la llamada de función se comporta como [IAddrBook::D etails](iaddrbook-details.md). Si este parámetro es NULL o un MAPIUID cero, esta función se comporta como [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> [entrada] La libreta de direcciones usada para abrir el identificador de entrada. No puede ser NULL.
    
 _cbEntryID1_
  
> [entrada] Recuento de bytes del primer identificador de entrada especificado por el _parámetro lpEntryID1._ 
    
 _lpEntryID1_
  
> [entrada] Puntero al primer identificador de entrada que representa la entrada de la libreta de direcciones que se debe comparar.
    
 _cbEntryID2_
  
> [entrada] Recuento de bytes del segundo identificador de entrada especificado por el _parámetro lpEntryID2._ 
    
 _lpEntryID2_
  
> [entrada] Puntero al segundo identificador de entrada usado en la comparación que representa la entrada de la libreta de direcciones que se debe comparar.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpulResult_
  
> [salida] Puntero a la ubicación que contiene los resultados de la comparación. 
    

