---
title: HrEntryIDFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrEntryIDFromSz
api_type:
- COM
ms.assetid: 14c171ec-0aec-43ab-8be8-e6bc0ce28a58
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 2b7ef789c80f85f3539ec3bbd0caf4a8adc50f3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817051"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**Se aplica a**: Outlook 
  
Vuelve a crear un identificador de entrada de su codificación de ASCII. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a>Sintaxis

 _sz_
  
> [entrada] Puntero a la cadena de ASCII desde el que se va a crear un identificador de entrada. 
    
 _placa de circuitos impresos_
  
> [out] Puntero al tamaño, en bytes, del identificador de entrada indicada por el parámetro _ppentry_ . 
    
 _ppentry_
  
> [out] Puntero a un puntero a la estructura [ENTRYID](entryid.md) devuelto que contiene el nuevo identificador de entrada. 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La recreación fue correcta.
    
MAPI_E_INVALID_ENTRYID
  
> El identificador de entrada no es válido.
    
## <a name="remarks"></a>Notas

Las funciones **HrEntryIDFromSz** y [HrSzFromEntryID](hrszfromentryid.md) proporcionan conversión entre la cadena y formatos binarios de los identificadores de entrada. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

La función **HrEntryIDFromSz** asigna memoria de la cadena de ASCII mediante la función [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  

