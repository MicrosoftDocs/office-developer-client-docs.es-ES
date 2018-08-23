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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 366208b8288aeb61bf1bb78f2c9f10b400a3dc26
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567597"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parámetros

 _cb_
  
> [entrada] Tamaño, en bytes, del identificador de entrada que señala el parámetro _pentry_ . 
    
 _pentry_
  
> [entrada] Puntero a una estructura [ENTRYID](entryid.md) que contiene el identificador de entrada que se va a codificar. 
    
 _psz_
  
> [out] Puntero a la cadena devuelta de ASCII.
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Las funciones [HrEntryIDFromSz](hrentryidfromsz.md) y **HrSzFromEntryID** proporcionan conversión entre la cadena y formatos binarios de los identificadores de entrada. Con MAPI, debe usar las estructuras de datos binarios. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

La función **HrSzFromEntryID** asigna memoria de la cadena de ASCII mediante la función [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  

