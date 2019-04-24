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
ms.openlocfilehash: 4020a9161a51994ebe5b7e339d26f7612ad47361
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346420"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Codifica un identificador de entrada en una cadena ASCII. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a>Parameters

 _cb_
  
> a Tamaño, en bytes, del identificador de entrada al que apunta el parámetro _pentry_ . 
    
 _pentry_
  
> a Puntero a una estructura [EntryID](entryid.md) que contiene el identificador de entrada que se va a codificar. 
    
 _PSZ_
  
> contempla Puntero a la cadena ASCII devuelta.
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Las funciones [HrEntryIDFromSz](hrentryidfromsz.md) y **HrSzFromEntryID** proporcionan conversión entre los formatos binarios y de cadena de los identificadores de entrada. Con MAPI, debe usar estructuras con datos binarios. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

La función **HrSzFromEntryID** asigna memoria para la cadena ASCII mediante la función [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  

