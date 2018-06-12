---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 1b957c02f331038ee9104f01806720d2f8e0b542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817068"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**Se aplica a**: Outlook 
  
Codifica un identificador de entrada en una cadena ASCII. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a>Sintaxis

 _cb_
  
> [entrada] Tamaño, en bytes, del identificador de entrada que señala el parámetro _pentry_ . 
    
 _pentry_
  
> [entrada] Puntero a una estructura [ENTRYID](entryid.md) que contiene el identificador de entrada que se va a codificar. 
    
 _psz_
  
> [out] Puntero a la cadena devuelta de ASCII.
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Observaciones

Las funciones [HrEntryIDFromSz](hrentryidfromsz.md) y **HrSzFromEntryID** proporcionan conversión entre la cadena y formatos binarios de los identificadores de entrada. Con MAPI, debe usar las estructuras de datos binarios. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

La función **HrSzFromEntryID** asigna memoria de la cadena de ASCII mediante la función [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  

